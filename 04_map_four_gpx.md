**QGIS Walkthrough 4: A line map of the Cardiff half-marathon**

**Task**

- Build a line and points map of the Cardiff half-marathon and produce a pdf map

- Download the [GPX file](https://raw.githubusercontent.com/aodhanlutetiae/QGIS/main/cardiff_half_marathon.gpx) that's in this repository

- Import using Data Source manager (look for file under Vector) or Layer / Add Layer / Add Vector Layer

<!-- - Collect the route files into a group (right-click / 'Group Selected') -->

- Add a base layer (WEB) and adjust the opacity on it to 20% (RC: Properties / Transparency)

- Adjust the colour and size of the points (Trackpoints) and line (Tracks) via right-click and 'Properties'

- Reorder the layers to have the finish point layer on top (Waypoints). Adjust the icon.

<!-- - Select the T text tool (View / Toolbars / Annotations toolbar) and add a textbox beside the finish ('Create text annotation at point'). Double click on the textbox to edit it -->

- Open PROJECT / New Print Layout and add a title when prompted. Under Add Item, select Add Map. Your map is now selected: drag a rectangle over the empty print page to select the space it will occupy.

- Add Item / Add Scale Bar (click and drag on map to place)
- Add Item / Add Label (then edit under 'Item Properties' on the bottom right)

- Under Layout, export as SVG, image or pdf
