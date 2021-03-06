# Today I Learned - CLI

## Resize an image from command line

    convert -resize 50% original.png resized.jpg

`convert` is part of the ImageMagick package.

## List files and exclude directories

    find . -name '*.js' ! -path '*/vendor/*'

## Search and replace a pattern in all matching files

    git grep -l 'pattern' | xargs sed -i 's/pattern/relacement/g'

## Merge/concat/paste lines separated by a space.

    paste -s -d':'

Useful when the output of one command in on multiple lines, and a single line is wanted.

## Get the last field when using cut

(Without having to count its index)

    grep 'pattern' | rev | cut -d'/' -f 1 | rev

Uses the `rev` command to reverse all characters, select the first field,
then reverse again.
