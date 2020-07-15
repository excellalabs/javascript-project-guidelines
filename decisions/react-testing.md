# React Testing

The React community offers many options for component test harnesses, each with their own testing philosophy, nuances, and unique syntax. We recommend [@testing-library/react](https://www.npmjs.com/package/@testing-library/react) for unit/component/integration testing because it focuses on testing functionality rather than implementation, and [cypress](https://www.npmjs.com/package/cypress) for E2E testing because of it's ease-of-use and rich feature-set.

## Why

By focusing on testing functionality rather than implementation specifics, developers are enabled to rework the way components achieve results without needing to rewrite tests. This increases confidence in the refactor, tests what really needs to be tested, and reduces time to accomplish a task. Additionally, it shifts developer mindset away from implementation-first, and towards business-first.

## Unit Testing Libraries

- React Testing Library vs Enzyme vs Test Renderer
  - Each has use cases, but most applications tend to use multiple of these
  - These libs are necessary for rendering a React component tree / composition

### React Testing Library ([@testing-library/react](https://www.npmjs.com/package/@testing-library/react))

- Built more for black-box style testing, focus on user interactions and results
- Community tends to be favoring this approach
- Much easier to test with hooks, functional components where the components do not exist as instantiated classes
- No shallow rendering

### [Enzyme](https://www.npmjs.com/package/enzyme)

- Low level, can check implementation details
- Better for class components or when implementation details are required
- Shallow rendering is available
- Built and maintained by AirBnB

### [Test Renderer](https://www.npmjs.com/package/react-test-renderer)

- Provided with React
- Shallow feature-set

## E2E Testing

- Cypress vs Puppeteer
- For overly large components (ie. large children trees) it may be better to just use E2E tests for that, rather than try a complicated integration test via Jest + renderer

### [Cypress](https://www.npmjs.com/package/cypress)

- Cypress types can conflict with Jest types, when TypeScript is used
  - Could move Cypress to a separate project / repo
- Agnostic of framework, only cares about the DOM
- Supports mocking API calls, can capture that traffic, helps isolate the front-end
- Supports Gherkin via plugin
- Follows freemium model – part you pay for is storage for videos when capturing runs
- Only runs on Chromium & Firefox
- Bundles Electron, for a built-in browser
- Has a console, to watch tests and replay

### [Puppeteer](https://www.npmjs.com/package/puppeteer)

- Favored by hobbyists
- Only runs with Chromium

## Best Practices

### Defining Unit vs Integration vs E2E tests

Where is the line between Unit tests (Jest), Integration tests (renderer), and E2E (Cypress)?

- Individual functions can be tested using Jest only, and ideally are not reliant on instantiating a component in order to be accessed (in fact, this is nealy impossible with functional components)
- Individual components, tested on their own should utilize Jest and your choice of component renderer. These are still considered Unit tests as a component is the smallest piece of a React application.
- Multiple components working together should still use Jest and the component renderer, but are more commonly considered integration tests since the goal of these tests should be to examine the interaction between the two components.
- Whole features or workflows are best tested via Cypress as End-to-End tests since they often encompass multiple pages, lengthy processes, API/database interactions and complex business logic.

### Snapshot tests

Use snapshot tests when the specifics of how someing is rendered matters (aria-labels, styling, or images, etc). However, they should never be the only test that a given component has, unless it's something static, like a footer.

- Dangerous, can be overused and falsely inflate test coverage
- The snapshots themselves are often never examined by developers
- Too easy to just update them and move on when breaks occur

Value: Understanding scope of change, checking expectations
