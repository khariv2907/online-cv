# About
CV - Khariv Ivan

Last updated 24.07.2021

[Go to CV](https://khariv2907.github.io/cv/)
# Usage
[Install bundler](https://jekyllrb.com/docs/installation/ubuntu/)

[Run server locally](https://help.github.com/en/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll)
## Building site locally
```bash
sudo apt-get install ruby-full build-essential zlib1g-dev

echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

gem install jekyll bundler
```
## Run site locally
```bash
bundle exec jekyll serve
```
## Install WkHtmlToPdf
[Go to official site](https://wkhtmltopdf.org/)
## Build PDF
#####1. Switch to cv-pdf branch
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