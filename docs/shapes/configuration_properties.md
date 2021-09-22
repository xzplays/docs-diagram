---
sidebar_label: Shape API properties
title: Shape API Properties 
description: text
---

# Shape API properties

## Common properties

- **id** - (*string/number*) the unique id of a shape;
- **type** - (*string*) the type of the shape (by default: "card" in the org chart mode, "topic" in the mindmap mode);
- **x** - (*number*) the x coordinate of the shape position;
- **y** - (*number*) the y coordinate of the shape position;
- **text** - (*string | string[]*) the text to be rendered in a shape. The property can be set as an array of string values while [configuring a **custom shape** only](common_guides/configuration.md#creatingcustomshapes); ```todo поменять ссылку```
- **editable** - (*boolean*) enables/disables the ability to edit the text of the shape by double-clicking on it; *true* by default. <br>*The property is not available for a custom shape.*
- **height** - (*number*) the height of a shape;
- **width** - (*number*) the width of a shape;
- **fixed** - (*boolean*) enables/disables movement and resizing of a shape, *false* by default;
- **hidden** - (*boolean*) defines, whether a shape will be hidden;
- **css** - (*string*) the name of the CSS class that should be applied to the shape;
- **[key: string]** - (*any*) - your own property. For details, check the [Custom shape](../custom_shape/) article. <br>*Overriding the internal properties of the diagram shape object is forbidden as it causes the incorrect work of the diagram and its editor.*
## Properties specific for "topic", flow chart, and custom shapes

- **fill** - (*string*) the color of the shape, "#DEDEDE" by default;
- **stroke** - (*string*) the color of the shape outline, "#DEDEDE" by default;
- **strokeWidth** - (*number*) the width of the shape outline, 1 by default;
- **strokeType** - (*string*) the type of the stroke outline, "line" (default), "dash" for a dashed line;
- **strokeDash** - (*string*) the pattern of dashes and spaces for a dashed outline;
- **fontColor** - (*string*) the color of the text font, "#4C4C4C" by default;
- **fontStyle** - (*string*) the style of the text font, can be "normal" (default), "italic" or "oblique";
- **fontWeight** - (*string*) the text font weight, possible values are: "normal" (default), "bold", "bolder", "lighter", values "100"-"900", where "400" is the same as normal, and "600"+ is the boldest font;
- **fontSize** - (*number*) - the size of the font in pixels, 14 by default;
- **textAlign** - (*string*) - the alignment of text in a shape:"left","center"(default),"right";
- **textVerticalAlign** - (*string*) - the vertical alignment of text in a shape:"top","center"(default),"bottom";
- **lineHeight** - (*number*) the height of a line, 14 by default;

## Properties specific for "img-card" and custom shapes

- **img** - (*string*) the image of a shape;
- **title** - (*string*) the title of a shape;
- **headerColor** - (*string*) the color of the header of the shape, any CSS legal color value;

## Properties specific for the default mode

- **angle** - (*number*) the angle of shape rotation;

## Properties specific for the org chart mode

- **parent** - (*string|number*) the id of the parent shape;
- **dx** - (*number*) the left offset of the shape;
- **dy** - (*number*) the top offset of the shape;
- **dir** - (*string*) the direction of shapes connecting. To connect shapes vertically, set the attribute to the "vertical" value<br> {{editor	https://snippet.dhtmlx.com/98tzmzpg	Diagram. With nested vertical lists}};
- **open** - (*boolean*) defines, whether the child items of the current shape will be shown. *True* by default;

## Properties specific for the mindmap mode

- **parent** - (*string|number*) the id of the parent shape;
- **dx** - (*number*) the left offset of the shape;
- **dy** - (*number*) the top offset of the shape;
- **open** - (*boolean*) defines, whether the child items of the current shape will be shown. *True* by default;
- **openDir** - (*object*) shows/hides the child items of the root shape. The object takes two attributes:
    - **left** - (*boolean*) -  shows/hides the child items to the left of the root shape;
    - **right** - (*boolean*) - shows/hides the child items to the right of the root shape.

