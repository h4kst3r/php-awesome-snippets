# PHP awesome snippets - VScode extension

[![VScode](https://img.shields.io/badge/Extension-VScode-blueviolet.svg)]()
![Snippets](https://img.shields.io/badge/Type-Snippets-yellow.svg)
![PHP7](https://img.shields.io/badge/PHP-%5E7.0-blue.svg)
![PHP5](https://img.shields.io/badge/PHP-%5E5.4-blue.svg)
[![PSR-1](https://img.shields.io/badge/Standard-PSR--1-%2326A69A.svg)](https://www.php-fig.org/psr/psr-1/)
[![PSR-2](https://img.shields.io/badge/Standard-PSR--2-%2326A69A.svg)](https://www.php-fig.org/psr/psr-2/)
[![PSR-12](https://img.shields.io/badge/Standard-PSR--12-%2326A69A.svg)](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md)
[![MIT](https://img.shields.io/badge/License-MIT-red.svg)](LICENSE)

This extension provide a fullset of snippets for PHP devs. You can use it to avoid wasting time typing Class blocks, function signatures or other common PHP statements.

The code generated is as compliant as possible with [PSR-1](https://www.php-fig.org/psr/psr-1/), [PSR-2](https://www.php-fig.org/psr/psr-2/) and [PSR-12](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md) (*Review* stage) coding standard provided by [PHP-FIG](https://www.php-fig.org/).

Snippets are PHP7 oriented (type hinting and return type) but PHP5 compatibility is also provided (see [Functions](#function-snip) and [Methods](#method-snip) sections).

This work is inspired by PHPstorm (*PHP Live Templates*) and other works available on VScode marketplace like [PHP Snippets VS Code](https://github.com/heberalmeida/php-snippets) or [PHP Snippet Pack](https://github.com/jm-mwi/vscode-php-snippets/).

## Usage
Type a snippet (or part of it), press `Enter` or `Tab` (if `editor.tabCompletion` set to `true` in your settings) and the snippet will expand just right there.

## Features

These snippets try to be as intuitive as possible and to avoid conflicts with previous or built-in snippets.

> ***Tip:*** Snippets provided in this extension support `tab` to next/previous placeholder.

> ***Tip:*** If you want to use snippets and completion in placeholders 
> look at the [Extension settings](#ext-settings) section.

----
### PHP tags

| Snippet | Output |
| --- | --- |
| php | `<?php ...?>` |
| po | `<?php...` |
| pc | `?>` |
| peco | `<?= ... ?>` |

----
### Statements and common functions calls

| Snippet | Output |
| --- | --- |
| eco | `echo "...";` |
| inc | `include '...';` |
| inco | `include_once '...';` |
| rqr | `require '...';` |
| rqro | `require_once '...';` |
| df | `define("...", "...");` |
| pr | `print_r(...);` |
| vd | `var_dump(...);` |
| vx | `var_export(...);` |

----
### <a id="function-snip"></a>Functions

| Snippet | Output |
| --- | --- |
| fn | `function func_name(Type $args): void {...}` |
| fna | `function (Type $args): void {...}` |
| fnu | `function (Type $args) use ($vars): void {...}` |

> ***Tip:*** You can call the `functions` snippets above without type hinting 
> and return type (**PHP5 compatible**) by using **`-`** as prefix.
> * `-fna` for `function ($args) {...}`

----
### Control structures

| Snippet | Output |
| --- | --- |
| ifb | `if (condition) {...}` |
| ifel | `if (condition) {...} else {...}` |
| ifelif | `if (condition) {...} elseif (condition) {...} else {...}` |
| sw | `switch ($variable) { case 'label': ... break; ... default: ... break; }` |
| cs | `case 'label': ... break;` *[1]* |
| tern | `condition ? if_true : if_false;` |

###### *[1]* Addon snippet: use with 'sw' snippet to add `case` if needed.

> ***Tip:*** The others `if` `else` forms are also available if needed:
> 
> | Snippet | Output |
> | --- | --- |
> | ifend | `if (condition): ... endif;` |
> | ifelend | `if (condition): ... else: ... endif;` |
> | ifelifend | `if (condition): ... elseif (condition): ... else: ... endif;` |

----
### Loops structures

| Snippet | Output |
| --- | --- |
| fore | `foreach ($iterable as $item) {...}` |
| forek | `foreach ($iterable as $key => $item) {...}` |
| forl | `for ($i = 0; $i < $limit; $i++) {...}` |
| wl | `while ($variable <= $limit) {...}` |
| dowl | `do {...} while ($variable <= $limit);` |

> ***Tip:*** The others loop forms are also available if needed:
> 
> | Snippet | Output |
> | --- | --- |
> | foren | `foreach ($iterable as $item): {...} endforeach;` |
> | forenk | `foreach ($iterable as $key => $item): {...} endforeach;` |
> | forlen | `for ($i = 0; $i < $limit; $i++): {...} endfor;` |
> | wlen | `while ($variable <= $limit): {...} endwhile;` |

----
### Class, interfaces and trait

| Snippet | Output |
| --- | --- |
| cl | `class ClassName {...}` |
| clx | `class ClassName extends MotherClass {...}` |
| cli | `class ClassName implements Interfaces {...}` |
| clxi | `class ClassName extends MotherClass implements Interfaces {...}` |
| in | `interface InterfaceName {...}` |
| inx | `interface InterfaceName extends Interfaces {...}` |
| trt | `trait TraitName {...}` |

> ***Tip:*** You can call `Class` snippets above with `abstract` or `final` form 
> by using **`a`** or **`f`** as prefix.
> * `acl` for `abstract class ClassName {...}`
> * `fcli` for `final class ClassName implements Interfaces {...}`

----
### <a id="method-snip"></a>Methods

**Constructor**

| Snippet | Output |
| --- | --- |
| pubc | `public function __construct(Type $args) {...}` |
| proc | `protected function __construct(Type $args) {...}` |
| pric | `private function __construct(Type $args) {...}` |

**Method**

| Snippet | Output |
| --- | --- |
|| **Public methods** |
| pubf | `public function methodName(Type $args): void {...}` |
| pubsf | `public static function methodName(Type $args): void {...}` |
|| **Protected methods** |
| prof | `protected function methodName(Type $args): void {...}` |
| prosf | `protected static function methodName(Type $args): void {...}` |
|| **Private methods** |
| prif | `private function methodName(Type $args): void {...}` |
| prisf | `private static function methodName(Type $args): void {...}` |

> ***Tip:*** You can call `methods` snippets above with `abstract` or `final` form 
> by using **`a`** or **`f`** as prefix.  
> * `aprof` for `abstract protected function methodName(Type $args): void {...}`
> * `fpubsf` for `final public static function methodName(Type $args): void {...}` 

> ***Tip:*** You can call the `methods` snippets above without type hinting 
> and return type (**PHP5 compatible**) by using **`-`** as prefix.
> * `-apubf` for `abstract public function methodName(parameters) {...}`

## Requirements

All you need is VScode installed on your machine.

* Install then the extension from the extension menu.

* You can also Press `F1` then type:

    `ext install php-awesome-snippets`

## <a id="ext-settings"></a>Extension Settings

The VScode default behavior deactivate IntelliSense suggestions when you're filling placeholders. However if you want to use completion and snippets inside placeholders :
* Open your settings.json file ( **{ }** icon at the top right corner of the settings tab).

* Add this line anywhere you want: `"editor.suggest.snippetsPreventQuickSuggestions": false`

Now you can call snippets and any suggestion in placeholders without typing `Ctrl+space`.

## Known Issues

Sometimes IntelliSense freezes loading or simply don't find the snippet. Backspace and try again, it should work.

## Release Notes

All notable changes to this project will be documented in [CHANGELOG.md](CHANGELOG.md).