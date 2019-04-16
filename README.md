# PHP awesome snippets - VScode extension

This extension provide a fullset of snippets for PHP devs. You can use it to avoid wasting time typing Class blocks, function signatures or other common PHP statements.

The code generated is as compliant as possible with [PSR-1](https://www.php-fig.org/psr/psr-1/), [PSR-2](https://www.php-fig.org/psr/psr-2/) and [PSR-12](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md) (in *Review* stage) coding standard provided by [PHP-FIG](https://www.php-fig.org/).

Snippets are PHP7 oriented (type hinting and return type) but PHP5 compatibility is also provided (see [function](#function-snip) and [method](#method-snip) sections).


This work is inspired by PHPstorm snippets and other works available on VScode marketplace like [PHP Snippets VS Code](https://github.com/heberalmeida/php-snippets) or [PHP Snippet Pack](https://github.com/jm-mwi/vscode-php-snippets/).

## Features

These snippets try to be as intuitive as possible trying to avoid conflicts with previous or built-in snippets.

> Tip: Snippets provided in this extension support 
> `tab` to next/previous placeholder `...` or __*`txtToReplace`*__.


### PHP tags

| Snippet | Output |
| --- | --- |
| php | `<?php ...?>`|
| po | `<?php...`|
| pc | `?>`|
| peco | `<?= ... ?>`|

### Statements and common functions calls

| Snippet | Output |
| --- | --- |
| inc | `include '...';`|
| inco | `include_once '...';`|
| rqr | `require '...';`|
| rqro | `require_once '...';`|
| df | `define("...", "...");`|
| eco | `echo "...";`|
| pr | `print_r(...);`|
| vd | `var_dump(...);`|
| vx | `var_export(...);`|

### <a id="function-snip"></a>Function blocks

> Tip: You can call the snippets below without type hinting 
> and return type (**PHP5 compatible**) by using '-' as prefix ( e.g : `-fna` ).

| Snippet | Output |
| --- | --- |
| fn | `function` __*`func_name`*__`(`__*`Type $args`*__`):` __*`void`*__ `{...}`|
| fna | `function (`__*`Type $args`*__`):` __*`void`*__ `{...}`|
| fnu | `function (`__*`Type $args`*__`) use (`__*`$vars`*__`):` __*`void`*__ `{...}`|


## Requirements

All you need is VScode installed on your machine.

* Install then the extension from the extension menu.

* You can also Press `F1` then type:

    `ext install php-awesome-snippets`

## Extension Settings

No settings needed

## Known Issues

## Release Notes

