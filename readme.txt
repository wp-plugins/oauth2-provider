=== OAuth2 Complete For WordPress ===

Contributors: justingreerbbi
Donate link: http://justin-greer.com/donate
Tags: oauth2, OAuth provider, Provider, OAuth, OAuth client, Single Sign On, SSO
Requires at least: 3.7
Tested up to: 3.9.1
Stable tag: 2.0.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Your site will be able provided Single Sign On and also deliver authorized user data using the built in OAuth 2.0 Daft 20.

== Description ==

OAuth2 Complete is a ONE OF A KIND plugin that instantly turns your WordPress website into a valid OAuth v2 Provider. The plugin is built using OAuth2 Draft 20 standards. The backend is designed or extremely easy use for any level of experience. OAuth is a great tool but leaves most developers behind since it a bit technical.
The plugin has already done the hard part for you.

Current Features Features:

* Allows for Single Sign On Abilities
* Backend Panel for adding Apps/Clients
* 3 Methods pre built in to allow for a plug and play system

== Installation ==

1. Upload `ouath2-complete` to the `/wp-content/plugins/` directory or use the built in plugin install by WordPress
1. Activate the plugin through the 'Plugins' menu in WordPress
1. Click 'Settings' and then 'permalinks'. Then simply click 'Save Changes' to flush the rewrite rules so that OAuth2 Provider
1. Your Ready to Rock

== Frequently Asked Questions ==

= How do I add a APP/Client? =

Visit the OAuth2 Complete dashboard by clicking `Provider` in the WordPress admin panel. Once you are in the dashboard there is a form to label `Add a Client`. Give your client a name and a redirect URI. The redirect URI is the HTTP location where the user will be returned to after authenticating (Your client should provide this for you). Click `Add Client` and you will that the client has been added to your Client Manager.

= How does a client connect to my website to use the Single Sign On? =

Currently there is 3 Methods that OAuth2 Provider has built in:

1. http://example.com/oauth/authorize

1. http://example.com/oauth/request_token

1. http://example.com/oauth/request_access

Authorize requires only 3 parameters:

* client_id
* response_type - Supported value's = `code`
* state
* Example call `http://example.com/oauth/authorize?client_id=the_client_id&state=anything_you_want&response_type=code`

Request Token Requires only 4 parameters

* code - This is auth code returned from the authorize call
* grant_type - Supported value's = `authorization_code`
* client_id
* client_secret
* Example call `http://example.com/oauth/request_token?code=the_auth_key_sent_back_from_the_authorize_call&grant_typ=authorization_code&client_id=the_client_id&client_secret=the_client_secret`

Request Access Requires only 1 parameter

* access_token - This is the access_token provided from the Request Token call
* Example Call `http://example.com/oauth/request_access?access_token=the_token_from_the_request_call`


NOTE: All returns will be in JSON format.

= Is there support for this plugin? Can you help me? =

You can visit our <a href="http://justin-greer.com/forums/forum/wordpress-oauth2-provider-plugin/" title="WordPress OAuth2 Provider Plugin">support forum</a> for support. Although it takes the hard part away from dealing with OAuth it will require some knowledge on your behalf. I am glad to help as much as reasonably possible but there has to be a line drawn somewhere.

= Can you set this up for me on my current website? =

Can I? "YES". But thats a different story. You are more than welcome to contact us with if you should ever need assistance.

= What information does the a authorized client have access to? =

By default OAuth2 Provider delivers <strong>ALL</strong> the information about the user that logged in. We are planning on adding a easy to use dashboard to limit data. 
EDIT: The plugin does not return the users name password as of 2.0. This was recommend and patched by Joel Wickard.

= Do you have a tutorial I can follow ? =

Not really but I do provide a sample PHP client that can be downloaded at https://github.com/justingreerbbi/wordpress-oauth. The client shows you how to connect to to your WordPress site after installing this plugin. It also gives basic example of how to store sessions, gather data, and other basic functionalities to get you up and going as soon as possible.

== Upgrade Notice ==

When Upgrading OAuth2 Provider I seriously recommend creating a backup of your site. I will try to create updates that will be flawless. Hopefully any future updates will not change to the point where it will stop working. All updates will be ran through multiple tests before being released.
== Screenshots ==

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
