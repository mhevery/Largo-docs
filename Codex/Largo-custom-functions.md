**A**

- `largo_acm_default_url( $url )`: Sets a default ad network URL for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Currently a placeholder. Found in `inc/ad-codes.php`.
- `largo_acm_output_html( $output_html, $tag_id )`: Outputs placeholder ads using http://placehold.it/. Found in `inc/ad-codes.php`.
- `largo_acm_output_tokens( $output_tokens, $tag_id, $code_to_display )`: Demo function to assign values to output tokens for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Found in `inc/ad-codes.php`.
- `largo_acm_whiltelisted_script_urls( $whitelisted_urls )`: Whitelists additional ad network URLs for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Found in `inc/ad-codes.php`
- `_largo_action_wp_update_nav_menu()`: Tracks when nav menus were last edited, to make cache purging for `largo_cached_nav_menu` easier. 
- `largo_ad_tags_ids( $ad_tag_ids )`: Adds ad tags for the [Ad Code Manager plugin](http://wordpress.org/extend/plugins/ad-code-manager/). Found in `inc/ad-codes.php`. 
- `largo_admin_footer_text( $default_text )`: A [filter](http://codex.wordpress.org/Function_Reference/add_filter) that replaces the admin page footer text with "This website powered by <a href="http://largoproject.org">Project Largo</a> from the <a href="http://investigativenewsnetwork.org">Investigative News Network</a> and <a href="http://wordpress.org">WordPress</a>."
- `largo_admin_menu()`: Removes the Link Manager menu item that [was deprecated in WordPress 3.5](http://codex.wordpress.org/Links_Manager)

**C**

- `largo_cached_nav_menu( $args = array(), $prime_cache = false )`: Wrapper function around `wp_nav_menu()` that will cache the wp_nav_menu for all tag/category pages used in the nav menus
- `largo_custom_less_variables_init()`: Sets which LESS files will be combiled into CSS files
	- Default settings:
		- files: 'carousel.less', 'editor-style.less', 'style.less', 'top-stories.less'
		- directories: get_template_directory() . '/less/', get_template_directory_uri() . '/css/'
		- LESS variables: 'variables.less'
	- API functions begin with `largo_clv`:
		- `largo_clv_register_directory_paths( $less_dir, $css_dir_uri )`
		- `largo_clv_register_variables_less_file( $variables_less_file )`
- `largo_custom_login_logo()`: Adds the Largo logo to the login page

**D**

- `largo_dashboard_widgets_member()`: Cleans up dashboard for INN members, if `INN_MEMBER` is set to TRUE in `functions.php`
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
- `largo_dashboard_widgets_nonmember()`: Cleans up Dashboard for nonmembers if `INN_MEMBER` is set to FALSE in `functions.php`
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
- `largo_dashboard_network_news()`: Widget that displays one item from http://feeds.feedburner.com/INNArticles
- `largo_dashboard_member_news()`: Widget that displays three items from http://feeds.feedburner.com/INNMemberInvestigations
- `largo_dashboard_quick_links()`: Links to Largo Project documentation at http://largoproject.org

**F**

- `largo_full_text_feed()`: Creates a full-text RSS feed at hxxp://example.org/?feed=fulltext (even if the site is using excerpts in the main feed)

**M**

- `largo_mailchimp_rss()`: Creates a custom RSS feed for Mailchip's RSS feed import, including thumbnail images. References `/feed-mailchimp.rss`. Use the `*|RSSITEM:IMAGE|*` merge tag in your MailChimp template.



		
