[[ Back to All Guidelines ]](../readme.md)

# FE Web Guidelines

## Prerequisites
- Choice of IDE
- Choice of Prettier

## Basic Idea of a Crowdbotics Project
Directory structure (common for all BE/FE/Mobile)


## Getting Started
We have standardized the folder name `frontend` to be used for React Web application codebase.

### Choice of Language
- Javascript
- Typescript (Recommended)

### Setting up your local development environment
Once you have:
 1. Invitation to CB Dashboard for the project, and
 2. Invitation to "write / push" access to the project Git repository 

Clone the project on your local system (using the `git clone ...` command).

If your project already has the `frontend` folder, you can skip the next section (Choice of Build Tool).

### Choice of Build Tool
For the fresh project that you're starting from scratch, it is recommended to use either of the tools below:
- The _old-school_ **Create React App (CRA)**
  - More features and larger ecosystem
  - Recommended *for larger and more complex applications*
- The _modern_ **React + Vite**
  - Simple and fast setup, quicker development
  - Recommended *for smaller and simpler applications*

Once you have made the choice of the build tool that you're going to use, inside the root directory of your project, initialise the react web app project in the `frontend` folder with the command respective to your build tool.

For **Create React App (CRA)**
Use the commands:
```
npx create-react-app frontend
cd frontend
npm start
```
Check the [CRA documentation](https://create-react-app.dev/docs/getting-started/) for more information.

For **React + Vite** 
Use the command (the extra double dash is needed):
```
npm create vite@latest frontend -- --template react
```
You could also use their wizard by using the following command and choose the desired options (please make sure to enter `frontend` for Project Name):
```
npm create vite@latest
```
Check the [React + Vite documentation](https://vitejs.dev/guide/) for more information.

### Recommended Directory Structure
Below is a recommended structure of files and folders that can be followed in most of the projects. There could be elements that don't apply to your project, however, we expect developers to take inspiration from the following and keep your project structure as clean and intutive as possible.

Please keep in mind the reusability, maintainability when designing the architecture.
```
frontend
└── src
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
    │   │   (for raster formats like png, jpg, etc.)
    │   │
    │   ├── styles
    │   │   ├── colors.scss
    │   │   ├── global.scss
    │   │   └── mixins.scss
    │   │
    │   ├── svgs
    │   │   ├── logo.svg
    │   │   ├── icon-home.js
    │   │   └── ...
    │   │
    │   └── index.js
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
    │   
    └── README.md
```

### Web Build Folder
The Crowdbotics projects support the following locations as either places where you can drop your frontend React web build:
- `backend/web_build`
- `public`

## Best Practices
- Application Security - handling of data
- GitFlow
- Use dot env
- Component Naming (ScreenHome, AppSelectbox, ModalProductDetails, etc.)
- Indentation (2 spaces preferred - standard across all files)
- Have a global CSS and then component level CSS
- Accessibility Standards

## Recommended Libraries / Packages
- Redux Toolkit (aka RTK Query) except for file uploads
- Tanstack Query
- Tanstack Table
- React Bootstrap
- Formik
