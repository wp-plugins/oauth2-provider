=== WP OAuth Server ===

Contributors: justingreerbbi
Donate link: http://justin-greer.com/
Tags: oauth2, OAuth provider, Provider, OAuth, OAuth client, Single Sign On, SSO
Requires at least: 3.9
Tested up to: 4.1
Stable tag: 1.0.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Use WordPress to Power Your OAuth Server and become a OAuth Provider

== Description ==

Support for WP OAuth as been discontinued on WP.ORG and has been moved to WP OAuth. Please visit http://wp-oauth.com for details, support and the plugin itself.

== Installation ==

1. Upload `oauth-provider` to the `/wp-content/plugins/` directory or use the built in plugin install by WordPress
1. Activate the plugin through the 'Plugins' menu in WordPress
1. Click 'Settings' and then 'permalinks'. Then simply click 'Save Changes' to flush the rewrite rules so that OAuth2 Provider
1. Your Ready to Rock

== Frequently Asked Questions ==

== Upgrade Notice ==

== Screenshots ==

1. Adding a Client

== Changelog ==

= 1.0.0 =
* INITIAL BUILD

= 1.0.1 =
* Re-worked Readme.txt
* Fixed absolute paths causing 404 Error when WordPress is running under a sub directory (Using admin_url() currently)

= 1.0.2 = 
* Fixed Broken login redirect

= 1.0.3 =
* Fixed Admin URL links for plugin dashboard

= 2.0.0 =
* Rebuild init plugin code structure for more flexibility and scalability.
* Added prefix to all DB connections
* Changed install query to use the InnoDB engine for better support and performance.
* Fixed improper loading of plugin stylesheet.
* Removed garbage data when plugin is activated. It was not being used and cluttering the codebase as well as the database.
* Move action template_redirect to rewrites file
* Added login form support for installs that are installed in sub directory
* Added missing in documentation for when calling requesting_token
* Suppressed some errors that was preventing a proper JSON return when `WP_DEBUG` was enabled.
* Added a client sample script to help learn the basics of connecting to the provider plugin.
* Add legacy installer that will hopefully keep old data in tacked while updating to the new structure with no data loss.
* Removed plugin logging as it was not really needed and caused more issues that it was worth.

= 3.0.0 =
* Updated and rebuilt structure.
* Visit <a href="http://wp-oauth.com">http://wp-oauth.com</a> for documentation and more information.

= 3.0.1 =
* Updated cover image.
* Fixed documentation links.
* Added "Server Status" tab
* Cleaned up "Advanced Configuration" contents.

= 3.0.2 =
* Readded Authorization Code Enable Option
* API unavaliable error now uses OAuth Response object
* API now reports when access token is not provided during resource calls

= 3.0.3 =
* Modified how clients are added and edited
* Add Pro Features
* Added additional information to "Server Status" Tab
* Minor Clean Up