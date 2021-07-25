# CV
Last updated 25.07.2021

[Go to CV website](https://khariv2907.github.io/cv/)

## Links
- [Install bundler (Ubuntu)](https://jekyllrb.com/docs/installation/ubuntu/)
- [About GitHub Pages and Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)
- [Installing and Run Jekyll in Macbook Air M1](https://alexmanrique.com/blog/development/2021/02/05/using-jekyll-in-macbook-air-m1.html)
- [WkHtmlToPdf](https://wkhtmltopdf.org/)

## How to Build
### Ubuntu / WSL
#### Install Ruby and other prerequisites
```bash
sudo apt-get install ruby-full build-essential zlib1g-dev
```

#### Add environment variables
```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

#### Install bundler and jekyll
In you project root directory run:
```bash
gem install jekyll bundler
```

### MacOS (Apple Silicon)
#### Install rbenv
```bash
brew install rbenv

# Verification that rbenv is set up properly
type rbenv 

rbenv init

eval "$(rbenv init -)"
```

Now you should add this `eval "$(rbenv init -)"` to the your `~/.zshrc` file.

#### Install ruby
```bash
rbenv install 2.7.2
rbenv global 2.7.2
```

Check that ruby is installed
```bash
ruby -v
```

#### Install bundler and jekyll
In you project root directory run:

```bash
arch -x86_64 gem install --user-install bundler jekyll
bundle update
bundle install
```


## How to Run
### Ubuntu / WSL
In you project root directory run:
```bash
bundle exec jekyll serve
```

### MacOS (Apple Silicon)
```bash
bundle exec jekyll serve --drafts
```


## Create PDF file
#### Step 1. Switch to the `cv-pdf` branch
```git
git checkout cv-pdf
```
#####2. Run script
###### Windows 10
```bash
cvtopdf.ps1
```
If 'ExecutionPolicy' error appears run command bellow in PowerSchell
```bash
Set-ExecutionPolicy RemoteSigned
```
###### Ubuntu
###### MacOS

##### 3. Copy to master branch
```git
git checkout master
git checkout cv-pdf cv.pdf
```