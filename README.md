Cartolacote documentation
=========================

Requirements
------------

* sudo apt-get install python3-sphinx
* sudo apt install make
* sudo apt-get update
* sudo apt install python3-pip
* pip3 install PyStemmer

Installation
------------

```bash
git clone https://github.com/sitnyon/cartolacote-documentation.git cartolacote-documentation
mkdir cartolacote-docs-build
cd cartolacote-docs-build
git clone https://github.com/sitnyon/cartolacote-documentation.git html
cd html
git branch gh-pages
git symbolic-ref HEAD refs/heads/gh-pages
rm .git/index
git clean -fdx
touch .nojekyll
cd ../../cartolacote-documentation/docs
make html
``` 