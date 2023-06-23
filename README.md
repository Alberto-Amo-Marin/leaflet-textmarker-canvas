# leaflet-textmarker-canvas
Repo for rendering Text (based on Leaflet Markers with divIcons) in a custom Canvas.
Inspired in: https://gitee.com/panzhiyue/Leaflet-CanvasMarker
And in: https://github.com/eJuke/Leaflet.Canvas-Markers

# How to use it?
First you need to install rbush:
`npm i rbush`

Then in your project do this:

```typescript
import { CanvasMarkerLayer } from 'src/app/text-marker-canvas.js';

//first you need a map in Leaflet that has been created
var map = Map('map').
     setView([41.66, -4.72],
     15);
     
//After that we create the canvasMarkerLayer and add it to the map
let ciLayer = new CanvasMarkerLayer({
              collisionFlg: true,
            }).addTo(this.map);

//Then we create the marker
var marker = new Marker(([country[0], country[1]], {
    icon: L.divIcon({
      iconSize: "auto",
      html: "<b>" + country[2] + "</b>"
    })
  }));

//And we add the marker to the layer
ciLayer.addLayer(marker);
```
