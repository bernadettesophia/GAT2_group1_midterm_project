# GAT2_group1_midterm_project

## Walkability Assessment of Graz, Austria

This project evaluates the walkability of Graz, Austria using a GIS-based methodology based on the paper:

> Kevic, K., Kuveždic Divjak, A., Zrno, K., & Vilicic, M. (2024).
> Open Data Supporting GIS-based Walkability Assessment: Case Study for City of Zagreb, Croatia.
> ISPRS Archives, XLVIII-5-2024, 23–29.
> https://doi.org/10.5194/isprs-archives-XLVIII-5-2024-23-2024

The workflow uses open data from OSM, population statistics, environmental indicators (green and blue infrastructure) and H3 hexagonal grids to compute walkability scores for different perspectives.

### Project Overview

The goal was to construct a walkability index by combining: 

1. Point-of-Interest Accessibility in different categories:

- Retail
- Food
- Civic
- Entertainment
- Office
- Sport

2. Distance Analysis

- Walking network
- Haversine distance

3. Environmental indicators

- Green and blue spaces
- Population density


The walkability index was calculated for each H3 hexagon by combining accessibility score (daily and leisure perspective) and environmental score.

### Data sources

- District boundaries (Overpass Turbo (n.d.). Overpass API web interface. https://overpass-turbo.eu/ (Accessed December 2, 2025))
- Overpass Code for district boundaries:
  [out:json][timeout:25];
  area["name"="Graz"]->.g;
  relation(area.g)["boundary"="administrative"]["admin_level"="10"];
  out geom;

- Population statistic (Stadt Graz (2025). Zahlen + Fakten: Bevölkerung, Bezirke, Wirtschaft, Geografie.                                                             https://www.graz.at/cms/beitrag/10034466/7772565/Zahlen_Fakten_Bevoelkerung_Bezirke_Wirtschaft.html (Accessed December 2, 2025))

- POIs and walking network (OpenStreetMap via OSMnx)

- Green and blue spaces (Copernicus Land Monitoring Service (n.d.). Urban Atlas Land Cover / Land Use 2018 (vector). https://land.copernicus.eu/en/products/urban-   atlas/urban-atlas-2018 (Accessed December 2, 2025))

**Packages used**
Geopandas, Pandas, NumPy, OSMnx, NetworkX, h3, Matplotlib, Shapely, Fiona, Rasterio, KeplerGl

**Authors**
Paul Badin, Bernadette Kakuska, Elias Pfleger, Clemens Wallisch





