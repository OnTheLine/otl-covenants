# otl-covenants
Leaflet map of racist property covenants in Connecticut town land records, 1920s-50s

## Demo with caption
https://ontheline.github.io/otl-covenants/index-caption.html

## Embedded in two sites
- https://ontheline.trincoll.edu
- https://myCTdeed.com

## Data
- map.geojson -- spatial data joined with contents of table below, stored in this GitHub
- otl-covenants-table -- working copy of data in Google Sheet https://docs.google.com/spreadsheets/d/1yLGLmTzrkiaVJENkbWISFTSfH-Gm569UD-O206kPSFo/edit#gid=322703715, with backup XLSX in this GitHub repo
- table-ct-land-records-online -- working copy in Google Sheet https://docs.google.com/spreadsheets/d/1t6UFa-y7HmiulmLxydlfXevpquFRF5JZD7OsBxdq0R4/edit#gid=0 and backup CSV in this GitHub repo

## Credits
- Property deed research in Connecticut towns:
  - Katie Campbell: West Hartford, Summer 2010
  - David K. Ware: Manchester (see “The Black and White of Greenway: Racially Restrictive Covenants in Manchester, Connecticut,” 2020, https://ssrn.com/abstract=3546228), Newington 2023, East Haddam 2024, East Hampton 2024, East Hartford 2025, Columbia 2025
  - June Gold: Hamden, 2023-24; Woodbridge 2024; Cheshire 2024
- Leaflet map by Ilya Ilyakou and Jack Dougherty, which replaces the 2012 UConn MAGIC Google Map http://magic.lib.uconn.edu/otl/doclink_covenant.html
- If you know of other restrictive covenants by race or religion, anywhere in Connecticut, contact the author [jack.dougherty@trincoll.edu](mailto:jack.dougherty@trincoll.edu)

## Documents in PDF folder but not included on map

### Unresolved location for 1923 anti-Jewish covenant by Jacob Bauer in East Hampton CT
- [online link to Bauer documents in PDF folder](https://github.com/OnTheLine/otl-covenants/blob/main/pdf/easthampton_bauer_jacob.pdf)
- 15 Sept 1923 deed from Jacob Bauer to Leo J. Hedrick, v46 p511, Town of East Hampton CT includes an anti-Jewish restriction: “The said premises shall not be conveyed or leased to any person of the jewish race or extraction.” The “land with a bungalow” is described with these boundaries:
  - Northerly by land of grantor (Bauer) 250 feet
  - Easterly by highway and Lake Pocotopaug, 50 feet
  - Southerly by land of the grantor (Bauer) 250 feet
  - Westerly by land of the grantor (Bauer) 50 feet
- Unresolved problem: This 1923 Jacob Bauer property cannot be definitively linked to a specific land parcel on the 1927 Bauer Terrace map (or a more recent map). The best possible match *might* be lot #25 on the 1927 map, known today as parcels 12B and 13B on the current East Hampton GIS tax map, a vacant lot with the address 83 North Main St. But land records for the 1923 Bauer property are unclear after November 1925, so cannot definitively link Bauer ownership to 1927 lot #25.
- Our research team decided that we cannot reliably place it on our online map, but we archived it in this public repository so that anyone may read it, refer to it, and write about its existence.

### 1936 "American citizens" covenant for 2 Perkins Road, Woodbridge CT
- [online link to 2 Perkins Road documents in PDF folder](https://github.com/OnTheLine/otl-covenants/blob/main/pdf/woodbridge_2_perkins_rd.pdf)
- 29 July 1936 deed from Margaret L. Rusden Westcott to John E. Vance restricts sale or rental "to persons not American citizens" for individual property known today as 2 Perkins Road, Woodbridge CT
- Town property card mistakenly lists equivalent property as 4 Perkins Road, which does not exist in Town GIS map, and maps clearly show the current address is 2 Perkins Road.
- Our research team decided that this "American citizen" restriction currently is not covered by CT Public Act 21-173 and does not match our focus on racial restrictions. But archived it in this public repository so that anyone may read it, refer to it, and write about its existence.

### Additional leads to follow up on
see working Google Sheet https://docs.google.com/spreadsheets/d/1RtxNexc0S8gZyZVimdwM0FO-kq8xPw3HMaP2Ku5a8KI/edit#gid=0

## East Hartford TEMP notes
- Bellew Terrace, 1929 deed with subdivision map (Terry Rd, Wind Rd, Burnside Ave), ready for Jack to draw boundaries
- Knollwood Road (currently no subdivision name), 1941 deed from Richard J. Devitt to Arthur and Ruth Dinsmore for 64 Knollwood Road. TODO: Jack will search newspapers for any reference to Knollwood or Devitt to find clues for a subdivision map in property records, to extend our finding beyond the one listed home, and draw boundaries
- Shannon Heights, 1938 deed with subdivision map (Forbes St, north side lots 1-3, Olaf Benson, 4-6, then south side lots 7-16), ready for Jack to draw boundaries
- Stanley and Prospect St area (currently no subdivision named), 1926 deed with 1926 and 1927 maps of "Property of Estate of Charles S. Barnes," bought by MJ Desmond Construction Company, Martin J. Desmond, around 73 Stanley St. TODO: Jack to search newspapers for any subdivision name, but ready to draw boundaries
- Sunset Ridge (need to confirm if this is the subdivisio name), 1930 deed from Sunset Ridge Country Club to Jennie Higbie, for one parcel of land along Kennedy St, but unclear if this is part of a larger subdivision. Map from property records represents best guess so far. TODO: Jack to research newspapers for any clues about Sunset Ridge subdivision, in order to confirm map (or find more maps in EH property records online) to draw boundaries
- Westview Drive (currently no subdivision name), 1942 deed with subdivision map labeled "Property of Richard J. Devitt" Ridgewood Rd, Westview Drive, Silver Lane), ready for Jack to draw boundaries

## How to update:
- Overview: draw in GeoJson.io, data entry in Google Sheet, join in MapShaper, republish in Datawrapper, save to GitHub
- Scan historical documents, add metadata, and upload to `pdf` GitHub folder using id format
- to draw new polygons, upload to geojson.io, draw and name id, then export
- to enter new data, go to data in Google Sheet; avoid empty rows at bottom for cleaner pivot table
- download data as CSV
- upload existing map.geojson to mapshaper.org
- console: -filter-fields id   (to remove all fields except geospatial id)
- upload CSV and rename to 'data'
- console: -join data keys=id,id
- export with option: extension='.geojson', upload to GitHub
- save XLSX backup to https://github.com/ontheline/otl-covenants
- Republish two linked Datawrapper tables in OTL Team folder
- Racist Covenants Located To Date by Connecticut Town https://app.datawrapper.de/archive/team/Fj3ATkF7/63725#/dCnch
- Search by Street Name for CT Racist Covenants https://app.datawrapper.de/archive/team/Fj3ATkF7/63725#/j4lCy
- Live map and two tables appears on live sites: https://myCTdeed.com and (only map and main table in book) https://ontheline.trincoll.edu/restricting.html
