---
sidebar_label: toolbar
title: toolbar Property
description: You can learn about the toolbar property in the documentation of the DHTMLX JavaScript Diagram library. Browse developer guides and API reference, try out code examples and live demos, and download a free 30-day evaluation version of DHTMLX Diagram.
---

# toolbar

### Description

@short: Optional. An array of icon objects which sets a toolbar with buttons for items

### Usage

~~~js
toolbar?: [
    {
	    id: string,
        content: string,
	    check?: function,
	    css?: function,
        tooltip?: string
    },
    {...} // other icon objects
];
~~~

### Parameters

The **toolbar** array includes a set of icon objects. Each icon object can have the following parameters:

- `id` - (required) the id of the icon
- `content` - (required) the content of the icon. It can contain an HTML element with the name of the icon class
- `check` - (optional) checks whether the icon should be applied to the item. The function takes an item object and returns *true*, if the icon will be rendered for this item
- `css` - (optional) the function which returns the name(s) of CSS class(es) that should be applied to the item
- `tooltip` - (optional) a tooltip which appears on hovering over the icon

### Example

~~~js
const diagram = new dhx.Diagram("diagram_container", { 
	type: "org", 
	select: true,
	margin: {
    	y: 65
    },
    toolbar: [{
        id: "download",
        content: "<i class='dxi dxi-download'></i>",
        tooltip: "Download",
    },
    {
        id: "info",
        content: "<i class='dxi dxi-information-outline'></i>",
        tooltip: "Info",
    }]
});
~~~

**Change log:**

- The **tooltip** parameter is added in v5.0

**Related articles**:

- [Setting toolbar for items](../../../guides/diagram/configuration/#setting-toolbar-for-items)
- [Default icons](https://docs.dhtmlx.com/suite/helpers/icon/)

**Related sample**: [Diagram. Configuration. Per-shape toolbar](https://snippet.dhtmlx.com/4if395hd)
