# setting-up-atom-for-rails-development

using Atom Package Manager (apm) to install packages.

#### Base linter
apm install linter
apm install linter-ruby
apm install linter-scss-lint
apm install linter-coffeelint
apm install linter-rubocop
apm install linter-haml

#### nicer code
apm install atom-beautify
apm install atom-css-comb

#### testing
apm install ruby-test
apm install cucumber
apm install cucumber-step # open the step definition

#### language highlighting
apm install language-rspec
apm install language-haml
apm install language-docker

#### other
apm install minimap # Shows you a tiny preview of the file on the right
apm install Sublime-Style-Column-Selection # Allows you to select columns
apm install toggle-quotes
apm install trailing-spaces

#### Install dependencies for some of the packages.

1. gem install scss-lint
2. gem install rubocop
3. gem install coffee-script
4. npm install -g coffeelint
5. rbenv rehash # if you use rbenv

#### Edit Atom config (~/.atom/config.cson).

"ruby-test":
  specFramework: "rspec"
  rspecAllCommand: "bundle exec rspec --tty spec"
  rspecFileCommand: "bundle exec rspec --tty {relative_path}"
  rspecSingleCommand: "bundle exec rspec --tty {relative_path}:{line_number}"
  cucumberAllCommand: "bundle exec cucumber --color features"
  cucumberFileCommand: "bundle exec cucumber --color {relative_path}"
  cucumberSingleCommand: "bundle exec cucumber --color {relative_path}:{line_number}"
"linter-rubocop":
  command: "/Users/[yourname]/.rbenv/shims/rubocop"
