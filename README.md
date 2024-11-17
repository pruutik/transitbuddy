# Hello 581

This is a very basic demonstration of how to update some HTML elements based on detecting 2 markers and the distance between them.

# Stuff I added on top of the basic demo

```javascript
function showDistance(markers)
```

This is where the most important parts happen. The basic idea is that we get the corners for
2 markers in view and use `posit.pose(corners)` to estimate their 3d position.

Then we calculate the distance between them with `calculateDistance(point1, point2)`.
We then updated the "distance" element in the html to display the distance and change the colour
based on if the markers are "far" or "close" to each other.

The other important function is `updateProxemicButton(howClose, near, medium, far)` which
uses the distance to update a button "proxemicButton" in the UI depending on how close the
markers are to each other.

All the other code basically comes from the basic example in the [js-aruco2 library](https://damianofalcioni.github.io/js-aruco2/)
that I'm using.

- Create markers: [here](https://damianofalcioni.github.io/js-aruco2/samples/marker-creator/marker-creator.html?dictionary=ARUCO_MIP_36h12)
- js-aruco2 library: [https://damianofalcioni.github.io/js-aruco2/](https://damianofalcioni.github.io/js-aruco2/)
