# Java Script Guidelines

## What Is This?
This guide is the reccomendations of the Excella JavaScript community on some key architectural decisions for Javascript 
Projects. These are meant to be guidelines for projects and not a singular source of truth. There are always exceptions to
the rule. However if a project wants to deviate from these reccomendations, they should have a good thought out reason for doing so that they expect will significantly benefit the project and/or client.

## Why Does This Exist?
It was noticed that while a lot of projects at Excella use JavaScript, we are using often different tools and techniques. This hurts us in a few ways: We do the same research over and over again on projects to choose technologies, developers need to learn different technologies to do the same thing differently on different projects (which results in less expertise and longer ramp up times), we are unable to train individuals in certain areas of JavaScript unless we know what project they will be on, and it is harder to identify the right skillsets for projects forstaffing purposes. By alligning our approach we can cut down on some of this churn and difficulty.

## [Typescript](./decisions/typescript.md)
We reccomend that all JavaScript projects (Angular, React, or Node) should use TypeScript. The benefits that it provides outweighs the time it takes to set it up as long as the project is running for more than a week.

## [React State Management](./decisions/react-state-management.md)
We reccomend that either Hooks/Context API or ReDux be used for state management. Hooks/Context should be used 
for applications with simple state management since it comes with React and is easy to use, and Redux should be used 
for applications with complex state management due to its robustness.
