# Apermo AdminBar #
* Contributors: apermo
* Tags: admin bar, admin, development, staging
* Requires at least: 4.0
* Tested up to: 4.5.3
* Stable tag: 0.9.4
* License: GNU General Public License v2 or later
* License URI: http://www.gnu.org/licenses/gpl-2.0.html

This plugin lets allows you to add links between a development, staging and live version of your website, and adds them to the AdminBar

## Description ##

This plugin alters the AdminBar and adds links to development, staging and live version of your website, furthermore it allows you to choose a color scheme of your AdminBar for all users on a website, including the frontend

If you want to participate in the development [head over to GitHub](https://github.com/apermo/apermo-adminbar)!

## Installation ##

1. Upload the plugin files to the `/wp-content/plugins/apermo-adminbar` directory, or install the plugin through the WordPress plugins screen directly.
2. Activate the 'Apermo AdminBar' plugin through the 'Plugins' menu in WordPress
3. Open Settings -> Apermo AdminBar to set up the links and colors (currently you have to repeat this on all sites)

## Frequently Asked Questions ##

### How can I help with the development of this plugin? ###
Head over to the [GitHub Repository](https://github.com/apermo/apermo-adminbar) and start reading. Every bit of help is highly appreciated!

### I have more than 3 sites, can I add more? ###
You can do so with `add_filter( 'ap-ab-type', 'your_filter' );`

### I want more color schemes! ###
Feel free to add more, there are other plugins that do so. Or have a look at [wp_admin_css_color() in the WordPress Codex](https://codex.wordpress.org/Function_Reference/wp_admin_css_color)

### Can I save the color schemes to my theme? ###
Yes, you can. Simply add and alter the following example somewhere to the functions.php of your theme

```
add_filter( 'apermo-adminbar-sites', 'sites_filter' );

function sites_filter( $sites ) {
    $sites['dev']['url'] = 'http://dev.your-site.tld';
    $sites['staging']['url'] = 'http://staging.your-site.tld';
    $sites['live']['url'] = 'https://www.your-site.tld';
    return $sites;
}
```

## Changelog ##

### 0.9.4 ###
* added an export and import option
* minor improvements

### 0.9.3 ###
* Removed Scheme URL from saved options
* added filter 'apermo-adminbar-sites' to give the option of saving the settings in a theme

### 0.9.2 ###
* Some minor code improvements

### 0.9.1 ###
* Bug fixes and optimizations - Thanks to @kau-boy for the help

### 0.9.0 ###
* Initial Release