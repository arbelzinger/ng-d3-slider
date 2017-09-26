[TOC]

# NgD3Slider
----------
Unlike the regular and boring html input range slider, this baby is pure **SVG** created using **Angular4** modularity combined with **D3.js v4** capabilities
Check out the <a href="https://embed.plnkr.co/JQo42K/" target="_blank">Demo</a> on Plunker
Check out the <a href="https://github.com/arbelzinger/ng-d3-slider.git" target="_blank">source code</a> on Github

*Easy to modify Easy to style*

Install
-------------
----------
> $ npm install ng-d3-slider --save

Then add the following code at the top of your `app.module.ts file`
```
import {D3SliderDirective} from 'ng-d3-slider/d3-slider.directive'
```
And you're good to go!!!

----------
How to use
-------------
----------

**First try**

For a simple default all you gotta do is add the directive name to a div with an 'id' attr and an Angular input attr called 'length' with a number value
*Example:*
```
 <div ngD3Slider id="slider1"  [length]="200"></div>
```
Now you can *play*  with the slider by adding all the possible attributes suggested below

List of Attributes
----------------------
----------

|Attribute Type| Key             | Type   | Default value|Example     |
|--------------|:----------------|:-------|--------------|--------|
|HTML attr     |`id`             |string  |**- required**||
|Input         |`[length]`       |number  |**- required**|[example](#value)|
|Input         |`[maxValue]`     |number  | `1`          |[example](#value)|
|Input         |`[minValue]`     |number  | `0`          |[example](#value)|
|Input         |`[initialValue]` |number  | `null`       |[example](#value)|
|Input         |`[lineWidth]`    |number  |  `6`         |[example](#style)|
|Input         |`[color]`        |string  | `"#51CB3F"`  |[example](#style)|
|Input         |`[emptyColor]`   |string  | `"#ECECEC"`  |[example](#style)|
|Input         |`[thumbColor]`   |string  |  `"white"`   |[example](#style)|
|Input         |`[thumbSize]`    |number  | `6`          |[example](#style)|
|Input         |`[direction]`    |string  | `"LTR"`      |[example](#direction)|
|Input         |`[vertical]`     |boolean | `false`      |[example](#vertical)|
|Input         |`[disable]`      |string  | `null`       |[example](#disable)|
|Output        |`(selectedValue)`|function|              |[example](#value)|

Examples
----------------------
----------
<a id="value"></a>
**Playing with values**
```
<div ngD3Slider id="slider2" [length]="200" [maxValue]="200" [minValue]="100" [initialValue]="150
(selectedValue)="selectedValue($event)"></div>
```
* `maxValue` should alway be greater than `minValue`
* `initialValue` should alway be greater than `minValue` and smaller than `maxValue`
*  `selectedValue` returns the value selected after the slider's thumb is released

<a id="style"></a>
**Styling the slider**
```
<div ngD3Slider id="slider3" [length]="200" [lineWidth]="7" [color]="'#456789'" [emptyColor]="'orange'"
 [thumbColor]="'pink'" [thumbSize]="8"></div>
```
* `color`, `emptyColor` and `thumbColor` could be given hex,rgb,rgba or html color strings
* `thumbSize` maximum value is 10

<a id="direction"></a>
**Change direction of slider**
```
<div ngD3Slider id="slider4" [length]="200" [direction]="'RTL'" >
</div>
```
* `direction` possible values are `RTL` and `LTR`

<a id="vertical"></a>
**Vertical slider**
```
<div ngD3Slider id="slider5" [length]="200" [vertical]="'true'" >
</div>
```
<a id="disable"></a>
     **Disable slider**
```
<div ngD3Slider id="slider6" [length]="200" [disable]="'disable'" ></div>
```



