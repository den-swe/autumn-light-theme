<div style="padding: 0 25px 0">
  <div align="center">
    <img height="128px"
     src="https://github.com/den-swe/autumn-light-theme/blob/921bec8aaca06bdad02d225a7eefcb7719d15e22/images/autumn.png" 
     alt="Autumn Light Theme logo">
  </div>
</div>
<h1 align="center">Autumn Light Theme (Cursive)</h1>
<h3 align="center" style="border:none">
The theme is assembled thanks to the colors from Autumn Theme (jb). 
  A combination of cursive font and FiraDank Font.</h3>
<br/>
</div>

> Italics and a special FiraDank font have been added.


## Usage
1. Install font `Fira Dank` from
   [den-swe/FiraDank](https://github.com/den-swe/FiraDank)
2. Use the font in VSCode settings (fontSize and anti-aliasing is optional)
   
```json
"editor.fontFamily": "'FiraDank'",
"editor.fontLigatures": true,
"editor.fontSize": 14,
"workbench.fontAliasing": "antialiased",
```

3. Install this theme from VSCode.
4. Install extension
   [Custom Css and Js](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)
   in VSCode
5. Configure custom css in your VSCode config

```json
"vscode_custom_css.imports": ["file:///Users/user/projects/vscode-css.css"],
```

6. With the following contents (to make cursive "monospaced")

```css
.mtki {
  margin-left: 1px;
  font-size: 1.em;
  font-weight: bold;
}
```

## Problem description

Using the custom css alternative for Operator Mono is pretty cumbersome because
of the
[Optimizations in Syntax Highlighting](https://code.visualstudio.com/blogs/2017/02/08/syntax-highlighting-optimizations)
that removed a lot of the classes and replaced them with keywords like `.mtk12`
`.mtki` `.mtkb` etc.

## Solution

This theme requires only minor customizations using the 'Custom CSS and Js
Loader' extension.

This theme is explicitly setting `font-style: italic` for these scopes (like
Operator Mono does):

- keyword.control
- storage.type
- variable.language.this
- entity.other.attribute-name
- comment.block

Furthermore, there are Ligatures available in Fira Code that we want to use. For
that the theme defines specific rules:

- storage.type.function.arrow
- punctuation.definition.comment

## Contributions

Any contribution is welcome. Please provide a good use case when things aren't
the way we expect
