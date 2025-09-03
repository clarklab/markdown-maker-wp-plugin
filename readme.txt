=== Markdown Maker ===
Contributors: yourwordpressusername
Donate link: https://example.com/donate
Tags: markdown, export, developer, content, conversion
Requires at least: 5.0
Tested up to: 6.4
Requires PHP: 7.4
Stable tag: 1.0.0
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Developer-focused plugin to convert WordPress posts/pages to clean, LLM-ready Markdown format.

== Description ==

Markdown Maker is a lightweight, developer-focused WordPress plugin that provides two simple functions to convert WordPress posts and pages into clean, well-formatted Markdown. Perfect for developers who need to extract content for documentation, AI/LLM processing, or external tools.

**Key Features:**

* Convert any WordPress post/page to clean Markdown format
* Copy content to clipboard functionality
* Download content as .md files
* LLM-ready output with metadata headers
* Developer-friendly template functions
* Secure implementation with proper nonces and data sanitization

**Developer Functions:**

The plugin provides two main functions for manual insertion into theme templates:

1. `markdown_maker_copy_link()` - Outputs a link that copies post content as Markdown to clipboard
2. `markdown_maker_download_link()` - Outputs a link that downloads post content as a .md file

**Example Usage:**

```php
// Basic usage
<?php echo markdown_maker_copy_link(); ?>
<?php echo markdown_maker_download_link(); ?>

// With custom parameters
<?php echo markdown_maker_copy_link( get_the_ID(), 'Copy MD', 'For LLM agents', 'btn btn-primary' ); ?>
<?php echo markdown_maker_download_link( get_the_ID(), 'Download MD', 'Save locally', 'download-btn' ); ?>
```

**Markdown Output Includes:**
* Post metadata (title, author, date, URL)
* Clean content conversion (headings, lists, links, images, etc.)
* Proper attribution and context for LLM consumption
* Categories and tags (for posts)
* Excerpt (if available)

== Installation ==

1. Upload the plugin files to the `/wp-content/plugins/markdown-maker` directory, or install the plugin through the WordPress plugins screen directly.
2. Activate the plugin through the 'Plugins' screen in WordPress.
3. Use the provided functions in your theme templates where needed.

== Frequently Asked Questions ==

= How do I use this plugin? =

This plugin is designed for developers. You need to manually add the provided functions to your theme templates where you want the copy/download functionality to appear.

= Where should I place the functions? =

Common locations include:
* single.php or page.php templates
* Custom post type templates
* Admin areas (with proper permissions checks)
* Custom shortcodes or blocks

= Is the output compatible with LLMs? =

Yes! The Markdown output is specifically formatted to be LLM-friendly with proper metadata headers and clean content structure.

= Does this work with custom post types? =

Yes, the plugin works with any public post type including custom post types.

== Screenshots ==

1. Copy to clipboard functionality in action
2. Download link generating clean Markdown files
3. Example of LLM-ready Markdown output with metadata

== Changelog ==

= 1.0.0 =
* Initial release
* Copy to clipboard functionality
* Download as Markdown file
* LLM-ready output format
* Secure implementation with nonces and data sanitization

== Upgrade Notice ==

= 1.0.0 =
Initial release of Markdown Maker plugin.