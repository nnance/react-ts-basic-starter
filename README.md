# react-ts-basic-starter
React TypeScript prototype template

This is a sample project setup with a minimal tooling setup.  The build tooling is entirely based on TypeScript and uses SystemJS for loading dependencies in the browser.  Project setup is naive and not intended for production use cases but is great for prototypes as it is a minimal setup.

This README will also explain step-by-step how you can set up this repository so you can understand how each component fits together.

## Getting Started

The following steps are how to build and run the development server.

### Building the repo

```
npm run build
```

### Running build in watch mode
```
npm run build:watch
```

### Running the development server
To run the development mode in live reload.  Run the build in watch mode as described above and run the following command at the same time.
```
npm run server
```

## How to setup a similar project
Below are a couple of options which includes a one liner as well as a roll your own.  In both cases I recommend adding the commands to the package json file.

### Fastest option
```
mkdir my-npm-pkg && cd my-npm-pkg
/bin/bash -c "$(curl -fsSL https://gist.githubusercontent.com/nnance/43a4c529877efaf54e68f0ecabb0013c/raw/261e977cc75a7d9a9d992a78dcfc3ea9e6446804/create-react-ts.sh)"
```

### Initialize the project
```
mkdir my-npm-pkg && cd my-npm-pkg
git init && npm init -y
```
### Install dev dependencies
This project only uses npm for development dependencies
```
npm i -D  @types/react @types/react-dom live-server typescript
```
### Initialize TypeScript
```
tsc --init --module system --moduleResolution node --jsx react --sourceMap --esModuleInterop --target es5 --lib es6,dom --outFile ./dist/index.js
```
### Download the following files
```
curl https://raw.githubusercontent.com/nnance/react-ts-basic-starter/master/.gitignore > .gitignore
curl https://raw.githubusercontent.com/nnance/react-ts-basic-starter/master/index.html > index.html
curl https://raw.githubusercontent.com/nnance/react-ts-basic-starter/master/index.tsx > index.tsx
```
### Add the following commands to package.json
```json
"build": "tsc",
"build:watch": "tsc --watch",
"server": "live-server --ignorePattern=.ts --ignore=./node_modules",
```
### Happy coding
See the Getting Started section to start the project in development mode.