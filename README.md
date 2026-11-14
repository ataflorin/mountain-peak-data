# Mountain Peak data

Static data for the Mountain Peak watch app, served by GitHub Pages at
`https://ataflorin.github.io/mountain-peak-data/`.

Per 1 x 1 degree tile (named after its south-west corner, `N46E025`): `v1/t/N46E025.json`
(its country and how many files it has), its summits in `v1/p/N46E025.<i>.json` and its terrain
in four quarters `v1/d/N46E025.<q>.json` and its towns, lakes, huts, passes and glaciers in
`v1/o/N46E025.<i>.json`, every file a few kilobytes so that a watch can take it. For views wider
than 50 km, the far land in 2 x 2 degree blocks: terrain in 2' cells `v1/c/<key>.json` and the
highest summits `v1/cs/<key>.json`. The whole globe's land, 56 S to 83 N.
`v1/index.json` lists the tiles and the country each lies in. The format is described in
`tools/make_data.py` of the app, which writes these files.

## Sources

- Summits: [GeoNames](https://www.geonames.org/), licensed under
  [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- Summits' country, towns, lakes, huts, passes, glaciers: GeoNames, as above.
- Terrain: the [Terrain Tiles on AWS](https://registry.opendata.aws/terrain-tiles/) (merged from
  SRTM, GMTED, ETOPO1 and national elevation models; see their attribution list), reduced to 30"
  and 2' cells holding the highest ground in each.
