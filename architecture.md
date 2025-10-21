# Frontend architecture 

## ⭐ Introduction

### Purpose
This document provides an architectural overview of the system.
It is intended to capture and convey the significant architectural decisions which have been made on the system.

### Stack overview
- Script language: [Typescript](https://www.typescriptlang.org/)
- Monorepo build system: [Nx](https://nx.dev/)
- Frontend library: [ReactJS](https://reactjs.org/), [NextJS](https://nextjs.org/)
- State management: [Redux toolkit](https://redux-toolkit.js.org/)
- Styling: [Styled components](https://styled-components.com/)
- Unit testing: [Jest](https://jestjs.io/), [React testing library](https://testing-library.com/docs/react-testing-library/intro/)

## 🚀 Motivation
Here are some key requirements and system constraints that have a significant bearing on the architecture:
- Develop high-end frontend apps for the organization, using cutting-edge technologies
- Improve the organization's frontend clients experience
- Replace all organization's frontend apps with new ReactJS apps, served with Server Side Rendering using NextJS
- Align all technological stack across the organization's Frontend project apps
- Prevent technological overload
- Increase the organization's Frontend unit testing coverage, and code reliability
- Increase project apps readability for the organization developers
- Allow the organization developers mobility & support across all Frontend apps

## 💭 Considerations
In examining the relevant technologies, the leading consideration was to choose the leading technologies, which will enable the achievement of results in a short time, without compromising on the quality of development.

### State management
_* Here we will explain our state management selection_ * 

### Styling
_* Here we will explain our styling solution selection_ *

### Unit testing
_* Here we will explain our testing library selection_ *

## 📂 Project structure

```
project root
│   📄 README.md
│   📄 package.json    
│
└───📁 apps
│   └───📁 app1
│   │   │   .babelrc
│   │   │   .browserslistrc
│   │   │   .eslintrc.json
│   │   │   📄 jest.config.json
│   │   │   📄 tsconfig.app.json
│   │   │   📄 tsconfig.json
│   │   │   📄 tsconfig.spec.json
│   │   └────📁 src
│   │
│   └───📁 app2
│   └───📁 app3
│
└───📁 libs
    └───📁 lib1
    └───📁 lib2 
```

### Apps
The `apps` folder contains all nx auto-generated apps, and must be generated using the `nx g @nrwl/react:app my-app` cli command.
All the app files should be created within the app's folder, including all the supporting components, hooks, services etc.

### Libs
The `libs` folder contains the commonly used libraries for all Y2 Frontend apps. A new library must be generated using the `nx g @nrwl/react:lib my-lib` cli command.
Avoid adding an app-related hooks to the `libs` folder. hooks should be inside the `/app/lib` folder, unless the hook can be commonly used by all frontend apps.

## 🔏 Coding standards
Development must meet the [AirBnB standards](https://github.com/airbnb/javascript).
Code which does not apply with the standard should not be approved and/or merged into the `main` branch.


###### *Document last updated on July 6th, 2023 by [Erez Carmel](mailto:erezcarmel@gmail.com)*
