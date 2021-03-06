# Angular UI Components for ManageIQ

[![score](https://www.bithound.io/github/ManageIQ/ui-components/badges/score.svg)](https://www.bithound.io/github/ManageIQ/ui-components)
[![dependencies](https://www.bithound.io/github/ManageIQ/ui-components/badges/dependencies.svg)](https://www.bithound.io/github/ManageIQ/ui-components/master/dependencies/npm)
[![bitHound Dev Dependencies](https://www.bithound.io/github/ManageIQ/ui-components/badges/devDependencies.svg)](https://www.bithound.io/github/ManageIQ/ui-components/master/dependencies/npm)
[![Known Vulnerabilities](https://snyk.io/test/github/mtho11/ui-components/badge.svg)](https://snyk.io/test/github/mtho11/ui-components)
[![Build Status](https://travis-ci.org/ManageIQ/ui-components.svg)](https://travis-ci.org/ManageIQ/ui-components)
[![Coverage Status](https://coveralls.io/repos/github/ManageIQ/ui-components/badge.svg)](https://coveralls.io/github/ManageIQ/ui-components)


## Purpose

The purpose of this repository is to provide reusable components for the [ManageIQ](http:github.com/manageiq/manageiq) 
project. These are not general purpose components, but specific to ManageIQ, however, reusable across all of 
ManageIQ (providers). The intention is to provide components that are reusable in various ways. Many of these components
are 'Smart Components' that know how to communicate to backend endpoints(data-driven by provider) and retrieve relevant data for 
the component's configuration.

As we achieve greater reuse, the idea is to move more and more components to this repository. Creating a repository for
*smart* reusable components (specific to a domain) across providers.

## Architectural Goals

* Separate git repository from ManageIQ
* Components communicate via REST with ManageIQ API
* Maintain routing inside ManageIQ (routes.rb)

## Technologies

* Angular 1.5+ (soon to be Angular 2.x)
* Typescript
* Webpack
* Npm Libraries 
* Bower (soon to be removed and replaced with npm/yarn)

## Architecture

![ManageIQ UI Components Architecture](MiQ-UI-Architecture.jpg)

## Angular 1.5 Components

We are recommending [Angular 1.5 Components](https://docs.angularjs.org/guide/component) instead of Angular Directives
for better compatibility and easier upgrade to Angular 2.0.

For a great overview of using Angular 1.5.x Components please see: [NG-Conf 2016: Components, Components, Components!...and Angular 1.5 - Pete Bacon Darwin](https://www.youtube.com/watch?list=PLOETEcp3DkCq788xapkP_OU-78jhTf68j&v=AMwjDibFxno&ab_channel=ng-conf)


## Development Environment

You need to have installed [Node.js >= 6  and npm >= 3](https://docs.npmjs.com/getting-started/installing-node) on your system.
It is recommended to use a node version manager such as [n](https://www.npmjs.com/package/n). If you have node installed then it is 
just `npm install -g n` and then `n lts` to use the latest LTS version of node (see the doces for switching versions).

Install these node packages globally in the system
```
npm install -g typings bower webpack wiredep-cli typescript typescript-formatter
```

Install local node dependencies
```
npm install
```

To run:
```
npm start
```

To run tests:
```
npm t
```

Before submitting code, run the following command to format the code according to the tslint rules:
```
tsmft -r
```

This formats the code according to the tslint rules.

#### Documentation

If you want to see documentation for each component, controller, filter, etc. run
```
npm run-script build-docs
```
This will generate docs from JS docs and after running `npm start` this documentation will be available on `localhost:4000/docs`
