# Jekyll Boilerplate

A boilerplate for Jekyll with some extra functionalities provided by [Jekyll Assets](https://github.com/ixti/jekyll-assets/) and other plug-ins.

If you need a simpler Jekyll boilerplate following the standard folder structure, [Jekyll Base](https://github.com/danielmcgraw/Jekyll-Base) is a good option.

(<https://github.com/h5bp/html5-boilerplate>)

## Quick start

1. Make sure you have `ruby 1.8.7` or higher installed:

		$ ruby -v

	The answer should be something like: `ruby 1.8.7 (2012-02-08 patchlevel 358) [universal-darwin11.0]`.   
	If you do not have `ruby` installed follow the [Ruby install instructions](http://www.ruby-lang.org/en/downloads/)

2. Install **Jekyll**

		$ sudo gem install jekyll

	Or follow the [Jekyll install instructions](https://github.com/mojombo/jekyll/wiki/install)
	
3. Install **Jekyll Assets**

		$ sudo gem install jekyll-assets

	Or follow the [Jekyll Assets install instructions](https://github.com/ixti/jekyll-assets/#installation)
	
4. Download or clone this repository in your folder.

		$ git clone https://github.com/nalmeida/jekyll-bootstrap.git .

	
5. Run Jekyll

		$ jekyll --server
	

## Features

### Parsing assets trought Jekyll Assets Plugin

- `{{ 'css/main.css' | asset_path }}` Generates de path to file: `/assets/css/main-MD5HASH.css`
- `{{ 'js/main.js' | asset_path }}` Generates de path to file: `/assets/js/main-MD5HASH.js`
- `{{ 'js/lib/jquery/jquery.min.js' | asset_path }}` Generates de path to file: `/assets/js/lib/jquery/jquery.min-MD5HASH.js`
- `{{ 'img/YOUR-IMAGE.jpg' | asset_path }}` Would generates de path to file: /assets/img/YOUR-IMAGE-MD5HASH.jpg **This can and should be used inside SASS and CSS 
files.**

### Listing "Markdown Posts" inside _posts folder

	<ul>
	{% for post in site.posts %}
		<li><span>{{ post.date | date: "%B %e, %Y" }}</span> <a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
	</ul>


## Dependencies

 - [Ruby](http://www.ruby-lang.org/en/downloads/)
 - [Jekyll](https://github.com/mojombo/jekyll): A simple, blog aware, static site generator
 - [Jekyll Assets](https://github.com/ixti/jekyll-assets/): Adds Rails-alike assets pipeline.