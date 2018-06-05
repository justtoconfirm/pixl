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

## Remove file

```
$ git rm <file_name>
$ git commit -m "Removed file"
$ git push
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

### Helper Classes

| Class              | Description                                                            |
| ------------------ | ---------------------------------------------------------------------- | 
| `.hide`            | Hides element (display: none)                                          |
| `.invisible`       | Hidden element that takes up space (visibility: hidden)                |
| `.bold`            | Set the font weight to be bold                                         |
| `.underline`       | Set underline                                                          |
| `.left`            | Float left                                                             |
| `.right`           | Float right                                                            |
| `.text-center`     | Centre align the inner content of a block element                      |
| `.text-left`       | Left align the inner content of a block element                        |
| `.text-right`      | Right align the inner content of a block element                       |
| `.no-margin`       | Set the margin to 0                                                    |
| `.no-padding`      | Set the padding to 0                                                   | 

### Lists

| Class              | Description                                                                                 |
| ------------------ | ------------------------------------------------------------------------------------------- | 
| `.bare-list`       | Remove bullet points from list elements and remove padding-left to align list with content  |

Example:

```html
<ul class="bare-list">
   <li>One</li>
   <li>Two</li>
</ul>
```

### Licence

MIT
