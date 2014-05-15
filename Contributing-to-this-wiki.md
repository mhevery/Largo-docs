**This wiki is currently a work in progress.**

This wiki is not editable by the general public. To contribute, submit an issue on [INN/Largo-docs](https://github.com/INN/Largo-docs) or make a pull request there. A list of items that need to be completed can be found in [[TODO]].

----------

# Stylebook

## General style

Directories are named in Title Case with dashes joining words..

    Directory-Name
    A-Very-Long-Directory-Name
    Name

Files are named in sentence case with dashes separating words. Dashes will be stripped from the filename and used as the wiki article name. The file extension will be stripped and the file name will become the URL of that page in the wiki. 

    This-is-a-Wiki-Page.md    <- Filename
    This is a Wiki Page       <- Article name
    This-is-a-Wiki-Page       <- URL


## Typography

`h2` and below use sentence case, unless it's a proper noun:

	## This header is not in title case

	## Official Plugin Name is a proper noun

Menu interactions or series of buttons that should be clicked are done *in italics*:

	Enable this feature in *Dashboard &gt; Appearance &gt; Theme Options &gt; Basic Settings*

## Formatting and links

Per the [Gollum wiki](https://github.com/gollum/gollum/wiki), links use double brackets:

    '[[Home]] links to the home page, because the page title is in double brackets.
    '[[This links to the home page as well|Home]]
    '[[What is displayed on the page|What is linked to]]
    '[[Text|http://example.com]] if you don't want to use Markdown
    
# Contributing

Fork [INN/Largo-docs](https://github.com/INN/Largo-docs), make your changes, and submit a pull request. 

Pages are written in [GitHub-Flavored Markdown](https://help.github.com/articles/github-flavored-markdown) with [Gollum](https://github.com/gollum/gollum/wiki) syntax for images and internal links.


