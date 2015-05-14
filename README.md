# docs-spring-cloud-services
Documentation for Spring Cloud Services Product

# Running Locally

1. on OSX, install xcode command line tools ```xcode-select --install```

1. Install rbenv, ruby 2.0.0-p481, bundler, and bookbindery
  
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
  
1. clone this repo and my fork of the main Pivotal CF docs repo so it's folder is sibling to this repo 
  
  ```
git clone git@github.com:pivotal-cf/docs-spring-cloud-services.git
git clone git@github.com:willtran-/docs-book-pivotalcf.git
  ```

1. update the main docs site
  
  ```
cd docs-book-pivotalcf
bookbinder bind local
  ```
  
1. Run the site locally

  ```
cd final_app
rackup
  ```
  
1. Repeat the last 2 steps when you make changes to docs-spring-cloud-services

## Files to change

In docs-book-pivotalcf:
- /master_middleman/source/subnavs/spring_cloud_subnav.erb

In docs-spring-cloud-services:
- All files from the root of this repo



