# E2E Testing

While there are multiple options for E2E testing in React, We recommend [cypress](https://www.npmjs.com/package/cypress) because of it's ease-of-use and rich feature-set.

- Cypress vs Puppeteer
- For overly large components (ie. large children trees) it may be better to just use E2E tests for that, rather than try a complicated integration test via Jest + renderer
- Whole features or workflows are best tested via Cypress as End-to-End tests since they often encompass multiple pages, lengthy processes, API/database interactions and complex business logic.

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
