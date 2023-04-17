# Technology Map - front-end web technology

What else to learn in addition to what we have already covered in [this course](../README.md)?

(Note: this list is biased by my personal experience and interests, there are many more interesting technologies out there!)

## How to choose technology for your next project?

- It is widely used
- It is of high quality
- It handles most of our needs
- We need substantial parts of it
- It is consistent with our other technologies
- https://www.fullstackagile.eu/2020/01/20/build-or-buy/

Legend:

- :green_heart: good popular things I recommend
- :eyes: relevant to try

## Rendering

- :green_heart: [SVG](https://developer.mozilla.org/en-US/docs/Web/SVG) - declarative vector graphics
- :green_heart: [Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) - procedural 2D graphics
- :eyes: [WebGL](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API) - procedural 3D graphics
- :eyes: [MathML](https://developer.mozilla.org/en-US/docs/Web/MathML) - declarative math notation

## CSS

- :green_heart: [Pseudo classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) - styling based on element state
- :green_heart: [Specificity](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance) - cascading, inheritance, overriding
- :green_heart: [Stacking context](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context) - z-index and transforms
- :eyes: [Gradients](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Images/Using_CSS_gradients)
- :eyes: [Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
- :green_heart: [Tailwind CSS](https://tailwindcss.com/) - class library
- :eyes: [UnoCSS](https://unocss.dev/) - class library
- :green_heart: Creating a design system

## JavaScript

- :green_heart: [Prototypical inheritance](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
- :green_heart: [Proxy](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy)
- :green_heart: [Generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*)

## TypeScript

- :green_heart: [Type operators](https://www.typescriptlang.org/docs/handbook/2/types-from-types.html), like `keyof`, `typeof`, `[]`
- :green_heart: [Utility types](https://www.typescriptlang.org/docs/handbook/utility-types.html) - like `Record`, `Pick`, `Omit`, `ReturnType`
- :eyes: [Conditional types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)
- :green_heart: [Mapped types](https://www.typescriptlang.org/docs/handbook/2/mapped-types.html)

## Web APIs

- :green_heart: [HTML Drag and Drop](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API)
- :green_heart: [Clipboard](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard_API)
- :eyes: [Geolocation](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API)
- :green_heart: [Web Workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API) - keep slow tasks off the main thread
- :green_heart: [IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) - a transactional database
- :green_heart: [WebRTC](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API) - streaming audio and video
- :eyes: [Payment](https://developer.mozilla.org/en-US/docs/Web/API/Payment_Request_API)
- :eyes: [Audio](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)

## React

- :green_heart: [ErrorBoundary](https://github.com/bvaughn/react-error-boundary) for error handling
- :green_heart: [useMemo](https://react.dev/reference/react/useMemo) for data memoization
- :green_heart: [useCallback](https://react.dev/reference/react/useCallback) for function memoization
- :green_heart: [memo](https://react.dev/reference/react/memo) for component memoization
- :green_heart: [lazy](https://react.dev/reference/react/lazy) for delayed loading
- :eyes: [Suspense](https://react.dev/reference/react/Suspense) for loading indicators
- :eyes: [useRef](https://react.dev/reference/react/useRef)
- :eyes: [React Server Components](https://github.com/reactjs/rfcs/blob/main/text/0188-server-components.md) - (work in progress) hybrid client and server rendering

## Components and functions

- :green_heart: [Headless UI](https://headlessui.com/) - components; bring your own styling
- :green_heart: [Material UI](https://mui.com/) - components with styling
- :eyes: [Chakra UI](https://chakra-ui.com/) - components with styling
- :eyes: [React Spring](https://github.com/pmndrs/react-spring) - animations
- :green_heart: [Ramda](https://github.com/ramda/ramda) - immutable data structure manipulation
- :green_heart: [date-fns](https://github.com/date-fns/date-fns) - tima and date manipulation
- :green_heart: [clsx](https://github.com/lukeed/clsx) - className manipulation

## State management

- :green_heart: [Redux Toolkit](https://redux-toolkit.js.org/)
- :eyes: [Recoil](https://recoiljs.org/)

## HTTP

- Query and caching libraries
  - :eyes: [React Query](https://tanstack.com/query/)
  - :green_heart: [Redux Toolkit Query](https://redux-toolkit.js.org/rtk-query/overview)
- OpenAPI - schema for REST APIs
  - :green_heart: [FastAPI](https://fastapi.tiangolo.com/) - for Python APIs
  - :green_heart: [openapi-typescript](https://github.com/drwpow/openapi-typescript) - generate types from OpenAPI schema
- :eyes: [GraphQL](https://graphql.org/) - query language for APIs
- :eyes: [tRPC](https://trpc.io/) - end-to-end type safety

## Routing

- :green_heart: [React Router](https://reactrouter.com/)

## Security

- :green_heart: [OAUTH](https://aaronparecki.com/oauth-2-simplified/) - integrate with an identity provider

## Cross-platform support

- :green_heart: [React Native](https://reactnative.dev/) - JavaScript and React on mobile devices
- :green_heart: [React Native for Web](https://necolas.github.io/react-native-web/) - React Native components for web apps
- :eyes: [Electron](https://www.electronjs.org/) - HTML, CSS and JavaScript on desktops
- :eyes: [Tauri](https://tauri.app/) - HTML, CSS and JavaScript on desktops
- :eyes: [WebAssembly - WASM](https://developer.mozilla.org/en-US/docs/WebAssembly) - compiled languages in web browsers

## Architecture

- :green_heart: [Micro front-ends](https://martinfowler.com/articles/micro-frontends.html) - modular front-ends for scalable development
- :green_heart: [Content management systems - CMS](https://en.wikipedia.org/wiki/Content_management_system) - editable apps
- :green_heart: [Single-Page App - SPA](https://en.wikipedia.org/wiki/Single-page_application)
- :green_heart: [Progressive Web App - PWA](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps) - native app features, such as offline support offline support
- :green_heart: Multi-Page Application - MPA
- :green_heart: [Static Site Generation - SSG](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Introduction#static_site_generators) - avoid dynamic HTML
- :eyes: [Server Side Rendering - SSR](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Introduction#server-side_rendering) - minimize dynamic HTML

## Testing

- :green_heart: [Vitest](https://vitest.dev/)
- :green_heart: [Testing Library](https://testing-library.com/)
- :green_heart: [Mocking time and timers](https://vitest.dev/guide/mocking.html)
- :green_heart: [msw](https://mswjs.io/) - mock HTTP requests
- :green_heart: [Playwright](https://playwright.dev/) - run tests in real browsers
- :eyes: [Cypress](https://www.cypress.io/) - run tests in real browsers
- :green_heart: [Jest](https://jestjs.io/) - older popular test runner

## Performance profiling

- :green_heart: [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)
- :eyes: [`<Profiler>`](https://react.dev/reference/react/Profiler)
- :green_heart: [Firefox Profiler](https://profiler.firefox.com/docs/#/)
- :green_heart: [Chrome Profiler](https://developer.chrome.com/docs/devtools/performance/)

## Frameworks

- :green_heart: [Angular](https://angular.io/)
- :green_heart: [Next.js](https://nextjs.org/) - popular React framework
- :eyes: [Solid](https://www.solidjs.com/)
- :eyes: [Svelte](https://svelte.dev/)
- :eyes: [Vue](https://vuejs.org/)

## Bundlers

- :green_heart: [Vite](https://vitejs.dev/)
- :green_heart: [Webpack](https://webpack.js.org/) - older popular bundler

## Module and package management

- :green_heart: [npm](https://docs.npmjs.com/) - package manager
- :eyes: [nx](https://nx.dev/) - build system
- :eyes: [pnpm](https://pnpm.io/) - package manager
- :green_heart: [yarn](https://yarnpkg.com/) - package manager
