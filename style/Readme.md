# Style

A guide for programming in style.

Use [Hound](https://houndci.com) to automatically review your code and comment on GitHub pull requests for violations of the Ruby portions of this style guide.

## Git

* Squash multiple trivial commits into a single commit.
* Write a [good commit message](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html).

## Formatting

* Avoid inline comments.
* Break long lines after 80 characters.
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
* Use empty lines around multi-line blocks.
* Use spaces around operators, after commas, after colons and semicolons, around ```{``` and before ```}```.
* Use [uppercase for SQL key words and lowercase for SQL identifiers](http://www.postgresql.org/docs/9.2/static/sql-syntax-lexical.html#SQL-SYNTAX-IDENTIFIERS).

## Naming

* Avoid abbreviations.
* Avoid types in names (```user_array```, ```CalculatorClass````).
* Name the enumeration parameter the singular of the collection.
* Name variables, methods, and classes to reveal intent.
* Treat acronyms as words in names (```XmlHttpRequest``` not ```XMLHTTPRequest```), even if the acronym is the entire name (class ```Html``` not class ```HTML```).

## Organization

* Order methods so that caller methods are earlier in the file than the methods they call.
* Order methods so that methods are as close as possible to other methods they call.

## CSS/Sass

### Formatting

* Use the _Scss_ syntax
* Use hyphens when naming mixins, extends, classes, functions & variables: ```span-columns``` not ```span_columns``` or ```spanColumns```.
* Use space between property and value: ```width:``` 20px not ```width:20px```.
* Use a blank line above selector that has styles.
* Prefer hex color codes ```#000```.
* Use ```//``` for comment blocks not ```/* */```.
* Use a space between selector and ```{```.
* Use singe quotation marks for attribute selectors and property values.
* Use only lowercase, including colors.
* Don' add a unit specification after ```0``` values, unless required by mixin.

### Order

* Use alphabetical order for declarations.
* Place @extends and @includes at the top of your declaration list.
* Place media queries directly after the declaration list.
* Place concatenated selectors second.
* Place pseudo states and elements third.
* Place nested selectors last.

### Selectors

* Don't use ID's for style.
* Use meaningful names: ```$visual-grid-color``` not ```$color``` or ```$vslgrd-clr```.
* Use ID and class names that are as short as possible but as long as necessary.
* Append the prefix js- to ID's that are used by Javascript.
* Avoid using the direct descendant selector >.
* Avoid nesting more than 4 selectors deep.
* Don't nest more than 6 selectors deep.
* Use HTML tags on vague classes that need a qualifier like ```header.application``` not ```.main```.
* Avoid using the HTML tag in the class name: ```section.news``` not ```section.news-section```.
* Avoid using HTML tags on classes for generic markup ```<div>```, ```<span>```: ```.widgets``` not ```div.widgets```.
* Avoid using HTML tags on classes with specific class names like ```.featured-articles```.
* Avoid using comma delimited selectors.
* Avoid nesting within a media query.

### Organization

* Use [Foundation](http://foundation.zurb.com) as grid framework and Sass Library
* Use HTML structure for ordering of selectors. Don't just put styles at the bottom of the Sass file.
* Prefer the same file structure that is found in app/views.
* Avoid having files longer than 100 lines.

## CoffeeScript

* Initialize arrays using ```[]```.
* Initialize empty objects and hashes using ```{}```.
* Use hyphen-separated filenames, such as ```coffee-script.coffee```.
* Use ```PascalCase``` for classes, ```lowerCamelCase``` for variables and functions, ```SCREAMING_SNAKE_CASE``` for constants, ```_single_leading_underscore``` for private variables and functions.
* Prefer ```is``` and ```isn't``` to ```==``` and ```!=```.
* Prefer ```or``` and ```and``` to ```||``` and ```&&```.

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
* Use ```PascalCase``` for classes and modules, ```snake_case``` for variables and methods, ```SCREAMING_SNAKE_CASE``` for constants.
* Use ```def self.method```, not ```def Class.method``` or ```class << self```.
* Use ```def``` with parentheses when there are arguments. Omit the parentheses when the method doesn’t accept any arguments.
* Use ```each```, not ```for```, for iteration.
* Use the JSON style hash syntax instead of hashrockets.
* Use heredocs for multi-line strings.

## ERb
* When wrapping long lines, keep the method name on the same line as the ERb interpolation operator and keep each method argument on its own line.
* Prefer double quotes for attributes.

## HTML
* Prefer double quotes for attributes.

## Rails

* Avoid ```member``` and ```collection``` routes.
* Use private instead of protected when defining controller methods.
* Name date columns with ```_on``` suffixes.
* Name datetime columns with ```_at``` suffixes.
* Name initializers for their gem name.
* Order ActiveRecord associations alphabetically by attribute name.
* Order ActiveRecord validations alphabetically by attribute name.
* Order controller contents: filters, public methods, private methods.
* Order i18n translations alphabetically by key name.
* Order model contents: constants, macros, public methods, private methods.
* Put application-wide partials in the ```app/views/application``` directory.
* Use the default ```render 'partial'``` syntax over ```render partial: 'partial'```.

### Routes

* Avoid the ```:except``` option in routes.
* Order resourceful routes alphabetically by name.
* Use the ```:only``` option to explicitly state exposed routes.

### Email

* Use one ```ActionMailer``` for the app. Name it ```Mailer```.

### Testing/RSpec

* Avoid the ```private``` keyword in specs.
* Order ActiveRecord association tests alphabetically by attribute name.
* Order ActiveRecord validation tests alphabetically by attribute name.
* Prefer ```eq``` to ```==```.
* Seperate setup, exercise, verification, and teardown phases with newlines.
* Prefer [```let``` and ```let!```](http://stackoverflow.com/questions/5359558/when-to-use-rspec-let/5359979#5359979) to ```before```.
* Use RSpec's [```expect syntax```](http://myronmars.to/n/dev-blog/2012/06/rspecs-new-expectation-syntax).
* Use ```not_to``` instead of ```to_not``` in RSpec expectations.
* Use [contexts to organize](http://betterspecs.org/#contexts) your tests.
* Use 'should' to prefix ```it``` block descriptions.
* Name outer ```describe``` blocks after the method under test. Use ```.method``` for class methods and ```#method``` for instance methods.

#### Factories

* Order ```factories.rb``` contents: sequences, traits, factory definitions.
* Order factory definitions alphabetically by factory name.
* Use one ```factories.rb``` file per project.

## Objective-C

* Use [objective-clean](http://objclean.com) for automated style checking.
* Use the Netflower's ```StyleSettings.plist``` contained in the ```lib``` directory as the configuration file.
