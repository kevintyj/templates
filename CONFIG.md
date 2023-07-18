# Config for vanilla TS project

### Uses Vite, TS, SCSS, ESLint, Prettier, Stylelint, SCSS, Husky, Lint Staged, Commitlint

Create using npm

```bash
npm create vite
```

Add ESLint, Prettier, and integrations

```bash
pnpm i eslint \
    eslint-config-prettier \
    eslint-plugin-prettier \
    eslint-plugin-vue \
    eslint-plugin-html \
    prettier
```

Initialize ESLint config

```bash
npm init @eslint/config
```

> JSON config was used for ease of use

Add `.prettierignore`

```
# Artifacts
build
dist
coverage

# Packages
**/.git
**/node_modules
```

Add `.eslintrc.json`

```json
{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": [
    "standard-with-typescript",
    "plugin:@typescript-eslint/recommended",
    "plugin:@typescript-eslint/recommended-requiring-type-checking",
    "prettier"
  ],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module",
    "project": "./tsconfig.json"
  },
  "plugins": [
    "@typescript-eslint",
    "prettier"
  ],
  "rules": {
    "prettier/prettier": "error",
    "@typescript-eslint/no-non-null-assertion": "off"
  }
}
```

Add `.eslintignore`

```
# Artifacts
build
dist
coverage
```

Add `.prettierrc.json`

```json
{
  "tabWidth": 2,
  "useTabs": true,
  "semi": true,
  "singleQuote": true,
  "trailingComma": "es5",
  "jsxBracketSameLine": true
}
```

Add [stylelint](https://stylelint.io/user-guide/get-started/)

```bash
npm init stylelint
```

Add [stylelint-prettier](https://github.com/prettier/stylelint-prettier)

```bash
pnpm install --save-dev stylelint-prettier prettier
```

Add `stylelintrc.json`

```json
{
  "extends": [
    "stylelint-prettier/recommended",
    "stylelint-config-standard"
  ]
}
```

Add [stylelint-scss](https://www.npmjs.com/package/stylelint-scss)

```bash
pnpm install --save-dev stylelint-scss
```

Modify `.stylelintrc.json`

```json
{
  "plugins": [
    "stylelint-scss"
  ],
  "extends": [
    "stylelint-prettier/recommended",
    "stylelint-config-standard"
  ],
  "rules": {
    "at-rule-no-unknown": null,
    "scss/at-rule-no-unknown": true
  }
}
```

Add SCSS

```bash
pnpm install --save-dev sass
```

Add Husky & Lint Staged

```bash
pnpm install --save-dev husky lint-staged
```

Setup Husky

```bash
pnpm dlx husky-init && pnpm install
```

Add Commitlint

```bash
pnpm i --save-dev @commitlint/{cli,config-conventional}
```

Add `.commitlintrc.json`

```json
{
  "extends": [
    "@commitlint/config-conventional"
  ]
}
```

