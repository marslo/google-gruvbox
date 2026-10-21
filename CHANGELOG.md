## [2.0.1](https://github.com/marslo/google-gruvbox/compare/v2.0.0...v2.0.1) (2026-10-21)

### Code Refactoring

* **css**: convert both userstyles to plain brace css ([499d9aa](https://github.com/marslo/google-gruvbox/commit/499d9aa19b9c95be579e16340a176f3f2b77f747))
  - rewrite stylus indent syntax as standard `{}` css, keeping every comment
  - drop `@preprocessor stylus` from the classic style
  - switch material to the `uso` preprocessor with `html:root` palette overrides
  - inline the `Dark Hard` palette and remove the stylus hash, mixin and `unquote()`
  - keep compiled output identical for all six palettes

### Documentation

* **readme**: describe the plain css and uso palette layout ([5a80962](https://github.com/marslo/google-gruvbox/commit/5a80962dcb766bf6cfae64768ccff3744c2c03fa))

### CI/CD

* **lint**: lint the userstyles as plain css ([0c145f5](https://github.com/marslo/google-gruvbox/commit/0c145f558a539ee351726b7c4f58912a0acdeb9e))
  - drop `postcss-styl` custom syntax and its pre-commit dependency
  - restore the compact `.stylelintrc.json` layout, keeping `c-wiz`
  - keep `styl` as a typos word for the changelog history

## [2.0.0](https://github.com/marslo/google-gruvbox/compare/v1.0.21...v2.0.0) (2026-10-21)

### ⚠ BREAKING CHANGE

* **material:** add `google-gruvbox-material.user.css` for google search and translate, which may break existing styles if users switch to this new style

### Features

* **material**: add gruvbox-material style with switchable palettes ([c5caa30](https://github.com/marslo/google-gruvbox/commit/c5caa3049bdc1354eb009a71cbeafa187d136a21))
  - add `google-gruvbox-material.user.css` for google search and translate
  - switch dark/light × hard/medium/soft via a `Palette` dropdown ( `@var select palette` )
  - map hardcoded colors and google `--m3c*` tokens onto palette variables
  - invert the google apps icon only for dark palettes

### Documentation

* **readme**: convert to markdown and document both styles ([1c21feb](https://github.com/marslo/google-gruvbox/commit/1c21febd2b9141e7e2dccf1a58158b21011c075c))
  - convert `README.org` to markdown
  - list classic, material and upstream styles with install links
  - document palettes, scope and the stylus indentation pitfall

### CI/CD

* **release**, **lint**: adopt semantic-release and pre-commit tooling ([de6c8ca](https://github.com/marslo/google-gruvbox/commit/de6c8ca6d04d2de42c5ff71c02e1b6fb9bb418c7))
  - add semantic-release config bumping `@version` in both userstyles
  - add pre-commit hooks and the pre-commit github workflow
  - lint the stylus-syntax userstyles via stylelint + `postcss-styl`
  - exclude `*.user.css` from typos so obfuscated google class names stay intact
  - seed `CHANGELOG.md` with the `1.0.21` release

## 1.0.21 (2026-10-21)

### Bug Fixes

* **translate**: indent `.qt6jm` so the last translate rules stay scoped to translate instead of applying to every site
