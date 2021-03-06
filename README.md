i18n
====

Translate messages emited by the other modules.

## How to Use?

### Configuration

#### v0.2.x

`config.translations` is an object in the following format:

Example:

```JSON
{
  "I am.": "Je suis.",
  "You are.": {
      "fr": "Tu es.",
      "ro": "Tu ești."
  },
  ...
}
```

`config.translates` is an array of miids that emit the `message` event.

#### v0.1.x

##### DEPRECATED IN v0.2.x

`config.translations` is an array of objects in the following format:

Example:

```JSON
  [
      {
          "old": "I am.",
          "new": "Je suis."
      },
      {
          "old": "You are.",
          "new": {
              "fr": "Tu es.",
              "ro": "Tu ești."
          }
      },
      ...
  ]
```

`config.listen` is an array of miids that emit the `message` event.
## Changelog

### v0.4.0
 - transferred the module to the new jxMono organization
 - updated Bind to `v0.4.0`, Events to `v0.4.0`

### v0.3.0
 - Updated deps

### v0.2.7
 - Updated to Events v0.1.8 and Bind v0.2.1

### v0.2.6
 - Update to Bind `v0.1.7`

### v0.2.5
 - We don't accept JSON booleans, numbers and so on, but only objects.

### v0.2.4
 - Dynamically add miids to listen to using `listenTo` function.

### v0.2.3
 - Update to Bind `v0.2.0`

### v0.2.2
 - Update to Events `v0.1.4` and Bind `v0.1.5`

### v0.2.1
 - Fixed translating of messages that are not in `config.translations`.

### v0.2.0
 - Update to Events `v0.1.3` and Bind `v0.1.3`
 - Renamed `main.js` into `i18n.js`
 - New format of `config.translations`: object instead of array
 - Renamed `config.listen` into `config.translates` to prevent overwriting of Events configuration (that uses `config.listen`).

#### Migration from `v0.1.x` to `v0.2.0`:
 - Replace `config.translations` array with an object, like described in [**How to use** section](#v02x)
 - Replace `config.listen` with `config.translates`

### v0.1.1
 - Fixed translating strings.

### v0.1.0
 - Initial release
