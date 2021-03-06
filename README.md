# Gemma
[![npm-version](https://img.shields.io/npm/v/gemma.svg?style=flat)](https://www.npmjs.com/package/gemma)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)

## Functional/atomic/whatever-we’re-calling-it CSS for fun and (complete lack of) profit
Built for performance and (re)usability, Gemma is a collection of foundational styles and classes for creating beautifully simple, highly effective CSS.

## Philosophy
Gemma’s philosophical approach to CSS is nothing new, but tried and true. It favours:

- mobile-first, lightweight styles
- responsive design as a default
- forming both basic and more nuanced components from independent, highly recombinable pieces (think Lego!)
- designing systems that are easy for developers and designers to learn and use
- keeping CSS bundles compact and quick to deliver to users

## Usage

The easiest way to use Gemma is to source it from Unpkg:

```html
<link rel='stylesheet' href='https://unpkg.com/gemma@1.1.0/public/gemma.min.css'>
```

Or you can include it as a project dependency via NPM:

```
npm i --save gemma
```

…in which case, you’ll need to import the compiled, minified code:

```css
@import '../path-to-your-copy-of/gemma/public/gemma.min.css';
```

## Class naming
Class names in Gemma follow these naming conventions:

- For classes which deal with properties that take **named** attributes, e.g. `text-align`, the class name will begin with that property’s name as an acronym, e.g. `ta`, followed by a dash, and an acronym for the attribute name, e.g. `c` for `center`. Full example: `ta-c` = `text-align: center`
- For classes which deal with properties that take **numerical** attributes, e.g. `padding-right`, the class name will begin with that property’s name as an acronym, followed by the number (without units, and **not** preceded by a dash). Full example: `pr1` = `padding-right: 1<unit/increment>`

*(Note: where several property names are part of a larger CSS module, e.g. flexbox, classes are preceded with a letter to indicate this module. Therefore the flexbox-related property `align-content` can be set with classes beginning with `fac` for `(flex) align-content`.)*

This system may seem overly concise at first, but after using the system for awhile, it should start to feel natural. The brevity of this naming system saves you from typing more characters than necessary, and saves space in your markup. (On a personal note, previous CSS libraries that I’ve worked on have erred more on the side of verbosity, where the class for `text-align: left` would be `align-left`. While this felt fool-proof at first, after several months of usage, typing such a comparatively long class name became annoying, especially once the library classes had become memorised.)

## Development
**Full disclosure:** I built Gemma primarily as a personal exercise. If you’re looking for something that will be regularly updated, you might consider something more active and full-featured, like [Tachyons](https://tachyons.io).

With that said, if you want to work on Gemma as a fork or to submit a contribution:

1. Clone the latest master branch of the repository (`git clone https://github.com/colepeters/gemma.git`)
2. `cd` to the repository and install dependencies via npm (`cd gemma && npm i`)

Development tasks are currently managed with npm scripts:

### `npm run lint`
Gemma ships with a [linting configuration](https://github.com/colepeters/gemma/blob/master/.stylelintrc) which is passed to [Stylelint](https://github.com/stylelint/stylelint). The lint task will examine all CSS files in the source directory, and output any linting errors to the command line via [postcss-reporter](https://github.com/postcss/postcss-reporter).

### `npm run compile`
Passes all source CSS files to [postcss-cssnext](https://github.com/MoOx/postcss-cssnext), via [postcss-cli](https://github.com/postcss/postcss-cli). This transforms source CSS custom properties to their computed values and minifies the output, resulting in a `gemma.min.css` file.

* * *

Additional useful information can be found in [the source files readme](https://github.com/colepeters/gemma/tree/master/src).

## Inspiration
Gemma’s philosophical and stylistic leanings have been heavily influenced by the following projects:

- [BassCSS](http://basscss.com)
- [Tachyons](http://tachyons.io)
- [OOCSS](https://github.com/stubbornella/oocss)

and the following people:

- [@jxnblk](http://jxnblk.com)
- [@mrmrs](http://mrmrs.io)
- [@stubbornella](http://www.stubbornella.org/content/)
- [@necolas](http://nicolasgallagher.com/)
- [@csswizardry](http://csswizardry.com/)

(and likely more whom I’ve forgotten to mention).

* * *

_A gemma (/ˈdʒɛmə/ with a soft "g", as in "general") is a single cell, or a mass of cells, that detaches from the parent and develops into a new individual._
