# plugin-boilerplate

> A boilerplate for Ampify plugin

### Install and Run

```shell script
$ git clone && yarn && yarn test
```

### Ampify Plugin

In order to develop an Ampify plugin,
you need to export to functions:

- `prepare`: preparing the dom for Ampfiy.
- `run`: run plugin's manipulation.

Inside the Plugin's code, you have access to the `DOM` as expected.

### Testing

Easy to test it using `Jest`, or any other tool of convenience.

Check out [index.test.js](./index.test.js).

### 3rd Party Libraries

You can use any 3rd party libraries installed with `npm` or `yarn`.

### Naming convention

Plugin name should be unique and under the `@ampify` namespace,
Followed by `plugin-` and its name after.

Eg: For a plugin named `toggle` it would be: `@ampify/plugin-toggle` and `package.json` file should look like this:

```json
{
  "name": "@ampify/plugin-toggle",
  "version": "1.0.0",
  "main": "index.js",
  "license": "MIT"
}
```

### Submit plugin

To publish plugin you should open pull request to Ampify's Plugin repository (TBA).

### Caveats

Be aware that the plugin will run in another website,
So you don't have control of what this website changed to the `window` object or `Prototype`.

It is best advised to use 3rd party utility library,
like `lodash`, and not depend on js native methods as they could have been changed by the website.
