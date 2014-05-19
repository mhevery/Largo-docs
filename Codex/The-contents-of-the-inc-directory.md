	WordPress theme custom functions are defined in `functions.php`. To make maintenance and the creation of child themes easier, Largo splits its custom functions out into separate files in the `/inc` directory. 

## Miscellaneous functions:

- `ad-codes.php`: If you have the [Ad Codes Manager](http://wordpress.org/extend/plugins/ad-code-manager/) plugin installed, this provides:
	- some additional whitelisting
	- ad tag locations for Largo
- `cached-core-functions.php`: 
	- caches the `wp_nav_menu` for all tag and category pages used in the nav menus
	- tracks when the nav menus were last edited
- `custom-feeds.php`:
	- creates a full-text RSS feed
	- creates a feed for easy MailChimp RSS import, using `feed-mailchimp.php` from the template directory (the root directory of the Largo theme). 
- `custom-less-variables.php`: If Custom LESS is enabled in *Appearance &gt; Theme Options &gt; Advanced*, then `functions.php` includes this file. 
	- defines class `Largo_Custom_Less_Variables`
	- compiles custom LESS
	- provides UI for testing and publishing custom LESS
- `dashboard.php`: customizes admin dashboard for members and nonmembers
	- adds "Recent Stories from INN Members" for members, an RSS feed from http://feeds.feedburner.com/INNMemberInvestigations
	- adds "Project Largo Help" for members and nonmembers, a series of Project Largo links
	- adds "INN Network News" for members and nonmembers, an RSS feed from http://feeds.feedburner.com/INNArticles
	- adds Largo log to login page
	- adds Largo credit line to admin footer
	- hides the Link Manager menu item that [was deprecated in WordPress 3.5](http://codex.wordpress.org/Links_Manager) but supported for legacy reasons.
- `editor.php`: Adds the TinyMCE plugin  to insert modules into posts.
- `enqueue.php`: Hooks for JavaScript and CSS.
- `featured-content.php`: 
	- gets the featured posts
	- gets the main feature
	- ensures that there can be only one sticky post
	- determines if there are featured posts on archive pages
	- determines if there are featured posts on the homepage
- `header-footer.php`: Contains the header, the footer copyright text, social links, favicon, SEO tags, and removes some spare elements from `<head>`. 
- `home-template-functions.php`: Functions to get the single post for the home-single template and to get the series posts for the hero-side-series template. 
- `home-templates.php`: Finds homepage templates, finds their thumbnails, loads them.
- `images.php`: Removes `<a>` tags around attachments, returns the home icon, clears the home icon cache. 
- `largo-plugin-init.php`: Registers Largo's required plugins, has example code that can be used by child themes to register required plugins. 
- `metabox-api.php`: Defines the custom post metaboxes in the editor, provides a way to add a field to a metabox container. 
- `nav-menus.php`: Donation button, "Don't Miss" label, footer nav label, enhanced menu walker supporting second-level dropdown menus. 
- `open-graph.php`: Generates the Open Graph tags, and parses Twitter URLs for usernames. 
- `post-meta.php`: 
	- moves the author dropdown to the publish metabox
	- removes some metaboxes from the edit screens
	- shows all (unhides) all the other metaboxes by default
	- adds some custom metaboxes to the post edit screens using the Largo Metabox API in `/inc/metabox-api.php` and provides their contents
- `post-tags.php`: Functions related to the post page: publish time, author name, author link, post byline, post social links, author gravatar image, post pagination, post excerpts, next/previous post, post comments, post-type icon.
- `post-templates.php`: Adds ability to select a custom post template for single posts. 
- `related-content.php`: Functions and the class `Largo_Related` that provide related posts for a post. 
- `robots.php`: Defaults for robots.txt. 
- `sidebars.php`: Registers sidebars, builds a dropdown menu of them.
- `taxonomies.php`: Functions relating to custom taxonomies: 
	- register the prominence and series custom taxonomies
	- determine if a post is in a series
	- output custom taxonomy terms attached to a posts
	- output format for series custom taxonomy at bottom of single posts
	- sort posts in proper landing-page order for a series
	- sort posts featured-first for category archive
- `term-icons.php`: 
- `term-meta.php`: 
- `term-sidebars.php`: 
- `update.php`: 
- `users.php`: 
- `widgets`: 
- `widgets.php`: 
- `wp-taxonomy-landing`: 

## Functions in directories:

- **Customizer**: 
- **Picturefill**: 
- **WP-Taxonomy-Landing**: 

## Widgets:


