# Custom Error Pages

Create custom `401` and `403` error pages with any **WordPress** theme without
writing a single line of code, set it up and forget it.

## Description

**WordPress** offers inbuilt support for custom `404` pages on all themes. But 
what about custom pages for other common errors like `401` and `403`? You end up
seeing a bland error page of the Web Server.

With this plugin you can easily create custom `401` and `403` error pages with
any theme without writing a single line of code!!! And the best part is that you
set it and forget it. Yes, you don't have to do any changes even if you change
themes. The heading and text you want on `401` and `403` error pages are
displayed on the currently active theme.

## Further Reading
* [Create WordPress 401 and 403 error pages](https://websistent.com/WordPress-custom-403-401-error-page/) WITHOUT using this plugin.
* The [Custom Error Pages Plugin](https://websistent.com/WordPress-plugins/custom-error-pages/) official homepage.

## Installation

1. Install and activate the custom error pages plugin.
2. From the **wp-admin** go to *Settings > Custom Error Pages*, fill in the
   heading and content boxes, save the changes and preview it.
3. Configure your web server to use a custom error page.

Apache users edit your `.htaccess` file and add the following lines.

	ErrorDocument 403 /index.php?status=403
	ErrorDocument 401 /index.php?status=401

Nginx users edit your `nginx.conf` file and add the following lines.

	error_page	403 = /index.php?status=403
	error_page	401 = /index.php?status=401

Try accessing a file or directory which is forbidden like

http://www.example.com/.htaccess

http://www.example.com/wp-includes/

Did you see a custom `403` page in all the glory of your theme?

## Frequently Asked Questions

### Should I do anything if I change themes?
No not at all. You just install the plugin set it and forget it. The plugin
isn't theme bound so it'll work even after switching themes.

### I noticed define( 'DONOTCACHEPAGE', TRUE ); in the plugin code what is it for?
This tells caching plugins like W3 Total Cache and WP Super Cache not to cache
the `401` and `403` error pages. This does **NOT** affect the cacheability any
other pages of your site.

### Does this plugin automatically edit the .htaccess or nginx.conf file?
No it doesn't. You have to manually edit it and add the necessary configuration
specified in the plugin's option page.

## Credits

This plugin was written by @jesinwp.

Version `1.2` in that repository was made by @sizious, so it's unofficial.
