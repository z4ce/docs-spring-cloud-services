# docs-spring-cloud-services
Documentation for Spring Cloud Services Product

# Running Locally

(See also: [&#8220;Streamlined Development Workflow&#8221;](https://github.com/pivotal-cf/docs-book-pivotalcf#streamlined-development-workflow) in [pivotal-cf/docs-book-pivotalcf](https://github.com/pivotal-cf/docs-book-pivotalcf).)

1. On OS X, install Xcode Command Line Tools:

  ```
xcode-select --install
  ```

1. Install rbenv, ruby 2.0.0-p481, bundler, and bookbindery:
  
  ```
brew install rbenv ruby-build

# Add rbenv to bash so that it loads every time you open a terminal
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile

# Install Ruby and bookbinder
rbenv install 2.0.0-p481
rbenv global 2.0.0-p481
gem install bookbindery
  ```
  
1. Clone this repo, `docs-book-scs`, and `docs-layout-repo`.
  
  ```
git clone git@github.com:pivotal-cf/docs-spring-cloud-services.git
git clone git@github.com:pivotal-cf/docs-book-scs.git
git clone git@github.com:pivotal-cf/docs-layout-repo.git
  ```

1. Update the main docs site:
  
  ```
cd docs-book-scs
bookbinder bind local
  ```
  
1. Run the site locally:

  ```
cd final_app
bundle install
rackup
  ```
  
1. Repeat the last two steps when you make changes to docs-spring-cloud-services.

## Files to change

In docs-book-scs:
- /master_middleman/source/subnavs/spring_cloud_subnav.erb

In docs-spring-cloud-services:
- All files from the root of this repo



