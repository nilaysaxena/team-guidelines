# FE Web Development

## Prerequisites
Choice of IDE
Choice of Prettier

## Basic Idea of a Crowdbotics Project
Directory structure (common for all BE/FE/Mobile)

## Getting Started
Create a folder called "frontend"

### Choice of Build Tools
The _old-school_ **Create React App (CRA)** (More features and larger ecosystem)
The _modern_ **React + Vite** (Simple and fast setup, quicker development)

### Choice of Language
Javascript
Typescript (Recommended)

### Directory Structure
Below is a recommended structure of files and folders that can be followed in most of the projects. There could be elements that don't apply to your project, however, we expect developers to take inspiration from the following and keep your project structure as clean and intutive as possible.

Please keep in mind the reusability, maintainability when designing the architecture.
```
src
├── api
│   ├── authService.js
│   ├── userProfileService.js
│   ├── ...
│   └── endpoints.js
│
├── assets
│   ├── fonts
│   ├── icons
│   ├── images
│       (for raster formats like png, jpg, etc.)
│   ├── styles
│   │   ├── colors.scss
│   │   ├── global.scss
│   │   └── mixins.scss
│   │
│   ├── svgs
│   │   ├── colors.scss
│   │   ├── global.scss
│   │   └── mixins.scss
│   │
│   └── index.js
│       (export above assets under some variable like ALL_ASSETS)
│
├── components
│   ├── atoms
│       (tiny reusable components, like form fields, icons, etc.)
│   ├── molecules
│       (combination of atoms)
│   └── organisms
│       (larger components, like layout wrappers, page containers, modals, etc.)
│
├── configs
│   ├── app-config.js
│   │   (export some variable like APP_CONFIG having all configurations)
│   └── ...
│
├── constants
│   ├── auth-route-names.js
│   ├── unauth-route-names.js
│   └── ...
│
├── contexts
│   (use contexts wisely, don't put all the app data here)
│
├── routes
│
├── screens
│   ├── login.js
│   ├── forgot-password.js
│   ├── dashboard
│   │   ├── home.scss
│   │   ├── home.js
│   │   ├── widget-one.js
│   │   ├── widget-two.js
│   │   └── ...
│   ├── settings
│   │   ├── profile.js
│   │   └── ...
│   └── ...
│
├── types
│   (for typescript projects, global type definitions maintained here)
│
├── utils
│   ├── api-utils.js
│   ├── date-utils.js
│   ├── custom-hooks.js
│   ├── validations.js
│   └── ...
│
├── routes.js
│   (authenticated/unauthenticated route definitions)
└── README.md
```

## Best Practices
Application Security - handling of data
GitFlow
Use dot env
Component Naming (ScreenHome, AppSelectbox, ModalProductDetails, etc.)
Indentation (2 spaces perferred - standard across all files)
Have a global CSS and then component level CSS
Accessibility Standards

## Recommended Libraries / Packages
Redux Toolkit (aka RTK Query) except for file uploads
Tanstack Query
Tanstack Table
React Bootstrap
