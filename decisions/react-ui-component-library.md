# React UI Component Library

We recommend standing on the shoulders of giants whenever possible. For that reason, we suggest leveraging Google's Material UI design spec via [@material-ui/core](https://www.npmjs.com/package/@material-ui/core). Where that fails to offer something you need, we suggest looking to [KendoUI](https://demos.telerik.com/kendo-ui/) for a solution. We view building your own UI Component Library to be a last resort that should be avoided if at all possible.

If those recommendations won't work for you, see our suggested considerations for choosing something else, below.

## Material-UI

- Well-defined design spec
- Well-maintained
- 508 support
- Works seamlessly with Formik
- Built-in labels (important for ARIA)
- Built-in error messaging

## KendoUI

- Useable in React and Angular, so it's a learn-once, use-everywhere investment
- Well tested and documented
- Offers many UI components that other libraries don't have (like spreadsheets, etc)
- Requires licensing

### Considerations when choosing a UI Component Library:

- Accessibility (508)
- Functionality
  - Input Masking
  - Auto-complete (type-ahead)
- USWDS Compatibility (for Federal Clients)
- Extensible / customizable
- Look & Feel
- Documentation
- Code/Repo health
  - How large is the dev team?
  - When was it last updated?
  - How frequently does the dev team make breaking changes?
