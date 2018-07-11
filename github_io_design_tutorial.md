
### Built with Jekyll
Jekyll is a simple, blog-aware, static site generator. It takes a template directory containing raw text files in various formats, runs it through Markdown and Liquid converters, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your project's page, blog, or website from GitHub's servers for free (taken from Jekyll's website: http://jekyllrb.com/docs/home/).

### Get your workstation set up
* Install Ruby
* Install RubyGems , preferably not in root
* Install Nodejs (Optional)
* Install Jekyll using the shell command 'gem install jekyll bundler'

### Basic Usage (recommended)
In one terminal, build the jekyll site, watching for any changes (run in site root directory)
```
$  jekyll build --watch
```
In another terminal, start a local server (run in site root directory)
```
$  jekyll serve
```
If you're running Mac and your pages aren't rebuilding, then you may need to run
```
$ jekyll serve --force_polling
```
View the site in your browser at
```
localhost:4000/msr-student-template/
```

## Adding Images
For now, images need to be manually formatted into a square aspect ratio.  No scaling for small images is performed, so images under 500px may throw off the template for higher resolution screens.  On the to-do list.


## File structure
```
|-- README.md (this)
|-- _config.yml (overall configuration file for the site)
|-- _includes (all the markup partials)
|   |-- footer.html
|   |-- head.html
|   |-- header.html
|-- _layouts (page markup templates)
|   |-- about.html
|   |-- contact.html
|   |-- main.html
|   |-- project.html
|-- _projects (markdown files that make up the "projects" jekyll collection)
|   |-- 2014-09-22-project-1.md
|   |-- 2014-09-23-project-2.md
|   |-- 2014-09-24-project-3.md
|   |-- 2014-09-25-project-4.md
|   |-- 2014-09-26-project-5.md
|   |-- 2014-09-27-project-6.md
|   |-- 2014-09-28-project-7.md
|   |-- 2014-09-29-project-8.md
|-- _site (the entire site after it is processed by Jekyll)
|   |-- README.md
|   |-- about
|   |-- contact
|   |-- feed.xml
|   |-- index.html
|   |-- projects
|   |-- public
|-- about.md (about page markdown)
|-- contact.md (contact page markdown)
|-- feed.xml (contains general information about Jekyll's usage)
|-- index.html (home page of the site)
|-- public (static content including fonts, images, js, and css files)
|   |-- fonts
|   |-- images
|   |-- javascripts
|   |-- stylesheets
```

### The Jekyll Engine
First, if you look inside the \_site directory, you'll see that no directories or files there begin with an underscore (\_). The contents of that directory are the end result of Jekyll's processing engine. All of the files and directories in the root directory of the repository that do begin with an underscore, on the other hand, are "raw". They either include markup that will be included within pages of the final site or they contain markdown and "Front Matter" (which I'll explain later) that will be converted into markup by Jekyll's engine. One of the two commands that you need to run in order to host the site on a local server:
```
jekyll build --watch
```
runs that engine, processing and reprocessing the "raw" files every time you make a change to a file. The files and directories in the root directory of the repository that _don't_ begin with an underscore are ignored by Jekyll and will remain the exact same in the _site directory.
