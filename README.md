# UI5 - library - Signature control

## Version: 1.0.0

## Overview

SAP UI5 custom control for Signature in SVG using d3. Supports both mouse and touch events.
<br/>
This control extends [sap.ui.core.Control](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.Control)

> Tested with Open UI5 version 1.58.3
> which internally uses d3 version 3.4.12

## Constructor

Creates and initializes a new control with the given sId and settings.

```js
new ui5.sign.Signature(sId?, mSettings?)
```

## Control Properties

| Name            | Type                                                                                | Default value      | Description                                                                            |
| --------------- | ----------------------------------------------------------------------------------- | ------------------ | -------------------------------------------------------------------------------------- |
| height          | [sap.ui.core.CSSSize](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSSize)   | 100%               | Defines height of control                                                              |
| width           | [sap.ui.core.CSSSize](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSSize)   | 100%               | Defines width of control                                                               |
| backgroundColor | [sap.ui.core.CSSColor](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSColor) | rgb(221, 221, 221) | Defines background color for the control                                               |
| penColor        | [sap.ui.core.CSSColor](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSColor) | black              | Defines color of pen to draw signature                                                 |
| penSize         | int                                                                                 | 2                  | Size of pen for drawing. <br/> _**Note:**_ Throws error when value is set less than 1. |
| editable        | boolean                                                                             | true               | Defines whether the control can be modified by the user or not.                        |

## Control API

### Summary

