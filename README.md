# Java Script Guidelines

## [Typescript](./decisions/typescript.md)
We reccomend that all JavaScript projects (Angular, React, or Node) should use TypeScript. The benefits that it provides outweighs the time it takes to set it up as long as the project is running for more than a week.

## [React State Management](./decisions/react-state-management.md)
We reccomend that either Hooks/Context API or ReDux be used for state management. Hooks/Context should be used 
for applications with simple state management since it comes with React and is easy to use, and Redux should be used 
for applications with complex state management due to its robustness.
