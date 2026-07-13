# Quiz with SVG maps

Quiz where you get a name and should click on the correct region on
the map.

Try it on:

* [Swedish "landskap"](https://uablrek.github.io/landskap/landskap.html)
* [Peruvian regions](https://uablrek.github.io/landskap/peru.html)

## Maps

The maps are [SVG](https://en.wikipedia.org/wiki/SVG), and must be
embedded in html for [easy manipulation from javascript](
https://stackoverflow.com/questions/14068031/embedding-external-svg-in-html-for-javascript-manipulation)

The maps are derived from:

* [Sweden](http://commons.wikimedia.org/wiki/File:Sverigekarta-Landskap.svg)
* [Perú](https://commons.wikimedia.org/wiki/File:Peru_-_%28Template%29.svg)

The original maps are created with [Inkscape](https://inkscape.org/),
and should be cleaned with [svgo](https://svgo.dev/):

```
svgo --config=svgo.config.mjs --pretty - < original.svg > clean.svg
```

Then you must add a region name as `id` for all region paths.

## License

The derived maps have the same License as the originals (as they
must). The scripts are under CC-BY-4.0 License.

## Character encoding

I created the first version around 2012 with `iso-8859-1` encoding,
and `XHTML 1.0`. That must be updated to `utf-8`, and `HTML5`.

```
iconv -c -t UTF-8 -f ISO8859-1 input_file > output_file
```
(doesn't work)
