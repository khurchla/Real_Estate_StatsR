# Limited Liability Company Real Estate Owners in Philadelphia

Final project for MICA MPS Data Analytics & Visualization, statistics course (R), December 2020. Kathryn Hurchla.

- `Kathryn_Hurchla_final_project_RE_LLC_Slidy.Rmd`: R Markdown source (Slidy presentation)
- `Kathryn_Hurchla_final_project_RE_LLC_Slidy.html`: rendered presentation. Open it in a web browser.

## Data
The analysis uses the City of Philadelphia **Real Estate Transfers** dataset (`RTT_SUMMARY`), filtered to deeds (`document_type = 'DEED'`). The resulting CSV (about 290 MB, pulled 2020-12-10) is too large for GitHub, so it isn't included here.

- Dataset: https://opendataphilly.org/dataset/real-estate-transfers
- Download used, via the City's public Carto SQL API (no key required):
  `https://phl.carto.com/api/v2/sql?filename=RTT_SUMMARY&format=csv&skipfields=cartodb_id,the_geom,the_geom_webmercator&q=SELECT *, ST_Y(the_geom) AS lat, ST_X(the_geom) AS lng FROM RTT_SUMMARY WHERE document_type = 'DEED'`
- Save the file as `files/RTT_Summary_Deeds.csv` in the working directory. The Rmd reads it from there. See the Rmd's data section for full details.

Note: the City's data has been updated since 2020, so a new download won't exactly match the original results.
