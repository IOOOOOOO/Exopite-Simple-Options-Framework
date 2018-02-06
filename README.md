# Exopite-Simple-Options-Framework

## Fast, easy and lightweight option/metabox form generator.

- Author: Joe Szalai
- Version: 20180113
- Plugin URL: https://joe.szalai.org/exopite/exopite-simple-options-framework/
- GitHub URL: https://github.com/JoeSz/Exopite-Simple-Options-Framework
- Author URL: https://joe.szalai.org
- License: GNU General Public License v3 or later
- License URI: http://www.gnu.org/licenses/gpl-3.0.html

### NOTE

The Framework still in development stage.

Documentation is still in-progress.

The Framework based on some CodeStar Framework, MetaBox.io code and design. The fields configs desgin also based on CodeStar Framework.
I created this framework for plugins and metaboxes. Not for Themes. For Themes I recommend CodeStar Framework.

### DESCRIPTION

WHY?
I need someting fast, easy and lightweight to generate option page and/or metabox for my plugins and/or post types.

I also love to create/program someting new (for me) to have fun and leary every day.

For my theme I use CodeStar Framework, so I created similarly. Unfortunately CodeStar Framework based on static class, can not initialize multiple times and this is required for plugns.

#### Lightweight

No ads, Files are loaded only when required. Minimum footprint.

#### Integration

Easy to integrate with any plugin or post type (even WordPress theme, but it is not designed to do so).

#### Open Source

Exopite Simple Options is free and available on Github. Feel free to submit patches or add more features.

### FEATURES

Available fields:

- ace_field
- video (mp4/oembed)
- upload (multiple)
- attached (Attached files/images/etc... to the post -> only for Metabox, multiselect, AJAX delete)
- notice
- editor (WYSIWYG WordPress Editor)
- text
- password
- color (rgb/rgba/html5)
- image
- textarea
- switcher
- date (datepicker/html5)
- checkbox
- radio
- button_bar
- select (single/multiselect + posttype)
- panel
- content
- number
- range
- tap_list (radio/checkbox)
- image_select (radio/checkbox)
- meta (readonly -> to the post -> only for Metabox)

![](assets/screenshot-1.png)

### REQUIREMENTS

Server

* WordPress 4.9+ (May work with earlier versions too)
* PHP 5.6+ (Required)
* jQuery 1.9.1+

Browsers

* Modern Browsers
* Firefox, Chrome, Safari, Opera, IE 10+
* Tested on Firefox, Chrome, Edge, IE 11

### INSTALLATION

Copy to plugin/theme folder.

Hook to 'init'.

```php
$config = array(

    'type'              => 'menu',                          // Required, menu or metabox
    'id'                => $this->plugin_name,              // Required, meta box id, unique per page,
                                                            //   to save: get_option( id )
    'menu'              => 'plugins.php',                   // Required, sub page to your options page
    'submenu'           => true,                            // Required for submenu
    'title'             => 'The name',                      // The name of this page
    'capability'        => 'manage_options',                // The capability needed to view the page
    'tabbed'            => false,                           // Separate sections to tabs

);

$fields[] = array(
    'name'   => 'first',
    'title'  => 'Section First',
    'fields' => array(

        // fields...

        array(
            'id'      => 'autoload',
            'type'    => 'switcher',
            'title'   => 'Field title',
            'default' => 'yes',
        ),

    ),
);

$fields[] = array(
    'name'   => 'second',
    'title'  => 'Section Second',
    'fields' => array(

        // fields...

        array(
            'id'      => 'autoload',
            'type'    => 'switcher',
            'title'   => 'Field title',
            'default' => 'yes',
        ),

    ),
);

$options_panel = new Exopite_Simple_Options_Framework( $config, $fields );
```

Example: 
https://github.com/JoeSz/WordPress-Plugin-Boilerplate-Tutorial/blob/e1b1a561a08de46411f6705aa5bf33eee96b5fc1/plugin-name/admin/class-plugin-name-admin.php#L104

### CHANGELOG

= 20180113 - 2018-01-13 =
* Add meta field.

= 20180107 - 2018-01-07 =
* Add button field.

= 20180102 - 2018-01-02 =
* Initial release.

### LICENSE DETAILS

The GPL license of Sticky anything without cloning it grants you the right to use, study, share (copy), modify and (re)distribute the software, as long as these license terms are retained.

### DISCLAMER

NO WARRANTY OF ANY KIND! USE THIS SOFTWARES AND INFORMATIONS AT YOUR OWN RISK!
[READ DISCLAMER.TXT!](https://joe.szalai.org/disclaimer/)
License: GNU General Public License v3

[![forthebadge](http://forthebadge.com/images/badges/built-by-developers.svg)](http://forthebadge.com) [![forthebadge](http://forthebadge.com/images/badges/for-you.svg)](http://forthebadge.com)
