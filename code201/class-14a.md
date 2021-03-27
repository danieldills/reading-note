## CSS

- Transforms property comes in two different settings, two-dimensional and three-dimensional transforms. Transform is a new to alter elements with alternative way to size, positon, and change elements.

- Transform Syntax
```
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

- 2D Transforms
    - work on two-dimensional plane, on the x and y axes (horizontal and vertical)
- 2D Rotate provides ability to rotate an element fro 0 to 360 degrees. Positive will rotate clockwise, negative counterclockwise.

- HTML
```
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
```

- CSS
```
.box-1 {
  transform: rotate(20deg);
}
.box-2 {
  transform: rotate(-55deg);
}
```
- 3D Tranforms
    - with three-dimensional transforms you can change elements on teh z axis, giving additional control of depths
- 3D Rotate transform values, rotateX, rotateY, and rotateZ

- HTML
```
<figure class="box-1">Box 1</figure>
<figure class="box-2">Box 2</figure>
<figure class="box-3">Box 3</figure>
```

- CSS
```
.box-1 {
  transform: perspective(200px) rotateX(45deg);
}
.box-2 {
  transform: perspective(200px) rotateY(45deg);
}
.box-3 {
  transform: perspective(200px) rotateZ(45deg);
}
```

### 8 Simple Transitions That Will Wow Users!
1. Fade In
```
.fade
{
        opacity:0.5;
}
.fade:hover
{
        opacity:1;
}
```
1. Change Color
```
.color:hover
{
        background:#53a7ea;
}
```
1. Grow & Shrink
```
.grow:hover
{
        -webkit-transform: scale(1.3);
        -ms-transform: scale(1.3);
        transform: scale(1.3);
}
```
1. Rotate elements
```
.rotate:hover
{
        -webkit-transform: rotateZ(-30deg);
        -ms-transform: rotateZ(-30deg);
        transform: rotateZ(-30deg);
}
```
1. Square to circle
```
.circle:hover
{
        border-radius:50%;
}
```
1. 3D Shadow
```
.threed:hover
{
        box-shadow:
                1px 1px #53a7ea,
                2px 2px #53a7ea,
                3px 3px #53a7ea;
        -webkit-transform: translateX(-3px);
        transform: translateX(-3px);
}
```
1. Swing
```
.swing:hover
{
        -webkit-animation: swing 1s ease;
        animation: swing 1s ease;
        -webkit-animation-iteration-count: 1;
        animation-iteration-count: 1;
}
```
1. Inset Border
```
.border:hover
{
        box-shadow: inset 0 0 0 25px #53a7ea;
}
```

[<== Back](README.md)