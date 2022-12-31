# Getting Started - front-end web technology - 2023-01-30

## Who is Lars Thorup?

- Freelance software engineer: React, TypeScript, Node.js, Python, SQL, AWS
- Invert Inc (2022), ZeroNorth (2021), BASE lifescience (2020)
- CTO and co-founder at Triggerz (2015-2020)
- External Lecturer at ITU (2001-2002)
- Master in Computer Science (1994)
- [LinkedIn](https://www.linkedin.com/in/larsthorup/)

![](./lars-2016-03-24-350px.jpg)

## Why is front-end web technology exiciting?

- Low barrier to entry
  - In one day you can learn how to build and deploy an app that your parents can then use on their phone
  - Easy to hire people globally to build and deliver new products

## Overview of the entire course

1. [Getting Started](.)
1. HTML, CSS, JS
1. JavaScript, TypeScript
1. React
1. Testing
1. Forms, routing
1. UX, styling
1. REST, HTTP
1. Auth, security
1. State
1. Animation
1. Architecture: SPA, PWA, MPA
1. What's left to learn?

## Getting started

Goal: get a tiny front-end web application running locally on your machine and deployed to the cloud.

### Node.js

- Install from https://nodejs.org/en/ unless you have it already
- `node --version`
  - Should be at least version 16.

### Git repo

- GitHub / GitLab, create blank repo
- `git clone (repo-url)`
- `cd (directory)`

### Create sample application

- `npm create vite@latest . -- --template react-ts`
- `npm install`

### Run locally

- `npm run dev`

![](./vite-react-ts.png)

### Extend application to invoke API

In the file `src/App.tsx`, first add this definition of an `AlbumPicker` React component:

```tsx
function AlbumPicker() {
  const [albums, setAlbums] = useState<string[]>([]);
  async function handleSubmit(e: FormEvent) {
    e.preventDefault();
    const target = e.target as typeof e.target & {
      artist: { value: string };
    };
    const artist = encodeURIComponent(target.artist.value);
    const url = `https://musicbrainz.org/ws/2/release?fmt=json&query=artist:${artist}`;
    const response = await fetch(url);
    const mbResult = (await response.json()) as {
      releases: { title: string }[];
    };
    const { releases } = mbResult;
    setAlbums(releases.map(({ title }) => title));
  }
  return (
    <form onSubmit={handleSubmit}>
      <label>
        Artist name:
        <input name="artist" />
      </label>
      <button type="submit">Search</button>
      <p>Albums:</p>
      <ol>
        {albums.map((album) => (
          <li>{album}</li>
        ))}
      </ol>
    </form>
  );
}
```

And then insert an instance of this component into the JSX of the app:

```tsx
<AlbumPicker />
```

### Debugging

Print out information, and view in the "console" tab in the developer tools of the browser (right click + Inspect):

```tsx
console.log(mbResult);
```

Look at the "network" tab in the developer tools.

### Deploy to cloud

Get access on Netlify:

- Sign up for a free plan on [Netlify](netlify.com).
  - You can also use [Vercel](vercel.com)
  - or GitHub / GitLab / Cloudflare Pages
- `npm install -g netlify-cli`
- `ntl --version`
  - Should be at least 12.5

Connect project to Netlify

- `ntl init`
  - Decline giving access to GitHub account (ctrl-c)

Deploy latest code:

- `npm run build`
- `ntl deploy`

Share the URL with friends & family :)

### Read the code

Try to get a cursory understanding by reading through the code of App.tsx several times. Help your understanding by sprinkling `console.log` statements here and there. You will learn how all the bits and pieces fit together plus a lot more, during this course.

### Additional exercises

1. Include additional information about each album, such as release date.
1. Add an additional input field to allow the user to filter on album name too.

## Next time

HTML, CSS, JS
