# Total plastic pollution - Data package

This data package contains the data that powers the chart ["Total plastic pollution"](https://ourworldindata.org/grapher/plastic-pollution?v=1&csvType=full&useColumnShortNames=false&emission_type=total_burned_debris&emissions_source=all&measure=total) on the Our World in Data website. It was downloaded on September 4, 2026.

### Active Filters

A filtered subset of the full data was downloaded. The following filters were applied:

## CSV structure

Each row is an observation for an entity (usually a country or region) at a timepoint.

- "Entity" — the name of the entity, e.g. "United States".
- "Code" — our internal entity code. For most countries this is the [ISO alpha-3](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) code, e.g. "USA"; historical and other non-standard entities get a custom code.
- "Year" or "Day" — the timepoint. Annual data has a "Year" column holding an integer year; otherwise a "Day" column holds a date string in the form "YYYY-MM-DD".
- The final column is the data column — the time series that powers the chart. Downloaded with the "full data" option it corresponds to the time series below; with "only selected data visible in the chart" it is transformed depending on the chart type, so the correspondence may be less direct.


## Metadata.json structure

The .metadata.json file contains metadata about the data package. The "charts" key contains information to recreate the chart, like the title, subtitle etc. The "columns" key contains information about each of the columns in the csv, like the unit, timespan covered, citation for the data etc.

## How we process data at Our World in Data

Our World in Data is almost never the original producer of the data - almost all of the data we use has been compiled by others. If you want to re-use data, it is your responsibility to ensure that you adhere to the sources' license and to credit them correctly. Please note that a single time series may have more than one source - e.g. when we stitch together data from different time periods by different producers or when we calculate per capita metrics using population data from a second source.

Preparing this data involves several processing steps. Depending on the data, this can include standardizing country names and world region definitions, converting units, calculating derived indicators such as per capita measures, as well as adding or adapting metadata such as the name or the description given to an indicator.
[Read about our data pipeline](https://docs.owid.io/projects/etl/).

## Detailed information about the data


### Total plastic pollution
Estimated total amount of plastic waste released to the environment each year through debris and open burning from municipal sources such as households, shops, and offices.
Last updated: January 14, 2026  
Next expected update: January 2027  
Date range: 2020–2020  
Unit: tonnes  
Source: Cottom et al. (2024) – with minor processing by Our World in Data  

#### How to cite this data

Cottom et al. (2024) – with minor processing by Our World in Data

#### What you should know about this data
- Plastic pollution is plastic that is no longer contained because it escapes from collection, disposal, or recycling and enters the environment.
- This data covers only macroplastics, which are plastic pieces larger than 5 millimeters.
- Total plastic pollution is the sum of debris (unburned plastic that escapes into the environment as physical items) and plastic burned in open, uncontrolled fires.
- Plastic pollution is attributed to five land-based sources: uncollected waste, littering, losses during collection and transport, uncontrolled disposal sites (open dumps), and rejects from sorting and reprocessing.
- Cottom et al. (2024) developed the [SPOT model](https://www.nature.com/articles/s41586-024-07758-6) model, which first fills gaps in municipal waste data using statistical predictions. It then estimates how plastic flows through the waste system and quantifies the uncertainty in those estimates. The model produces results for around 50,700 municipalities, which are subsequently aggregated to country and regional totals.
- This data covers plastic that comes from land-based municipal solid waste (everyday waste from households and similar sources). It does not include pollution from making plastic, textiles, sea-based sources (like fishing gear), electronic waste, or plastic that is exported as waste and then lost elsewhere.
- Values are model-based estimates and come with uncertainty. They should be interpreted as approximate estimates rather than exact measurements.


## Sources

These are the sources behind the data in this package. Each time series above names the ones it draws on in its citation.

### Cottom et al. – A local-to-global emissions inventory of macroplastic pollution

This dataset provides national, regional, and global estimates of plastic waste generation, collection, and emissions from the SPOT (Spatial Plastic Optimization Tool) material flow analysis model. It includes comprehensive metrics on waste generation, collection coverage, disposal methods, and resulting emissions of macroplastics to the environment.

The data covers waste generation (WG), properly collected waste (PWG), per capita metrics, plastic debris emissions, burn emissions, litter, uncollected waste, collection and disposal emissions, recycling, collection coverage, disposal types (controlled/uncontrolled), management practices, and population without collection services.

Producer: Cottom et al.  
Published: 2024-07-19  
Retrieved on: 2026-01-14  
Retrieved from: https://www.nature.com/articles/s41586-024-07758-6  
License: CC BY 4.0 (https://www.nature.com/articles/s41586-024-07758-6)  

Citation: Cottom, J., Cook, E., Veeken, A. et al. A local-to-global emissions inventory of macroplastic pollution. Nature (2024). https://doi.org/10.1038/s41586-024-07758-6

    