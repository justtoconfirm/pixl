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

## Checkout new branch

Create a new feature branch from the `master` branch in GitHub.

```
$ git fetch
$ git checkout <branch_name>
```

## Merge branch

```
$ git checkout <branch_name>
$ git merge <branch_name_to_merge>
$ git push
```

## Delete branch

```
$ git branch -d <branch_name>
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

**Font style**

| Class              | Description                                                            |
| ------------------ | ---------------------------------------------------------------------- | 
| `.italic`          | The browser displays an italic font style                              |
| `.normal`          | The browser displays a normal font style. This is default              |
| `.oblique`         | The browser displays an oblique font style                             |

**Font weight**

| Class              | Description                                                            |
| ------------------ | ---------------------------------------------------------------------- | 
| `.bold`            | Defines thick characters                                               |
| `.bolder`          | Defines thicker characters                                             |
| `.lighter`         | Defines lighter characters                                             |

**Text alignment**

| Class              | Description                                                            |
| ------------------ | ---------------------------------------------------------------------- | 
| `.text-center`     | Centre align the letters in the selected text                          |
| `.text-left`       | Left align the letters in the selected text                            |
| `.text-right`      | Right align the letters in the selected text                           |  

**Text transform**

| Class              | Description                                                            |
| ------------------ | ---------------------------------------------------------------------- | 
| `.text-capitalize` | Capitalizes the first letter of each word in the text                  |
| `.text-lowercase`  | All of the letters in the selected text become lowercase               |
| `.text-uppercase`  | All of the letters in the selected text become uppercase               |

**Alignment**

| Class              | Description                                                            |
| ------------------ | ---------------------------------------------------------------------- | 
| `.center`          | Centre align a block element. Clearfix not required                    |
| `.left`            | Left align                                                             |
| `.right`           | Right align                                                            |

The `.clearfix` class should be added to the parent element when using the alignment classes of `.left` or `.right`.

```
<div class='clearfix'>
    <div class='right'> ... </div>
</div>
```

Should you need to centre align a block element, use the `.center` class. No clearfix is required, but a class will be needed to provide a width (can be in pixels). 

In this example, the `.box` class provides a width for the container.

```
<div class='box center'> ... </div>
```

### Font

**@font-face**

Place the font files within the `dist/font` directory.

The `@include` directive is used to import the font files into the Pixl library. 

In this example, we are using the `JosefinSans-Bold` font. The file extension is not needed to use the font.

```
@include font-face( 'JosefinSans-Bold' );
```

The `font-style` and `font-weight` properties can also be applied. Should no value be provided, the properties will not be included in the CSS output.

```
@include font-face( 'JosefinSans-Bold', italic, bold );

// Just the font-style property
@include font-face( 'JosefinSans-Bold', italic, null );

// Just the font-weight property
@include font-face( 'JosefinSans-Bold', null, bold );
```

The following font properties can be used:

| Property              | Values                                                                 |
| --------------------- | ---------------------------------------------------------------------- | 
| `font-style`          | normal / italic / oblique                                              |
| `font-weight`         | normal / bold / 100 / 200 / 300 / 400 / 500 / 600 / 700 / 800 / 900    |


Apply the font to an element using the `font-family` property. Use the font name as the value, again without the file extension.

```
.element {
    font-family: 'JosefinSans-Bold';
}
```

Further font values can be listed within the `font-family` property to provide a fallback should the main font be unavailable.

```
.element {
    font-family: 'JosefinSans-Bold', Gill Sans Extrabold, sans-serif;
}
```

### Mixins

**Font Size**

The base font size is 16px. This mixin will output the font-size in rem and a pixel fallback for older browsers.

```
// Will output rem and pixel font sizes 
.element {
    @include font-size( 20 );
}

// Set the base font size to be 14px
.element {
    @include font-size( 20, 14 );
}
```

**Prefixes**

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