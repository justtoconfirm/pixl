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