# JavaScript Guidelines

## What Is This?

This guide is the recommendations of the Excella JavaScript community on some key architectural decisions for Javascript
Projects. These are meant to be guidelines for projects and not a singular source of truth. There are always exceptions to
the rule. However if a project wants to deviate from these recommendations, they should have a good thought out reason for doing so that they expect will significantly benefit the project and/or client.

## Why Does This Exist?

It was noticed that while a lot of projects at Excella use JavaScript, we are often using different tools and techniques. This hurts us in a few ways: We do the same research over and over again on projects to choose technologies, developers need to learn different technologies to do the same thing differently on different projects (which results in less expertise and longer ramp up times), we are unable to train individuals in certain areas of JavaScript unless we know what project they will be on, and it is harder to identify the right skillsets for projects forstaffing purposes. By alligning our approach we can cut down on some of this churn and difficulty.

## What's the <a href="https://github.com/excellalabs/javascript-project-guidelines/blob/main/expeditions/EXPEDITIONS.md">"eXpeditions" Directory</a> about?

In addition to vetted project guidelines, this repo also contains the findings of Excellians' PD time. These findings are stored here to preserve and radiate the knowledge Excellians have gleaned from their professional development.

While these findings have not undergone the same scrutiny as the outcomes from JavaScript Death Battles™, they are valuable as they are varied.

# General

## [Typescript](./decisions/typescript.md)

We recommend that all JavaScript projects (Angular, React, or Node) should use TypeScript. The benefits that it provides outweighs the time it takes to set it up as long as the project is running for more than a week.

# React

React is a rendering engine that leaves most other implementation decisions up to the developer.

## [State Management](./decisions/react-state-management.md)

We recommend that either Hooks/Context API or ReDux be used for state management. Hooks/Context should be used
for applications with simple state management since it comes with React and is easy to use, and Redux should be used
for applications with complex state management due to its robustness.

## [Testing Tools & Testing Best Practices](./decisions/react-testing.md)

The React community offers many options for component test harnesses, each with their own testing philosophy, nuances, and unique syntax. We recommend [@testing-library/react](https://www.npmjs.com/package/@testing-library/react) for unit/component/integration testing because it focuses on testing functionality rather than implementation, and [cypress](https://www.npmjs.com/package/cypress) for E2E testing because of it's ease-of-use and rich feature-set.

## [UI Component Library](./decisions/react-ui-component-library.md)

We recommend standing on the shoulders of giants whenever possible. For that reason, we suggest leveraging Google's Material UI design spec via [@material-ui/core](https://www.npmjs.com/package/@material-ui/core). Where that fails to offer something you need, we suggest looking to [KendoUI](https://demos.telerik.com/kendo-ui/) for a solution. We view building your own UI Component Library to be a last resort that should be avoided if at all possible.

## [Forms Library](./decisions/react-forms.md)

We reccomend using [Formik](https://formik.org/) and [Yup](https://github.com/jquense/yup) to handle form management in React. We have run into no big issues with it, it has been around the longest, and we have the most experience with it, so we see no reason to use another less mature library instead.

## [React Class vs. Function Components](./decisions/react-class-vs-function-components.md)

Both class and function components offer the same capabilities with slightly different syntax. We recommend function components for their simplicity and choosing to add hooks if you need state or side effects.

# Angular

Angular is a very opinionated framework, and thus has a highly opinionated community. For the most part, those opinions are right, and should be easy to follow. We are actively choosing to focus on building out recommendations for React first, since it has far fewer strong opinions and we are using it more and more on client work.

If you need help with Angular, please don't hesitate to reach out via Slack. Angular is largely favored over React by JavaScript developers at Excella, so do not take the lack of information here as any indicator that Angular is perfect, or that we don't have opinions about it.

# [API Architecture](./decisions/rest-vs-graphql.md)

REST has been the web standard for APIs for over a decade. The new contender is GraphQL, which has gained traction. GraphQL solves the issues of over-fetching and under-fetching. It uses resolvers to aggregate sources into one call and allows the client to define what data they need. Unfortunately, the tooling around testing, traceablity, and code generation are not mature enough in all languages to recommend it for general use.

For general use we recommend REST due to the maturity of the technology and tooling. An exception is when combining services in a gateway abstraction pattern. In this scenario, evaluate and consider GraphQL. Be advised, tooling for GraphQL is far more mature for nodejs than for other languages.

[meeting notes](.decisions/rest-vs-graphql.md)

## [GraphQL Library](./decisions/graphql-library.md)

We recommend the [Apollo](https://www.apollographql.com/) library when implementing GraphQL on Excella projects. But, this recommendation is primarily due to the fact that it is only library in which Excellians have project experience. The secondary factor is that it works with both React and Angular.

The runner up is [Relay](https://relay.dev/), backed by Facebook. It has quickly caught up with Apollo in popularity. But, Excella has very little expertise with it and it is only compatible with React.
