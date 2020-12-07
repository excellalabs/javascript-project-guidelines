# React Testing

The React community offers many options for component test harnesses, each with their own testing philosophy, nuances, and unique syntax. We recommend [@testing-library/react](https://www.npmjs.com/package/@testing-library/react) for unit/component/integration testing because it focuses on testing functionality rather than implementation.

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

## Best Practices

### Defining Unit vs Integration vs E2E tests

Where is the line between Unit tests (Jest) and Integration tests (renderer)?

- Individual functions can be tested using Jest only, and ideally are not reliant on instantiating a component in order to be accessed (in fact, this is nealy impossible with functional components)
- Individual components, tested on their own should utilize Jest and your choice of component renderer. These are still considered Unit tests as a component is the smallest piece of a React application.
- Multiple components working together should still use Jest and the component renderer, but are more commonly considered integration tests since the goal of these tests should be to examine the interaction between the two components.

### Snapshot tests

Use snapshot tests when the specifics of how someing is rendered matters (aria-labels, styling, or images, etc). However, they should never be the only test that a given component has, unless it's something static, like a footer.

- Dangerous, can be overused and falsely inflate test coverage
- The snapshots themselves are often never examined by developers
- Too easy to just update them and move on when breaks occur

Value: Understanding scope of change, checking expectations
