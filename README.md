# ESRI-GPSA-S4-Cougar-Habitat-Best-Location
This exercise presents an opportunity to apply the spatial analysis approach to identify areas that are suitable for cougar habitats. Although the data is real, the scenario, analysis, and resulting decisions are hypothetical. The purpose of this exercise is to show how you can use GIS to perform suitability analysis.

## Section 4 ##
**Exercise 1: Finding the Best Locations and Paths: Cougar Habitat**
- The scenario involves a study initiated by state park officials in Oregon to assess cougar populations in and around the park.
- A committee, consisting of state park and Department of Fish and Wildlife (DFW) representatives, is formed to manage the study.
- The GIS analyst's task is to conduct a suitability analysis to identify suitable cougar habitat by overlaying map layers representing various criteria, such as terrain, proximity to streams, and distance from major roads.
- Key questions include determining the study area limits, identifying areas with suitable habitat characteristics like steep forested slopes near streams but away from major roads, and quantifying potential locations meeting these criteria within or near the national forest.

1. Exercise Steps
   
   **Data Exploration and Preparation:**
   - The Department of Fish and Wildlife (DFW) proposes defining the study area using watershed boundaries for additional insights into watershed health.
   - This step involves filtering the Sub-watershed layer to delineate the study area for further analysis.
     <img width="935" alt="Screenshot 2024-02-15 094126" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/5d141ad2-3bf2-473f-9763-6bbcaa3c5fab">


   - The committee, in alignment with DFW's staff, opts to incorporate watersheds intersecting the national forest into the study area.
   - Specifically, the study is confined to three sub-watersheds situated in the southeast portion of the major watershed, covering the state park and a section of the national forest.
     <img width="937" alt="Screenshot 2024-02-15 094910" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/8d28e087-633d-46e3-aadc-1a208b347344">
     <img width="935" alt="Screenshot 2024-02-15 094938" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/97919adb-415f-4d2d-9724-5cf3a09315c2">
     <img width="937" alt="Screenshot 2024-02-15 095322" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/894f90e1-6f2b-47cc-b7ff-acc3bef7faec">

   -  Merged three sub-watersheds to create a study area boundary using the Dissolve Boundaries analysis tool.
     <img width="935" alt="Screenshot 2024-02-15 095658" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/e0d12164-56b7-43cc-9d1c-de5bd3648fe6">


  **Data Analysis and Modeling:**
  - Utilizing ArcGIS Online, I will filter data to devise a model identifying suitable cougar habitats based on criteria defined by state park experts.
  - Initially, the setup involves clipping criteria layers provided by DFW and the Department of Forestry, and integrating them into the map for analysis.
  - The committee outlines two habitat models: one reflecting narrower criteria per state park preferences and another broader version per DFW's preferences.

  **The first model focuses on areas meeting state park criteria, involving steep slopes (>18 degrees), forested regions (specified vegetation codes), proximity to streams (within 500 feet), and distance from highways (more than 1,500 feet).**
  -  Created a filter to identify the forested areas—one of your analysis criteria.
    <img width="935" alt="Screenshot 2024-02-15 102217" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/af963d0d-19bd-4bfb-b672-2c68236f33b6">

  - With the Slope, Stream and Highway layers turned on, I added an attribute query expression to find areas where the slope is considered steep (greater than 18 degrees).
    <img width="937" alt="Screenshot 2024-02-15 102953" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/9b34d0c1-4f7e-40dd-97ef-ca919add8489">

  - Continued querying areas located within 500 feet of a stream and specified the areas that need to be located more than 1,500 feet from a highway.
    <img width="936" alt="Screenshot 2024-02-15 103913" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/1818bb12-a6e2-4116-b217-8eca39dea936">

    <img width="935" alt="Screenshot 2024-02-15 104929" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/d1e02fd8-898c-4b92-b713-ab583895af24">

    <img width="936" alt="Screenshot 2024-02-15 112354" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/3ca950f4-fc84-47e3-acb6-a8f1573380cd">


  - Following the creation of Model 1, the focus shifts to developing Model 2, reflecting criteria outlined by the DFW for potential cougar habitat.
  - Similar to Model 1, Model 2 entails filtering data to identify suitable areas, with adjustments made to criteria as specified by the DFW.
    
  **Model 2's criteria include steep slopes (>18 degrees), forested regions (specified vegetation codes), proximity to streams (within 2,500 feet), and distance from highways (more than 500 feet), with an additional vegetation type (Grass-Shrub-Sapling or Regenerating Young Forest) factored in.**
  - Added Expression, and then entered criteria to display features where the VEG_CODE Is 121 (Grass-Shrub-Sapling Or Regenerating Young Forest).
    <img width="935" alt="Screenshot 2024-02-15 105636" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/b02b8b7c-7695-43a8-b54e-dfb98ace740a">

  - In the Find By Attributes And Location pane, I added four expressions to represent the criteria identified by the DFW.
    - to find areas where the slope is considered steep (greater than 18 degrees)
    - areas located within 2,500 feet of a stream.
    - suitable areas need to be within 2,500 feet of a stream.
    - areas need to be more than 500 feet from a highway.
    <img width="937" alt="Screenshot 2024-02-15 110010" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/7826fef9-63aa-40b0-905d-5477c96f2409">

    <img width="935" alt="Screenshot 2024-02-15 110356" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/d933507f-f639-4f23-bb50-588ffeaecf93">




  **Interpretation of Results:**
  - What is a suitable cougar habitat?
  - The outcome of the analysis led to two maps: Model 1 - Cougar Habitat - State Park and Model 2 - Cougar Habitat - DFW. The analysis results in both maps depict areas with steep, forested slopes located near streams but away from highways or major roads that are within the agreed-upon study area of the three combined sub-watersheds. Results displayed in each map vary based on the criteria provided by the state park versus the DFW.

  **Repeat or modify**
  - The spatial analysis approach is iterative, allowing for adjustments as needed throughout the process.
  - The committee identified a study area comprising three sub-watersheds in the southeast, covering the state park and part of the national forest.
  - Filters were applied to visualize these sub-layers, which were then combined to establish the study area.
  - Despite agreeing on the study area, each agency proposed slightly different criteria, leading to nuanced variations in the analysis.

  **Present results**
  - The two maps can be presented to facilitate discussions between State Park officials and the Department of Fish and Wildlife (DFW).

  **Make decisions**
  - Analysis feedback and discussions could lead to decisions made across the state of Oregon to more effectively protect cougars and park visitors.

**Exercise 2: Finding the Best Locations and Paths: Sharing Results**
- Sharing the results within a story created using ArcGIS StoryMaps—a customizable app builder.
- [ArcGIS StoryMaps](https://storymaps.arcgis.com/stories/f061cf64461a4b35b64567e243e88c4a) can create a story that includes both maps, which you will then share with project stakeholders.
- A swipe block is an interactive experience that enables readers to directly compare two maps or images simultaneously by using a draggable handle.
  
  <img width="623" alt="image" src="https://github.com/marianahiroki/ESRI-GPSA-S4-Cougar-Habitat-Best-Location/assets/110165879/c163a2f1-b2d1-47a7-ad6d-e18115d2ff14">

