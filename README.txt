=== Custom Add User ===

Contributors: harshit_ps
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=8764J82HE2VBN&lc=US&item_name=Harshit%20Sanghvi&item_number=custom_add_user&currency_code=USD&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted
Tags: custom, user, new, existing, add, promote, single, form, skip, invitation, shibboleth, ldap, activate, invite, expire, multisite, admin
Requires at least: 3.0.1
Tested up to: 4.6
Stable tag: 2.0.2
License: GPLv3 or later
License URI: http://www.gnu.org/licenses/gpl-3.0.html

Completely customize add user page with single form for adding brand new users or existing users in multisite.

== Description ==

This **WordPress plugin** provides completely customized experience for adding users with a **single form** for adding brand `new users` (single site or multisite installs) or `existing users` (in multisite). The users can be added without them requiring `account activation` (which is useful in private multisites where authentication is handled by third party systems such as Shibboleth/ LDAP). It also allows you to add `custom instructions` for adding users to your site.

**Use cases**

In a private multisite installation, you might often face three **_issues_** -

1. If user authentication is handled by external authentication systems such as `LDAP` or `Shibboleth`, you don't want the new user to be '`invited`' to join your site or one of the sites in your network. Instead, you would like to send them a `welcome email` skipping the invitation part which requires them to click the link to activate their account. Since user authentication is not handled by WordPress, it doesn't really make sense for WordPress to validate user activation.

2. When a user (site admin) tries to add another user to a site, an invitation gets sent to the invited user. When that invitation `expires`, the invited user cannot be added to a site for a time period as their username is on hold, which creates a lot of frustration for both - the site admin trying to add people to their site and users trying to access the site after the invitation has expired. Also until the invited user has accepted the invitation, no other site admins can add the same user to a different site in the multisite network. 

3. When a site admin adds a user to a site, the new user is also added to the `network users` table. If any site admin tries to add a user to other sites, they have to _know_ if the user already exists in any of the other sites in the network, for which they might not even have _access_ because only **super admins** can see the list of all users in the network. If the user already exists in the network and they try to add this user using the `'Add New User'` form instead of `'Add Existing User'` form, they will get an **error** saying the user already exists and vice versa. This leads to a lot of confusion among site admins as they have no idea if the user they are trying to add is a brand new or an existing user in the multisite installation.

This plugin addresses all the above issues by -

1. `Skipping` the invitation (activation link) email and automatically adding the user to the site instantly. A welcome email is sent as soon as site admin adds the user. (You can customize the text of `Welcome email` from network settings screen.)

2. `Hiding` the 'Add existing User' form, so that site admins only see one form for adding users.

3. `Handling` the 'brand new user' vs 'existing user' issue in the back-end after site admin submits the form. If the user doesn't exist, the plugin will create a new user and add it to the site. If the user already exists, it will add the user to the site.


== Installation ==

= From your WordPress dashboard =
1. Visit 'Plugins > Add New'
2. Search for 'Custom Add User'
3. Activate or Network Activate (multisite) 'Custom Add User' from your Plugins page.

= From WordPress.org =
1. Download 'custom-add-new'.
2. Upload the 'custom-user-new' directory to your '/wp-content/plugins/' directory, using your favorite method (ftp, sftp, scp, etc...)
3. Activate or Network Activate (multisite) *Custom Add User* from your Plugins page.

= Installing a zip file =
1. Create a zip of `custom-user-new` directory.
2. In the WordPress dashboard, navigate to the *Plugins* -> *Add New* page.
3. Click Upload Plugin.
4. Upload the zip file and click Install Now.
5. Click on *Activate* or *Network Activate* (multisite).

= Copying a Directory =
1. Copy the `custom-user-new` directory into your `wp-content/plugins` directory.
2. In the WordPress Network Admin dashboard, navigate to the *Plugins* page
3. Locate the menu item that reads “Custom New User Page"
4. Click on *Activate* or *Network Activate*  (multisite).

== Frequently Asked Questions ==

= How can I contribute? =

Make Pull requests to github repository.

== Screenshots ==

1. Single form for adding 'new' or 'existing' users with customizable instructions below the form.

== Changelog ==

= 2.0.2 =
* Fix - Adding an existing user should not throw out the errror "Sorry, username already exists."

= 2.0.1 =
* Bug fixes

= 2.0.0 =
* Preparing for WordPress.org release
* Removed bulk user import csv integration
* Single site & multisite compatible
* added custom css for hiding existing user form
* Removed username override

= 1.0.1 =
* Display Bulk User Import from CSV Form on Add User Page.

= 1.0.0 =
* Merged Add new and existing user form.

= 0.1.6 =
* Updated validate user function.

= 0.1.5 =
* Cleaned up obsolete code.

= 0.1.4 =
* Add existing user without confirmation.

= 0.1.3 =
* Configurable error message.

= 0.1.2 =
* Restricts usernames as email address in configurable list of domains.

= 0.1.1 =
* Minimized custom code.

= 0.1.0 =
* Network Settigns page.

= 0.0.1 =
* Initial release.

== Upgrade Notice ==

= 2.0.0 =
* A lot has changed. Please check the changelog.

= 1.0.1 =
* Display Bulk User Import from CSV Form on Add User Page.

= 1.0.0 =
* Merge Add new and existing user form.

= 0.1.4 =
* Add existing user without confirmation.

= 0.1.3 =
* Configurable error message.

= 0.1.2 =
* To restrict usernames as email address in configurable list of domains.

= 0.1.1 =
* To make it more reliable against future core updates.

= 0.1.0 =
* Upgrade to display network settings page.