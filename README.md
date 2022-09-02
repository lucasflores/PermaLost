# PermaLost
The goal of this project is to implement multiple machine learning/statistical methods, both interpolative and predictive, in order to creaet a powerful tool to assist archeologists/anthropologists to locate sites vulnerable to 'soft' artifact degradation due to increased permafrost melt due to global warming. This project will first focus on Greenland.

## Project Package Dependencies  
- pandas 
- geopandas 
- sklearn
- skforcast
- matplotlib

## The Problem

Melt and thaw of ground leads to decay of 'soft' artifacts -> race to save these from decay/rot

## The Project

In this project I will use permafrost data provided by the European Space Agency's (ESA) Climate Change Initiative (CCI) Permafrost project. It is derived from a thermal model driven and constrained by satellite data.

## The Data
Permafrost is an Essential Climate Variable (ECV) within the Global Climate Observing System (GCOS), which is characterized by subsurface temperatures and the depth of the seasonal thaw layer. Complementing ground-based monitoring networks, the Permafrost CCI project is establishing Earth Observation (EO) based products for the permafrost ECV spanning the last two decades. Since ground temperature and thaw depth cannot be directly observed from space-borne sensors, a variety of satellite and reanalysis data are combined in a ground thermal model. The algorithm uses remotely sensed data sets of Land Surface Temperature (MODIS LST/ ESA LST CCI) and landcover (ESA Landcover CCI) to drive the transient permafrost model CryoGrid CCI, which yields thaw depth and ground temperature at various depths, while ground temperature forms the basis for permafrost fraction.

### Temporal compositing
Grid products of CDRP v1 are released in annual files, covering the start to the end of the Julian year. This corresponds to average annual ground temperatures, as well as the maximum depth of seasonal thaw, which corresponds to the active layer thickness.
### Spatial resolution
The spatial resolution of the grid product is 926.63 m. Grid attributes are computed in each cell of that size within the time period indicated above. The spatial resolution is limited by the spatial resolution of
remotely sensed Landsurface Temperature.
### Product projection system
The Coordinate Reference System (CRS) used for CRDPv1 is Polar Stereographic projection (Arctic) based on the World Geodetic System 84 (WGS84) reference ellipsoid. The coordinates are specified in meters. It covers the northern hemisphere, extending down to 35 °N latitude in the North America and down to 25 °N in Asia

### **GTD** Ground temp (by depth) - **GST**, **T1m**, **T2m**, **T5m**, and **T10m**
This corresponds to average annual ground temperatures and is provided for specific depths,
Ground Surface Temperature, 1 meter beneath surface, 2 meters beneath surface, 5 meters beneath surface, and 10 meters beneath surface.

### **PFR** Permafrost extent (fraction)
The boundary of permafrost can be defined as
1. The geographical boundary between the continuous and discontinuous permafrost zones.
2. The margin of a discrete body of permafrost.

A permafrost region is commonly subdivided into permafrost zones based on the proportion of the ground that is perennially cryotic. The basic subdivision in high latitudes is into zones of continuous permafrost and discontinuous permafrost. REFERENCES: Muller, 1943; Brown, 1967, 1978; Washburn, 1979; Pewe, 1983. Continuous permafrost is the major subdivision of a permafrost region in which permafrost occurs everywhere beneath the exposed land surface with the exception of widely scattered sites. Taliks associated with rivers and lakes may occur in the continuous permafrost zone. REFERENCE: Brown, 1970. Discontinuous permafrost corresponds to permafrost occurring in some areas beneath the exposed land
surface throughout a geographic region where other areas are free of permafrost. Discontinuous permafrost occurs between the continuous permafrost zone and the southern latitudinal limit of permafrost in lowlands. Depending on the scale of mapping, several subzones can often be
distinguished, based on the percentage (or fraction) of the land surface underlain by permafrost, as shown in the following table.

### **ALT** Active Layer Thickness
Active Layer Thickness is the thickness of the layer of the ground that is subject to annual thawing and freezing in areas underlain by permafrost. The thickness of the active layer depends on such factors as the ambient air temperature, vegetation, drainage, soil or rock type and total water content, snowcover, and degree and orientation of slope. As a rule, the active layer is thin in the High Arctic (it can be less than 15 cm) and becomes thicker farther south (1 m or more).
The thickness of the active layer can vary from year to year, primarily due to variations in the mean annual air temperature, distribution of soil moisture, and snowcover

