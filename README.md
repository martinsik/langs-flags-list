This package is a map of "language => flag" pairs prepared to be used in code and CSS.

The main difference to other lists of flags is that this pairs languages to flag and not countries to flags. There are way more languages than countries so this list contains over 500 different languages including those that don't match any existing country such as Esperanto or Sumerian.

# Installation

```
npm i --save @textabledev/langs-flags-list
```

# Usage

This package contains three files:

## `lang-flags.css`

The basic class for all icons is `lang-icon` that defines the default size for all icons which is 25x15 pixels. Some flags are smaller, so their width is overridden in their class.

`lang-icon` doesn't define a path to the sprite image `lang-flags.png` so you can place is anywhere in your assets and then define `background-image` in your styles:

```
.lang-icon {
    background-image: url(../lang-flags.png);
}
```

Map of all flags mapped to CSS `lang-icon-*` classes. For example `lang-icon-en` is the flag of the United Kingdom. This class, however, only sets background position inside `lang-flags.png` so it always has to be used together with `lang-icon` class.

A complete example usage would look like the following:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Example usage of @textabledev/langs-flags-list package</title>
    <link rel="stylesheet" href="../lang-flags.css">
    <style>
        .lang-icon {
            background-image: url(../lang-flags.png);
        }
    </style>
</head>
<body>
    <span class="lang-icon lang-icon-en"></span>
    <span class="lang-icon lang-icon-aqc"></span>
    <span class="lang-icon lang-icon-cs"></span>
    <span class="lang-icon lang-icon-de"></span>
</body>
</html>
```

## lang-flags.json

Map of all language codes mapped to their names in English and their native language. For example `de` language code is represented as:

```
"de": {
    "nameNative": "Deutsch",
    "nameEnglish": "German"
},
``` 
 
## lang-flags.png

Sprite image with all flags. Position for each flag is defined in `lang-flags.css`.
