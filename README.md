Asset Saver
===========

A Drupal 7 module that provides the ability to save remote JavaScript and CSS files locally so that they can be minified and aggregated using Drupal's aggregation feature.

Usage
-----

Just pass a URL to `asset_saver_url_to_file()` and it will download and save the file locally, returning the Drupal URI to the file. This URI can easily be passed to `drupal_add_js()` or `drupal_add_css()`.

### Example

    drupal_add_js(asset_saver_url_to_file('http://example.com/best_lib_ever.js')
                 ,array('scope'      => 'header'
                       ,'group'      => JS_LIBRARY
                       ,'every_page' => true));
