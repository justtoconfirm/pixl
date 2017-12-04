# Pixl
Front-end web library

## Clone Repository

```
$ git clone https://github.com/justtoconfirm/pixl.git
```
## Install

```
$ cd pixl
$ npm install
```

## Compile

```
$ npm run build
```

## Updating Version

Update `package.json` version number when on the `master` branch. This can be either: 

- `MAJOR` version when you make incompatible API changes,
- `MINOR` version when you add functionality in a backwards-compatible manner, and
- `PATCH` version when you make backwards-compatible bug fixes.

Pixl follows [Semantic Versioning](https://semver.org/).

```
$ npm version minor
$ git push
```

You may have to sometimes use the `--force` flag if errors occur in the terminal.

```
$ npm version minor --force
$ git push
```

## Documentation

### Utility Classes

Applying utility classes to HTML:

```
<div class='text-center'> ... </div>
```

Text alignment.

| Class              | Description                                                     |
| ------------------ | --------------------------------------------------------------- | 
| `.text-center`     | Centre align text                                               |
| `.text-left`       | Left align text                                                 |
| `.text-right`      | Right align text                                                | 
| `.text-capitalize` | Capitalizes the first letter of each word in the selected text  |
| `.text-lowercase`  | Makes all of the letters in the selected text lowercase         |
| `.text-uppercase`  | Makes all of the letters in the selected text uppercase         | 

### Mixins

Vendor prefixes.

```
// All vendor prefixes will be applied
.element {
    @include prefix( 'border-radius', 5px );
}

.element {
    @include prefix( 'border-radius', 5px, webkit moz ms o );
}

// Only the webkit vendor prefix will be applied
.element {
    @include prefix( 'border-radius', 5px, webkit );
}
```

@font-face

The `@include` directive is used to import font files into the framework. File extensions do not need to be included. Here, we are using the `JosefinSans-Bold` font.

Font files should be placed within the `dist/font` directory.

```
@include font-face( 'JosefinSans-Bold' );
```

To apply the font to an element, use the `font-family` property. The value needs to be the same as the filename being used.

```
.element {
    font-family: 'JosefinSans-Bold';
}
```