# Bits.sass grid

Component for a CSS grid. The grid makes use of `inline-block` and
`box-sizing` to provide features that float-based layouts cannot.

N.B. This component relies on particular dimensions being applied to cells in
the grid via other classes. For example, [Bits.sass dimension](https://github.com/bits-sass/utils-dimension).
If you need gutters inbetween cells, see [Bits.sass space](https://github.com/bits-sass/utils-space).

Read more about [Bits.sass toolkit](https://github.com/bits-sass/bits.sass).

## Installation

* __Bower:__ `bower install --save bits-sass-grid`
* __Download:__ [zip](https://github.com/bits-sass/grid/zipball/master), [tar.gz](https://github.com/bits-sass/grid/tarball/master)
* __Git:__ `git clone https://github.com/bits-sass/grid.git`

## Available SASS variables

* `bits-components-ns` - components namespace, defaults to 'bits-'
* `bits-grid-columns` - list of generated columns

## Available classes

* `Grid` - core grid component
* `Grid--center` - horizontally center all grid units
* `Grid--middle` - vertically align all grid units to middle
* `Grid--bottom` - vertically align all grid units to bottom
* `Grid--[n]col` - (adjustable) grid of `n` columns
* `Grid-cell` - descendant class representing a unit
* `Grid-cell--center` - horizontally center one unit

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

## Requirements

* Sass 3.2+

## Browser support

* Google Chrome (latest)
* Opera (latest)
* Firefox 4+
* Safari 5+
* Internet Explorer 8+
