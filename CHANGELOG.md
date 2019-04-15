# Change Log

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

## [0.1.2](https://github.com/h4kst3r/php-awesome-snippets/compare/v0.1.1...v0.1.2) (2019-04-15)


### Bug Fixes

* **tag.json:** Change escaping for '$' sign avoiding VScode warning ([6d4e9a0](https://github.com/h4kst3r/php-awesome-snippets/commit/6d4e9a0))



## [0.1.1](https://github.com/h4kst3r/php-awesome-snippets/compare/v0.1.0...v0.1.1) (2019-04-15)
* Refactor code by dividing the main php.json in thematic snippets files to improve framework :
    - Tag snippets (open, close, short echo tag...)
    - Statement snippets (echo, define, include...)
    - Function snippets 
    - Global vars snippets ($_POST, $_GET, $_SESSION...)
    - Conditional snippets (if, if-else, if-endif...)
    - Loop snippets (foreach, while, for...)
    - Method snippets (public, private, static...) *PHP7 and PHP5 style*
    - Error snippets (throw, try-catch)

    *Features are incomplete and still in alpha stage with bugs and warnings*


# 0.1.0 (2019-04-15)
* Initial release with all features in alpha stages
* Some bugs : placeholders in superglobal snippets, duplicate placeholders
* Some conflicts with built-in snippets