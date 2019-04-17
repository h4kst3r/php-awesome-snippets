# PHP awesome snippets - VScode extension

This extension provide a fullset of snippets for PHP devs. You can use it to avoid wasting time typing Class blocks, function signatures or other common PHP statements.

The code generated is as compliant as possible with [PSR-1](https://www.php-fig.org/psr/psr-1/), [PSR-2](https://www.php-fig.org/psr/psr-2/) and [PSR-12](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md) (*Review* stage) coding standard provided by [PHP-FIG](https://www.php-fig.org/).

Snippets are PHP7 oriented (type hinting and return type) but PHP5 compatibility is also provided (see [function](#function-snip) and [method](#method-snip) sections).


This work is inspired by PHPstorm snippets and other works available on VScode marketplace like [PHP Snippets VS Code](https://github.com/heberalmeida/php-snippets) or [PHP Snippet Pack](https://github.com/jm-mwi/vscode-php-snippets/).

## Features

These snippets try to be as intuitive as possible and to avoid conflicts with previous or built-in snippets.

> ***Tip:*** Snippets provided in this extension support `tab` to next/previous placeholder.

> ***Tip:*** If you want to use snippets and completion in placeholders 
> look at the [Extension settings](#ext-settings) section.

### PHP tags

| Snippet | Output |
| --- | --- |
| php | `<?php ...?>` |
| po | `<?php...` |
| pc | `?>` |
| peco | `<?= ... ?>` |

### Statements and common functions calls

| Snippet | Output |
| --- | --- |
| inc | `include '...';` |
| inco | `include_once '...';` |
| rqr | `require '...';` |
| rqro | `require_once '...';` |
| df | `define("...", "...");` |
| eco | `echo "...";` |
| pr | `print_r(...);` |
| vd | `var_dump(...);` |
| vx | `var_export(...);` |

### <a id="function-snip"></a>Function blocks

> ***Tip:*** You can call the snippets below without type hinting 
> and return type (**PHP5 compatible**) by using **'-'** as prefix ( e.g : `-fna` ).

| Snippet | Output |
| --- | --- |
| fn | `function func_name(Type $args): void {...}` |
| fna | `function (Type $args): void {...}` |
| fnu | `function (Type $args) use ($vars): void {...}` |

## Control structures

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


### Class, interfaces, trait structures

> ***Tip:*** You can call `Class` snippets below with `abstract` or `final` form 
> by using **'a'** or **'f'** as prefix 
> ( e.g : `acl` for `abstract class`, `fcl` for `final class` ).

| Snippet | Output |
| --- | --- |
| cl | `class ClassName {...}` |
| clx | `class ClassName extends MotherClass {...}` |
| cli | `class ClassName implements Interfaces {...}` |
| clxi | `class ClassName extends MotherClass implements Interfaces {...}` |
| in | `interface InterfaceName {...}` |
| inx | `interface InterfaceName extends Interfaces {...}` |
| trt | `trait TraitName {...}` |


## Requirements

All you need is VScode installed on your machine.

* Install then the extension from the extension menu.

* You can also Press `F1` then type:

    `ext install php-awesome-snippets`

## <a id="ext-settings"></a>Extension Settings

The VScode default behavior deactivate IntelliSense suggestions when you're filling placeholders. However if you want to use completion and snippets inside placeholders :
* Open your settings.json file ( **{ }** icon at the top right corner of the setting tab).

* Add this line anywhere you want: `"editor.suggest.snippetsPreventQuickSuggestions": false`

Now you can call snippets and any suggestion in placeholders without typing `Ctrl+space`.


## Known Issues

## Release Notes

