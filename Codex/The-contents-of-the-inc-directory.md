WordPress theme custom functions are defined in `functions.php`. To make maintenance and the creatino of child themes easier, Largo splits its custom founctions out into separate files in the `/inc` directory. 

## Miscellaneous functions:

- `ad-codes.php`: If you have the [Ad Codes Manager](http://wordpress.org/extend/plugins/ad-code-manager/) plugin installed, this provides:
	- some additional whitelisting
	- ad tag locations for Largo
- `cached-core-functions.php`: caches the `wp_nav_menu` for all tag and category pages used in the nav menus, and tracks when the nav menus were last edited
- `custom-feeds.php`:
	- creates a full-text RSS feed
	- creates a feed for easy Mailchimp RSS import, using `feed-mailchimp.php` from the template directory (the root directory of the Largo theme). 
- `custom-less-variables.php`: If Custom LESS is enabled in *Appearance &gt; Theme Options &gt; Advanced*, then `functions.php` includes this file. 
	- compiles custom LESS
	- provides UI for testing and publishing custom LESS
- `dashboard.php`: customizes admin dashobard for members and nonmembers
	- adds "Recent Stories from INN Members" for members, an RSS feed from http://feeds.feedburner.com/INNMemberInvestigations
	- adds "Project Largo Help" for members and nonmembers, a series of Project Largo links
	- adds "INN Network News" for members and nonmembers, an RSS feed from http://feeds.feedburner.com/INNArticles
	- adds Largo log to login page
	- adds Largo credit line to admin footer
	- hides the Link Manager menu item that []was deprecated in WordPress 3.5](http://codex.wordpress.org/Links_Manager) but supported for legacy reasons
- `editor.php`: 
- `enqueue.php`: 
- `featured-content.php`: 
- `header-footer.php`: 
- `home-template-functions.php`: 
- `home-templates.php`: 
- `images.php`: 
- `largo-plugin-init.php`: 
- `metabox-api.php`: 
- `nav-menus.php`: 
- `open-graph.php`: 
- `picturefill`: 
- `post-meta.php`: 
- `post-tags.php`: 
- `post-templates.php`: 
- `related-content.php`: 
- `robots.php`: 
- `sidebars.php`: 
- `taxonomies.php`: 
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


