# Routing, animation - front-end web technology

Navigate between pages - smoothly!

Please read:

- [History API](https://developer.mozilla.org/en-US/docs/Web/API/History)
- [popstate event](https://developer.mozilla.org/en-US/docs/Web/API/Window/popstate_event)
- [Using CSS transforms](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transforms/Using_CSS_transforms)
- [Using CSS transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)

## Supplemental reading material

- [How to Create Your Own React Router](https://dev.to/franciscomendes10866/create-your-own-react-router-53ng)

## Why is routing exciting?

- Split information between pages to navigate between
- Back navigation - go back to where I came from
- Sharable deep links

## Why is animation exciting?

- Motion can show what
  - happens (e.g. click indication)
  - happened (e.g. routing)
  - will happen (e.g. call to action)
- Motion can draw attention
- CSS transitions are much more efficient than animating with JavaScript

## Server- or client-side routing?

Server-side routing:

- Multiple HTML files, also called an MPA
- Path-based routing: `/basket`, `/delivery`
- Benefit: sharable links
- Drawback: navigation loads a new HTML file, resetting all state

Client-side routing:

- Single HTML file, also called a Single Page App (SPA)
- Query-based routing: `/?page=basket`, `/?page=delivery`
- Benefit: sharable links, no page load on navigation

Path-based routing is possible with client-side routing, but require URL rewrite rules to be configured server side for sharable links to work.

## Client-side routing

- `window.location.search` - get the current route
- `URLSearchParams` - parse query part of URL
- listen for `popstate` event with `addEventListener`
- useEffect to synchronize URL with App state
- conditional render based on App state

## Client-side navigation

- `history.pushState` - to ensure that back will work
- `popstate`, `dispatchEvent` - trigger the listener to synchronize with app state

## CSS Transitions

- animatable properties: opacity, size, color, position, rotation, many more
- may use `transform` for relative changes: scale, translate, rotate
- `transition`: property, duration, timing-function, delay
- transitions acts on property changes on that element caused
- change properties with pseudo selector (e.g. `:hover`) or class names
- explore timing functions: - https://easings.net/

Sample call-to-action button transition:

```css
.call-to-action button {
  transition: transform 0.2s ease-in;
}

.call-to-action button:hover {
  transform: scale(1.1);
}
```

Sample navigation transition:

```css
.page {
  transition: opacity 0.4s ease-in;
}

.page.navigating {
  opacity: 0;
}

.page.navigated {
  opacity: 1;
}
```

## Next time

[State](..).
