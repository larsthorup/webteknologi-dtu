# Technology Map - front-end web technology

What else to learn in addition to what we have already covered in [this course](../README.md)?

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

- <span style="color:green">⬤</span> [SVG](https://developer.mozilla.org/en-US/docs/Web/SVG) - declarative vector graphics
- <span style="color:green">⬤</span> [Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) - procedural 2D graphics
- <span style="color:purple">⬤</span> [WebGL](https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API) - procedural 3D graphics
- <span style="color:purple">⬤</span> [MathML](https://developer.mozilla.org/en-US/docs/Web/MathML) - declarative math notation

## CSS

- <span style="color:green">⬤</span> [Pseudo classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) - styling based on element state
- <span style="color:green">⬤</span> [Specificity](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance) - cascading, inheritance, overriding
- <span style="color:green">⬤</span> [Stacking context](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context) - z-index and transforms
- <span style="color:purple">⬤</span> [Gradients](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Images/Using_CSS_gradients)
- <span style="color:purple">⬤</span> [Animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations)
- <span style="color:green">⬤</span> [Tailwind CSS](https://tailwindcss.com/) - class library
- <span style="color:purple">⬤</span> [UnoCSS](https://unocss.dev/) - class library
- <span style="color:green">⬤</span> Creating a design system

## JavaScript

- <span style="color:green">⬤</span> [Prototypical inheritance](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
- <span style="color:green">⬤</span> [Proxy](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy)
- <span style="color:green">⬤</span> [Generators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function*)

## TypeScript

- <span style="color:green">⬤</span> [Type operators](https://www.typescriptlang.org/docs/handbook/2/types-from-types.html), like `keyof`, `typeof`, `[]`
- <span style="color:green">⬤</span> [Utility types](https://www.typescriptlang.org/docs/handbook/utility-types.html) - like `Record`, `Pick`, `Omit`, `ReturnType`
- <span style="color:purple">⬤</span> [Conditional types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)
- <span style="color:green">⬤</span> [Mapped types](https://www.typescriptlang.org/docs/handbook/2/mapped-types.html)

## Web APIs

- <span style="color:green">⬤</span> [HTML Drag and Drop](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API)
- <span style="color:green">⬤</span> [Clipboard](https://developer.mozilla.org/en-US/docs/Web/API/Clipboard_API)
- <span style="color:purple">⬤</span> [Geolocation](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API)
- <span style="color:green">⬤</span> [Web Workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API) - keep slow tasks off the main thread
- <span style="color:green">⬤</span> [IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) - a transactional database
- <span style="color:green">⬤</span> [WebRTC](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API) - streaming audio and video
- <span style="color:purple">⬤</span> [Payment](https://developer.mozilla.org/en-US/docs/Web/API/Payment_Request_API)
- <span style="color:purple">⬤</span> [Audio](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)

## React

- <span style="color:green">⬤</span> [ErrorBoundary](https://github.com/bvaughn/react-error-boundary) for error handling
- <span style="color:green">⬤</span> [useMemo](https://react.dev/reference/react/useMemo) for data memoization
- <span style="color:green">⬤</span> [useCallback](https://react.dev/reference/react/useCallback) for function memoization
- <span style="color:green">⬤</span> [memo](https://react.dev/reference/react/memo) for component memoization
- <span style="color:green">⬤</span> [lazy](https://react.dev/reference/react/lazy) for delayed loading
- <span style="color:purple">⬤</span> [Suspense](https://react.dev/reference/react/Suspense) for loading indicators
- <span style="color:purple">⬤</span> [useRef](https://react.dev/reference/react/useRef)
- <span style="color:purple">⬤</span> [React Server Components](https://github.com/reactjs/rfcs/blob/main/text/0188-server-components.md) - (work in progress) hybrid client and server rendering

## Components

- <span style="color:green">⬤</span> [Headless UI](https://headlessui.com/) - bring your own styling
- <span style="color:green">⬤</span> [Material UI](https://mui.com/)
- <span style="color:purple">⬤</span> [Chakra UI](https://chakra-ui.com/)

## State management

- <span style="color:green">⬤</span> [Redux Toolkit](https://redux-toolkit.js.org/)
- <span style="color:purple">⬤</span> [Recoil](https://recoiljs.org/)

## HTTP

- Query and caching libraries
  - <span style="color:purple">⬤</span> [React Query](https://tanstack.com/query/)
  - <span style="color:green">⬤</span> [Redux Toolkit Query](https://redux-toolkit.js.org/rtk-query/overview)
- OpenAPI - schema for REST APIs
  - <span style="color:green">⬤</span> [FastAPI](https://fastapi.tiangolo.com/) - for Python APIs
  - <span style="color:green">⬤</span> [openapi-typescript](https://github.com/drwpow/openapi-typescript) - generate types from OpenAPI schema
- <span style="color:purple">⬤</span> [GraphQL](https://graphql.org/) - query language for APIs
- <span style="color:purple">⬤</span> [tRPC](https://trpc.io/) - end-to-end type safety

## Routing

- <span style="color:green">⬤</span> [React Router](https://reactrouter.com/)

## Security

- <span style="color:green">⬤</span> [OAUTH](https://aaronparecki.com/oauth-2-simplified/) - integrate with an identity provider

## Cross-platform support

- <span style="color:green">⬤</span> [React Native](https://reactnative.dev/) - JavaScript and React on mobile devices
- <span style="color:green">⬤</span> [React Native for Web](https://necolas.github.io/react-native-web/) - React Native components for web apps
- <span style="color:purple">⬤</span> [Electron](https://www.electronjs.org/) - HTML, CSS and JavaScript on desktops
- <span style="color:purple">⬤</span> [Tauri](https://tauri.app/) - HTML, CSS and JavaScript on desktops
- <span style="color:purple">⬤</span> [WebAssembly - WASM](https://developer.mozilla.org/en-US/docs/WebAssembly) - compiled languages in web browsers

## Architecture

- <span style="color:green">⬤</span> [Micro front-ends](https://martinfowler.com/articles/micro-frontends.html) - modular front-ends for scalable development
- <span style="color:green">⬤</span> [Content management systems - CMS](https://en.wikipedia.org/wiki/Content_management_system) - editable apps
- <span style="color:green">⬤</span> [Single-Page App - SPA](https://en.wikipedia.org/wiki/Single-page_application)
- <span style="color:green">⬤</span> [Progressive Web App - PWA](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps) - native app features, such as offline support offline support
- <span style="color:green">⬤</span> Multi-Page Application - MPA
- <span style="color:green">⬤</span> [Static Site Generation - SSG](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Introduction#static_site_generators) - avoid dynamic HTML
- <span style="color:purple">⬤</span> [Server Side Rendering - SSR](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/Introduction#server-side_rendering) - minimize dynamic HTML

## Testing

- <span style="color:green">⬤</span> [Vitest](https://vitest.dev/)
- <span style="color:green">⬤</span> [Mocking time and timers](https://vitest.dev/guide/mocking.html)
- <span style="color:green">⬤</span> [msw](https://mswjs.io/) - mock HTTP requests
- <span style="color:green">⬤</span> [Playwright](https://playwright.dev/) - run tests in real browsers
- <span style="color:purple">⬤</span> [Cypress](https://www.cypress.io/) - run tests in real browsers
- <span style="color:green">⬤</span> [Jest](https://jestjs.io/) - older popular test runner

## Performance profiling

- <span style="color:green">⬤</span> [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)
- <span style="color:purple">⬤</span> [`<Profiler>`](https://react.dev/reference/react/Profiler)
- <span style="color:green">⬤</span> [Firefox Profiler](https://profiler.firefox.com/docs/#/)
- <span style="color:green">⬤</span> [Chrome Profiler](https://developer.chrome.com/docs/devtools/performance/)

## Frameworks

- <span style="color:green">⬤</span> [Angular](https://angular.io/)
- <span style="color:green">⬤</span> [Next.js](https://nextjs.org/) - popular React framework
- <span style="color:purple">⬤</span> [Solid](https://www.solidjs.com/)
- <span style="color:purple">⬤</span> [Svelte](https://svelte.dev/)
- <span style="color:purple">⬤</span> [Vue](https://vuejs.org/)

## Bundlers

- <span style="color:green">⬤</span> [Vite](https://vitejs.dev/)
- <span style="color:green">⬤</span> [Webpack](https://webpack.js.org/) - older popular bundler

## Module and package management

- <span style="color:green">⬤</span> [npm](https://docs.npmjs.com/) - package manager
- <span style="color:purple">⬤</span> [nx](https://nx.dev/) - build system
- <span style="color:purple">⬤</span> [pnpm](https://pnpm.io/) - package manager
- <span style="color:green">⬤</span> [yarn](https://yarnpkg.com/) - package manager
