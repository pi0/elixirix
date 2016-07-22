# Elixirix
Easier and faster elixir

# Install

``` npm install --save elixirx ```

# Usage

### gulpfile.js

```javascript

var Elixir = require('laravel-elixir');
var Elixirx = require('elixirx');

Elixir(function (mix) {
    var app = new Elixirx(mix, 'myapp', true);
    
    
    app.css([
            Elixirx.npm('bootstrap/dist/css/bootstrap.min.css'),
            Elixirx.npm('font-awesome/css/font-awesome.min.css'),
    ]);

    app.js([
            Elixirx.npm('jquery/dist/jquery.min.js'),
            Elixirx.npm('tether/dist/js/tether.min.js'),
            Elixirx.npm('bootstrap/dist/js/bootstrap.min.js'),
    ]);
}

```

## Gulp
For compiling full vendors run `gulp --production`
For watch run `bash gulp watch`


# Project Structure

Most important thing is you will never worry about project structure. Assume you have a asset package called `myapp`.
Project Structure:

- assets
    - build (generated)
    - sass
        - myapp
            - myapp.base.scss
            - myapp.scss
    - js
           - myapp
               - myapp.base.js
               - myapp.js
- public
    - css
        - myapp.css (generated)
    - js
        - myapp.js (generated)
    

### git ignore
Append this:   
`resources/assets/build`
