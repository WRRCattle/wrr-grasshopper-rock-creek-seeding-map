# Grasshopper Fire & Rock Creek Irrigation District — Aerial Seeding Concept

**Prepared:** 18 August 2026 HST  
**Status:** Draft planning concept — not an executable flight mission  
**Map:** `index.html`

## Bottom Line

- The current WFIGS burned operational watershed overlaps the authoritative Rock Creek Zone across **6,413.43 acres**.
- Applying the workbook's terrain rules at a 12 m planning grid selects **5,581.97 acres** in Z1–Z3 and Z5–Z7 for aerial-compatible seed mixes.
- The draft requires **70,406.63 lb PLS** (**35.20 short tons PLS**) before conversion to actual bulk pounds from vendor seed tags.
- The base route model covers **100.000%** of each selected planning polygon with 8 m lanes plus modeled one-sided/variable-rate edge passes.
- Base planning time is **91.74 productive application hours**, **265.88 total flight hours**, and **299.46 total operating hours**. Cost estimation is intentionally deferred.

## Planning Areas and Mix Mass

| Zone | Selected acres | Aerial-compatible rate | PLS mass |
|---|---:|---:|---:|
| Z1 Riparian channel/bank — low | 50.92 | 10.54 lb/ac | 536.69 lb |
| Z2 Riparian channel/bank — high | 112.26 | 10.54 lb/ac | 1,183.27 lb |
| Z3 Riparian terrace/floodplain/wet meadow | 78.07 | 9.31 lb/ac | 726.83 lb |
| Z5 Upland scabland/oak-juniper | 394.08 | 10.392 lb/ac | 4,095.32 lb |
| Z6 Upland ponderosa/Douglas-fir | 1,171.75 | 11.27 lb/ac | 13,205.67 lb |
| Z7 Upland grand fir | 3,774.88 | 13.42 lb/ac | 50,658.85 lb |
| **Total** | **5,581.97** | — | **70,406.63 lb** |

PLS is not purchase or payload weight. Final bulk pounds must be calculated for each seed lot as `PLS lb ÷ (purity × germination)`. Until vendor tags exist, the sortie counts are lower-bound planning values.

## Flight-Time Scenarios

| Scenario | Swath | Application speed | Usable payload | Productive time | Total flight time | Total operating time | Provisional sorties |
|---|---:|---:|---:|---:|---:|---:|---:|
| Low-time bound | 10 m | 15 m/s | 100 kg | 48.92 h | 117.61 h | 133.71 h | 322 |
| **Base planning case** | **8 m** | **10 m/s** | **80 kg** | **91.74 h** | **265.88 h** | **299.46 h** | **403** |
| Conservative high-time bound | 6 m | 7 m/s | 60 kg | 174.74 h | 534.60 h | 605.81 h | 534 |

Total flight time includes modeled application tracks, fragmented-polygon turns, and a ferry allowance. Total operating time adds payload/battery turnaround. It does not include weather delays, maintenance, crew breaks, mobilization, regulatory pauses, failed sorties, or inaccessible staging sites.

The base map shows **2,052.09 application-track miles**, including **3,366 edge passes** needed to model 100% polygon coverage, and **7 mathematically efficient draft staging/refill points**. Fragmented riparian polygons produce many short segments and make turns a larger time driver than acreage alone would suggest.

## Aerial-Only Workbook Interpretation

- The workbook's doubled aerial/broadcast PLS rates are retained for compatible species.
- **Basin wildrye (`LECI4`) is removed from Z3:** the workbook explicitly requires row planting and says not to broadcast. Z3 falls from 11.71 to 9.31 lb PLS/ac.
- **Needle-and-thread (`HECO26`) is removed from Z5:** the workbook requires 3/4–1 inch placement and a separately set drill. Z5 falls from 10.992 to 10.392 lb PLS/ac.
- Z4 reservoir-margin plugs and all other plugs, cuttings, acorns, and nursery stock are outside this task.
- Z8 is not mapped because the available terrain package does not provide a current, verified dozer-line/landing/road-cut/firebreak inventory. It should be planned separately when disturbance vectors are available.

The detailed species-by-zone pounds are in `RCDIC_Aerial_Seeding_Zone_Mix_2026-08-18_v1.csv`.

## Terrain Classification

The selection starts with `Burned Watershed ∩ Rock Zone`, then applies these planning proxies:

