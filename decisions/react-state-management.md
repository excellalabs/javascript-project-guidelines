# React State Management

We recommend that either Hooks/Context API or ReDux be used for state management. Hooks/Context should be used
for applications with simple state management since it comes with React and is easy to use, and Redux should be used
for applications with complex state management due to its robustness.

## Why

React has a lot of good different state managment systems that we also looked at (MobX for example) however we felt that
the situations where one of Hooks/Context API or ReDux wouldn't be a good solution are few and far between. Additionally,
with ReDux being the most popular state management library, and Hooks/Context API being built into React, we feel more confident
on the longevity and support of these two systems as compared to other state management systems. By narrowing down our choice
to these two, we can cut down on the learning and ramp up time spent on state management from client to client and project to project.

## Benefits

### Hooks/Context API

- Comes built into React
- Designed to work similar to and seemlessly with the rest of React
- Easy to learn
- Light weight
- More versitile than other state management systems

### ReDux

- Able to manage complex state
- Powerful library
- Helps structure complex sate in applications
- Tools available make it easy to test applications
- Large community following

## Negatives

### Hooks/Context API

- Gets confusing/ lots of overhead with really complicated state management

### ReDux

- Complicated to learn
- Really large library is too big for some applications
