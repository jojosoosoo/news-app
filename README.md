# 프로젝트 생성

- `npx create-react-app ./`
- `npm i normalize.css`
- `npm i @emotion/react`
- `npm i @emotion/styled`

- .prettierrc.json 새 파일 만들기

```json
{
  "singleQuote": false,
  "semi": true,
  "useTabs": false,
  "tabWidth": 2,
  "trailingComma": "all",
  "printWidth": 80,
  "arrowParens": "avoid",
  "endOfLine": "auto"
}
```

- `npm i eslint --dev`
- `npm i eslint-config-react-app --save-dev`
- `npx eslint --init`
- `npm i eslint-config-prettier --save-dev`

- .eslintrc.js

```js
module.exports = {
  env: {
    browser: true,
    es2021: true,
    node: true,
  },
  extends: ["eslint:recommended", "plugin:react/recommended", "prettier"],
  overrides: [
    {
      env: {
        node: true,
      },
      files: [".eslintrc.{js,cjs}"],
      parserOptions: {
        sourceType: "script",
      },
    },
  ],
  parserOptions: {
    ecmaVersion: "latest",
    sourceType: "module",
  },
  plugins: ["react"],
  rules: {
    "react/react-in-jsx-scope": "off",
    "react/prop-types": "off",
    "no-unused-vars": "off",
  },
};
```

- `npm i @babel/plugin-proposal-private-property-in-object --dev`
- `npm i react-router-dom`
