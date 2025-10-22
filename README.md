# Global Effects of Road Development on Land Use Change — MateoGret

## Abstract
Road development increases, by 2050, more than 25 million more paved road lane-km (Dulac, 2013).  
Although roads and mobility generate socio-economic benefits, roads also have numerous negative impacts on the environment, ecology, climate and human health and well-being. In particular, research has showed that “the first cut is the deepest”, meaning that the first roads in environmental intact areas are triggering a huge number of environmental problems (Laurance et al., 2009, Laurance et al., 2017).  
Research has, however, mostly focused on specific interactions, e.g. between road development and deforestation (Kleinschroth and Healey, 2017) or on road development and settlement expansion (Veglio et al., 2025), and has not investigated the effects of roads on land use changes at the global scale.

## Goal
To investigate whether and how land-use changes between 1992 and 2010 are spatially associated with existing roads, using road density and distance to road as continuous spatial variables.  
The study focuses on spatial relationships, not on temporal causality.

## Methods

### Datasets
- GRIP dataset: Global road dataset (Mejiers et al., 2018) — download here:
  [GRIP global roads database | GLOBIO - Global biodiversity model for policy support - homepage](https://www.globio.info/download-grip-dataset)

- Global land use data (Matej et al., 2025; Table 5) — download here:
  [Table 5 – List of repository links for data download](https://www.nature.com/articles/s41597-025-04788-1/tables/5),
  and see the description of the layers:
  [Table 6 – List and description of land-use classes and data layers incorporated in the LUIcube](https://www.nature.com/articles/s41597-025-04788-1/tables/6).
  
### Spatial Analysis Workflow

#### 1. Land-Use Change Detection  
Compute land-use change (ΔLU) between 1992 and 2010 using 300 m resolution maps.  
For each grid cell *i*:
\[
\Delta LU_i = LU_{2010,i} - LU_{1992,i}
\]
Aggregate the data to 1 km cells and calculate:  
- **ΔLU_totalᵢ:** proportion of cell area that changed land-use class  
- **ΔLU_forest→agricultureᵢ**, **ΔLU_agriculture→urbanᵢ**, etc.

#### 2. Derive Continuous Road Variables  
From the GRIP dataset, calculate for each 1 km grid cell:
- **RoadDensityᵢ = total road length (km) / cell area (km²)**  
- **RoadDistᵢ = Euclidean distance from cell centroid to nearest road (km)**  

These continuous variables represent spatial intensity and proximity of road infrastructure.

#### 3. Spatial Overlay  
Combine ΔLUᵢ (from Step 1) with RoadDensityᵢ and RoadDistᵢ (from Step 2).  
Each 1 km cell contains both land-use change intensity and road characteristics.

#### 4. Statistical Analysis  
The spatial relationship between land-use change and road infrastructure will be examined using simple descriptive and correlation analyses.  
We will:
- Calculate the average land-use change (ΔLU) within defined distance and road density classes 
- Explore how the intensity of land-use change varies with increasing distance from roads or with higher road density.

The goal is to identify broad spatial patterns, rather than to model causal effects.

## Expected Results

- **Global map of road–land use relationships:**  
  Visualization of how land-use changes (1992–2010) cluster near roads, highlighting regions with high transformation intensity.

- **Country-level summary statistics:**  
  A table summarizing the proportion and type of land-use transitions within different distance or road-density classes.  
  For example, how many km² of forest were converted to agriculture within 5 km of a major road.


## References

- Dulac (2013). *Estimating road and railway infrastructure capacity and costs to 2050.*  
  [Transport Infrastructure Insights — International Energy Agency (IEA)](https://www.iea.org/reports/transport-infrastructure-insights)

- Laurance et al. (2019). *Impacts of linear clearings.*  
  [Smithsonian Repository Link](https://repository.si.edu/server/api/core/bitstreams/2abb548b-2ea5-4727-a46c-4a6af17e36fc/content)

- Kleinschroth and Healey (2017). *Impacts of logging roads on tropical forests.*  
  [Biotropica – Wiley Online Library](https://onlinelibrary.wiley.com/doi/10.1111/btp.12423)

- Laurance et al. (2014). *A global strategy for road building.* Nature.  
  [Nature Article](https://www.nature.com/articles/nature13717)

- Veglio et al. (2025). *A dialogue on global infrastructure-led urbanization: Concepts and reorientations.*  
  [SAGE Journals](https://journals.sagepub.com/home/epd)

- Meijers et al. (2018). *Global patterns of current and future road infrastructure.*  
  [IOPscience](https://iopscience.iop.org/article/10.1088/1748-9326/aabd42)

- Matej et al. (2025). *A global land-use data cube 1992–2020 based on the Human Appropriation of Net Primary Production.*  
  [Scientific Data (Nature)](https://www.nature.com/sdata/)


 
