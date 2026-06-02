# IasiStudy

*This md file shall compile existing work for the group own knowledge to study densification in the City of Iasi, Romania.*

   
## Study area
The municipality of Iasi, located in northeastern Romania, spans an area of 94 km² and had an estimated population of approximately 610,000 in 2023. As the second-largest
city in Romania, it presents a highly heterogeneous urban environment, combining a dense historic core, extensive residential neighborhoods from the communist period, transforming industrial
areas, and rapidly growing peri-urban zones. Population distribution varies significantly across the city, reflecting both long-standing urban structures and recent migratory movements
from surrounding rural areas. These demographic patterns, together with ongoing urban expansion, create a complex spatial structure that is particularly suitable for studying urban densification processes.
## Chalendges and dificulties

The 2011 orthophoto has 50 cm resolution instead of the 20 cm the FLAIR-HUB model was trained on, plus compression artifacts. This caused significantly noisier segmentation outputs, making the 2011 building footprint results unreliable enough that quantitative evaluation was skipped entirely for that year. The 2011 imagery also used standard (non-true) orthophotography, meaning building facades leak into the rooftop mask, overestimating footprint area by 8–15%.

FLAIR-HUB was trained on French imagery, so applying it to Romania introduces geographic domain shift. The 2024 true orthophoto also differs geometrically from the standard orthophotos used in training, affecting accuracy along building edges.

Even for 2024, the pipeline produces false positives from tree canopies, empty swimming pools, and synthetic sports pitches all sharing spectral signatures with rooftops. False negatives affect small or occluded buildings. Post-processing introduces its own issues: adjacent buildings get merged, and tile boundary seams cause duplication or clipping artefacts.

## Dataset and Maps 

*   
*  Building footprints for 2024, available as open data : DOI : TOBE ADDED 
*
*  Building footprints for 2011, available as open data : DOI : TOBE ADDED 
*
*  Building changes (construction, demolition,  ...) between 2011 and 2024, available as open data : DOI : TOBE ADDED 
*    
*  Maps>
*  
    

