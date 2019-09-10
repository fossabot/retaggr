# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

- Changed callback to be more comprehensive.
- Changed SauceNao to account for ratelimits properly.
- Changed E621 to accunt for ratelimits properly.
- Changed responses to namedtuples. Namedtuples can be better documented and permit dotted access.
  - Two new classes: ImageResult and ReverseResult.
  - Classes share attributes but differ in types on said attributes.
- Changed search_image in API classes:
  - Removed deprecated search_image
  - Renamed search_image_source to search_image.
  - As a result of this, search_image_source is effectively removed.
- Changed reverse_search in core class:
  - Removed deprecated reverse_search
  - Renamed search_image_source to reverse_search
  - As a result of this, search_image_source is effectively removed.
- Rename all mentions of booru to engine.
  - Renamed NotAValidBooruException to NotAValidEngineException
- Added new helper method to base API to handle ratelimits.
- Added VS Code Build and test tasks.
- Added new package variable: `__version__` and `version_info` to track versioning.
- Added sample `test.sh` for testing purposes.
- Fixed reverse_search to skip saucenao if on long ratelimit in reverse_search


## [1.2.0] - 2019-08-29

- Expanded base engine class to also permit searching for sources.
- Changed base engine class to have default behavior for searching for sources.
- Added SauceNao parser.
- Added source searching to Danbooru.
- Added source searching to E621.
- Added source searching to paheal.
- Removed code cruft.
- Added dedicated exception for options an engine isn't capable of.

## [1.1.1] - 2019-08-20

- Added PyPi dependencies.

## [1.1.0] - 2019-08-20

- Changed output from lists to sets to remove duplicitous items.
- Project released on PyPi.

## [1.0.0] - 2019-08-20

- Added base booru class
- Added Danbooru engine
- Added IQDB engine
- Added E621 engine
- Added paheal engine
- Added documentation
- Licensed project to LGPLv3
- Added core class
- Added config class

[Unreleased]: https://github.com/booru-utils/retaggr/compare/1.2.0...HEAD
[1.2.0]: https://github.com/booru-utils/retaggr/compare/1.1.1...1.2.0
[1.1.1]: https://github.com/booru-utils/retaggr/compare/1.1.0...1.1.1
[1.1.0]: https://github.com/booru-utils/retaggr/compare/1.0.0...1.1.0
[1.0.0]: https://github.com/booru-utils/retaggr/releases/tag/1.0.0