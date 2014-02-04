# Style

A guide for programming in style.

## Formatting

* Avoid inline comments.
* Break long lines after 100 characters.
* Delete trailing whitespace.
* End each file with a blank newline.
* Don't include spaces after ```(```, ```[``` or before ```]```, ```)```.
* Don't misspell.
* Don't vertically align tokens on consecutive lines.
* If you break up an argument list, keep the arguments on their own lines and closing parenthesis on its own line.
* If you break up a hash, keep the elements on their own lines and closing curly brace on its own line.
* Indent continued lines two spaces.
* Indent private methods equal to public methods.
* Use soft-tabs with a two space indent (no tabs).
* Use an empty line between methods and break up a method into logical paragraphs.
* Use newlines around multi-line blocks.
* Use spaces around operators, after commas, after colons and semicolons, around ```{``` and before ```}```.
* Use [uppercase for SQL key words and lowercase for SQL identifiers](http://www.postgresql.org/docs/9.2/static/sql-syntax-lexical.html#SQL-SYNTAX-IDENTIFIERS).

## Naming

* Avoid abbreviations.
* Avoid types in names (```user_array```).
* Name the enumeration parameter the singular of the collection.
* Name variables, methods, and classes to reveal intent.
* Treat acronyms as words in names (```XmlHttpRequest``` not ```XMLHTTPRequest```), even if the acronym is the entire name (class ```Html``` not class ```HTML```).
* Name variables holding a factory with ```_factory``` (```user_factory```).
* Name variables created by a factory after the factory (```user_factory``` creates ```user```).

## Organization

* Order methods so that caller methods are earlier in the file than the methods they call.
* Order methods so that methods are as close as possible to other methods they call.

## Ruby

* Avoid comments. Write [self-documenting code](http://en.wikipedia.org/wiki/Self-documenting).
* Avoid ternary operators (```boolean ? true : false```). Use multi-line ```if``` instead to emphasize code branches.
* Avoid explicit return statements.
* Avoid using semicolons.
* Don't use spaces after ```!```.
* Don't use ```self``` explicitly anywhere except class methods (```def self.method```) and assignments (```self.attribute =```).
* Don't use ```then``` for multi-line ```if/unless```.
* Don't use ```unless``` with ```else```. Rewrite these with the positive case first.
* Don't use parentheses around the condition of an ```if/unless/while```.
* Don't put a space between a method name and the opening parenthesis.
* Don't use ```||=``` to initialize boolean variables. (Consider what would happen if the current value happened to be false.)
* Prefer conditional modifiers (lines that end with conditionals) when you have a single-line body.
* Prefer ```detect``` over ```find```.
* Prefer ```inject``` over ```reduce```.
* Prefer ```map``` over ```collect```.
* Prefer ```select``` over ```find_all```.
* Prefer single quotes for strings.
* Use ```||=``` freely to initialize variables.
* Use ```_``` for unused block parameters.
* Use ```%{}``` for single-line strings needing interpolation and double-quotes.
* Use ```&&``` and ```||``` for Boolean expressions.
* Use ```{...}``` for single-line blocks. Use ```do..end``` for multi-line blocks.
* Use ```?``` suffix for predicate methods.
* Use ```!``` suffix for potentially "dangerous" methods (i.e. methods that modify self or the arguments, etc.). Bang methods should only exist if a non-bang method exists.
* Use ```CamelCase``` for classes and modules, ```snake_case``` for variables and methods, ```SCREAMING_SNAKE_CASE``` for constants.
* Use ```def self.method```, not ```def Class.method``` or ```class << self```.
* Use ```def``` with parentheses when there are arguments. Omit the parentheses when the method doesn’t accept any arguments.
* Use ```each```, not ```for```, for iteration.
* Use the JSON style hash syntax instead of hashrockets.
* Use heredocs for multi-line strings.
