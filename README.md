# uioposter
The document class `uioposter` is used to create scientific posters
that show affiliation with the University of Oslo.
It features the official colours and logo of the university.

For posters that display a collaboration with other institutions,
it is recommended that you use a more neutral design.

Also available on [Overleaf](https://www.overleaf.com/latex/templates/uioposter/tsmrpnztthrr).

##### Disclaimer
The design was originally created for portrait mode.
Landscape mode has only been treated as an afterthought,
with the layout being modified in the simplest possible way.
Admittedly, this leaves the appearance of landscape mode posters somewhat clunky.

![Image of portrait mode example](https://i.imgur.com/uxa0Hdm.png)

## Usage
At the core,
`uioposter` is the document class `beamer` together with the package `beamerposter`.
As such, you use the usual `beamer` syntax:
The poster consists of a single `frame`
that is typically divided into `columns`
and filled with instances of `block`, `exampleblock` and `alertblock`.
Alternatively, for complete control over placements, use the package `textpos`.

The headline collects data from the `\title`, `\author` and `\institute` commands.
Because of the university logo,
it is rarely necessary to specify the authors' departments.
Hence `\institute` can instead be used for contact information or be left out completely.

The cross-reference macro `\enumref{key}` prints numbers
in the same style as items in the `enumerate` environment.
This is useful for cross-referencing a numbered list.

## Class Options
By default,
posters are created in portrait mode.
To change this,
use the option `landscape`.
Use `norsk` to get the university logo in Norwegian.

The size of the poster can be specified with one of the options
`a0paper`, `a1paper`, `a2paper`, `a3paper`, `a4paper`, `a5paper` or `a6paper`.
The default is `a0paper`.
If you choose one of the other sizes,
the poster is first created in the A0 format and then shrunk.
The only impact of this is that if you specify the size of an image using absolute units,
such as centimeters,
then the image will turn out smaller than expected.

## Footline
The footline has the most extravagant use of white space in the design.
You can remove the footline by adding `\setbeamertemplate{footline}{}` to the preamble.
If you need more space,
but are not comfortable with removing the footline,
then you can use the `textpos` package to place white text on the footline.
This space is suitable for contact information or references.

## Dependencies
The following is loaded by `uioposter`:
* `beamer`
* `beamerposter`
* `beramono`
* `calc`
*  `etoolbox`
* `fontenc`
* `inputenx`
* `lmodern`
* `microtype`
* `pgfpages`
