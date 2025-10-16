# Global Effects of Road Development on Land Use Change — MateoGret

## Abstract
Road development increases, by 2050, more than 25 million more paved road lane-km (Dulac, 2013).  
Although roads and mobility generate socio-economic benefits, roads also have numerous negative impacts on the environment, ecology, climate and human health and well-being. In particular, research has showed that “the first cut is the deepest”, meaning that the first roads in environmental intact areas are triggering a huge number of environmental problems (Laurance et al., 2009, Laurance et al., 2017).  
Research has, however, mostly focused on specific interactions, e.g. between road development and deforestation (Kleinschroth and Healey, 2017) or on road development and settlement expansion (Veglio et al., 2025), and has not investigated the effects of roads on land use changes at the global scale.

## Goal
Investigate the effect of roads on land use changes globally.

## Methods

### Datasets
- GRIP dataset: Global road dataset (Mejiers et al., 2018)  
  Download here: [GRIP global roads database | GLOBIO - Global biodiversity model for policy support - homepage](https://www.globio.info)

- Global land use data: (Matej et al., 2025; Table 5)  
 Download here: [Table 5 – List of repository links for data download](https://dein-richtiger-link-aus-word.de)
and see the description of the layers:[Table 6 – Description of data layers](https://cds.climate.copernicus.eu/table6.pdf)
  
### Spatial analysis

1. Overlay:  
   Calculate the change in land uses between 2010 and 1992 using the difference between the raster pixels in the global land use data  
   *ESACCI-LC-L4-LCCS-Map-300m-P1Y-1992-v2.0.7cds.nc* and *ESACCI-LC-L4-LCCS-Map-300m-P1Y-2010-v2.0.7.tif.*  
   The raster cells will be 300×300 m.

2. Buffer Analysis:
   Aggregate the raster cells to 1 km.

3. Spatial Correlation:
   Overlay the land use change maps calculated in (2) with the global road dataset GRIP.

4. Raster Calculations:
   Analyze the relationship between road networks and different types of land use change (e.g., forest to agriculture, agriculture to urban), and evaluate how the extent of these changes varies across countries.

## Expected Results

- Global map illustrating the influence of roads on land use changes:  
  A worldwide map will be produced showing how roads have affected different types of land use changes between 1992 and 2010.  
  Each type of land use transition (e.g., forest → agriculture, agriculture → urban area) will be represented in a different color, allowing a visual interpretation of spatial patterns and regional hotspots of road-induced changes.

- Country-level summary table of land use changes influenced by roads: 
  A statistical table will summarize the extent and types of land use changes associated with road networks for each country.  
  The table will show, for example, how many square kilometers of forest were converted to agriculture or urban areas near roads, providing a comparative overview of the magnitude and nature of road-related land use change across countries.

---

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


 
