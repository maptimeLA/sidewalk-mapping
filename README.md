# sidewalk-mapping
Documenting the progress of mapping crossings, sidewalks, and the links between crossings and sidewalks. 

Will be mapping these pedestrian features in the Pico-Union area as seen below.
<img width="973" alt="PicoUnionMappingBoundary" src="https://github.com/user-attachments/assets/2d21d26a-670c-4833-acf6-fe1ee056cec2" />

### Why are we doing this?
- To learn how to use the OMS iD Editor
- To contribute to Phase I of the OpenSidewalks project by mapping the pedestrian transportation layer. The OpenSidewalks project consists of three mapping phases with each phase adding another layer to the pedestrian network. Phase 2 focuses on adding attributes that may affect pedestrian accessibility and navigation while Phase 3 entails adding features that can improve or impede pedestrian traversal (OS Mapping Guide, 105).

### Features to be mapped and there associated tags
Descriptions for pedesterian features and mapping geometry taken from the [OpenSidewalks (OS) Mapping Guide](https://sidewalks.washington.edu/2024/06/04/mapping-guide/).

|  Pedestrian Feature | Description | Phase I Tags | Additional Tags |
| :----: | ---- | --------| ------- |
| Crossing Line | "a line that extends from curb to curb, intersecting with the street at a shared connected crossing node" (OS Mapping Guide, 57)| `highway=footway` `footway=crossing` `crossing:marked=yes/no` *OMS now includes the preset tag `crossing=uncontrolled` but the OS mapping guide does not meniton it, we have included the tag in the mappings*| `surface=concrete/asphalt/cobblestones/gravel` `tactile_paving=yes/no` |
| Crossing Node | "a point where the crossing line intersects with the street it traverses" (OS Mapping Guide, 57) | `highway=crossing` `crossing:marked=yes/no` *OMS now includes the preset tag `crossing=uncontrolled` but the OS mapping guide does not meniton it* | |
| Curb Node | "points at either end of the crossing lines where the crossings meet the edge of the road" (OS Mapping Guide, 58) | `barrier=kerb` `kerb=raised/lowered/flush/rounded`| If `kerb=lowered` you can consider adding info about tactile paving by using the tag `tactile_paving=yes/no`. Other optional tags include `height=*` and `surface=*` |
| Sidewalk Line | "a center line on a pedestrian pathway that runs along the edge of the road" (OS Mapping Guide, 58) | `highway=footway` `footway=sidewalk` | Optional tags can include `surface=*`, `width=*`, and tags concerning sidewalk inclination |
| Footway Link Line | "a short footway that links links a crossing curb node to a sidewalk line" (OS Mapping Guide, 59) | `highway=footway` *In some cases already mapped footways may additionaly include the `footway=sidewalk` but that is okay and there is no need to remove it* | `surface=*` |

### Decision-making when mapping pedesterian features 

Crossings: 
- When there aren't sidewalks present, connect the crossings to curbs without adding footway links
- When curb ramps are diagonal instead of directional you can do either of the following:
- (1) Connect a crossing directly the corner curb ram OR (2) Draw a crossing directly across the street and connect to a raised curb and then add a path that connects the corssing to the curb ramp (OS Mapping Guide, 67). The OS mapping guide states that (2) is preferred so for the purposes of this excercise, we have chosen to map both paths pedestrians might take.

- When providing an additional pathway from the crossing to the curb ramp I am tagging the path as a crossing and tagging whether it is marked or unmarked based on the crossing it's connected to. I am doing this because if the additional path were to not exist and we did a crossing directly to the curb ramp, this path would be considered a crossing so therefore by extension the path that connects from a crossing to a curb is also a crossing and should be tagged as such. Question about these pathways, should these extra pathways to curb ramps be angled or should there be more points added to path? 




























