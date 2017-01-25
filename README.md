# GNUSim8085 website

How to build and run the site locally

Create a Gemfile containing following two lines

* gem "github-pages", group: :jekyll_plugins
* gem "jekyll-theme-hacker"

~~~ bash
$ sudo apt-get install jekyll
$ sudo apt-get install bundler
$ bundle install
$ jekyll build
$ jekyll serve
~~~
Open link http://127.0.0.1:4000/ in browser
