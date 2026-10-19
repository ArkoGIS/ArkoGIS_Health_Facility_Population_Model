## ArkoGIS – Health Facility Population Model (QGIS)

## Overview

The ArkoGIS Health Facility Population Model is an automated QGIS Processing Model designed to calculate the population per health facility within each administrative district.

Developed by **ArkoGIS | GIS Mapping & Spatial Analysis**, this model provides a reproducible workflow for assessing and comparing population burden relative to the number of mapped health facilities across administrative areas.

The resulting indicator can support preliminary public health planning, spatial analysis, health resource assessment, and research involving the geographic distribution of health facilities.

## Key Features

- **Automated Calculation:** Calculates the population-per-health-facility ratio for each district.
- **Administrative-Level Analysis:** Uses district boundaries, health facility locations, and population data.
- **Attribute Table Update:** Adds a new field named "PopPERFac" to the district layer to store the calculated values.
- **Reusable Workflow:** Can be applied to other administrative areas when compatible boundary, facility, and population data are available.
- **Further GIS Analysis:** The calculated indicator can be used for thematic mapping and additional spatial analysis in QGIS.

## Methodology

For each district, the model calculates the population per health facility using the following formula:

Population per Health Facility = (District Population Count) / (Number of Health Facilities in the District)

## Where:

- **District Population Count:** The population count provided in the selected population field.
- **Number of Health Facilities:** The number of mapped health facility points located within the district.

The calculated value is stored in a new attribute field named **"PopPERFac"** in the district layer.

Higher values indicate that more people are associated with each mapped health facility, allowing comparisons of relative population burden across districts.

**Interpretation Note:** Population per health facility is a preliminary planning indicator. It does not directly measure geographic accessibility, travel time, service capacity, facility utilization, or actual operational overload.

## Requirements

1. QGIS 3.x
2. A polygon layer representing district boundaries.
3. A point layer representing health facility locations.
4. A numerical population field in the district layer containing the population count for each district.

## How to Use

1. Load the district boundary and health facility layers into QGIS.
2. Open the ArkoGIS Health Facility Population Model in the QGIS Processing Modeler.
3. Select the district polygon layer.
4. Select the health facility point layer.
5. Select the numerical population field containing the population count for each district.
6. **Run** the model.
7. Check the district attribute table for the new **"PopPERFac"** field.

The model adds the calculated field to the district layer rather than automatically generating a separate output layer. The resulting values can then be used for further analysis and thematic mapping.

## Potential Applications

1. Comparing population per health facility across districts.
2. Identifying districts with relatively high population-to-facility ratios.
3. Supporting preliminary public health resource planning.
4. Preparing spatial indicators for public health research.
5. Supporting GIS-based health assessments in humanitarian settings.

## Limitations

The results depend on the accuracy and completeness of the population data, administrative boundaries, and health facility locations.

The indicator does not account for differences in facility size, staffing, service availability, operational capacity, or travel distance. Therefore, a high population-to-facility ratio should be interpreted as a relatively high population burden per mapped facility, not as direct evidence of inadequate geographic access or actual facility overload.

The results should be interpreted in the context of the quality and completeness of the input datasets.

## Citation

If you use this model in academic research or publications, please cite it as follows:

ArkoGIS. ArkoGIS Health Facility Population Model (QGIS). Version 1.0.0, 2026. GitHub: [https://github.com/ArkoGIS/ArkoGIS_Health_Facility_Population_Model/blob/main/].

## Author and Developer

**ArkoGIS | GIS Mapping & Spatial Analysis**

Developed by ArkoGIS for public health GIS, spatial analysis, and research applications.

## License

This project is licensed under the MIT License. See the "LICENSE" file for details.

Academic citation of the model is encouraged as described in the Citation section.
