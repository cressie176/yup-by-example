# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.1.0]
### Updated
- yup peer dependency to ^0.29.0

## [3.0.2]
### Updated
- Export TestDataSession

## [3.0.1]
### Updated
- Improved Readme

## [3.0.0]
### Breaking
- TestDataFactory has been made static and the stub function removed. There is no longer any need to defer schema initialisation behind an init function, although the TestDataFactory must still be initialised before any schema that uses the example method are built.
- The TestDataFactory no longer adds the example method for you. You have to do this explicitly in your schema using
    ```js
    const yupByExample = require('yup-by-example');
    yup.addMethod(mixed, 'example', yupByExample);
    ```
- Generators no longer need to be classes, and will not be instanciated by the factory. They just need to expose a generate method.
- Since generators are no longer instanciated, the chance instance is passed to the generate function.
- session.now has been removed. The now value is passed to generators via the now function.
- yupByExample no longer emits an 'example' event after generating a value (the other events are still emitted').

## [2.2.1]
- Added some keywords
- Improved readme
- Improved test coverage

## [2.2.0]
- Support yup validation and cast options
- Add debug
- Add TestDataSession.consumeProperty

## [2.1.0]
- Added static api for initialising the TestDataFactory

## [2.0.4]
### Updated
- Fixed build issue

## [2.0.3]
### Added
- session.incrementProperty

### Updated
- Fixed example

## [2.0.2]
### Updated
- Readme

## [2.0.1]
### Added
- Code Climate reporting

### Updated
- Readme

## [2.0.0]
### Breaking Changes
- `mixed.example()` now takes an object as its first parameter, with optional parameters `id` and `generator`. The `id` parameter is no longer used to resolve generators.
- `meta.sessionKey` is no longer used. Instead the example id forms the sessionKey.

## [1.1.0]
### Added
- TestDataSession events
- Literal Generators
- Made rel-date parameters optional

## [1.0.2]
### Changed
- Removed unused dev dependency

## [1.0.1]
### Changed
- Replaced Jest (slow) with Mocha (fast)

## [1.0.0]
- Everything!

