# Testing - front-end web technology - 2023-02-20

Verify that your UI works, automated.

Please read:

- Testing Libray:
  - @testing-library/react
    - [Introduction](https://testing-library.com/docs/react-testing-library/intro)
    - [Cheatsheet](https://testing-library.com/docs/react-testing-library/cheatsheet)
  - @testing-library/user-event
    - [Introduction](https://testing-library.com/docs/user-event/intro)
    - [Convenience APIs](https://testing-library.com/docs/user-event/convenience)
    - [Utility APIs](https://testing-library.com/docs/user-event/utility)
  - @testing-library/jest-dom
    - [jest-dom](https://github.com/testing-library/jest-dom)
- Vitest
  - [Getting Started](https://vitest.dev/guide/)
  - [Features](https://vitest.dev/guide/features.html)

## Questions for you

- How many of you have written at least 5 unit tests (in whatever language) before?
- How many of you have mocked a dependency while unit testing?

## Why is automated testing with Vitest and Testing Library exciting?

- Focus on testing from user point of view
- Good support for modules, TypeScript, JSX
- Fast and good debugging support
- Widely used / fast adoption, active and friendly community

## Setup

- jsdom to simulate browser in Node.js
- jest-dom with additional matchers
- setup file
- cleanup

## Vitest

- describe
- it
- expect, matchers
- run / watch
- coverage
- before / after
- mocking modules
- mocking functions, like fetch

## Testing Library

- setup
- render
- screen
- queries
- click
- type

## Getting Started

Testing app from first section of this course: [Getting Started](../01-getting-started/)

- Install deps

```bash
npm install vitest jsdom
npm install @testing-library/react @testing-library/user-event @testing-library/jest-dom
```

- Configure Vitest in `vite.config.ts`:

```ts
/// <reference types="vitest" />
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";

export default defineConfig({
  plugins: [react()],
  test: {
    environment: "jsdom",
    setupFiles: ["vitest.setup.ts"],
  },
});
```

- Configure Testing Library and jest-dom in `vitest.setup.ts`:

```ts
import matchers from "@testing-library/jest-dom/matchers";
import { cleanup } from "@testing-library/react";
import { afterEach, expect } from "vitest";

expect.extend(matchers);

afterEach(cleanup);
```

- Write test for initial App render in `App.test.tsx`:

```tsx
import { render, screen } from "@testing-library/react";
import { describe, expect, it } from "vitest";
import App from "./App";

describe(App.name, () => {
  it("should render", () => {
    render(<App />);
    expect(screen.getByLabelText("Artist name:")).toBeInTheDocument();
  });
});
```

- Run Vitest

```bash
npx vitest
```

- View coverage

```bash
npx vitest --run --coverage
```

- mock-response.json - save response of https://musicbrainz.org/ws/2/release?fmt=json&query=artist:rihanna

- Fix AlbumPicker component to work with jsdom

```tsx
const form = e.target as HTMLFormElement;
const formElements = form.elements as typeof form.elements & {
  artist: { value: string };
};
const artist = encodeURIComponent(formElements.artist.value);
```

```tsx
<form onSubmit={handleSubmit} name="search" aria-label="search">
```

- Write test for initial App render in `App.test.tsx`:

```tsx
describe(AlbumPicker.name, () => {
  afterEach(() => {
    vi.restoreAllMocks();
  });

  it("should show search results", async () => {
    const user = userEvent.setup();
    const rihannaUrl =
      "https://musicbrainz.org/ws/2/release?fmt=json&query=artist:rihanna";
    const mockFetch = vi
      .spyOn(window, "fetch")
      .mockImplementation(async (url: RequestInfo | URL) => {
        if (url === rihannaUrl) {
          return {
            json: async () => mockResponse,
          } as Response;
        } else {
          return {} as Response;
        }
      });

    render(<AlbumPicker />);

    const artistInput = screen.getByLabelText("Artist name:");
    await user.type(artistInput, "rihanna");
    const form = screen.getByRole("form", { name: "search" });
    fireEvent.submit(form);

    await screen.findByText("A Girl Like Me");

    expect(mockFetch).toHaveBeenCalledWith(rihannaUrl);
  });
});
```

## Debugging

View the page in a browser at specific points in your test with [vitest-preview](https://github.com/nvh95/vitest-preview).

## Contnuous Integration

Run tests on every push.

Add line inside "scripts" in `package.json`:

```json
"test": "tsc && vitest --run --coverage && vite build"
```

If your repo is on GitHub, create this `.github/workflows/ci.yml` file:

```yaml
name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
      - name: Use Node.js
        uses: actions/setup-node@v1
        with:
          node-version: "18"
      - run: npm ci
      - run: npm test
```

## Next time

[Forms](../06-forms/).
