# Bits.scss grid

Component for a CSS grid. The grid makes use of `inline-block` and
`box-sizing` to provide features that float-based layouts cannot.

N.B. This component relies on particular dimensions being applied to cells in
the grid via other classes. For example, [Bits.scss dimension](https://github.com/bits-scss/utils-dimension)
or the [Bits.scss grid layouts](https://github.com/bits-scss/grid-layouts) extension.

Read more about [Bits.scss toolkit](https://github.com/bits-scss/bits.scss).

## Installation

* __Bower:__ `bower install --save bits-scss-grid`
* __Download:__ [zip](https://github.com/bits-scss/grid/zipball/master), [tar.gz](https://github.com/bits-scss/grid/tarball/master)
* __Git:__ `git clone https://github.com/bits-scss/grid.git`

## Available SASS variables

* `bits-components-ns` - components namespace, defaults to 'bits-'
* `bits-grid-gutter` - size of grid gutter, defaults to 0

## Available classes

* `Grid` - core grid component
* `Grid--center` - horizontally centers all grid units
* `Grid-cell` - sub-object class reprezenting a unit
* `Grid-cell--center` - horizontally centers one unit

## Features

* Fluid layout.
* Intelligent cell wrapping.
* Horizontal centering of cells.
* Custom vertical alignment of cells (top, bottom, or middle).
* Cell width is controlled independently of grid gutter.
* Infinite nesting.
* Built-in redundancy.

## Usage

A simple grid is easy to create. A grid container can have any number of cells.
Each cell can be directly or indirectly styled to control their width and
alignment.

```html
<div class="Grid">
  <div class="Grid-cell u-size1of2"></div>
  <div class="Grid-cell u-size1of2"></div>
  <div class="Grid-cell u-size1of3"></div>
  <div class="Grid-cell u-size1of3"></div>
</div>
```

All cells within a grid can be centered by adding the `Grid--center` class to
the grid container:

```html
<div class="Grid Grid--center">
  <div class="Grid-cell u-size1of3"></div>
  <div class="Grid-cell u-size1of3"></div>
</div>
```

Or individual cells can be centered on their own line by adding the
`Grid-cell--center` class to a cell:

```html
<div class="Grid">
  <div class="Grid-cell u-size1of2"></div>
  <div class="Grid-cell u-size1of2"></div>
  <div class="Grid-cell Grid-cell--center u-size3of4"></div>
</div>
```

The core grid component includes no gutters by default.

If you need a gutter of, for example, 10px, set the appropriate variable:

```scss
$bits-grid-gutter: 10px;
```

## Requirements

* Sass 3.2+

## Browser support

* Google Chrome (latest)
* Opera (latest)
* Firefox 4+
* Safari 5+
* Internet Explorer 8+