- Z1: within 30 m of a modeled 10-acre channel, 1,331–2,800 ft, slope 0–8%.
- Z2: within 30 m of a modeled 10-acre channel, 2,800–5,100 ft, slope 0–8%.
- Z3: 30–120 m from a modeled channel, 1,331–5,100 ft, slope 0–5%.
- Z5: non-riparian terrain, 1,331–2,800 ft, slope 2–20%.
- Z6: non-riparian terrain, 2,800–3,500 ft, slope 5–40%.
- Z7: non-riparian terrain, 3,500–5,100 ft, slope 5–50%.

This leaves **748.08 acres** unmatched by the workbook rules and **39.14 acres** above 60% slope. Neither area receives an aerial seed route. The high-resolution 3 m classification identifies 5,626.07 candidate acres; majority aggregation to the 12 m planning grid produces the 5,581.97-acre routed footprint.

## Fire and Exposure Layers

- **Terrain Exposure – Burned Watershed** is the existing LiDAR-derived slope, flow-proximity, and contributing-area consequence model. It is not burn severity.
- **Provisional Satellite Burn Severity** is a separate 20 m Sentinel-2 L2A dNBR layer using 10 July pre-fire and 16 August post-fire imagery with Scene Classification Layer masking.
- Valid dNBR covers **4,607.03 acres** of the Rock/burn overlap: 1,211.80 unburned/regrowth, 140.06 low, 162.60 moderate-low, 204.60 moderate-high, and 2,887.97 high spectral change acres. **1,806.64 acres remain cloud-, smoke-, edge-, or no-data-unclassified.**
- The dNBR layer is provisional spectral change, not field-validated BAER/BARC soil burn severity. It does not alter the seeding footprint in this draft.

## Map Layers

The separate derivative map includes:

- Satellite, Topo, and Street views.
- Water Network, Badger Creek (Ten Acre Channel Network).
- Water Network, Rock Creek Reservoir (Ten Acre Channel Network).
- Slope Gradients: `<3%`, `3–8%`, `8–15%`, `15–30%`, `30–60%`, `>60%`.
- Elevation contours every 100 ft with 1,000 ft index contours.
- Terrain Exposure – Burned Watershed.
- Provisional Sentinel-2 dNBR.
- Aerial planting zones, base application tracks, non-dispensing ferry links, and draft staging/refill points.

## Hard Limitations

This concept deliberately ignores trees, utilities, poles, wires, structures, temporary fire infrastructure, road access, people, livestock, airspace, TFRs, wind, rotor wash, granule drift, battery thermal limits, radio links, GNSS quality, terrain-following clearance, operator certification, pesticide/seed-treatment rules, public-land authorization, and owner/agency permission. A boundary centerline and idealized section control do not guarantee that physical granules remain inside the polygon.

Rebuild the terrain and route package after the requested LiDAR flight, then calibrate the actual spread pattern, seed density, bulk conversion, payload recommendation, battery endurance, turn behavior, and refill cycle with the selected aircraft/operator before estimating cost or exporting a mission.

## Sources

- User-supplied `WRR_RockCreek_SEED_LIST_v1.0.xlsx`, SHA-256 `65cf2b462306527b46b2a1a1a7a430ceb781cc7231ad45e4bd94a5fa6b975e7e`.
- Current approved WFIGS perimeter and local processed source package dated 17 August 2026: [NIFC Open Data — WFIGS Interagency Fire Perimeters](https://data-nifc.opendata.arcgis.com/datasets/wfigs-interagency-fire-perimeters/about).
- Existing DOGAMI-derived 3 ft / 1 m terrain package and 17 August 2026 RCDIC current-fire products.
- Sentinel-2 L2A scenes through [Element 84 Earth Search STAC](https://earth-search.aws.element84.com/v1) and [Copernicus Data Space Ecosystem](https://dataspace.copernicus.eu/).
- [DJI AGRAS T100 official product page](https://ag.dji.com/t100): 100 kg maximum payload, 150 L spreading tank, 10 m effective spreading width, and 20 m/s maximum operation speed. DJI states recommended payload depends on aircraft status and surroundings.
- [USGS National Hydrography Dataset service](https://hydro.nationalmap.gov/arcgis/rest/services/nhd/MapServer).

## Files

- `index.html` — standalone derivative map.
- `RCDIC_Aerial_Seeding_Analysis_2026-08-18_v1.json` — assumptions and machine-readable results.
- `RCDIC_Aerial_Seeding_Flight_Time_2026-08-18_v1.csv` — scenario and zone timing.
- `RCDIC_Aerial_Seeding_Zone_Mix_2026-08-18_v1.csv` — species PLS pounds by zone.
- `assets/map-data.js` — map vectors and calculated summaries.
- `assets/Grasshopper_RockZone_Provisional_dNBR_20m_2026-08-18_v1.tif` — analysis raster.
- `tools/build_seeding_concept.py` — reproducible build script.
