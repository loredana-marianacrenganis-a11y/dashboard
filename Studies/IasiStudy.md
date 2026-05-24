# IasiStudy

*This md file shall compile existing work for the group own knowledge to study densification in the City of Iasi, Romania.*

   
## Study area
The municipality of Iași, located in northeastern Romania, spans an area of 94 km² and has an estimated population of approximately 610,000 in 2023. As the second-largest city in Romania, it presents a highly heterogeneous urban environment, combining a dense historic core, extensive residential neighborhoods from the communist period, transforming industrial areas, and rapidly growing peri-urban zones. Population distribution varies significantly across the city, reflecting both long-standing urban structures and recent migratory movements from surrounding rural areas. These demographic patterns, together with ongoing urban expansion, create a complex spatial structure that is particularly suitable for studying urban densification processes.
<img width="521" height="497" alt="image" src="https://github.com/user-attachments/assets/9ad68f3f-fae7-4f76-8563-ba686b83bdd6" />

## Chalendges and dificulties  
- Absence of Open Reference Data
  
One of the primary obstacles concerns the lack of open, complete, and temporally consistent building footprint data in Romania. OpenStreetMap data for the study area presents significant quality issues, with sparse coverage and low spatial accuracy characterized by random geometric deviations. Consequently, the generation of precise temporal snapshots of building stock becomes practically unfeasible without introducing substantial inconsistencies in both accuracy and completeness.
- Limitations of Historical Orthophoto Data
  
The 2011 orthophoto, acquired at 0.50 m resolution in RGB only, falls considerably short of the 0.20 m minimum resolution required by the FLAIR-HUB model. Furthermore, the dataset is affected by compression artifacts and standard orthophoto geometry, in which building facades are radially displaced onto rooftop footprints, systematically overestimating footprint area by 8 to 15 percent for tall structures. These combined factors severely constrained the temporal transferability of the model to the historical imagery.
- Domain Shift of the Deep Learning Model
  
FLAIR-HUB was originally trained on French aerial imagery, and its direct application to Romanian orthophotos introduces a measurable geographic domain shift. The 2024 imagery introduces an additional layer of domain discrepancy, as it constitutes a true orthophoto geometrically corrected through a high-resolution Digital Surface Model, whereas the training data consisted of standard orthophotos. This difference affects the spatial accuracy of predicted class boundaries, particularly along building edges.
- Systematic Detection Errors
  
Even when applied to the higher-quality 2024 dataset, the model generates false positives in areas containing dense tree canopies, empty swimming pools, and synthetic sports pitches, all of which exhibit spectral signatures closely resembling building rooftops. False negatives predominantly affect small structures and low-contrast surfaces. Additionally, tile boundary artifacts introduce local geometric distortions, resulting in the partial duplication or clipping of buildings located along orthophoto seams.
- Geometric Inconsistencies in Polygon Generation
  
The polygonization stage introduces further inaccuracies independent of the classification step. The morphological closing operation tends to merge adjacent buildings separated by gaps narrower than the kernel radius, while the Douglas-Peucker generalization algorithm oversimplifies complex building geometries. Both effects reduce the geometric fidelity of the extracted footprints relative to the actual built environment.
- Restricted Access to Geospatial Data
  
Despite recent national initiatives promoting the adoption of open geospatial data in Romania, practical implementation remains limited. Access to comprehensive, high-quality spatial datasets continues to be constrained, complicating both the validation of results and the potential upscaling of the methodology to a national level.
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
    

