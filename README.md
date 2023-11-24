# @kelysty/eslint-config

## Installation

Using `npm`:

```bash
npm install --save-dev eslint @kelysty/eslint-config
```

Using `yarn`:

```bash
yarn add --dev eslint @kelysty/eslint-config
```

## Usage

Add `.eslintrc` file in the project root with the following content:

```json
{
  "extends": ["@kelysty/eslint-config"],
  "root": true
}
```

### Client and Server

On the `client` side:

```json
{
  "extends": "@kelysty/eslint-config/client"
}
```

This ESLint configuration is extending another configuration from the react.js file, indicating that the code should be treated as ECMAScript modules and specifying that the environment is a browser.

On the `server` side:

```json
{
  "extends": "@kelysty/eslint-config/server"
}
```

This ESLint configuration file is tailored for Node.js environments, incorporating security-related rules to help identify and prevent potential security vulnerabilities in the code.

### Prettier

Using prettier don't forget to extend root .eslint file with:

```json
{
  "extends": ["@kelysty/eslint-config", "@kelysty/eslint-config/prettier"],
  "root": true
}
```

This configuration ensures that your ESLint setup aligns with Prettier's formatting conventions, helping you maintain a consistent code style throughout your project

### a11y

If you want to spot accessibility issues, extend root config with the additional rules:

```json
{
  "extends": ["@kelysty/eslint-config", "@kelysty/eslint-config/a11y"],
  "root": true
}
```

this ESLint configuration is tailored for projects that use React and JSX. It enforces recommended accessibility rules provided by the jsx-a11y plugin to help improve the accessibility of your React applications. The goal is to ensure that your UI is usable and understandable by as many people as possible, including those with disabilities

### Order

If you want to enforce a convention in module import order, extend root config with the additional rules:

```json
{
  "extends": ["@kelysty/eslint-config", "@kelysty/eslint-config/import-order"],
  "root": true
}
```

This configuration file is specifying rules related to the order of import statements in your code. It helps maintain a consistent and organized structure for your imports, promoting readability and maintainability
