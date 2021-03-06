# WoWCMS
Amazingly simple, small and secure flat file CMS made with PHP, jQuery, HTML, CSS and a flat JSON database.

### Installation
- unzip and upload the files wherever you wish WoWCMS to be installed
or
- clone from GitHub

### Requirements
 - PHP 5.5 or higher
 - .htaccess support

### Community, documentation, themes and plugins
- https://a6smile.com/wowcms

### Whats new in 1.2.0 beta
- custom functions.php file per theme - WoWCMS will automatically include your functions.php file if it exists in your themes folder (/themes/yourTheme/functions.php)
- added padding20 CSS class to the admin settings panel

### Features
 - no configuration required, unzip and upload
 - simple click and edit functionality
 - lightweight - runs on a couple hundred lines of code and 5 files
 - custom login URL
 - custom homepage
 - better password protection
 - highlighted current page
 - mobile responsive, easy to theme, 404 pages, clean URLs
 - easy page creating and deleting
 - better SEO support - custom title, keywords and description for each page
 - optional functions.php file - includes itself when you create it (the location of the functions.php should be inside your theme folder)
 - no known vulnerabilities - special thanks to yassineaddi, hypnito and other security researchers

### WoWCMS works by default on Apache. To make it work with NGINX, put the following code into your NGINX server config:
```
location ~ database.js {
	return 403;
}

autoindex off;

location / {
	if (!-e $request_filename) {
		rewrite ^(.+)$ /index.php?page=$1 break;
	}
}
```

### If any errors occur (500 internal server error), correct file permissions to 644 and folder permissions to 755. You can do this manually or with the short script below (added by Bill Carson)
  - `find ./ -type d -exec chmod 755 {} \;`
  - `find ./ -type f -exec chmod 644 {} \;`

### How to update from older versions?
- Updating from 1.1.0+ - use the one click update from your WoWCMS settings panel.
- Updating from 1.0.0 - replace your old index.php with the new one from the above download.

- Updating from 1.0.0 and older
 - Backup all your WoWCMS files.
 - Make a fresh installation of the latest WoWCMS anywhere on your server.
 - Copy your old content and paste it into the new installation.
 - Remove the old installation.
 - Move the new installation to the old WoWCMS installation location.

Updating is really easy with our click updater - included in versions 1.1.0 and above.

### Links
- WoWCMS website: https://a6smile.com/wowcms
