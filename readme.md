# AddQuicktag
This plugin make it easy, Quicktags add to the html - and visual-editor.

## Description
This plugin for WordPress make it easy, Quicktags add to the html - and visual-editor.. It is possible to ex- and import your Quicktags.

WP-AddQuicktag for WordPress is in originally by [Roel Meurders](http://roel.meurders.nl/ "Roel Meurders"). The versions of the Repo to AddQuicktag are newer versions, completly rewrite with version 2.0.0 and more functionalities.

The plugin add the quicktag on default to post types/ID `post`, `page` and `comment`. If you will also the plugin for other post types you can use a filter; see the follow example, an example plugin in the [Gist 1595155](https://gist.github.com/1595155) or use an example plugin iside this repo, the files end with `.example`.

	// add custom function to filter hook 'addquicktag_post_types'
	add_filter( 'addquicktag_post_types', 'my_addquicktag_post_types' );
	/**
	 * Return array $post_types with custom post types
	 * 
	 * @param   $post_type Array
	 * @return  $post_type Array
	 */
	function my_addquicktag_post_types( $post_types ) {
		
		$post_types[] = 'edit-comments';
		
		return $post_types;
	}

Also it is possible to filter the pages inside the backend. On default was the scripts include the pages `post.php`, `post-new.php` and `comment.php`. The follow example change this for an another page.

	add_filter( 'addquicktag_pages', 'my_addquicktag_pages' );
	/**
	 * Return array $page with custom page strings
	 * 
	 * @param   $page Array
	 * @return  $page Array
	 */
	function my_addquicktag_pages( $page ) {
		
		$page[] = 'edit-comments.php';
		
		return $page;
	}

See this Gist als example for add the Quicktags to the editor of comments: [Gist: 3076698](https://gist.github.com/3076698).
If you need the functionality, that the Quicktags of this plugin works on the Quickedit of comments as well, remove the `.example`-part of `addquicktag_quickedit_comment.php.example` filename. The file is a stand alone helper plugin for Add Quicktag and you'll need to activate this file (plugin) separately in 'Manage Plugins'.

## Bugs, technical hints or contribute
Please give me feedback, contribute and file technical bugs on this [GitHub Repo](https://github.com/bueltge/AddQuicktag), use Issues.

## Installation
### Requirements
 * WordPress version 3.0 and later (tested at 3.5-Alpha (nightly build))

### Installation
 1. Unpack the download-package
 2. Upload the files to the `/wp-content/plugins/` directory
 3. Activate the plugin through the 'Plugins' menu in WordPress or for the Network, if you will use in Multisite for all Sites
 4. Got to 'Settings' menu and configure the plugin


## Screenshots
 1. [Settings area in WordPress 3.3](https://github.com/bueltge/AddQuicktag/blob/master/screenshot-1.png)
 2. [Settings area in WordPress Network of an Multisite install 3.3](https://github.com/bueltge/AddQuicktag/blob/master/screenshot-2.png)
 3. [HTML Editor with new Quicktags](https://github.com/bueltge/AddQuicktag/blob/master/screenshot-3.png)
 4. [Visual editor with new Quicktags](https://github.com/bueltge/AddQuicktag/blob/master/screenshot-4.png)


## Other Notes
### Acknowledgements
**Thanks to**

 * German Translation by [myself](http://bueltge.de) ;)
 * French translation by [Jean-Michel MEYER](http://www.li-an.fr/blog)
 * Japanese translation by [Yuuichi](http://www.u-1.net/2011/12/29/2498/)

### Licence
Good news, this plugin is free for everyone! Since it's released under the GPL, you can use it free of charge on your personal or commercial blog. But if you enjoy this plugin, you can thank me and leave a [small donation](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=6069955 "Paypal Donate link") for the time I've spent writing and supporting this plugin. And I really don't want to know how many hours of my life this plugin has already eaten ;)

### Translations
The plugin comes with various translations, please refer to the [WordPress Codex](http://codex.wordpress.org/Installing_WordPress_in_Your_Language "Installing WordPress in Your Language") for more information about activating the translation. If you want to help to translate the plugin to your language, please have a look at the .pot file which contains all defintions and may be used with a [gettext](http://www.gnu.org/software/gettext/) editor like [Poedit](http://www.poedit.net/) (Windows) or the plugin [Localization](http://wordpress.org/extend/plugins/codestyling-localization/) for WordPress.

### Contact & Feedback
The plugin is designed and developed by me ([Frank Bültge](http://bueltge.de))

Please let me know if you like the plugin or you hate it or whatever ... Please fork it, add an issue for ideas and bugs.

### Disclaimer
I'm German and my English might be gruesome here and there. So please be patient with me and let me know of typos or grammatical farts. Thanks
