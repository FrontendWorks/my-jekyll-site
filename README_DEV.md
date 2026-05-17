# Readme for Developer

## Dev Setup

Steps to follow in Ubuntu-20 environment for local development and testing
```
sudo apt update
sudo apt install homebrew
brew install rbenv
echo >> /home/kartz/.zshrc
echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv zsh)"' >> /home/kartz/.zshrc
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv zsh)"
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(rbenv init -)"' >> ~/.zshrc
source ~/.zshrc
rbenv install -l
rbenv install 3.4.9
rbenv global 3.4.9
rbenv local 3.4.9
rbenv rehash
gem install bundler jekyll
bundle install
bundle exec jekyll serve # The site should be available at http://localhost:4000/
```

The _config.yml has an `exclude` attribute where I have added list of files to be excluded from the generated site, which can be double checked by looking into `_site/` after you run `bundle exec jekyll serve` locally on your machine.

# Production Deployment to Github Pages

```
JEKYLL_ENV=production bundle exec jekyll build
# git subtree push --prefix _site origin gh-pages
```