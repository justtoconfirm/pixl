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
$ npm version <update_type>
$ git push
```

## Documentation

### Helper Classes

| Class              | Description                                                                                     |
| ------------------ | ----------------------------------------------------------------------------------------------- | 
| `.hide`            | Hides element (display: none)                                                                   |
| `.invisible`       | Hidden element that takes up space (visibility: hidden)                                         |
| `.bold`            | Set the font weight to be bold                                                                  |
| `.underline`       | Set underline                                                                                   |
| `.left`            | Float left                                                                                      |
| `.right`           | Float right                                                                                     |
| `.text-center`     | Centre align the inner content of a block element                                               |
| `.text-left`       | Left align the inner content of a block element                                                 |
| `.text-right`      | Right align the inner content of a block element                                                |
| `.no-margin`       | Set the margin to 0                                                                             |
| `.no-padding`      | Set the padding to 0                                                                            |
| `.fixed`           | The element is positioned relative to the browser window and remains fixed in the same location | 

### Lists

| Class                | Description                                                                                 |
| -------------------- | ------------------------------------------------------------------------------------------- | 
| `.bare-list`         | Remove bullet points from list elements and remove padding-left to align list with content  |
| `.horizontal-list`   | Horizontal list                                                                             |

Example:

```html
<ul class="bare-list">
   <li>One</li>
   <li>Two</li>
</ul>
```

### Buttons

| Class                | Description                                                                                 |
| -------------------- | ------------------------------------------------------------------------------------------- | 
| `.btn`               | Button                                                                                      |
| `.btn--primary`      | Modifier class added to button to set the primary theme                                     |
| `.btn--alert`        | Modifier class added to button to set the alert theme                                       |

Example:

```html
<button class="btn" type="button">Button</button>
<button class="btn" type="submit">Submit</button>

<a href="#" class="btn">Button</button>
```

Button themes:

```html
<button class="btn btn--primary" type="button">Button</button>
<button class="btn btn--alert" type="button">Button</button>
```

### Panels

| Class                | Description                                                                                 |
| -------------------- | ------------------------------------------------------------------------------------------- | 
| `.panel`             | Panel with background colour                                                                |
| `.panel--primary`    | Modifier class added to panel to set the primary theme                                      |
| `.panel--alert`      | Modifier class added to panel to set the alert theme                                        |

Example:

```html
<div class="panel"> ... </div>

<div class="panel panel--primary"> ... </div>
<div class="panel panel--alert"> ... </div>
```

### Code

Example:

```html
<pre>
   <code>
      &lt;html&gt;
         &lt;body&gt;
   </code>
</pre>
```

To create a code-panel with a title and colour-coded title bar:

```html
<pre class="code-panel" rel="html" data-title="HTML example: index.html">
   <code>
      &lt;html&gt;
         &lt;body&gt;
   </code>
</pre>
```

| rel attribute        | Language                                                                                    |
| -------------------- | ------------------------------------------------------------------------------------------- | 
| `html`               | HTML                                                                                        |
| `css`                | CSS (Cascading Style Sheets)                                                                |

### Grid

```html
<section class="wrapper">

   <div class="row">
      <div class="col-12">
         Content here
      </div>
   </div>
   
   <div class="row">
      <div class="col-6">
         Content here
      </div>
      <div class="col-6">
         Content here
      </div>
   </div>

</section>
```

### Licence

MIT
