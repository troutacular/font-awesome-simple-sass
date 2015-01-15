# Font Awesome Simple Sass

This is a custom method of including [fontawesome.io] (http://fontawesome.io) fonts into your site without loading the entire css library.

To maintain this file, copy the font variables from [sccs/_variables.scss] (https://github.com/FortAwesome/Font-Awesome) and replace the `$fa-var-`
with `$fa-` in the list 'Font Awesome Variable List'.


## Example
`.item { @include fa-icon($fa-github,after,.5em,inside,green,true); }`


## Usage
`@include fa-icon([$icon], [placement], [padding], [alignment], [color], [replace-text]);`


### Icon
Use the name provided on http://fontawesome.io/icons/ as a variable 'fa-github-square' would be entered as '$fa-github-square'

Example: `$fa-check`


### Placement
Set the placement of the icon in relation to the element

`before`: the icon is placed before the element [default]

`after`: the icon is placed after the element


### Padding
Specify the amount of spacing between the icon and element.

`px`, `%`, `em`, `rem`

Recommended use of 'em' to keep spacing relevant to element


### Alignment
Specify where the icon should be in relation to the bounding box of the element being applied

`inside`: icon within the bounding box

`outside`: icon outside the bounding box with absolute positioning

_Note: 'outside' applies 'relative' positioning to the element_


### Color
Set the color of the icon. Default will inherit the element color.
`[string]`


### Replace Text
Set the variable to `true` to set the icon only and make the text transparent.  

`false`: [default]

`true`: sets the text to transparent and the icon defaults to #000 unless specified by `[color]`

_Note: The icon will be 1em of whatever you have the font set.  You can set the font size of that particular item larger to make the icon larger and will only affect that class/element selector._