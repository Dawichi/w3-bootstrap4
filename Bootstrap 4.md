# Bootstrap 4

1. [Containers](#1. Containers)
2. [Grid System](#2. Grid System)
3. [Text / Typography](#3. Text / Typography)
4. [Colors](#4. Colors)
5. [Tables](#5. Tables)
6. [Images](#6. Images)
7. [Jumbotron](#7. Jumbotron)
8. [Alerts](#8. Alerts)
9. [Buttons](#9. Buttons)
10. [Button Groups](#10. Button Groups)
11. [Badges](#11. Badges)
12. [Progress Bar](#12. Progress Bar)
13. [Spinners](#13. Spinners)
14. [Pagination](#14. Pagination)
15. [List Groups](#15. List Groups)
16. [Cards](#16. Cards)
17. [Dropdowns](#17. Dropdowns)






## 1. Containers

`.container` **fixed** width container.

`.container-fluid` **full** width container.



>For `.container-fluid`, width is always 100%.
>
>For `.container`, depends of the viewport width:

| .container | ExtraSmall | Small | Medium | Large | ExtraLarge |
| ---------- | ---------- | ----- | ------ | ----- | ---------- |
| max-width  | 100%       | 540px | 720px  | 960px | 1140px     |



#### 1.1 Container Padding

By default, containers have 15px left and right padding, with no top or bottom padding. `.pt-1`, `.pt-2`, ..., `.pt-5` classes add extra padding and margin to make them look better. Example:

```html
<div class="container pt-3"></div>
```



#### 1.2 Container Border and Color

Other utilities than are also often used together with `.container` is: `border ` for borders, `bg-color` for backgrounds and `text-color` for the text. Examples:

```html
<div class="container p-3 my-3 border"></div>
<div class="container p-3 my-3 bg-dark text-white"></div>
<div class="container p-3 my-3 bg-primary text-white"></div>
```



#### 1.3 Responsive Containers

The `.container-sm` , `.container-md`, `.container-lg`, `.container-xl` classes create responsive containers, with adaptative **max-width** props.

|      Class      | < 576px | ≥ 576px | ≥ 768px | ≥ 992px | ≥ 1200px |
| :-------------: | :-----: | :-----: | :-----: | :-----: | :------: |
| `.container-sm` |  100%   |  540px  |  720px  |  960px  |  1140px  |
| `.container-md` |  100%   |  100%   |  720px  |  960px  |  1140px  |
| `.container-lg` |  100%   |  100%   |  100%   |  960px  |  1140px  |
| `.container-xl` |  100%   |  100%   |  100%   |  100%   |  1140px  |



## 2. Grid System

Bootstrap's grid sysyem is built with flexbox and allows up to 12 columns across the page. If you don't want to use all 12 columns individually, you can group them together to create wider columns.

The system is responsive, the columns will re-arrange automatically depending on the screen size. Make sure that the sum adds up to 12 or fewer (it is not required to use all 12 available columns).



#### 2.1 Grid Classes

The grid system has 5 classes than can be combined to create more dynamic and flexible layouts. 

| < 576px |  ≥ 576px   |  ≥ 768px   |  ≥ 992px   |  ≥ 1200px  |
| :-----: | :--------: | :--------: | :--------: | :--------: |
| `.col-` | `.col-sm-` | `.col-md-` | `.col-lg-` | `.col-xl-` |

> **Tip:** Each class scales up, so if you wish to set the same widths for `sm` and `md`, you only need to specify `sm`.



**Basic structure of a Bootstrap4 Grid**

```html
<!-- Control the column width, and how they should appear on different devices -->
<div class="row">
	<div class="col-*-*"></div>
  	<div class="col-*-*"></div>
</div>
<div class="row">
  	<div class="col-*-*"></div>
  	<div class="col-*-*"></div>
  	<div class="col-*-*"></div>
</div>

<!-- Or let Bootstrap automatically handle the layout -->
<div class="row">
  	<div class="col"></div>
  	<div class="col"></div>
  	<div class="col"></div>
</div>
```

**First example:** create a row (`<div class="row">`). Then, add the desired number of columns (tags with appropriate `.col-*-*` classes). The first star (\*) represents the responsiveness: **sm**, **md**, **lg** or **xl**, while the second star represents a number, which should add up to 12 for each row.

**Second example:** instead of adding a number to each `col`, let bootstrap handle the layout, to create equal width columns: 2 `col` = 50% width. 3 cols = 33.33% width. 4 cols = 25% width, etc. You can also use `.col-sm|md|lg|xl` to make the columns responsive.

Some examples:
```html
<!-- 3 columns with equal size -->
<div class="row">
    <div class="col">.col</div>
    <div class="col">.col</div>
    <div class="col">.col</div>
</div>

<!-- 4 columns, each one is 3/12 width. Cause it is 'col-sm', on mobile phones or screens less than 576px wide, the columns will stack vertically -->
<div class="row">
  	<div class="col-sm-3">.col-sm-3</div>
  	<div class="col-sm-3">.col-sm-3</div>
  	<div class="col-sm-3">.col-sm-3</div>
  	<div class="col-sm-3">.col-sm-3</div>
</div>

<!-- 2 colums, one 4/12 width and another 8/12 width. Stacked on movile size and scaling on larger screens -->
<div class="row">
	<div class="col-sm-4">.col-sm-4</div>
  	<div class="col-sm-8">.col-sm-8</div>
</div>
```



## 3. Text / Typography

B4 uses as default:

```css
text{
    font-size: 16px,
	line-height: 1.5,
	font-family: Helvetica Neue, Helvetica, Arial, sans-serif
}
p { margin-top: 0, margin-bottom: 1rem }
```



**Headings**: B4 also modifies the `<h1>` - `<h6>` headings with a bolder font and increased font-size.



**Display**: Display headings are used to stand out more than normal headings, with 4 classes to choose from: `.display-1`, `.display-2`, `.display-3`, `.display-4`.



**Small**: On B4, `<small>` element is used to create a lighter secondary text on any heading, like: 

```html
<h1>Main heading text <small>secondary text smaller</small> </h1>
```



**Abbr**: B4 styles `<abbr>` with a dotter border bottom.



**Blockquote**: Add `.blockquote` and `.blockquote-footer` when quoting:

```html
<blockquote class="blockquote">
    <p>Any random quote that anybody never said</p>
    <div class="blockquote-footer">Albert Einstein, 2025</div>
  </blockquote>
```



**Other elements**: B4 also styles some html elements like `<dl>`, `<code>`, `<kbd>` (useful for show keyboard shortcuts) and `<pre>`.  



**More typography classes**:

|          Class          | Description                                         |
| :---------------------: | --------------------------------------------------- |
|   `.font-weight-bold`   | Bold text                                           |
|  `.font-weight-bolder`  | Bolder text                                         |
|     `.font-italic`      | Italic text                                         |
|  `.font-weight-light`   | Light weight text                                   |
| `.font-weight-lighter`  | Lighter weight text                                 |
|  `.font-weight-normal`  | Normal text                                         |
|         `.lead`         | Makes a paragraph stand out                         |
|        `.small`         | Smaller text (80% of the size of the parent)        |
|      `.text-left`       | Left-aligned text                                   |
|     `.text-*-left`      | Left-aligned text on X size of screens              |
|      `.text-break`      | Prevents long text from breaking layout             |
|     `.text-center`      | Indicates center-aligned text                       |
|    `.text-*-center`     | Indicates center-aligned text on X size of screens  |
| `.text-decoration-none` | Removes the underline from a link                   |
|      `.text-right`      | Indicates right-aligned text                        |
|     `.text-*-right`     | Indicates right-aligned text on X size of screens   |
|     `.text-justify`     | Indicates justified text                            |
|    `.text-monospace`    | Monospaced text                                     |
|     `.text-nowrap`      | Indicates no wrap text                              |
|    `.text-lowercase`    | Indicates lowercased text                           |
|      `.text-reset`      | Resets the color (inherits it from its parent)      |
|    `.text-uppercase`    | Indicates uppercased text                           |
|   `.text-capitalize`    | Indicates capitalized text                          |
|      `.initialism`      | An `<abbr>` element in a slightly smaller font size |
|    `.list-unstyled`     | Removes the default style on list items             |
|     `.list-inline`      | Places all list items on a single line              |
|    `.pre-scrollable`    | Makes a `<pre>` element scrollable                  |



## 4. Colors

#### Text colors

Contextual classes that can be used to provide "meaning through colors"

`.text-muted` - Muted

`.text-primary` - <span style="color:blue">Important</span>

`.text-success` - <span style="color:green">Success</span>

`.text-info` - <span style="color:blue">Information</span>

`.text-warning` - <span style="color:orange">Warning</span>

`.text-danger` - <span style="color:red">Danger</span>

`.text-secondary` - <span style="color:gray">Secondary text</span>

`.text-white` - White text

`.text-dark` - <span style="color:gray">Dark gray text</span>

`.text-body` - Body color text (often black)

`.text-light` - Light text



> It can be used for style `<link>`s too. And it's possible to modify the opacity by `.text-black-50` or `.text-white-50` for 50% opacity.



#### Background colors

The classes for background colors are: `.bg-primary`, `.bg-success`, `.bg-info`, `.bg-warning`, `.bg-danger`, `.bg-secondary`, `.bg-dark` and `.bg-light`.

![backgrounds](./imgs/1.png)



## 5. Tables

**Basic table**:  `.table` styles html tables with padding and horizontal dividers. 

![table](.\imgs\2.png)



**Striped rows**: `.table-striped` class adds zebra-stripes to a table.

![table-stripped](.\imgs\3.png)



**Bordered table**: `.table-bordered` class adds borders on all sides and cells.

![table-bordered](.\imgs\4.png)



**Over rows**: `.table-over` adds a hover effect (grey bg) on table rows.

**Dark table**: `.table-dark` adds a dark background and white color text.

**Dark striped table**: `.table-dark` and `.table-striped` can be combined.

**Dark over table**: `.table-dark` and `.table-over` can combine too.

**Borderless table**: `.table-borderless` removes borders from the table.



#### 5.1 Contextual table classes

Can be used to color the whole table (`<table>`), the table rows (`<tr>`) or table cells (`<td>`).

`.table-primary` - <span style="color:blue">Important</span>

`.table-success` - <span style="color:Green">Successful</span>

`.table-info` - <span style="color:blue">Information</span>

`.table-warning` - <span style="color:orange">Warning</span>

`.table-danger` - <span style="color:red">Danger</span>

`.table-active` - <span style="color:Grey">Hover color</span>

`.table-secondary` - <span style="color:Grey">Less important</span>

`.table-light` - <span style="color:gray">Light grey</span>

`.table-dark` - Dark gray



#### 5.2 Table heads and other tables

**Header row**: `.thead-dark` adds a dark background to a row, and `.thead-light` adds a gray one.

**Small table**: `.table-small`makes the tablet smaller by 50% normal cell padding.

**Responsive table**: `.table-responsive` adds a x-scrollbar if the table is too big horizontally. You can also decide when the table should get a scrollbar:

| Class                  | Screen width |
| ---------------------- | ------------ |
| `.table-responsive-sm` | < 576px      |
| `.table-responsive-md` | < 768px      |
| `.table-responsive-lg` | < 992px      |
| `.table-responsive-xl` | < 1200px     |



## 6. Images

`.rounded`: adds rounded corners.

`.rounded-circle`: shapes the image to a circle.

`.img-thumbnail`: shapes the image to a thumbnail (bordered).

![imgsexample](./imgs/5.png)



**Aligning Images**

Use `.float-left` and  `.float-right` classes to float an image.



**Centered Image**

For center an image, add`.mx-auto` ( `margin: auto` )  and `.d-block` ( `display: block` ). 

```html
<img src="centeredImage.jpg" class="mx-auto d-block">
```



**Responsive Images**

Images come in all sizes. So do screen. Responsive images automatically adjust to fit the size of the screen. 

Create responsive images by adding an `.img-fluid` class to the `<img>` tag. The image will then scale nicely to the parent element.

The `.img-fluid` class applies `max-width: 100%` and `height: auto` .



## 7. Jumbotron

A jumbotron indicates a big grey box for calling extra attention to some special content or information.

Use a `<div>` element with class `.jumbotron` to create one.

> **Tip:** Inside a jumbotron you can put nearly any valid HTML, including other Bootstrap elements/classes.



#### Full-width Jumbotron

Add `.jumbotron-fluid`, and a `.container` or `.container-fluid` inside of it.
```html
<div class="jumbotron jumbotron-fluid">
    <div class="container">
        <h1>Bootstrap Tutorial</h1>
        <p>Bootstrap is the most popular HTML, CSS...</p>
    </div>
</div>
```



## 8. Alerts

B4 provides an easy way to create predefined alert messages. The `.alert` class, followed by one of the contextual classes `.alert-success`, `.alert-info`, `.alert-warning`, `.alert-danger`, `.alert-primary`, `.alert-secondary`, `.alert-dark` or `.alert-light`:

![alerts](./imgs/6.png)

```html
<div class="alert alert-success">
    <strong>Success!</strong> Successful or positive action.
</div>
```



#### Alert Links

Add `.alert-link` class to any links inside the alert box to create a matching colored links.

```html
<div class="alert alert-success">
    <strong>Success!</strong> You should <a href="#" class="alert-link">read this message</a>.
</div>
```



#### Closing Alerts

To close the alert message, add a `.alert-dismissible` class to the alert container. Then add `class="close"` and `data-dismiss="alert"` to a link or button element.

```html
<div class="alert alert-success alert-dismissible">
    <button type="button" class="close" data-dismiss="alert">&times
    </button>
    <strong>Success!</strong> Successful or positive action.
</div>
```

> **Tip:** `&times;` (x) is an HTML entity that is the preferred icon for close buttons, rather than the letter "x".
>
> For a list of all HTML Entities, [visit our HTML Entities Reference](https://www.w3schools.com/charsets/ref_html_entities_4.asp)



#### Animated Alerts

The `.fade` and `.show` classes adds fading effect when closing the alert message.

```html
<div class="alert alert-danger alert-dismissible fade show">
```



## 9. Buttons

B4 provides different styles of buttons, that can be used on `<a>`, `<button>`, or `<input>` elements.

![buttons](./imgs/7.png)

```html
<button type="button" class="btn">Basic</button>
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-dark">Dark</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-link">Link</button>
```



#### Button Outline

B4 provides 8 outline/bordered buttons:

![buttonoutline](./imgs/8.png)

```html
<button type="button" class="btn btn-outline-primary">1</button>
<button type="button" class="btn btn-outline-secondary">2</button>
<button type="button" class="btn btn-outline-success">ok</button>
<button type="button" class="btn btn-outline-info">Info</button>
<button type="button" class="btn btn-outline-warning">Warn</button>
<button type="button" class="btn btn-outline-danger">Danger</button>
<button type="button" class="btn btn-outline-dark">Dark</button>
<button type="button" class="btn btn-outline-light text-dark"> Light</button>
```



#### Button Sizes

Use the `.btn-lg` or `btn-sm` classes for large or small buttons:

![buttonsizes](./imgs/9.png)

```html
<button type="button" class="btn btn-primary btn-lg">Large</button>
<button type="button" class="btn btn-primary">Default</button>
<button type="button" class="btn btn-primary btn-sm">Small</button>
```



#### Block Level Buttons

Add class `.btn-block` to create a block button with full width of parent element:

![buttonblock](./imgs/10.png)

```html
<button type="button" class="btn btn-primary btn-block"></button>
```



#### Active / Disabled Buttons

The class `.active` makes a button appear pressed, and the `disabled` attribute makes a button unclickable. The `<a>` elements don't support `disabled` attrib, so must use `.disabled` class to make it visually appear disabled. 

![activedisabledbtn](./imgs/11.png)

```html
<button type="button" class="btn btn-primary active">Active</button>
<button type="button" class="btn btn-primary" disabled>Dis</button>
<a href="#" class="btn btn-primary disabled">Disabled LINK</a>
```



#### Spinner Buttons

You can add "spinners" to a button (see [Spinners section](#13. Spinners) to learn more about it).

![loadingbtn](./imgs/12.png)

```html
<button class="btn btn-primary">
  	<span class="spinner-border spinner-border-sm"></span> Loading
</button>
```



## 10. Button Groups

B4 allows you to group a series of buttons together (on a single line) in a button group. Use a `<div>` with `.btn-group` class to create one:

![btngrp](./imgs/13.png)

```html
<div class="btn-group">
  <button type="button" class="btn btn-primary">Apple</button>
  <button type="button" class="btn btn-primary">Samsung</button>
  <button type="button" class="btn btn-primary">Sony</button>
</div>
```

> **Tip:** Instead of applying button sizes to every button in a group, use class `.btn-group-lg` or `.btn-group-sm` for a large or a small button group:



#### Vertical Button Group

B4 also supports vertical button groups. Use `.btn-group-vertical`

![verticalbtngrp](./imgs/14.png)



#### Nesting Button Groups & Dropdown Menus

Nest button groups to create dropdown menus (you will learn more about dropdowns in a later chapter)

![dropdownmenu](./imgs/15.png)

```html
<div class="btn-group">
  	<button type="button" class="btn btn-primary">Apple</button>
  	<button type="button" class="btn btn-primary">Samsung</button>
  	<div class="btn-group">
    	<button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown">
       Sony
    	</button>
    	<div class="dropdown-menu">
      	<a class="dropdown-item" href="#">Tablet</a>
      	<a class="dropdown-item" href="#">Smartphone</a>
    	</div>
  	</div>
</div>
```



#### Split Button Dropdowns

![splitbtndropdown](./imgs/16.png)

```html
<div class="btn-group">
  	<button type="button" class="btn btn-primary">Sony</button>
  	<button type="button" class="btn btn-primary dropdown-toggle dropdown-toggle-split" data-toggle="dropdown">
    	<span class="caret"></span>
  	</button>
  	<div class="dropdown-menu">
    	<a class="dropdown-item" href="#">Tablet</a>
    	<a class="dropdown-item" href="#">Smartphone</a>
  	</div>
</div>
```



#### Vertical Button Group w/ Dropdown

![verticalbtngrpwdropdown](./imgs/17.png)

```html
<div class="btn-group-vertical">
  	<button type="button" class="btn btn-primary">Apple</button>
  	<button type="button" class="btn btn-primary">Samsung</button>
  	<div class="btn-group">
    	<button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown">Sony</button>
       	<div class="dropdown-menu">
      		<a class="dropdown-item" href="#">Tablet</a>
      		<a class="dropdown-item" href="#">Smartphone</a>
    	</div>
  	</div>
</div>
```



#### Button Groups Side by Side

Button groups are "inline" by default, which makes them appear side by side when you have multiple groups:

![btngrpaside](./imgs/18.png)

```html
<div class="btn-group">
  <button type="button" class="btn btn-primary">Apple</button>
  <button type="button" class="btn btn-primary">Samsung</button>
  <button type="button" class="btn btn-primary">Sony</button>
</div>
<div class="btn-group">
  <button type="button" class="btn btn-primary">BMW</button>
  <button type="button" class="btn btn-primary">Mercedes</button>
  <button type="button" class="btn btn-primary">Volvo</button>
</div>
```



## 11. Badges

Badges are used to add additional information to any content. Use the `.badge` class together with a contextual class (like `.badge-secondary`) within `<span>` elements to create rectangular badges. Note that badges scale to match the size of the parent element (if any).



#### Contextual Badges

Use any of the contextual classes (`.badge-*`) to change the color of a badge:

![badges](imgs/19-bug.png)



#### Pill Badges

Use the `.badge-pill` class to make the badges more round:

![badges](./imgs/20-bug.png)



#### Badge inside an Element

An example of using a badge inside a button: ![badge](./imgs/21.png)

```html
<button type="button" class="btn btn-primary">
  	Messages <span class="badge badge-light"> 4 </span>
</button>
```



## 12. Progress Bar

It can be used to show users how far along they are in a process.

![progressbar](./imgs/22.png)

To create a default progress bar, add a `.progress` class to a container element and add the `.progress-bar` class to its child element. Use the CSS `width` property to set the % of progress.

```html
<div class="progress">
  	<div class="progress-bar" style="width:70%"></div>
</div>
```



#### Progress Bar Height

The default height of the progress bar is `16px`. Use the CSS `height` property to change it. You must set the same height for the progress container and bar:

![pbarheight](./imgs/23.png)

```html
<div class="progress" style="height:20px">
  	<div class="progress-bar" style="width:40%, height:20px"></div>
</div>
```



#### Progress Bar Labels

Add text inside the progress bar to show the visible percentage:

![pbadlabels](./imgs/24.png)

```html
<div class="progress">
  	<div class="progress-bar" style="width: 70%"> 70% </div>
</div>
```



#### Colored Progress Bar

By default the progress bar is blue (primary). Use any of the B4 contextual background classes to its color:

![pbarcolor](./imgs/25.png)

```html
<!-- Blue -->
<div class="progress">
  	<div class="progress-bar" style="width:10%"></div>
</div>

<!-- Green -->
<div class="progress">
  	<div class="progress-bar bg-success" style="width:20%"></div>
</div>

<!-- Turquoise -->
<div class="progress">
  	<div class="progress-bar bg-info" style="width:30%"></div>
</div>

<!-- Orange -->
<div class="progress">
   <div class="progress-bar bg-warning" style="width:40%"></div>
</div>

<!-- Red -->
<div class="progress">
  	<div class="progress-bar bg-danger" style="width:50%"></div>
</div>

<!-- White -->
<div class="progress border">
  	<div class="progress-bar bg-white" style="width:60%"></div>
</div>

<!-- Grey -->
<div class="progress">
  	<div class="progress-bar bg-secondary" style="width:70%"></div>
</div>

<!-- Light Grey -->
<div class="progress border">
  	<div class="progress-bar bg-light" style="width:80%"></div>
</div>

<!-- Dark Grey -->
<div class="progress">
  	<div class="progress-bar bg-dark" style="width:90%"></div>
</div>
```



#### Striped Progress Bar

Use the `.progress-bar-striped` class to add stripes to the progress bars:

![stripedpbar](./imgs/26.png)

```html
<div class="progress">
  <div class="progress-bar progress-bar-striped" style="width:40%"></div> </div>
```



#### Animated Progress Bar

Add the `.progress-bar-animated` class to  animate the striped progress bar

```html
<div class="progress-bar progress-bar-striped progress-bar-animated" style="width:40%"></div>
```



#### Multiple Progress Bars

Progress bars can also be stacked:

![multiplepbar](./imgs/27.png)

```html
<div class="progress">
  <div class="progress-bar bg-success" style="width:40%">Free</div>
  <div class="progress-bar bg-warning" style="width:10%">Warn</div>
  <div class="progress-bar bg-danger" style="width:20%">Danger</div>
</div>
```



## 13. Spinners

To create a spinner/loader, use the `.spinner-border` class:       ![spin](./imgs/28.png)

```html
<div class="spinner-border"></div>
```



#### Colored Spinners

Use any **text color utilites** to add a color to the spinner:

![spincolored](./imgs/29.png)

```html
<div class="spinner-border text-muted"></div>
<div class="spinner-border text-primary"></div>
<div class="spinner-border text-success"></div>
<div class="spinner-border text-info"></div>
<div class="spinner-border text-warning"></div>
<div class="spinner-border text-danger"></div>
<div class="spinner-border text-secondary"></div>
<div class="spinner-border text-dark"></div>
<div class="spinner-border text-light"></div>
```



#### Growing Spinners

Use the `.spinner-grow` class if you want the spinner/loader to grow instead:

![spingrow](./imgs/30.png)

```html
<div class="spinner-grow text-muted"></div>
<div class="spinner-grow text-primary"></div>
<div class="spinner-grow text-success"></div>
<div class="spinner-grow text-info"></div>
<div class="spinner-grow text-warning"></div>
<div class="spinner-grow text-danger"></div>
<div class="spinner-grow text-secondary"></div>
<div class="spinner-grow text-dark"></div>
<div class="spinner-grow text-light"></div>
```



#### Spinner Size

Use `.spinner-border-sm` or `.spinner-grow-sm` for a smaller spinner:  ![spinsize](./imgs/31.png)

```html
<div class="spinner-border spinner-border-sm"></div>
<div class="spinner-grow spinner-grow-sm"></div>
```



#### Spinner Buttons

You can also add spinners to a button, with or without text:

![spinbuton](./imgs/32.png)

````html
<button class="btn btn-primary">
	<span class="spinner-border spinner-border-sm"></span>
</button>

<button class="btn btn-primary">
  	<span class="spinner-border spinner-border-sm"></span> Loading..
</button>

<button class="btn btn-primary" disabled>
  	<span class="spinner-border spinner-border-sm"></span> Loading..
</button>

<button class="btn btn-primary" disabled>
      <span class="spinner-grow spinner-grow-sm"></span> Loading..
</button>
````



## 14. Pagination

For a multi-page web sites, you can add some sort of pagination.

![pag](./imgs/33.png)

For basic pagination, add `.pagination` class to an `<ul>` element. Then add the `.page-item` to each `<li>` and a `.page-link` class to each `<a>` inside `<li>`:

````html
<ul class="pagination">
   <li class="page-item"><a class="page-link" href="#">Pre</a></li>
   <li class="page-item"><a class="page-link" href="#">1</a></li>
   <li class="page-item"><a class="page-link" href="#">2</a></li>
   <li class="page-item"><a class="page-link" href="#">3</a></li>
   <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>
````



#### Active State

The `.active` class is used to "highlight" the current page:

![pageact](./imgs/34.png)

````html
<ul class="pagination">
   <li class="page-item"><a class="page-link" href="#">Pre</a></li>
   <li class="page-item"><a class="page-link" href="#">1</a></li>
   <li class="page-item active"><a class="page-link" href="#">2</a>    </li>
   <li class="page-item"><a class="page-link" href="#">3</a></li>
   <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>
````



#### Disabled State

The `.disabled` class is used for un-clickable links:

![pagedisabled](./imgs/35.png)

````html
<ul class="pagination">
   <li class="page-item disabled"><a class="page-link" href="#">Previous</a></li>
   <li class="page-item"><a class="page-link" href="#">1</a></li>
   <li class="page-item"><a class="page-link" href="#">2</a></li>
   <li class="page-item"><a class="page-link" href="#">3</a></li>
   <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>
````



#### Pagination Sizing

Pagination blocks can also be sized to a larger or a smaller size. Add class `.pagination-lg` for larger blocks or `.pagination-sm` for smaller blocks:

![pagesize](./imgs/36.png)

````html
<ul class="pagination pagination-lg">
  <li class="page-item"><a class="page-link" href="#">Pre</a></li>
  <li class="page-item"><a class="page-link" href="#">1</a></li>
  <li class="page-item"><a class="page-link" href="#">2</a></li>
  <li class="page-item"><a class="page-link" href="#">3</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>

<ul class="pagination pagination-sm">
  <li class="page-item"><a class="page-link" href="#">Pre</a></li>
  <li class="page-item"><a class="page-link" href="#">1</a></li>
  <li class="page-item"><a class="page-link" href="#">2</a></li>
  <li class="page-item"><a class="page-link" href="#">3</a></li>
  <li class="page-item"><a class="page-link" href="#">Next</a></li>
</ul>
````



#### Pagination Alignment

Use utility classes to change the alignment of the pagination:

![pagealign](./imgs/37.png)

````html
<!-- Default (left-aligned) -->
<ul class="pagination" style="margin:20px 0">
  	<li class="page-item">...</li>
</ul>

<!-- Center-aligned -->
<ul class="pagination justify-content-center" style="margin:20px 0">
  	<li class="page-item">...</li>
</ul>

<!-- Right-aligned -->
<ul class="pagination justify-content-end" style="margin:20px 0">
  	<li class="page-item">...</li>
</ul>
````

> **Tip:** Read more about Bootstrap 4 Utility/Helper classes in our [BS4 Utilities](https://www.w3schools.com/bootstrap4/bootstrap_utilities.asp).



#### Breadcrumbs

Another form for pagination, is breadcrumbs. 

![breadcrumbs](./imgs/38.png)

The `.breadcrumb` and `.breadcrumb-item` classes indicates the current page's location within a navigational hierarchy:

````html
<ul class="breadcrumb">
  	<li class="breadcrumb-item"><a href="#">Photos</a></li>
  	<li class="breadcrumb-item"><a href="#">Summer 2017</a></li>
  	<li class="breadcrumb-item"><a href="#">Italy</a></li>
  	<li class="breadcrumb-item active">Rome</li>
</ul>
````



## 15. List Groups

The basic list group is an unordered list with items. To create a list group, use an `<ul>` element with class `.list-group`, and `<li>` with `.list-group-item`:

![listgrp](./imgs/39-bug.png)

````html
<ul class="list-group">
  	<li class="list-group-item">First item</li>
  	<li class="list-group-item">Second item</li>
  	<li class="list-group-item">Third item</li>
</ul>
````



#### Active State

Use the `.active` class to highlight the current item:

![lacti](./imgs/40.png)

```html
<ul class="list-group">
  	<li class="list-group-item active">Active item</li>
  	<li class="list-group-item">Second item</li>
 	 <li class="list-group-item">Third item</li>
</ul>
```



#### List Group w/ Linked Items

To create a list group with linked items, use `<div>` instead of `<ul>` and `<a>` instead of `<li>`. Optionally, add the `.list-group-item-action` class if you want a grey background color on hover:

```html
<div class="list-group">
  <a href="#" class="list-group-item list-group-item-action">1</a>
  <a href="#" class="list-group-item list-group-item-action">2</a>
  <a href="#" class="list-group-item list-group-item-action">3</a>
</div>
```



#### Disabled Item

The `.disabled` class adds a lighter text color to the disabled item. And when used on links, it will remove the hover effect:

![disableditem](./imgs/41.png)

```html
<div class="list-group">
  <a href="#" class="list-group-item disabled">Disabled item</a>
  <a href="#" class="list-group-item disabled">Disabled item</a>
  <a href="#" class="list-group-item">Third item</a>
</div>
```



#### Flush / Remove Borders

The `.list-group-flush` class removes some borders and rounds corners:

```html
<ul class="list-group list-group-flush">
	<li class="list-group-item">First item</li>
  	<li class="list-group-item">Second item</li>
  	<li class="list-group-item">Third item</li>
</ul>
```



#### Horizontal List Groups

To display the list items horizontally instead of vertically, add `.list-group-horizontal` class to `.list-group`:

![horizontal](./imgs/42.png)

```html
<ul class="list-group list-group-horizontal">
  	<li class="list-group-item">First item</li>
  	<li class="list-group-item">Second item</li>
  	<li class="list-group-item">Third item</li>
</ul>
```



#### Contextual Classes

Contextual classes can be used to color list items:

![coloreditems](./imgs/43.png)

```html
<ul class="list-group">
  <li class="list-group-item list-group-item-success">Success</li>
  <li class="list-group-item list-group-item-secondary">Second</li>
  <li class="list-group-item list-group-item-info">Info</li>
  <li class="list-group-item list-group-item-warning">Warning</li>
  <li class="list-group-item list-group-item-danger">Danger</li>
  <li class="list-group-item list-group-item-primary">Primary</li>
  <li class="list-group-item list-group-item-dark">Dark</li>
  <li class="list-group-item list-group-item-light">Light</li>
</ul>
```



#### Link Items w/ Contextual Classes

```html
<div class="list-group">
  <a href="#" class="list-group-item list-group-item-action">Action item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-success">Success item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-secondary">Secondary item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-info">Info item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-warning">Warning item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-danger">Danger item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-primary">Primary item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-dark">Dark item</a>
  <a href="#" class="list-group-item list-group-item-action list-group-item-light">Light item</a>
</div>
```



#### List Group w/ Badges

Combine `.badge` classes with utility classes to add badges inside the list group:

![lgbadges](./imgs/44.png)

```html
<ul class="list-group">
  	<li class="list-group-item d-flex justify-content-between align-items-center">
    	Inbox
    	<span class="badge badge-primary badge-pill">12</span>
  	</li>
  	<li class="list-group-item d-flex justify-content-between align-items-center">
    	Ads
    	<span class="badge badge-primary badge-pill">50</span>
  	</li>
  	<li class="list-group-item d-flex justify-content-between align-items-center">
    	Junk
    	<span class="badge badge-primary badge-pill">99</span>
  	</li>
</ul>
```



## 16. Cards
<div><p style="width: 60%; float: left">A card in Bootstrap 4 is a bordered box with some padding around its content. It includes options for headers, footers, content, colors, etc.</p>
<img src="./imgs/45.png" alt="card" style="float: right; zoom: 67%;" />
</div>

















#### Basic card

A basic card is created with `.card` class, content inside has a `.card-body`:

![bcard](./imgs/46.png)

```` html
<div class="card"> <div class="card-body">Basic card</div> </div>
````



#### Header and Footer

The `.card-header` class adds a heading to the card and the `.card-footer` class adds a footer to the card:

![haf](./imgs/47.png)

```html
<div class="card">
  	<div class="card-header">Header</div>
  	<div class="card-body">Content</div>
  	<div class="card-footer">Footer</div>
</div>
```



#### Contextual Cards

To add a background color the card, use `.bg-primary`, `.bg-success`, `.bg-info`, `.bg-warning`, `.bg-danger`, `.bg-secondary`, `.bg-dark` and `.bg-light`.



#### Tiles, Text and Links

Use `.card-title` to add card titles to any heading element. The `.card-text` class is used to remove bottom margins for a `<p>` element if it is the last child (or the only one) inside `.card-body`. The `.card-link` class adds a blue color to any link, and a hover effect.

![titletextlink](./imgs/48.png)

```html
<div class="card">
  	<div class="card-body">
    	<h4 class="card-title">Card title</h4>
    	<p class="card-text">Some example text.</p>
    	<a href="#" class="card-link">Card link</a>
    	<a href="#" class="card-link">Another link</a>
  	</div>
</div>
```



#### Card Images

Add `.card-img-top` or `.card-img-bottom` to an `<img>` to place the image at the top or at the bottom inside the card. Note that we have added the image outside of the `.card-body` to span the entire width:

![cardimg](./imgs/49.png)

```html
<div class="card" style="width:400px">
  	<img class="card-img-top" src="im1.png" alt="Card image">
  	<div class="card-body">
    	<h4 class="card-title">John Doe</h4>
    	<p class="card-text">Some example text.</p>
    	<a href="#" class="btn btn-primary">See Profile</a>
 	 </div>
</div>
```



#### Stretched Link

Add the `.stretched-link` class to a link inside the card, and it will make the whole card clickable and hoverable (the card will act as a link):

```html
<a href="#" class="btn btn-primary stretched-link">See Profile</a>
```



#### Card Image Overlays

<div><p style="width: 60%; float: left">Turn an image into a card background and use <code>.card-img-overlay</code> to add text on top of the image:</p>
<img src="./imgs/50.png" alt="card" style="float: right; zoom: 45%;" />
</div>













```html
<div class="card" style="width:500px">
  	<img class="card-img-top" src="img1.png" alt="Card image">
  	<div class="card-img-overlay">
    	<h4 class="card-title">John Doe</h4>
    	<p class="card-text">Some example text.</p>
    	<a href="#" class="btn btn-primary">See Profile</a>
 	 </div>
</div>
```



#### Card Columns

The `.card-columns` class creates a masonry-like grid of cards (like pinterest). The layout will automatically adjust as you insert more cards.

> **Note:** The cards are displayed vertically on small screens ( < 576px )

<img src="./imgs/51.png" alt="cardcol" style="zoom:67%;" />

```html
<div class="card-columns">
  <div class="card bg-primary">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the first card</p>
    </div>
  </div>
  <div class="card bg-warning">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the second card</p>
    </div>
  </div>
  <div class="card bg-success">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the third card</p>
    </div>
  </div>
  <div class="card bg-danger">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the fourth card</p>
    </div>
  </div>
  <div class="card bg-light">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the fifth card</p>
    </div>
  </div>
  <div class="card bg-info">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the sixth card</p>
    </div>
  </div>
</div>
```



#### Card Deck

The `.card-deck` class creates a grid of cards that are of **equal height and width**. The layout will automatically adjust as you insert more cards.

> **Note:** The cards are displayed vertically on small screens ( < 576px ).

<img src="./imgs/52.png" alt="carddeck" style="zoom:67%;" />

```html
<div class="card-deck">
  <div class="card bg-primary">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the first card</p>
    </div>
  </div>
  <div class="card bg-warning">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the second card</p>
    </div>
  </div>
  <div class="card bg-success">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the third card</p>
    </div>
  </div>
  <div class="card bg-danger">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the fourth card</p>
    </div>
  </div>
</div>
```



#### Card Group

The `.card-group` class is similar to `.card-deck`. The only difference is that the `.card-group` class removes left and right margins between each card.

>  **Note:** The cards are displayed vertically on small screens ( < 576px ), **WITH** top and bottom margin:

<img src="./imgs/53.png" alt="cardgrp" style="zoom:67%;" />

```html
<div class="card-group">
  <div class="card bg-primary">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the first card</p>
    </div>
  </div>
  <div class="card bg-warning">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the second card</p>
    </div>
  </div>
  <div class="card bg-success">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the third card</p>
    </div>
  </div>
  <div class="card bg-danger">
    <div class="card-body text-center">
      <p class="card-text">Some text inside the fourth card</p>
    </div>
  </div>
</div>
```



## 17. Dropdowns

<div><p style="width: 60%; float: left">A dropdown is a toggleable menu that allows the user to choose one value from a predefined list:</p>
<img src="./imgs/54.png" alt="card" style="float: right; zoom: 80%;" />
</div>







```html
<div class="dropdown">
	<button type="button" class="btn btn-primary dropdown-toggle" data-toggle="dropdown">Dropdown button</button>
  	<div class="dropdown-menu">
        <a class="dropdown-item" href="#">Link 1</a>
    	<a class="dropdown-item" href="#">Link 2</a>
    	<a class="dropdown-item" href="#">Link 3</a>
  	</div>
</div>
```

**Example explained:** The `.dropdown` class indicates a dropdown menu. To open the dropdown menu, use a button or a link with a class of `.dropdown-toggle` and the `data-toggle="dropdown"` attribute.

Add the `.dropdown-menu` class to a `<div>` element to build the dropdown. Then add the `.dropdown-item` class to each element (`<a>` or `<button>`) inside it.



#### Dropdown Divider

The `.dropdown-divider` class is used to separate links inside the dropdown menu with a thin horizontal border:

<img src="./imgs/55.png" alt="dddivider" style="zoom: 80%;" />

```html
<div class="dropdown-divider"> </div>
```



#### Dropdown Header

The `.dropdown-header` class is used to add headers inside the dropdown:

<img src="./imgs/56.png" alt="ddh" style="zoom:80%;" />

```html
<div class="dropdown-header">Dropdown header 1</div>
```



#### Disabled and Active items

Highlight a specific dropdown item with the `.active` class. To disable an item in the dropdown menu, use the `.disabled` class.

<img src="./imgs/57.png" alt="disabledactivedd" style="zoom:80%;" />

```html
<a class="dropdown-item active" href="#">Active</a>
<a class="dropdown-item disabled" href="#">Disabled</a>
```



#### Dropdown Position

You can also create a "dropright" or "dropleft" menu, by adding the `.dropright` or `.dropleft` class to the dropdown. Note that the arrow is added automatically:

<div>
<img src="./imgs/58.png" alt="58" style="zoom:80%; float:left" />
<img src="./imgs/59.png" alt="59" style="zoom:80%; float:right" />
</div>





````html
<div class="dropdown dropright"></div>
<div class="dropdown dropleft"></div>
````



#### Dropdown Menu Right





































