# Shell Goodies

Here are some shell commands I use pretty often.

## Thumbnail All Images in Directory

Requires *convert* from ImageMagick.

	$ ls . | while read IMAGE; do convert "$IMAGE" -size 100x100 "small-$IMAGE"; done

## Reduce Tab Indent of File

	$ sed -e 's/^\t//' myfile.txt > myfile-lesstab.txt

## Nano with 4-Space Indenting

	$ nano -ET 4 myfile.txt

## Take a Screenshot

Requires *scrot*.

	$ scrot myscreen.png

## Encode/Decode Spoiler Text

	$ cat myspoiler.txt | rot13

## Converting Documents with Pandoc

### ODT

	$ pandoc -Sso output.odt input.md

### PDF

	$ pandoc -Sso output.pdf input.md

### EPUB

	$ pandoc -Sso output.pdf input.md
