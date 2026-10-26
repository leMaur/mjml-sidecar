# Changelog

All notable changes to `mjml-sidecar` will be documented in this file.

## 1.1.101 - 2026-10-26

### What's Changed

* Bump the Lambda's `mjml` dependency from 4.x to 5.4.1. This clears every advisory `npm audit` reported for the 4.x tree (`mj-include` directory traversal in mjml, `html-minifier` ReDoS, `lodash` prototype pollution, `brace-expansion`/`minimatch`/`picomatch`/`braces` ReDoS).
* Add `cssnano` as a direct Lambda dependency. mjml 5 minifies with `htmlnano`, which cannot resolve the `cssnano` copy mjml-core nests under its own `node_modules`, so `minify: true` silently skipped CSS minification.
* Regenerate `lambda/package-lock.json` and the committed `lambda/node_modules`.

Note: mjml 5 ignores `mj-include` by default (`ignoreIncludes: true`). `spatie/mjml-php` keeps sending `ignoreIncludes: false`, so behaviour is unchanged for that client.

## 1.1.100 - 2026-10-26

### What's Changed

* The Lambda handler awaits `mjml2html`, which is asynchronous from mjml 5 on. With mjml 4 the await is a no-op. This tag still ships mjml 4.x; use 1.1.101 for the mjml 5 tree.

## 1.1.99 - 2026-05-19

### What's Changed

* Add Laravel 13 to the `illuminate/contracts` constraint.

## 1.1.1 - 2025-07-14

### What's Changed

* Bump dependabot/fetch-metadata from 2.3.0 to 2.4.0 by @dependabot[bot] in https://github.com/spatie/mjml-sidecar/pull/14
* Support Laravel 12 by @danielboendergaard in https://github.com/spatie/mjml-sidecar/pull/16

### New Contributors

* @danielboendergaard made their first contribution in https://github.com/spatie/mjml-sidecar/pull/16

**Full Changelog**: https://github.com/spatie/mjml-sidecar/compare/1.1.0...1.1.1

## 1.1.0 - 2025-03-27

### What's Changed

* Bump aglipanci/laravel-pint-action from 2.3.0 to 2.3.1 by @dependabot in https://github.com/spatie/mjml-sidecar/pull/4
* Bump dependabot/fetch-metadata from 1.6.0 to 2.0.0 by @dependabot in https://github.com/spatie/mjml-sidecar/pull/6
* Bump aglipanci/laravel-pint-action from 2.3.1 to 2.4 by @dependabot in https://github.com/spatie/mjml-sidecar/pull/7
* Bump dependabot/fetch-metadata from 2.0.0 to 2.1.0 by @dependabot in https://github.com/spatie/mjml-sidecar/pull/8
* Bump dependabot/fetch-metadata from 2.1.0 to 2.2.0 by @dependabot in https://github.com/spatie/mjml-sidecar/pull/9
* Bump dependabot/fetch-metadata from 2.2.0 to 2.3.0 by @dependabot in https://github.com/spatie/mjml-sidecar/pull/10
* Bump aglipanci/laravel-pint-action from 2.4 to 2.5 by @dependabot in https://github.com/spatie/mjml-sidecar/pull/11
* run CI with 8.3, 8.4, L11, L12 too by @Nielsvanpach in https://github.com/spatie/mjml-sidecar/pull/13

### New Contributors

* @Nielsvanpach made their first contribution in https://github.com/spatie/mjml-sidecar/pull/13

**Full Changelog**: https://github.com/spatie/mjml-sidecar/compare/1.0.1...1.1.0

## 1.0.1 - 2023-10-27

### What's Changed

- Bump actions/checkout from 3 to 4 by @dependabot in https://github.com/spatie/mjml-sidecar/pull/2
- Bump stefanzweifel/git-auto-commit-action from 4 to 5 by @dependabot in https://github.com/spatie/mjml-sidecar/pull/3

**Full Changelog**: https://github.com/spatie/mjml-sidecar/compare/1.0.0...1.0.1

## 1.0.0 - 2023-08-25

- initial release

## 0.0.1 - 2023-08-23

- Initial release

**Full Changelog**: https://github.com/spatie/mjml-sidecar/commits/0.0.1