| Method                                    | Description                                                                                                                                        |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| [clear](#clear)                           | Clears SVG content of the control                                                                                                                  |
| [getBackgroundColor](#getBackgroundColor) | Gets current value of property `backgroundColor`                                                                                                   |
| [getEditable](#getEditable)               | Gets current value of property `editable`                                                                                                          |
| [getHeight](#getHeight)                   | Gets current value of property `height`                                                                                                            |
| [getPenColor](#getPenColor)               | Gets current value of property `penColor`                                                                                                          |
| [getPenSize](#getPenSize)                 | Gets current value of property `penSize`                                                                                                           |
| [getSVGString](#getSVGString)             | Returns SVG as string                                                                                                                              |
| [getWidth](#getWidth)                     | Gets current value of property `width`                                                                                                             |
| [setBackgroundColor](#setBackgroundColor) | Sets new value for property `backgroundColor`                                                                                                      |
| [setEditable](#setEditable)               | Sets new value for property `editable`                                                                                                             |
| [setHeight](#setHeight)                   | Sets new value for property `height`                                                                                                               |
| [setPenColor](#setPenColor)               | Sets new value for property `penColor`                                                                                                             |
| [setPenSize](#setPenSize)                 | Sets new value for property `penSize`                                                                                                              |
| [setSVGString](#setSVGString)             | Provided SVG string input is rendered onto the screen <br/> Also set's property `editable` to false which makes the control not editable for input |
| [setWidth](#setWidth)                     | Sets new value for property `width`                                                                                                                |

### clear

Clears SVG content of the control.
<br/>
Visibility: <span style="color:green">_public_</span>

```js
clear() : ui5.sign.Signature
```

| Returns                         | Description                                           |
| ------------------------------- | ----------------------------------------------------- |
| [ui5.sign.Signature](#overview) | Reference to `this` in order to allow method chaining |

### getBackgroundColor

Gets current value of property `backgroundColor`
<br/>
Defines background color of control
<br/>
Visibility: <span style="color:green">_public_</span>

```js
getBackgroundColor() : sap.ui.core.CSSColor
```

| Returns                                                                              | Description                         |
| ------------------------------------------------------------------------------------ | ----------------------------------- |
| [sap.ui.core.CSSColor](#https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSColor) | Value of property `backgroundColor` |

### getEditable

Gets current value of property `editable`
<br/>
Defines whether the control can be modified by the user or not
<br/>
Visibility: <span style="color:green">_public_</span>

```js
getEditable() : boolean
```

| Returns | Description                  |
| ------- | ---------------------------- |
| boolean | Value of property `editable` |

### getHeight

Gets current value of property `height`
<br/>
Defines height of control
<br/>
Visibility: <span style="color:green">_public_</span>

```js
getHeight() : sap.ui.core.CSSSize
```

| Returns                                                                           | Description                |
| --------------------------------------------------------------------------------- | -------------------------- |
| [sap.ui.core.CSSSize](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSSize) | Value of property `height` |

### getPenColor

Gets current value of property `penColor`
<br/>
Defines pen color of control used to draw signature
<br/>
Visibility: <span style="color:green">_public_</span>

```js
getPenColor() : sap.ui.core.CSSColor
```

| Returns                                                                              | Description                  |
| ------------------------------------------------------------------------------------ | ---------------------------- |
| [sap.ui.core.CSSColor](#https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSColor) | Value of property `penColor` |

### getPenSize

Gets current value of property `penSize`
<br/>
Defines pen size of control
<br/>
Visibility: <span style="color:green">_public_</span>

```js
getPenSize() : sap.ui.core.CSSSize
```

| Returns                                                                            | Description                 |
| ---------------------------------------------------------------------------------- | --------------------------- |
| [sap.ui.core.CSSSize](#https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSSize) | Value of property `penSize` |

### getSVGString

Gets SVG content of the control as string
<br/>
Visibility: <span style="color:green">_public_</span>

```js
getSVGString() : string
```

| Returns | Description |
| ------- | ----------- |
| string  | SVG value   |

### getWidth

Gets current value of property `width`
<br/>
Defines width of control
<br/>
Visibility: <span style="color:green">_public_</span>

```js
getWidth() : sap.ui.core.CSSSize
```

| Returns                                                                           | Description               |
| --------------------------------------------------------------------------------- | ------------------------- |
| [sap.ui.core.CSSSize](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSSize) | Value of property `width` |

### setBackgroundColor

Sets new value for property `backgroundColor`
<br/>
Visibility: <span style="color:green">_public_</span>

```js
setBackgroundColor(sColor) : ui5.sign.Signature
```

| Param  | Type                                                                                | Description                              |
| ------ | ----------------------------------------------------------------------------------- | ---------------------------------------- |
| sColor | [sap.ui.core.CSSColor](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSColor) | New value for property `backgroundColor` |

| Returns                         | Description                                           |
| ------------------------------- | ----------------------------------------------------- |
| [ui5.sign.Signature](#overview) | Reference to `this` in order to allow method chaining |

### setEditable

Sets new value for property `editable`
<br/>
Visibility: <span style="color:green">_public_</span>

```js
setEditable(bEditable) : ui5.sign.Signature
```

| Param     | Type    | Description                       |
| --------- | ------- | --------------------------------- |
| bEditable | boolean | New value for property `editable` |

| Returns                         | Description                                           |
| ------------------------------- | ----------------------------------------------------- |
| [ui5.sign.Signature](#overview) | Reference to `this` in order to allow method chaining |

### setHeight

Sets new value for property `height`
<br/>
Visibility: <span style="color:green">_public_</span>

```js
setHeight(sHeight) : sap.ui.core.CSSSize
```

| Param   | Type                                                                              | Description                     |
| ------- | --------------------------------------------------------------------------------- | ------------------------------- |
| sHeight | [sap.ui.core.CSSSize](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSSize) | New value for property `height` |

| Returns                         | Description                                           |
| ------------------------------- | ----------------------------------------------------- |
| [ui5.sign.Signature](#overview) | Reference to `this` in order to allow method chaining |

### setPenColor

Sets new value for property `penColor`
<br/>
Visibility: <span style="color:green">_public_</span>

```js
setPenColor(sColor) : ui5.sign.Signature
```

| Param  | Type                                                                                | Description                       |
| ------ | ----------------------------------------------------------------------------------- | --------------------------------- |
| sColor | [sap.ui.core.CSSColor](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSColor) | New value for property `penColor` |

| Returns                         | Description                                           |
| ------------------------------- | ----------------------------------------------------- |
| [ui5.sign.Signature](#overview) | Reference to `this` in order to allow method chaining |

### setPenSize

Sets new value for property `penSize`
<br/>
Throws error if set value is less than 1
<br/>
Visibility: <span style="color:green">_public_</span>

```js
setPenSize(nSize) : int
```

| Param | Type | Description                      |
| ----- | ---- | -------------------------------- |
| nSize | int  | New value for property `penSize` |

| Returns                         | Description                                           |
| ------------------------------- | ----------------------------------------------------- |
| [ui5.sign.Signature](#overview) | Reference to `this` in order to allow method chaining |

### setSVGString

Provided SVG string input is rendered onto the screen <br/> Also set's property `editable` to false which makes the control not editable for input
<br/>
Visibility: <span style="color:green">_public_</span>

```js
setSVGString(sSVGString) : ui5.sign.Signature
```

| Param      | Type   | Description   |
| ---------- | ------ | ------------- |
| sSVGString | string | SVG as string |

| Returns                         | Description                                           |
| ------------------------------- | ----------------------------------------------------- |
| [ui5.sign.Signature](#overview) | Reference to `this` in order to allow method chaining |

### setWidth

Sets new value for property `width`
<br/>
Visibility: <span style="color:green">_public_</span>

```js
setWidth(sWidth) : ui5.sign.Signature
```

| Param  | Type                                                                              | Description                    |
| ------ | --------------------------------------------------------------------------------- | ------------------------------ |
| sWidth | [sap.ui.core.CSSSize](https://sapui5.hana.ondemand.com/#/api/sap.ui.core.CSSSize) | New value for property `width` |

| Returns                         | Description                                           |
| ------------------------------- | ----------------------------------------------------- |
| [ui5.sign.Signature](#overview) | Reference to `this` in order to allow method chaining |
