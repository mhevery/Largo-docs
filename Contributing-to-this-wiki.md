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

    This-is-a-Largo-wiki-page.md    <- Filename
    This is a Largo wiki page       <- Article name
    This-is-a-Largo-wiki-page       <- URL


## Typography

`h2` and below use sentence case, unless it's a proper noun:

	## This header is not in title case
	
	## Official Plugin Name is a proper noun

Menu interactions or series of buttons that should be clicked are done *in italics*:

	Enable this feature in *Dashboard &gt; Appearance &gt; Theme Options &gt; Basic Settings*
	
Functions and filenames use `code tags`

	- `largo_header()`: outputs the header. Found in `/inc/header-footer.php`.

## Formatting and links

Per the [Gollum wiki](https://github.com/gollum/gollum/wiki), links between pages use double brackets around the page title:

    '[[Home]] links to the home page, because the page title is in double brackets.
    '[[A link to this page|Contributing to this wiki]]
    '[[What is displayed on the page|What is linked to]]
    '[[Text|http://example.com]] if you don't want to use Markdown's [text](http://example.com)

<!-- the ' before the [[ is so Gollum doesn't linkify these links. Gollum ignores Markdown escaping conventions -->
    
# Contributing

The easiest way to improve this wiki is to [file an issue](https://github.com/INN/Largo-docs/issues) with your proposed change. Filing an issue requires you to [create a GitHub account](https://github.com/join?return_to=https%3A%2F%2Fgithub.com%2FINN%2FLargo-docs%2Fissues%2Fnew) or use your existing one. 

If you want to take it a bit further, [fork INN/Largo-docs](https://github.com/INN/Largo-docs/fork), make your changes, test them, and submit a pull request. More information about that can be found [here](https://github.com/INN/Largo-docs/tree/master/README.md). 

If you'd rather not create yet another account online, [contact INN directly](http://investigativenewsnetwork.org/contact/). 

Pages are written in [GitHub-Flavored Markdown](https://help.github.com/articles/github-flavored-markdown) with [Gollum](https://github.com/gollum/gollum/wiki) syntax for images and internal links.

## Testing your commit

Testing your changes requires you to push the files to a GitHub Wiki, from the command line. The easiest way to do that is to create a copy of the Largo WordPress theme, enable a wiki there, and then push your edited wiki to your wiki.

1. [Fork the INN/Largo repository.](https://github.com/INN/Largo/fork)
2. Go to https://github.com/yourname/Largo/settings and enable wikis, under "Features".
3. Go to https://github.com/yourname/Largo/wiki and copy the "Clone this wiki locally" link.
4. Go to the directory that has your clone of the Largo-wiki repository. 
5. `git remote add wiki git@github.com:yourname/Largo.wiki.git` where `yourname` is your GitHub user name.
6. `git push -u wiki yourbranch:master` - where `yourbranch` is the branch containing your edits. You're pushing it to the master branch of yourname/Largo/wiki because the only branch displayed on the wiki is the master branch. 
7. Check your edits at https://github.com/yourname/Largo/wiki. 
