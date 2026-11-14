# Mountain Peak data

Static data for the Mountain Peak watch app, served by GitHub Pages at
`https://ataflorin.github.io/mountain-peak-data/`.

One file per 1 x 1 degree tile, `v1/tiles/N46E025.json` (named after its south-west corner),
with the named summits in it and its terrain; `v1/index.json` lists the tiles and the country
each lies in. The format is described in `tools/make_data.py` of the app, which writes these
files.

## Sources

- Summits: [GeoNames](https://www.geonames.org/), licensed under
  [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
- Terrain: SRTM elevation data (NASA / USGS, public domain), from the
  [AWS Terrain Tiles](https://registry.opendata.aws/terrain-tiles/), reduced to 30" cells
  holding the highest ground in each.
