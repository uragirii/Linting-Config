# Linting Config

This repository contains my personal configuration file for ESLint and Prettier. Both are Linters and I use the VS Code extensions for them also

I'm following the Airbnb's Javascript Styling Guide as a refrence but also turning off some of the rules that I don't want (See [.eslintrc.json](.eslintrc.json) file)

## Commands
First, install some dev dependencies

```
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node
```
After this, install the peer dependencies for `eslint-config-airbnb`
```
npx install-peerdeps --dev eslint-config-airbnb
```

## Files
Either download or save the `.eslintrc.json` & `.prettierrc.json` files or just copy paste from down

### `.prettierrc.json`
```
{
  "semi": false,
  "singleQuote": true
}
```

### `.eslintrc.json`
```
{
  "extends": ["airbnb", "prettier", "plugin:node/recommended"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "object-shorthand": "off",
    "class-methods-use-this": "off"
  }
}
```

## Comments
If you want to dont throw error on `console.log` statements, just set another flag in rules: `"no-console": "off"`

I like to be warned when I'm using `console.log`s just to be reminded to remove them after debugging. Also, I will update the list depending on my requirements, and feel free to fork it to tune it according to your own.

Although I don't like using classes in Javascript, i'm setting class methods to false. For `prettier` I've have enabled format on save in VS Code to true.

## References

- ESLint Rules : https://eslint.org/docs/rules/
- Prettier Options : https://prettier.io/docs/en/options.html
- Airbnb Style Guide : https://github.com/airbnb/javascript
- eslint-config-airbnb : https://www.npmjs.com/package/eslint-config-airbnb
