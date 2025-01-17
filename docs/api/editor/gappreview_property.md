---
sidebar_label: gapPreview
title: gapPreview Property of Editor
description: You can learn about the gapPreview property of editor in the documentation of the DHTMLX JavaScript Diagram library. Browse developer guides and API reference, try out code examples and live demos, and download a free 30-day evaluation version of DHTMLX Diagram.
---

# gapPreview

:::info
The property is available only in the default mode of the editor (*type:"default"*)
:::

### Description

@short: Optional. Specifies the space between the items rendered in the left panel

### Usage

~~~js
gapPreview?: string | number;
~~~

### Default config

~~~js
gapPreview: "6px 8px"
// sets 6px gap for the top and bottom sides and 8px gap for the right and left sides
~~~ 

### Example

~~~js
const editor = new dhx.DiagramEditor("editor_container", {
    gapPreview: 10
});
~~~

The value of the **gapPreview** property can be redefined for a separate shape via the **gap** attribute of the [preview](../../../shapes/configuration_properties/#properties-specific-for-the-default-mode) property of the shape object:

~~~js
const defaults = {card: {
    preview: {
        scale: 0.72, 
        gap: 2
    }
}
 
const editor = new dhx.DiagramEditor("editor_container", {
    shapeSections: {
        "org chart shapes": ["card", "img-card"],
        "flowchart shapes": [true]
    },
    scalePreview: 0.65,
    defaults: defaults         
});
~~~

**Related articles**:  [Left Panel](../../../guides/diagram_editor/left_panel/)