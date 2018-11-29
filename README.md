# Geometric.js
A JavaScript library with geometric functions.

[![Build Status](https://travis-ci.org/HarryStevens/geometric.svg?branch=master)](https://travis-ci.org/HarryStevens/geometric)

## Installation

### Web browser
In vanilla, a `geometric` global is exported. You can use the latest version from unpkg.
```html
<script src="https://unpkg.com/geometric@0.0.6/build/geometric.js"></script>
<script src="https://unpkg.com/geometric@0.0.6/build/geometric.min.js"></script>
```
If you'd rather host it yourself, download the latest release from the [`build` directory](https://github.com/HarryStevens/geometric/tree/master/build).

### npm

```bash
npm i geometric -S
```
```js
var geometric = require("geometric");
```

## API

<a name="angleDegrees" href="#angleDegrees">#</a> geometric.<b>angleDegrees</b>(<em>pointA</em>, <em>pointB</em>)

Calculate the angle between two points in [degrees](https://en.wikipedia.org/wiki/Degree_(angle)).

```js
geometric.angleDegrees([0, 0], [1, 0]); // 0
geometric.angleDegrees([0, 0], [-1, 0]); // 180
```

<a name="angleRadians" href="#angleRadians">#</a> geometric.<b>angleRadians</b>(<em>pointA</em>, <em>pointB</em>)

Calculate the angle between two points in [radians](https://en.wikipedia.org/wiki/Radian).

```js
geometric.angleRadians([0, 0], [1, 0]); // 0
geometric.angleRadians([0, 0], [-1, 0]); // π
```

<a name="distance" href="#distance">#</a> geometric.<b>distance</b>(<em>pointA</em>, <em>pointB</em>)

Calculate the distance between two points.

```js
geometric.distance([1, 0], [1, 0]); // 0
geometric.distance([1, 0], [-1, 0]); // 2
```

<a name="midpoint" href="#midpoint">#</a> geometric.<b>midpoint</b>(<em>pointA</em>, <em>pointB</em>)

Calculate the midpoint between two points.

```js
geometric.midpoint([0, 0], [1, 0]); // [0.5, 0]
geometric.midpoint([0, 0], [-1, 0]); // [-0.5, 0]
```

<a name="translateDegrees" href="#translateDegrees">#</a> geometric.<b>translateDegrees</b>(<em>point</em>, <em>angleInDegrees</em>, <em>distance</em>)

Translates a point by an angle in degrees and distance.

```js
geometric.translateDegrees([0, 0], 0, 1) // [1, 0]
geometric.translateDegrees([0, 0], 90, 1).map(d => Math.round(d)) // [0, 1] (Rounding is necessary to produce this clean result because arithmetic in JavaScript is done in [binary floating point](https://en.wikipedia.org/wiki/Double-precision_floating-point_format#JavaScript))
```

<a name="translateRadians" href="#translateRadians">#</a> geometric.<b>translateRadians</b>(<em>point</em>, <em>angleInRadians</em>, <em>distance</em>)

Translates a point by an angle in [radians](https://en.wikipedia.org/wiki/Radian) and distance.

```js
geometric.translateRadians([0, 0], 0, 1) // [1, 0]
geometric.translateRadians([0, 0], Math.PI / 2, 1).map(d => Math.round(d)) // [0, 1] (Rounding is necessary to produce this clean result because arithmetic in JavaScript is done in [binary floating point](https://en.wikipedia.org/wiki/Double-precision_floating-point_format#JavaScript))
```