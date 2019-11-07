# imfonts
Create sample images of all fonts accessible to ImageMagick

## Usage:

  imfont [ _fontname_ ]

### All fonts by default

<img align="right" src="README.md.d/GillSansShadowedMTPro-Light.png">

    imfont

When _fontname_ is omitted, sample images are created for all fonts on
the system. Each file has the same name as a font + `.png`. For
example, to the right is the file named `GillSansShadowedMTPro-Light.png`.


<br clear=all />

### Specific fonts

    imfont regex

If _fontname_ is specified, a single image is created with all
matching fonts in it. For example, this is the result on my machine of
`imfont Wood`.

	
<img src="README.md.d/Wood.png">

_Fontname_ is case insensitive and can be a regular expression.
For example,

    imfont "optima|omega"

<img src="README.md.d/OptimaOmega.png">

## List font names

If you simply want to list the fonts ImageMagick knows about, use this

    convert -list font | grep Font:
	
