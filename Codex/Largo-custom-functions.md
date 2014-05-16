Sorted alphabetically. If a function is prefixed with "largo," the prefix is ignored. 

**A**

- `largo_acm_default_url( $url )`: Sets a default ad network URL for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Currently a placeholder. Found in `inc/ad-codes.php`.
- `largo_acm_output_html( $output_html, $tag_id )`: Outputs placeholder ads using http://placehold.it/. Found in `inc/ad-codes.php`.
- `largo_acm_output_tokens( $output_tokens, $tag_id, $code_to_display )`: Demo function to assign values to output tokens for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Found in `inc/ad-codes.php`.
- `largo_acm_whiltelisted_script_urls( $whitelisted_urls )`: Whitelists additional ad network URLs for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Found in `inc/ad-codes.php`
- `_largo_action_wp_update_nav_menu()`: Tracks when nav menus were last edited, to make cache purging for `largo_cached_nav_menu` easier. Found in `inc/cached-core-functions.php`. 
- `largo_ad_tags_ids( $ad_tag_ids )`: Adds ad tags for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Found in `inc/ad-codes.php`. 
- `largo_add_mce_plugin( $plugin_array )`: Adds `/js/tinymce/plugins/largo/editor_plugin.js` to the plugin array. Found in `inc/editor.php`
- `largo_add_mce_buttons()`: If the user has enabled rich editing, then this filters `mce_external_plugins` with `largo_add_mce_plugin` and filters `mce_buttons` with `largo_register_mce_buttons`. Found in `/inc/editor.php`.
- `largo_admin_footer_text( $default_text )`: A [filter](http://codex.wordpress.org/Function_Reference/add_filter) that replaces the admin page footer text with "This website powered by <a href="http://largoproject.org">Project Largo</a> from the <a href="http://investigativenewsnetwork.org">Investigative News Network</a> and <a href="http://wordpress.org">WordPress</a>."  Found in `/inc/dashboard.php`.
- `largo_admin_menu()`: Removes the Link Manager menu item that [was deprecated in WordPress 3.5](http://codex.wordpress.org/Links_Manager).  Found in `/inc/dashboard.php`.

**C**

- `largo_cached_nav_menu( $args = array(), $prime_cache = false )`: Wrapper function around `wp_nav_menu()` that will cache the wp_nav_menu for all tag/category pages used in the nav menus. Found in `inc/cached-core-functions.php`. 
- `largo_copyright_message()`: Copyright message for the footer. Found in `/inc/header-footer.php`. 
- `largo_custom_less_variables_init()`: Sets which LESS files will be compiled into CSS files. Found in `inc/custom-less-variables.php`.
	- Default settings:
		- files: 'carousel.less', 'editor-style.less', 'style.less', 'top-stories.less'
		- directories: get_template_directory() . '/less/', get_template_directory_uri() . '/css/'
		- LESS variables: 'variables.less'
	- API functions begin with `largo_clv`:
		- `largo_clv_register_files( $files )`: Register the Less files to compile into CSS files
		- `largo_clv_register_directory_paths( $less_dir, $css_dir_uri )`: Set the file path for the directory with the LESS files and URI for the directory with the outputted CSS.
		- `largo_clv_register_variables_less_file( $variables_less_file )`: Sets the variable.less file
- `largo_custom_login_logo()`: Adds the Largo logo to the login page. Found in `inc/cached-core-functions.php`. 

**D**

- `largo_dashboard_widgets_member()`: Cleans up dashboard for INN members, if `INN_MEMBER` is set to TRUE in `functions.php`. Found in `/inc/dashboard.php`.
	- Removes the following Dashboard widgets:
		- dashboard_plugins
		- dashboard_secondary
		- dashboard_primary
		- dashboard_incoming_links
		- dashboard_recent_comments
		- dashboard_recent_drafts
		- dashboard_quick_press
	- Adds the following Dashboard widgets: 
		- largo_dashboard_network_news
		- largo_dashboard_member_news
		- largo_dashboard_quick_links
- `largo_dashboard_widgets_nonmember()`: Cleans up Dashboard for nonmembers if `INN_MEMBER` is set to FALSE in `functions.php`. Found in `/inc/dashboard.php`.
	- Removes the following Dashboard widgets:
		- dashboard_plugins
		- dashboard_secondary
		- dashboard_primary
		- dashboard_incoming_links
		- dashboard_recent_comments
	- Adds the following Dashboard widgets: 
		- largo_dashboard_network_news
		- largo_dashboard_member_news
		- largo_dashboard_quick_links
- `largo_dashboard_network_news()`: Widget that displays one item from http://feeds.feedburner.com/INNArticles. Found in `/inc/dashboard.php`.
- `largo_dashboard_member_news()`: Widget that displays three items from http://feeds.feedburner.com/INNMemberInvestigations Found in `/inc/dashboard.php`.
- `largo_dashboard_quick_links()`: Links to Largo Project documentation at http://largoproject.org. Found in `/inc/dashboard.php`.

**E**

- `largo_enqueue_js()`: Enqueues JavaScript and CSS assets. For more information on enqueueing, see [wp_enqueue_style](http://codex.wordpress.org/Function_Reference/wp_enqueue_style) and [wp_enqueue_script](http://codex.wordpress.org/Function_Reference/wp_enqueue_script). Found in `/inc/enqueue.php`.
- `largo_enqueue_admin_scripts()`: Enqueues JavaScript and CSS for the admin dashboard. For more information on enqueueing, see [wp_enqueue_style](http://codex.wordpress.org/Function_Reference/wp_enqueue_style) and [wp_enqueue_script](http://codex.wordpress.org/Function_Reference/wp_enqueue_script). Found in `/inc/enqueue.php`.

**F**

- `largo_full_text_feed()`: Creates a full-text RSS feed at hxxp://example.org/?feed=fulltext (even if the site is using excerpts in the main feed). Found in `/inc/custom-feeds.php`.
- `largo_footer_js()`: Social media scripts, loaded in the footer. Found in `/inc/enqueue.php`.
	- Google Plus
	- Twitter
	- Facebook
	
**G**

- `largo_get_featured_posts( $args = array() )`: Gets featured posts, from a customizable taxonomy. Found in `/inc/featured-content.php`.
	- Defaults: 
- `largo_get_the_main_feature()`: Provides "main" feature associated with a post, if there is a feature. Found in `/inc/featured-content.php`.
- `largo_google_analytics()`: Add Google Analytics code to the footer. You must add your GA ID to the theme settings for this to work, in *Appearance &gt; Theme Options &gt; Basic Settings*. Found in `/inc/enqueue.php`.

**H**

- `largo_header()`: outputs the header. Found in `/inc/header-footer.php`.
- `largo_header_js()`: outputs JavaScript that determines which size of the header banner image to load, based on window width. Found in `/inc/enqueue.php`.
- `largo_have_featured_posts()`: Determines if there are any featured posts. Found in `/inc/featured-content.php`.
- `largo_have_homepage_featured_posts()`: Determines if there are any featured posts on the homepage. Found in `/inc/featured-content.php`.

**M**

- `largo_mailchimp_rss()`: Creates a custom RSS feed for MailChimp's RSS feed import, including thumbnail images. References `/feed-mailchimp.rss`. Use the `*|RSSITEM:IMAGE|*` merge tag in your MailChimp template. Found in `/inc/cached-core-functions.php`. 
- `largo_module_shortcode( $atts, $content, $code )`: Adds the shortcode module, used for pullquotes and asides within posts. Included for backwards compatibility; no longer used. Found in `/inc/editor.php`.

**R**

- `largo_register_mce_buttons( $buttons )`: Registers TinyMCE buttons. Found in `/inc/editor.php`.

**S** 

- `largo_scrub_sticky_posts( $after, $before )`: If a post is marked as sticky, this unsticks any other sticky posts on the blog, so that we only have one sticky post at a time. Found in `/inc/featured-content.php`.
- `largo_seo()`: SEO tags for the `<head>`, including noindex and additional Google News tags. Found in `/inc/header-footer.php`.
- `largo_shortcut_icons()`: Outputs favicon and Apple Touch icons for `<head>`. Found in `/inc/header-footer.php`.
- `largo_social_links()`: Outputs a `<li>` for each social media link in the theme options. Found in `/inc/header-footer.php`.

**T**

- `largo_tinymce_config( $init )`: Removes weird span tags inserted by TinyMCE. Found in `/inc/editor.php`.


		
