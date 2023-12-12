[[ Back to All Guidelines ]](../readme.md)

# FE Mobile Guidelines

## Prerequisites
- Choice of IDE
- Choice of Prettier

## Basic Idea of a Crowdbotics Project
(Link to Directory structure in General Guidelines) (common for all BE/FE/Mobile)

## Getting Started
With respect to mobile development, the CB repository has the following folders in every project codebase:
- src
- ios
- android
(add some explanation to above and/or add more details)

### Choice of Language
- Javascript
- Typescript (Recommended)

### Setting up your local development environment
Once you have:
 1. Invitation to CB Dashboard for the project, and
 2. Invitation to "write / push" access to the project Git repository 

Clone the project on your local system (using the `git clone ...` command).

### Recommended Directory Structure
Below is a recommended structure of files and folders that can be followed in most of the projects. There could be elements that don't apply to your project, however, we expect developers to take inspiration from the following and keep your project structure as clean and intutive as possible.

Please keep in mind the reusability, maintainability when designing the architecture.
```
src
├── api
│   ├── authService.ts
│   ├── userProfileService.ts
│   ├── ...
│   └── endpoints.ts
│
├── assets
│   ├── icons
│   ├── images
│   │   (for raster formats like png, jpg, etc.)
│   │
│   ├── svgs
│   │   ├── logo.tsx
│   │   ├── icon-home.tsx
│   │   └── ...
│   │
│   └── index.ts
│       (export above assets under some variable like ALL_ASSETS)
│
├── components
│   ├── atoms
│   │   (tiny reusable components, like form fields, icons, etc.)
│   │
│   ├── molecules
│   │   (combination of atoms)
│   │
│   └── organisms
│       (larger components, like layout wrappers, screen containers, modals, bottom sheets wrappers, etc.)
│
├── configs
│   ├── app-config.ts
│   │   (export some variable like APP_CONFIG having all configurations)
│   └── ...
│
├── constants
│   ├── navigation-route-names.ts
│   └── ...
│
├── contexts
│   (use contexts wisely, don't put all the app data here)
│
├── navigation
│   ├── navigation-stack.tsx
│   └── ...
│
├── screens
│   ├── login.tsx
│   ├── forgot-password.tsx
│   ├── dashboard
│   │   ├── home.tsx
│   │   ├── components
│   │   │   ├── header.tsx
│   │   │   ├── item-listing.tsx
│   │   │   └── ...
│   │   └── ...
│   ├── settings
│   │   ├── profile.tsx
│   │   └── ...
│   └── ...
│
├── types
│   (for typescript projects, global type definitions maintained here)
│
├── utils
│   ├── api-utils.ts
│   ├── date-utils.ts
│   ├── custom-hooks.ts
│   ├── validations.ts
│   └── ...
│   
└── README.md
```

## Best Practices
- Application Security - handling of data
- GitFlow  (including branch naming, mention JIRA ticket with a short message) - link to General Guidelines
- Use dot env
- Component Naming (ScreenHome, AppSelectbox, ModalProductDetails, etc.)
- Indentation (2 spaces preferred - standard across all files)
- Have a global CSS and then component level CSS
- Accessibility Standards
- ...

## Recommended Libraries / Packages
- Redux Toolkit (aka RTK Query) except for file uploads
- Tanstack Query
- React Bootstrap
- Formik
- ...
