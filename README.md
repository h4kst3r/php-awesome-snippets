# PHP Awesome Snippets - VScode extension

[![VScode](https://img.shields.io/badge/Extension-VScode-blueviolet.svg)](https://marketplace.visualstudio.com/items?itemName=hakcorp.php-awesome-snippets)
![Snippets](https://img.shields.io/badge/Type-Snippets-yellow.svg)
![PHP7](https://img.shields.io/badge/PHP-%5E7.0-blue.svg)
![PHP5](https://img.shields.io/badge/PHP-%5E5.4-blue.svg)
[![SemVer](https://img.shields.io/badge/SemVer-1.1.3-%23B71C1C.svg)](https://github.com/h4kst3r/php-awesome-snippets/blob/master/CHANGELOG.md)
[![MIT](https://img.shields.io/badge/License-MIT-%2300C853.svg)](https://github.com/h4kst3r/php-awesome-snippets/blob/master/LICENSE)

[![PSR-1](https://img.shields.io/badge/Standard-PSR--1-%2326A69A.svg)](https://www.php-fig.org/psr/psr-1/)
[![PSR-2](https://img.shields.io/badge/Standard-PSR--2-%2326A69A.svg)](https://www.php-fig.org/psr/psr-2/)
[![PSR-12](https://img.shields.io/badge/Standard-PSR--12-%2326A69A.svg)](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md)

**This [VScode extension](https://marketplace.visualstudio.com/items?itemName=hakcorp.php-awesome-snippets) provide a fullset of snippets for PHP devs. It's pretty simple !**

You can use it to avoid wasting time typing Class blocks, function signatures or other common PHP statements.

![Demo PHP Awesome Snippets](img/snipdemo.gif)

The code generated is **as compliant as possible** with [PSR-1](https://www.php-fig.org/psr/psr-1/), [PSR-2](https://www.php-fig.org/psr/psr-2/) and [PSR-12](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md) (*Review* stage) coding standards provided by [PHP-FIG](https://www.php-fig.org/).

Snippets are PHP7 oriented (type hinting and return type) but PHP5 compatibility is also provided (see [Functions](#function-snip) and [Methods](#method-snip) sections).

This work is inspired by PHPstorm (*PHP Live Templates*) and other works available on VScode marketplace like [PHP Snippets VS Code](https://github.com/heberalmeida/php-snippets) or [PHP Snippet Pack](https://github.com/jm-mwi/vscode-php-snippets/).

## Usage
Type a snippet (or part of it), press `Enter` or `Tab` (if `editor.tabCompletion` set to `true` in your settings) and the snippet will expand just right there.

> ***Tip :*** Snippets provided in this extension support `tab` to next/previous placeholder.

These snippets are meant to work in **PHP context** (VScode file). However there are also available in **Plain Text context** for convenience and PHP tags are available in **HTML** one.

## Features

These snippets try to be **as intuitive as possible** and to avoid conflicts with previous or built-in snippets.

Placeholders are quite *'easy to use'* though some need optimizations.
> ***Tip :*** If you want to use snippets and completion in placeholders 
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
### Superglobals

| Snippet | Output |
| --- | --- |
| gget | `$_GET["..."]` |
| gpost | `$_POST["..."]` |
| gss | `$_SESSION["..."]` |
| gfile | `$_FILES['...']['...']` |
| gcook | `$_COOKIE["..."]` |
| gser | `$_SERVER["..."]` |
| greq | `$_REQUEST["..."]` |
| genv | `$_ENV["..."]` |
| gglob | `$GLOBALS["..."]` |

----
### Arrays

| Snippet | Output |
| --- | --- |
| arr | `[value, value, ...];` |
| ark | `['key' => value, 'key' => value,...]` |
| kv | `'key' => value,` **[1]** |
| va | `value, ` **[1]** |

* **[1]** Addon snippet : use with `arr` or `ark` snippet to add `value` or `key => value` if needed.

----
### Statements and common functions calls

| Snippet | Output |
| --- | --- |
| eco | `echo "...";` |
| inc | `include __DIR__.'...';` |
| inco | `include_once __DIR__.'...';` |
| rqr | `require __DIR__.'...';` |
| rqro | `require_once __DIR__.'...';` |
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

***Tip :*** You can call `functions` snippets above without type hinting and return type (**PHP5 compatibility**) by using **`-`** as prefix.
> * `-fna` for `function ($args) {...}` *(anonymous function block)*

----
### Control structures

| Snippet | Output |
| --- | --- |
| ifb | `if (condition) {...}` |
| ifel | `if (condition) {...} else {...}` |
| ifelif | `if (condition) {...} elseif (condition) {...} else {...}` |
| sw | `switch ($variable) { case 'label': ... break; ... default: ... break; }` |
| cs | `case 'label': ... break;` **[1]** |
| tern | `condition ? if_true : if_false;` |

* **[1]** Addon snippet : use with `sw` snippet to add `case` if needed.

***Tip :*** Other `if ... else` form is also available if needed:
 
> | Snippet | Output |
> | --- | --- |
> | ifen | `if (condition): ... endif;` |
> | ifelen | `if (condition): ... else: ... endif;` |
> | ifelifen | `if (condition): ... elseif (condition): ... else: ... endif;` |

----
### Loops structures

| Snippet | Output |
| --- | --- |
| fore | `foreach ($iterable as $item) {...}` |
| forek | `foreach ($iterable as $key => $item) {...}` |
| forl | `for ($i = 0; $i < $limit; $i++) {...}` |
| wl | `while ($variable <= $limit) {...}` |
| dowl | `do {...} while ($variable <= $limit);` |

***Tip :*** Other loops form is also available if needed: 

> | Snippet | Output |
> | --- | --- |
> | foren | `foreach ($iterable as $item): {...} endforeach;` |
> | forenk | `foreach ($iterable as $key => $item): {...} endforeach;` |
> | forlen | `for ($i = 0; $i < $limit; $i++): {...} endfor;` |
> | wlen | `while ($variable <= $limit): {...} endwhile;` |

----
### Classes, interfaces and traits

| Snippet | Output |
| --- | --- |
| cl | `class ClassName {...}` |
| clx | `class ClassName extends MotherClass {...}` |
| cli | `class ClassName implements Interfaces {...}` |
| clxi | `class ClassName extends MotherClass implements Interfaces {...}` |
| in | `interface InterfaceName {...}` |
| inx | `interface InterfaceName extends Interfaces {...}` |
| trt | `trait TraitName {...}` |

***Tip :*** You can call `Class` snippets above with `abstract` or `final` form by using **`a`** or **`f`** as prefix.
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

***Tip :*** You can call `methods` snippets above with `abstract` or `final` form by using **`a`** or **`f`** as prefix.  
> * `aprof` for `abstract protected function methodName(Type $args): void {...}`
> * `fpubsf` for `final public static function methodName(Type $args): void {...}` 

***Tip :*** You can call `methods` snippets above without type hinting 
and return type (**PHP5 compatibility**) by using **`-`** as prefix.
> * `-apubf` for `abstract public function methodName(parameters) {...}`

----
### Errors

| Snippet | Output |
| --- | --- |
| tryc | `try {...} catch (\Throwable $e) {...}` |
| tryf | `try {...} catch (\Throwable $e) {...} finally {...}` |
| cat | `catch (\Throwable $e) {...}` **[1]** |
| fy | `finally {...}` **[2]** |
| thr | `throw new SomeException("Error statement");` |

* **[1]** Addon snippet : use with `tryc` or `tryf` snippet to add `catch` if needed.
* **[2]** Addon snippet : use with `tryc` snippet to add `finally` if needed.

## Requirements

All you need is VScode installed on your machine.

* Install the extension from `Extensions` menu.

* You can also press `F1` then type:

    `ext install hakcorp.php-awesome-snippets`

## <a id="ext-settings"></a>Extension Settings

The VScode default behavior deactivate IntelliSense suggestions when you're filling placeholders. However if you want to use completion and snippets inside placeholders :

* Open your settings.json file ( **{ }** icon at the top right corner of the settings tab).

* Add this line anywhere you want: `"editor.suggest.snippetsPreventQuickSuggestions": false`

Now you can call snippets and any suggestion in placeholders without typing `Ctrl+space`.

## Known Issues

If suggestions menu does not open, press `Ctrl+space` to open it manually.

Sometimes IntelliSense freezes loading or simply doesn't select the called snippet. Backspace and try again, it should work.

## Release Notes

All notable changes to this project will be documented in [CHANGELOG.md](https://github.com/h4kst3r/php-awesome-snippets/blob/master/CHANGELOG.md).

## License

[MIT](https://github.com/h4kst3r/php-awesome-snippets/blob/master/LICENSE) License