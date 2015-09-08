# Clock JavaScript Coding Standard

This is an extension of standard minus the comma first and multi vars. We'd have
loved to stick with standard 100% but we have a lot of active legacy projects
and with this minor change we were able to easily nick all the good stuff that
standard have defined.

## Usage

In your project folder:

```
npm install --save-dev eslint-config-clock
npm install --save-dev eslint-config-standard
npm install --save-dev eslint-plugin-standard
```

Then create a `.eslintrc` in the project root.

```json
{
  "extends": "clock"
}
```

Any override to the standards should go in this file.

## Legacy Updates

The following can be used to fix some inconsistencies from our `jshint/jscs`
projects.

```
/function\s([^\s]+?)\(/ to function $1 (

') )'' to '))'

'function(' to 'function (''

'( ' to '('

',function' to ', function'

\/\* jshint maxcomplexity: (\d+) */ to /* eslint complexity: [ 2, $1 ] */
```