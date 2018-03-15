---
title: Style
order: 402
section: Utils
---

```javascript
var Style = require('sketch/dom').Style
```

```javascript
var shape = new Shape({
  style: {
    borders: [{ color: '#c0ffee' }],
  },
})

shape.style.fills = [
  {
    color: '#c0ffee',
    fillType: Style.FillType.color,
  },
]
```

A utility class to represent the style of a Layer.

| Properties                                                    |                               |
| ------------------------------------------------------------- | ----------------------------- |
| fills<span class="arg-type">[Fill](#fill)[]</span>            | The fills of a Layer.         |
| borders<span class="arg-type">[Border](#border)[]</span>      | The borders of a Layer.       |
| shadows<span class="arg-type">[Shadow](#shadow)[]</span>      | The shadows of a Layer.       |
| innerShadows<span class="arg-type">[Shadow](#shadow)[]</span> | The inner shadows of a Layer. |

## Fill

```javascript
shape.style.fills = [
  {
    color: '#c0ffee',
    fillType: Style.FillType.color,
  },
]
```

An object that represent a Fill.

| Properties                                                  |                                                  |
| ----------------------------------------------------------- | ------------------------------------------------ |
| fillType<span class="arg-type">[FillType](#filltype)</span> | The type of the fill.                            |
| color<span class="arg-type">string</span>                   | A rgba hex-string (`#000000ff` is opaque black). |
| gradient<span class="arg-type">[Gradient](#gradient)</span> | The gradient of the fill.                        |
| enabled<span class="arg-type">boolean</span>                | Wether the fill is active or not.                |

## `Style.FillType`

```javascript
Style.FillType.color
```

Enumeration of the types of fill.

| Value      |
| ---------- |
| `color`    |
| `gradient` |
| `pattern`  |
| `noise`    |

## Border

```javascript
shape.style.borders = [
  {
    color: '#c0ffee',
    fillType: Style.FillType.color,
    position: Style.BorderPosition.Inside,
  },
]
```

An object that represent a Border.

| Properties                                                              |                                                  |
| ----------------------------------------------------------------------- | ------------------------------------------------ |
| fillType<span class="arg-type">[FillType](#filltype)</span>             | The type of the fill of the border.              |
| color<span class="arg-type">string</span>                               | A rgba hex-string (`#000000ff` is opaque black). |
| gradient<span class="arg-type">[Gradient](#gradient)</span>             | The gradient of the fill.                        |
| enabled<span class="arg-type">boolean</span>                            | Wether the border is active or not.              |
| position<span class="arg-type">[BorderPosition](#borderposition)</span> | The position of the border.                      |
| thickness<span class="arg-type">number</span>                           | The thickness of the border.                     |

## `Style.BorderPosition`

```javascript
Style.BorderPosition.Center
```

Enumeration of the positions of a border.

| Value     |
| --------- |
| `Center`  |
| `Inside`  |
| `Outside` |

## Shadow

```javascript
shape.style.shadows = [
  {
    color: '#c0ffee',
    fillType: Style.FillType.color,
  },
]
```

```javascript
shape.style.innerShadows = [
  {
    color: '#c0ffee',
    fillType: Style.FillType.color,
  },
]
```

An object that represent a Fill.

| Properties                                   |                                                  |
| -------------------------------------------- | ------------------------------------------------ |
| color<span class="arg-type">string</span>    | A rgba hex-string (`#000000ff` is opaque black). |
| blur<span class="arg-type">number</span>     | The blur radius of the shadow.                   |
| x<span class="arg-type">number</span>        | The horizontal offset of the shadow.             |
| y<span class="arg-type">number</span>        | The vertical offset of the shadow.               |
| spread<span class="arg-type">number</span>   | The spread of the shadow.                        |
| enabled<span class="arg-type">boolean</span> | Wether the fill is active or not.                |