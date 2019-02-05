# Dot Files

Editor, eslint, prettier, postcss, git, stylelint config files.

## Base

- `.editorconfig` : default
- `.gitattributes` : default
- `.gitignore` : default
- `.stylelintrc.js` : default
- `.prettierrc.js` : default
- `.eslintrc.js` : JavaScript Standard Style

## Edits

Changes from base structure.

### .editorconfig

No edit.

### .gitattributes

No edit.

### .gitignore

Sage, laravel, sails.js, yarn, npm related files added.

### .stylelintrc.js

No edit.

### .prettierrc

`rcVerbose` option removed. Latest version with this option causing error.
Below options change to make it work with eslint configuration.

printWidth: 100
singleQuote: true
trailingComma: 'es5'
bracketSpacing: true
parser: 'babel'
requirePragma: false
proseWrap: 'preserve'
arrowParens: 'avoid'

### .eslintrc.js

Require semicolons instead of ASI (semi)
The professional and modern thing to do is not to omit optional tokens, but to always use them, since explicit > implicit.

```
semi: ['error', 'always'],
```

Require trailing commas for arrays and object when multiline.
This changed coz makes copy paste or changing places mcuh easier.

```
"comma-dangle": [
"error",
{
"arrays": "only-multiline",
"objects": "only-multiline",
"imports": "never",
"exports": "never",
"functions": "never"
}
],
```

Disallow a space before function parenthesis except asyncArrow.
This changed coz prettier do not have option.

```
"space-before-function-paren": [
"error",
{
"anonymous": "never",
"named": "never",
"asyncArrow": "always"
}
],
```

#### Beware of this eslint rules

env

```
env: {
  es6: true,
  node: true,
},
```

globals

```
globals: {
  document: false,
  navigator: false,
  window: false,
},
```

#### Beware of this gitignore rules

package-lock.json
yarn.lock

##### Post CSS Sorting

Post CSS Sorting settings located at .postcss.config.json file.
Post CSS will not look for this file. This should be added to ide settings.
Simple copy paste will be enough.

**IDE Addons**
[sublime](https://github.com/hudochenkov/sublime-postcss-sorting)
[vscode](https://github.com/mrmlnc/vscode-postcss-sorting)

###### Related Links

- [EditorConfig](http://editorconfig.org/)
- [JavaScript Standard Style](https://github.com/standard/standard)
- [gitattributes](https://git-scm.com/docs/gitattributes)
- [gitignore](https://git-scm.com/docs/gitignore)
- [ESLint](https://eslint.org/)
- [Prettier](https://prettier.io/)
- [stylelint](https://stylelint.io/)
- [PostCSS Sorting](https://github.com/hudochenkov/postcss-sorting)
