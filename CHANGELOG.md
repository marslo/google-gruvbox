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
