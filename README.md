# ttag for pre-commit

Helps to create a pre-commit hook that can use ttag for checking translations.

For pre-commit: see https://github.com/pre-commit/pre-commit

For ttag: see https://ttag.js.org/

Inspired by https://github.com/pre-commit/mirrors-eslint

## Using eslint with pre-commit
Add this to your .pre-commit-config.yaml:

- repo: https://github.com/solarmonkey/pre-commit-ttag
    rev: 1.7.19 # only version now, may change later
    hooks:
      - id: ttag
        args: ["check", "./frontend/i18n/nl.po", "./frontend/app/"]
        stages: [push]
        always_run: true
