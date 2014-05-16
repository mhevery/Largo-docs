Sorted alphabetically. If a function is prefixed with "largo," the prefix is ignored. 

**A**

- `largo_acm_default_url( $url )`: Sets a default ad network URL for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Currently a placeholder. Found in `inc/ad-codes.php`.
- `largo_acm_output_html( $output_html, $tag_id )`: Outputs placeholder ads using http://placehold.it/. Found in `inc/ad-codes.php`.
- `largo_acm_output_tokens( $output_tokens, $tag_id, $code_to_display )`: Demo function to assign values to output tokens for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Found in `inc/ad-codes.php`.
- `largo_acm_whiltelisted_script_urls( $whitelisted_urls )`: Whitelists additional ad network URLs for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Found in `inc/ad-codes.php`
- `_largo_action_wp_update_nav_menu()`: Tracks when nav menus were last edited, to make cache purging for `largo_cached_nav_menu` easier. Found in `inc/cached-core-functions.php`. 
- `largo_ad_tags_ids( $ad_tag_ids )`: Adds ad tags for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Found in `inc/ad-codes.php`. 
- `largo_add_dont_miss_label( $items, $args )`: Prepends static label to the beginning of the "Don't Miss" header area, as set in *Appearance &gt; Theme Options &gt; Basic Settings*. Found in `/inc/nav-menus.php`. 
- `largo_add_footer_menu_label( $items, $args )`: Prepends static lable to the beginning of the footer menu area, as set in *Appearance &gt; Theme Options &gt; Basic Settings*. Found in `/inc/nav-menus.php`. 
- `largo_add_mce_plugin( $plugin_array )`: Adds `/js/tinymce/plugins/largo/editor_plugin.js` to the plugin array. Found in `inc/editor.php`
- `largo_add_mce_buttons()`: If the user has enabled rich editing, then this filters `mce_external_plugins` with `largo_add_mce_plugin` and filters `mce_buttons` with `largo_register_mce_buttons`. Found in `/inc/editor.php`.
- `largo_add_meta_box( $id, $title, $callbacks = array(), $post_types = 'post', $context = 'advanced', $priority = 'default' )`: Defines a metabox container. Found in `/inc/metabox-api.php`.
- `largo_add_meta_content( $callback, $box_id )`: Adds a field to a metabox container. Found in `/inc/metabox-api.php`.
- `largo_admin_footer_text( $default_text )`: A [filter](http://codex.wordpress.org/Function_Reference/add_filter) that replaces the admin page footer text with "This website powered by <a href="http://largoproject.org">Project Largo</a> from the <a href="http://investigativenewsnetwork.org">Investigative News Network</a> and <a href="http://wordpress.org">WordPress</a>."  Found in `/inc/dashboard.php`.
- `largo_admin_menu()`: Removes the Link Manager menu item that [was deprecated in WordPress 3.5](http://codex.wordpress.org/Links_Manager).  Found in `/inc/dashboard.php`.
- `largo_attachment_image_link_remove_filter( $content )`: Filters `'the_content'` and removes links to attachments. Found in `/inc/images.php`.

**B**

- class `Bootstrap_Walker_Nav_Menu`: Extends `Walker_Nav_Menu`. It's an enhanced mnu walker that supports up to second-level dropdown menus using appropriate markup for Bootstrap. Found in `/inc/nav-menus.php`. 
- `largo_byline_meta_box_display()`: Contents for the byline metabox. Found in `/inc/post-meta.php`. 

**C**

- `largo_cached_nav_menu( $args = array(), $prime_cache = false )`: Wrapper function around `wp_nav_menu()` that will cache the wp_nav_menu for all tag/category pages used in the nav menus. Found in `inc/cached-core-functions.php`. 
- `largo_change_default_hidden_metaboxes( $hidden, $screen )`: Shows all metaboxes in the edit interface by default. Found in `/inc/post-meta.php`. 
- `largo_clear_home_icon_cache( $option )`: Clears the homepage icon cache when options are updated. Found in `/inc/images.php`.
- `largo_copyright_message()`: Copyright message for the footer. Found in `/inc/header-footer.php`. 
- `largo_custom_disclaimer_meta_box_display()`: Content for the Disclaimer metabox. `Found in /inc/post-meta.php`.
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
- `largo_custom_related_meta_box_display()`: Content for the Additional Options metabox. Found in `/inc/post-meta.php`. 

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
- `largo_donate_button()`: Output a donate button, based on theme options. Found in `/inc/nav-menus.php`. 

**E**

- `largo_enqueue_admin_scripts()`: Enqueues JavaScript and CSS for the admin dashboard. For more information on enqueueing, see [wp_enqueue_style](http://codex.wordpress.org/Function_Reference/wp_enqueue_style) and [wp_enqueue_script](http://codex.wordpress.org/Function_Reference/wp_enqueue_script). Found in `/inc/enqueue.php`.
- `largo_enqueue_home_assets()`: Enqueues scripts and styles for the home page. For more information on enqueueing, see [wp_enqueue_style](http://codex.wordpress.org/Function_Reference/wp_enqueue_style) and [wp_enqueue_script](http://codex.wordpress.org/Function_Reference/wp_enqueue_script). Found in `/inc/home-templates.php`. 
- `largo_enqueue_js()`: Enqueues JavaScript and CSS assets. For more information on enqueueing, see [wp_enqueue_style](http://codex.wordpress.org/Function_Reference/wp_enqueue_style) and [wp_enqueue_script](http://codex.wordpress.org/Function_Reference/wp_enqueue_script). Found in `/inc/enqueue.php`.

**F**

- `largo_featured_video_meta_box_display()`: Content for the Featured Video metabox. Found in `/inc/post-meta.php`. 
- `largo_full_text_feed()`: Creates a full-text RSS feed at hxxp://example.org/?feed=fulltext (even if the site is using excerpts in the main feed). Found in `/inc/custom-feeds.php`.
- `largo_footer_js()`: Social media scripts, loaded in the footer. Found in `/inc/enqueue.php`.
	- Google Plus
	- Twitter
	- Facebook
	
**G**

- `largo_get_featured_posts( $args = array() )`: Gets featured posts, from a customizable taxonomy. Found in `/inc/featured-content.php`.
	- Defaults: 
	
		```
		'showposts' => 3,
        'offset' 	=> 0,
        'orderby' 	=> 'date',
        'order' 	=> 'DESC',
        'tax_query' => array(
			array(
				'taxonomy' 	=> 'prominence',
				'field' 	=> 'slug',
				'terms' 	=> 'footer-featured'
			)
		),
        'ignore_sticky_posts' => 1,
        ```

- `largo_get_home_templates()`: Scans theme and parent theme for homepage templates. Returns an array of templates, with friendly names as keys and arrays with 'path' and 'thumb' as values. Found in `/inc/home-templates.php`. 
- `largo_get_home_thumb( $theme, $file )`: Returns the URL of the thumbnail image for a homepage template, or a default `/homepages/no-thumb.png`. Found in `/inc/home-templates.php`. 
- `largo_get_the_main_feature()`: Provides "main" feature associated with a post, if there is a feature. Found in `/inc/featured-content.php`.
- `largo_google_analytics()`: Add Google Analytics code to the footer. You must add your GA ID to the theme settings for this to work, in *Appearance &gt; Theme Options &gt; Basic Settings*. Found in `/inc/enqueue.php`.

**H**

- `largo_have_featured_posts()`: Determines if there are any featured posts. Found in `/inc/featured-content.php`.
- `largo_have_homepage_featured_posts()`: Determines if there are any featured posts on the homepage. Found in `/inc/featured-content.php`.
- `largo_header()`: outputs the header. Found in `/inc/header-footer.php`.
- `largo_header_js()`: outputs JavaScript that determines which size of the header banner image to load, based on window width. Found in `/inc/enqueue.php`.
- `largo_home_hero_side_series()`: Gets the various posts for the homepage hero-side-series template. Found in `/inc/home-template-functions.php`.
- `largo_home_icon( $class='', $size = 'home-logo' )`: If there is a square icon logo, it returns the image. If there is not, it returns `<i class="icon-home ' . esc_attr( $class ) . '"></i>`. Found in `/inc/images.php`. 
- `largo_home_single_top()`: Gets the post to display at the top of the home single template. Found in `/inc/home-template-functions.php`.
- `largo_home_template_path()`: Returns the full path to the HPH file of the current homepage template. Found in `/inc/home-templates.php`. 

**L**

- `largo_layout_meta_box_display()`: Contents for the Layout Options metabox. Found in `/inc/post-meta.php`
- `largo_load_custom_template_functions()`: Loads `/inc/home-template-functions.php`. Found in `/inc/home-templates.php`. 

**M**

- `largo_mailchimp_rss()`: Creates a custom RSS feed for MailChimp's RSS feed import, including thumbnail images. References `/feed-mailchimp.rss`. Use the `*|RSSITEM:IMAGE|*` merge tag in your MailChimp template. Found in `/inc/cached-core-functions.php`. 
- `_largo_meta_box_save( $post_id )`: Private function to handle saving inputs registered with `largo_register_meta_input()`. Found in `/inc/metabox-api.php`.
- `_largo_metaboxes_content( $post, $callbacks = array() )`: Private function to generate fields and mark up within Largo metaboxes. Found in `/inc/metabox-api.php`.
- `_largo_metaboxes_generate()`: Private function to actually generate the metaboxes, via add_action. Found in `/inc/metabox-api.php`.
- `largo_module_shortcode( $atts, $content, $code )`: Adds the shortcode module, used for pullquotes and asides within posts. Included for backwards compatibility; no longer used. Found in `/inc/editor.php`.
- `largo_move_author_to_publish_metabox()`: Moved author dropdown to the "Publish" metabox so it's easier to find. Found in `/inc/post-meta.php`.

**O**

- `largo_opengraph()`: Adds appropriate Open Graph, Twitter Cards, and Google Publisher tags to the header based on the page type displayed. Found in `/inc/open-graph.php`. 

**R**

- `largo_register_mce_buttons( $buttons )`: Registers TinyMCE buttons. Found in `/inc/editor.php`.
- `largo_register_meta_input( $input_names, $presave_fn )`: Call this function from within a `largo_add_meta_field` callback to register an input as a post meta field. Found in `/inc/metabox-api.php`. 
- `largo_register_home_sidebars()`: Registers the sidebars specified in the chosen homepage template, and sets the value for `$largo['home_rail']`. Found in `/inc/home-templates.php`. 
- `largo_register_required_plugins()`: Registers plugins required by Largo, nags logged-in users about it in the Dashboard. Found in `/ing/largo-plugin-init.php`.
- `largo_remove_default_post_screen_metaboxes()`: Hides the tackbacks, slug, revisions, author and comments metaboxes to clean up the post and page edit screens. 

**S** 

- `largo_scrub_sticky_posts( $after, $before )`: If a post is marked as sticky, this unsticks any other sticky posts on the blog, so that we only have one sticky post at a time. Found in `/inc/featured-content.php`.
- `largo_seo()`: SEO tags for the `<head>`, including noindex and additional Google News tags. Found in `/inc/header-footer.php`.
- `largo_shortcut_icons()`: Outputs favicon and Apple Touch icons for `<head>`. Found in `/inc/header-footer.php`.
- `largo_social_links()`: Outputs a `<li>` for each social media link in the theme options. Found in `/inc/header-footer.php`.

**T**

- `largo_tinymce_config( $init )`: Removes weird span tags inserted by TinyMCE. Found in `/inc/editor.php`.
- `largo_top_tag_display()`: Additional content for the Additional Options metabox. Found in `/inc/post-meta.php`. 
- `largo_top_terms_js()`: Loads JavaScript for the top-terms selector in `largo_top_tag_display()`. Found in `/inc/post-meta.php`. 
- `largo_twitter_url_to_username ( $url )`: Takes a Twitter URL, finds the username without the @. Found in `/inc/open-graph.php`.


		
