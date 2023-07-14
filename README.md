## Overview:
- The map supports scrolling, zooming in, zooming out, and pathfinding between two given street intersections

![URy1qWD0NNGL4IHSOL7rporaapjalGsqvSpTvX0MxDwcpDUW5OFCmDGIddlapspPnoCDuVCd3d3M7C_Yjrv6ouCt-v6gNrDwjGOl493XP_AxQya62dPi4KP4sQCpxGh5FVqnn3VRHHeGcTGEcFCXF1BL=s2048](https://github.com/dl423/Interactive-Map-With-Path-Finding/assets/81783344/7530e05a-124c-476b-aa0e-7c497f117b4f)

## Pathfinding Capability:
- Uses Dijkstra's algorithm to find the from a path from one street intersection on the map to another
- Performance: takes 0.234 seconds to find a path across the widest span of the Toronto map

https://github.com/dl423/Interactive-Map-With-Path-Finding/assets/81783344/a78407a3-0cb4-425f-b449-1306432333e8

## Zooming in:
- Most street names and map sites are hidden are low zoom levels
- Increasing numbers of street names and map sites show up as the user zooms into the map repeatedly

https://github.com/dl423/Interactive-Map-With-Path-Finding/assets/81783344/813fb041-e260-4b3d-8d10-5aef47dae914


## Technical Implementation:
- Programming Language: C++
- IDE: Netbeans installed on Linux
- Used Git for version control of the program code with two other teammates
- Used the StreetsDatabaseAPI to fetch geographic data from OpenStreetMap (OSM)
  - The most important geographic data were those pertaining to the streets. The network of streets are viewed as comprising of intersections and street segments
  - A number of helper functions were implemented to extend the functionality of the API, for instance:
    - Function to find the travel time on a given street segment
    - Function to find all intersections that are adjacent to a given intersection
  - Function to find all intersections that exist in common between two given streets
- Implemented the user interface using EZGL
  - Streets, geographic features and points of interest were drawn onto the EZGL interface
- Dijkstra's algorithm was used for implementing the pathfinding functionality
  - Used a priority queue to store the cost to reach each wavefront node (intersection) and to retrieve the current least-cost node (intersection)
- Made use of Valgrind to check for memory leaks
