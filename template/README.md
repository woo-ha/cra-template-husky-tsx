# 🥕 Create React App Husky TSX Template

Create React App template with husky and lint-staged to automate prettier and eslint configured.
This template allows user to
This template is focused on simplicity by removing non-critical files including test files from `npx create-react-app --template typescript`.

## Getting Started

### install

```ts
// When you want to create a folder with the name you created
npx create-react-app [foldername] --template husky-tsx

// When you want to create files in the current folder
npx create-react-app --template husky-tsx .
```

### Prettier

The pre-set Prettiter format is as follows. You can change Prettier format as you want.

```json
{
  "bracketSpacing": true,
  "jsxBracketSameLine": false,
  "jsxSingleQuote": true,
  "singleQuote": true,
  "proseWrap": "preserve",
  "semi": true,
  "printWidth": 100,
  "endOfLine": "lf",
  "useTabs": false,
  "tabWidth": 2,
  "trailingComma": "all",
  "arrowParens": "always"
}
```

### ESLint

The pre-set ESLint format is as follows. You can change Eslint format as you want.

```json
{
  "env": {
    "es2021": true,
    "browser": true
  },
  "extends": [
    "eslint:recommended",
    "prettier",
    "plugin:react/recommended",
    "plugin:@typescript-eslint/recommended"
  ],
  "parser": "@typescript-eslint/parse",
  "plugins": ["react", "@typescript-eslint"],
  "rules": {
    "no-var": "error",
    "no-multiple-empty-lines": "error",
    "no-console": ["warn", { "allow": ["warn", "error", "info"] }],
    "eqeqeq": "error",
    "dot-notation": "error",
    "no-unused-vars": "error"
  }
}
```

###

## Available Default Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

### `npm run postinstall`

Run `husky install` to install husky in the current project and set up Git hook.

Husky creates a Git hook setup file in the project's .git directory and activates it. This will allow you to automate code checking, formatting, and test runs later using Git hooks such as pre-commit, pre-push, etc.

The husky install command is a step in initializing and setting Husky to a project, where you can then add or modify a hook-related script within the .husky directory to configure the desired behavior.

### `npm run format`

Run `prettier --ignore-path .gitignore --write 'src/**/*.{ts,tsx,scss,css,json} --cached` to format the code all files that have changed.

This command performs prefix formatting for files with extensions .ts, .tsx, .scss, .css, .json within the src directory. However, the path and file specified in the .gitignore file are excluded from formatting. This helps to respect Gitignore rules while applying code formatting. It also skips files that have not changed quickly without having to re-examine them.

### `npm run lint`

Run `eslint --ext .js,.jsx,.ts,.tsx src --color --cached` to apply ESLint rules for JavaScript and TypeScript files.

This command applies ESLint rules for JavaScript and TypeScript files within the src directory and checks for code style and potential errors. Only files with extensions .js, .jsx, .ts, .tsx are scanned, so other files within the project are ignored. Also, use the --color option to display the results more readable. It also skips files that have not changed quickly without having to re-examine them.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
