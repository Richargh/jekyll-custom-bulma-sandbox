# Readme

A simple template for your software project documentation that your want to push to Github-Pages based documentation.

## Usage

There are two ways to use this template: check that it works locally with a local Jekyll installation or push it to Github directly :) 
If you do decide to publish to Github-Pages you need to enable it in your Github Repository Settings and for source pick `master branch /docs folder`.

### Local 

1. [Install Ruby](https://www.ruby-lang.org/en/documentation/installation/) version 2.4.0 or above (check with `ruby -v`). I had a lot of fun with this one because macOS comes with an old Ruby version. [Rubyenv](https://github.com/rbenv/rbenv#installation) did wonders for me:
    * `brew install rbenv`  
    * `rbenv init`  
    * Close terminal  
    * `which ruby` should now point to _~/.rbenv/shims/ruby_  
    * `rbenv install -v 2.6.3`
    * `rbenv local 2.6.3`
    * `ruby -v` should now be 2.6.3 for this directory  
2. Go into the docs directory  
  `cd docs`
3. Build the site and make it available on a local server:  
  `bundle exec jekyll serve`
4. Now browse to http://localhost:4000

### Github

Github uses Jekyll to render static site content for Github-Pages. Content in a top-level _docs folder_ or in a _branch gh-pages_ is automatically rendered.

Github does not support all Jekyll plugins however and only supports those it has whitelisted. If you want asciidoc rendering, you need to put it some effort because that plugin is not whitelisted (21. 8. 2019). Because Github does not support it, you need to **set up your own Jekyll** in your build pipeline and render the content yourself.

## About Jekyll

[Jekyll](https://jekyllrb.com) is a static site renderer written in Ruby and most notably it is directly supported by Github. 

### SASS

Jekyll supports the [Sass (syntactically awesome style sheets)](https://sass-lang.com/) preprocessor. 

Sass lets you [use features that don't exist in CSS](https://sass-lang.com/guide) yet like variables, nesting, mixins, inheritance, import&embed and standard math operators like "+, -, /, %". According to the State of CSS the [other popular preprocessors](https://2019.stateofcss.com/technologies/pre-post-processors/) are [PostCSS](https://postcss.org/), [less](http://lesscss.org/) and [stylus](http://stylus-lang.com/).

> Sass supports [two different syntaxes](https://sass-lang.com/documentation/syntax). Each one can import the other, so it's up to you and your team which one to choose.

The most popular syntax is the "SCSS" syntax which uses the file extension `.scss`. It's mostly a **superset of CSS**, so essentially all valid CSS is valid SCSS as well. 

The second syntax, with the file extension `.sass`, was was Sass’s original syntax and still goes by the name "Sass". 

> It [supports all the same features](https://sass-lang.com/documentation/syntax) as "SCSS", but it uses indentation instead of curly braces and semicolons to describe the format of the document.