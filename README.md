# Mountain Peak data

Static data for the Mountain Peak watch app, served by GitHub Pages at
`https://ataflorin.github.io/mountain-peak-data/`.

Per 1 x 1 degree tile (named after its south-west corner, `N46E025`): `v1/t/N46E025.json`
(its country and how many files it has), its summits in `v1/p/N46E025.<i>.json` and its terrain
in four quarters `v1/d/N46E025.<q>.json`, every file a few kilobytes so that a watch can take it.
`v1/index.json` lists the tiles and the country each lies in. The format is described in
`tools/make_data.py` of the app, which writes these files.

## Sources

- Summits: [GeoNames](https://www.geonames.org/), licensed under
  [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- Terrain: SRTM elevation data (NASA / USGS, public domain), from the
  [AWS Terrain Tiles](https://registry.opendata.aws/terrain-tiles/), reduced to 30" cells
  holding the highest ground in each.
