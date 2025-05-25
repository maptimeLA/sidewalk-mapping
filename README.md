# sidewalk-mapping
Documenting the progress of mapping crossings, sidewalks, and the links between crossings and sidewalks. 

Will be mapping these pedestrian features in the Pico-Union area, an area bewtween Alvarado St and Union Ave.

### Why are we doing this?
- To learn how to use the OMS iD Editor
- To contribute to Phase I of the OpenSidewalks project by mapping the pedestrian transportation layer. The OpenSidewalks project consists of three mapping phases with each phase adding another layer to the pedestrian network. 

### Features to be mapped and there associated tags
Descriptions for pedesterian features and mapping geometry taken from the [OpenSidewalks (OS) Mapping Guide](https://sidewalks.washington.edu/2024/06/04/mapping-guide/).

|  Pedestrian Feature | Description | Phase I Tags | Additional Tags |
| :----: | ---- | --------| ------- |
| Crossing Line | "a line that extends from curb to curb, intersecting with the street at a shared connected crossing node" (OS Mapping Guide, 57)| `highway=footway` `footway=crossing` `crossing:markings=yes/no` | |
| Crossing Node | "a point where the crossing line intersects with the street it traverses" (OS Mapping Guide, 57) | `highway=crossing` | |
| Curb Node | "points at either end of the crossing lines where the crossings meet the edge of the road" (OS Mapping Guide, 58) | `barrier=kerb` (make note about how Phase I doesn't require the tag `kerb=raised/lowered/flush/rounded` but for the purposes of this project I will be using this tag for curbs during Phase I) | If `kerb=lowered` you can consider adding info about tactile paving by using the tag `tactile_paving=yes/no`. |
| Sidewalk Line | "a center line on a pedestrian pathway that runs along the edge of the road" (OS Mapping Guide, 58) | `highway=footway` `footway=sidewalk` | additonal tags can include info on the surface type, the width and the inclination |
| Link Line | "a short links that serve as footway that links a crossing curb node to a sidewalk line" (OS Mapping Guide, 59) | `highway=footway` (make note about how link can also include the footway=sidewalk tag) | |


