# Annotorious Parse.com Plugin

A simple [Annotorious](http://github.com/annotorious/annotorious) plugin that stores annotations on [Parse.com](http://parse.com/).

This plugin is based on the [annotorious-elasticsearch-plugin](https://github.com/annotorious/annotorious-elasticsearch-plugin) and is licensed under the [WTFPL](http://en.wikipedia.org/wiki/WTFPL).

## Using this Plugin

Copy the files to your server/Webspace and set it up with your page as described below.

1. The plugin uses jQuery and Parse.com's javascript SDK. Therefore you need to import these thwo libraries before importing the plugin script.
2. Add the plugin script to your page just like any other Annotorious plugin. Make sure the plugin script is
   loaded __after__ the main Annotorious script.
3. Attach the plugin to Annotorious using the ``anno.addPlugin`` API method.
4. Specify your application id and your javascript key  using the ``app_id`` and ``js_key``. config params.

## Example

    ....
      <head>
        <!-- Import main Annotorious script and CSS -->
        <link rel="stylesheet" href="http://annotorious.github.com/latest/annotorious.css" type="text/css" />
        <script src="http://annotorious.github.com/latest/annotorious.min.js"></script>
        
        <!-- Import jQuery - the plugin depends on it! -->
         <script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.1/jquery.min.js"></script>

        <!-- Import Parse's javascript sdk - the plugin depends on it! -->
        <script src="https://unpkg.com/parse@1.10.0/dist/parse.min.js"></script>
        
        <!-- Import the css styles -->
        <link rel="stylesheet" href="anno-parse-plugin.css" type="text/css" /> 

        <!-- Import the plugin script -->
        <script src="anno-parse-plugin.js"></script>
        
        <!-- Use Annotorious' JavaScript API to attach and activate the plugin -->
        <script>
         anno.addPlugin('Parse', { app_id: 'YOUR_PARSE_APPLICATION_ID', js_key: 'YOUR_PARSE_JAVASCRIPT_KEY' });
        </script>
      <head>
    ....

## [Live Demo](http://dommmel.github.io/annotorious-parse-plugin)

    
