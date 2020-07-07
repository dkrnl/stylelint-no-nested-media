# stylelint-no-nested-media
Disallow nested @media rules

For example, the following patterns are considered violations:

```scss
@media (max-width: 600px) { 
    @media (min-width: 500px) { }
}
```

The following patterns are not considered violations:

```scss
@media (min-width: 500px) and (max-width: 600px) { }
```

## Installation

1. If you haven't, install [stylelint]:

```
npm install stylelint --save-dev
```

2.  Install `stylelint-no-nested-media`:

```
npm install stylelint-no-nested-media --save-dev
```

## Usage

Add `stylelint-no-nested-media` to your stylelint config `plugins` array, then add rules you need to the rules list. All rules from stylelint-no-nested-media need to be namespaced with `pitcher`.

```json
{
    "plugins": [
        "stylelint-no-nested-media"
    ],
    "rules": {
        "pitcher/no-nested-media": true
    }
}
```
