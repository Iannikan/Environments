# React project set up in VSCODE

## required software

Node >= 8.10 <br/>
npm >= 5.6

## Create React App

```bash
npx create-react-app my-app
```

## set up linter

[Source](https://blog.echobind.com/integrating-prettier-eslint-airbnb-style-guide-in-vscode-47f07b5d7d6a)
Download the Prettier, and ESLint extensions for VSCode <br/>
Install the eslint and prettier libraries into project

```bash
yarn add -D eslint prettier
```

<br/>
install Airbnb config

```bash
npx install-peerdeps --dev eslint-config-airbnb
```

<br/>
install eslint-config-prettier,  eslint-plugin-prettier and  babel-eslint

```bash
yarn add -D eslint-config-prettier eslint-plugin-prettier babel-eslint
```

<br/>
create a .eslint.json file in the projects root directory with the following content

```json
{
  "extends": ["airbnb", "prettier"],
  "parser": "babel-eslint",
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": ["error"]
  }
}
```

<br/>
Addd a .prettierrc file to the projects root directory with the following content

```json
{
  "printWidth": 100,
  "singleQuote": true
}
```

Add the following line to your user settings JSON file
<br/>
"editor.formatOnSave: true
