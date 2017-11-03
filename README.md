# Package Bundling

Contenders for JS bundling

- `browserify`
- `webpack`
- `rollup`

## Browserify

Pros

- simple to script, unix pipe style
- Large ecosystem

Cons

- lots of buggy plugins

## Webpack

Pros

- Widely used, especially with React
- Support for bundle splitting and live code update

Cons

- Live code update only makes sense with CSS and react
- Huge, complex config file
- Lots of assumptions
- Wants to own your entire build pipeline, including some wacky approaches to CSS
- All-or-nothing
- Doesn't support ES6 modules correctly, it's its own format with ES6 syntax

## Rollup

Pros

- Supports ES6 modules
- Tree-shaking dead code elimination
- Fast
- Doesn't take over your CSS pipeline
- Healthy plugin ecosystem

Cons

- None?!


# CSS Bundling

Contenders

- `less`
- `sass`
- `postcss`
- `webpack`

## Webpack

Pros

- Support for bundle splitting and live code update

Cons

- Super complex
- Has weird opinions

## Less

Pros

- Most native to the PHP ecosystem

Cons

- PHP compiler is slow and old, JS compiler is better

## Sass

Pros

- Most common CSS metalanguage

Cons

- Compiler is a C dependency that's kinda hard to manage well

## PostCSS

Pros

- Simple, flexible toolchain in javascript
- Large ecosystem of minimal plugins

Cons

- No LESS or Sass macro language without involving those compilers

# Conclusions

`postcss` makes the most sense, I think. If we use a SMACSS approach to CSS, we need Sass's power a lot less. Nested rules are alreadym inimized, so it becomes a complex macro langauge on top of what could just be plain CSS.

`postcss` can handle annoying things like auto-prefixing and small cleanups though, and minification

`rollup` is the best for frontend javascript. It's a lot easier to get right than a webpack config, it's capable, and it uses REAL es6 modules.
