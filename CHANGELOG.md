## [2.2.1](https://github.com/marslo/google-gruvbox/compare/v2.2.0...v2.2.1) (2026-10-24)

### Bug Fixes

* **google-search**: make the sponsored results heading and advertiser names readable by overriding google's dark and inline text colors ([d1bdf15](https://github.com/marslo/google-gruvbox/commit/d1bdf156e8060a3bee1e1042d72c1ef319fbb641))
  - set the `Sponsored results` heading ( `.L8u9l` ) to `--fg-primary`
  - override the advertiser name's inline `color:#202124` ( `.Aozhyc` ) with `--fg-secondary`

## [2.2.0](https://github.com/marslo/google-gruvbox/compare/v2.1.0...v2.2.0) (2026-10-22)

### Features

* **google-search**, **translate**: extend gruvbox theming to google bar popups, homepage menus, result widgets and translate panels, with refreshed readme screenshots ([c789f62](https://github.com/marslo/google-gruvbox/commit/c789f6262c1142c4b8f9fa7cc87bbca0c9406e93))
  - add an `ogs.google.com` section for the app launcher / account popups, scoped via `stylus-iframe`
  - theme homepage settings, input `+` menu, tooltips and the sticky header
  - recolor show more / view all pills and related-search chips
  - map gm3 color tokens on translate; outline mode chips, current one in cyan
  - refresh readme screenshots and list the popup section in the scope table

### Bug Fixes

* **google-search**: theme the google.com homepage search box, suggestion dropdown and buttons so they match the results page ([634c303](https://github.com/marslo/google-gruvbox/commit/634c303f865cf88947d4d28f70730c9c7bc0e000))

## [2.1.0](https://github.com/marslo/google-gruvbox/compare/v2.0.2...v2.1.0) (2026-10-22)

### Features

* **google-search**: theme and widen google ai mode in both material and redux styles ([74e6241](https://github.com/marslo/google-gruvbox/commit/74e62419404e6f37a9567f7d4c7dc2f9bfa0016a))
  - remap google ai mode color tokens to gruvbox palette vars
  - recolor hardcoded sidebar, thread list and `...` menu highlights
  - widen top nav, response column and input plate to `85vw`
  - use mono font for ai mode input and add `--bg-hover` / `--on-accent` to redux
  - prefer `Titillium Nerd Font Upright` in material sans font stack
* **redux**, **palette**: add a dark / light palette switch to google gruvbox redux by porting the palette-aware material rules, and list userstyles.world installs in readme ([0e902d6](https://github.com/marslo/google-gruvbox/commit/0e902d62b49894f7d4732d3817d0b8e4ab21b3b2))
  - add a `uso` `palette` select with gruvbox `Dark` ( default ) and `Light`
  - port material's palette-aware rules, replacing hardcoded dark colors
  - define the tokens shared rules need in each section's default palette
  - document redux palettes and split install links into github / userstyles.world

### Bug Fixes

* **google-search**: drop empty result card frames and recolor ai highlights with gruvbox blue ([e400a8c](https://github.com/marslo/google-gruvbox/commit/e400a8c3ef526bf3245c316da16cf8dc6a239a8e))
  - collapse `.MjjYud` cards with no visible content, including lazy-load placeholders
  - map the `--jwFC2e` highlight token to gruvbox blue blended into the background

### Documentation

* **readme**, **meta**: document google ai mode across readme, userstyle headers and section comments ([704e1e8](https://github.com/marslo/google-gruvbox/commit/704e1e8bb12b6233a379cf67edb217de2847242b))

## [2.0.2](https://github.com/marslo/google-gruvbox/compare/v2.0.1...v2.0.2) (2026-10-21)

### Bug Fixes

* **translate**: replace light borders and backgrounds with palette colors across chips, panels and language picker ([8ccf019](https://github.com/marslo/google-gruvbox/commit/8ccf0197dbb1a6a48d87bc2e0582da7f48fe40a6))
  - add contrasting text color to Text/Images/Documents/Websites chips
  - theme history/saved panel border, item separators and language pills with `--bg-third`
  - theme history footer and `Manage all activity` link
  - theme history/saved circle buttons and `More translations` divider
  - theme language picker container, header background and border

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
