# Change Log

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

# [0.3.0](https://github.com/h4kst3r/php-awesome-snippets/compare/v0.2.0...v0.3.0) (2019-04-16)


### Bug Fixes

* **function.json:** Modify escaping for '$' sign avoiding VScode warnings ([2909561](https://github.com/h4kst3r/php-awesome-snippets/commit/2909561))


### Features

* **function.json:** Add anonymous function snippet - PHP7 and PHP5 ([7347054](https://github.com/h4kst3r/php-awesome-snippets/commit/7347054))
* **function.json:** Add anonymous function with use snippets - PHP7 and PHP5 ([6aa4b68](https://github.com/h4kst3r/php-awesome-snippets/commit/6aa4b68))



# [0.2.0](https://github.com/h4kst3r/php-awesome-snippets/compare/v0.1.2...v0.2.0) (2019-04-15)


### Features

* **statement.json:** Add print_r snippet ([d3caaa0](https://github.com/h4kst3r/php-awesome-snippets/commit/d3caaa0))
* **statement.json:** Add var_export snippet ([6e56781](https://github.com/h4kst3r/php-awesome-snippets/commit/6e56781))
* **statement.json:** Add var_dump snippet ([45d3211](https://github.com/h4kst3r/php-awesome-snippets/commit/45d3211))



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