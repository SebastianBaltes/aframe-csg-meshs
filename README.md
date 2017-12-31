# aframe-csg-meshs

An [A-Frame](https://aframe.io) component for runtime Constructive Solid Geometry (boolean mesh operations). It is based on [ThreeCSG](https://github.com/chandlerprall/ThreeCSG) which it contains as a source copy in a slightly modified version.

<a href="https://sebastianbaltes.github.io/aframe-csg-meshs/examples/index.html">Click here to view demo
 
<img src="https://sebastianbaltes.github.io/aframe-csg-meshs/examples/csg-meshs-example.jpg"></a>

## Properties

The component takes three optional properties:

  * union
  * subtract
  * intersect
  
All properties work the same: They are Selector-Arrays to reference the corresponding meshs 
that will be unioned with / subtracted from / intersected with the meshs of this entity.
The full object tree is considered.

## Installation

### Browser


Install and use by directly including the aframe-csg-meshs/index.js:

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/0.7.0/aframe.min.js"></script>
  <script src="https://unpkg.com/aframe-csg-meshs/index.js"></script>
</head>

<body>
  
   <a-scene>
        <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9" shadow csg-meshs="subtract: #sphere"></a-box>
        <a-sphere id="sphere" position="0 1.25 -3" radius="1.25" color="#EF2D5E"  material="transparent: true; opacity: 0.1"></a-sphere>
        <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D" shadow csg-meshs="subtract: #sphere"></a-cylinder>
        <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4" shadow></a-plane>
        <a-sky color="#ECECEC"></a-sky>
    </a-scene>
  
</body>
```

### npm

Install via npm:

```bash
npm install aframe-csg-meshs
```

Then require and use.

```js
require('aframe');
require('aframe-csg-meshs');
```
