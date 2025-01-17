---
sidebar_label: filter()
title: filter Method of Data Collection
description: You can learn about the filter method of data collection in the documentation of the DHTMLX JavaScript Diagram library. Browse developer guides and API reference, try out code examples and live demos, and download a free 30-day evaluation version of DHTMLX Diagram.
---

# filter()

### Description

@short: Filters items in the diagram

### Usage

~~~js
filter(
	rule?: function, 
	config?: object
): void;

// or

filter(
	rule?: object,
	config?: object
): void;
~~~

### Parameters

- `rule` - (optional) the filtering criteria. The parameter can be:
  - a function
  - or an object which can have following attributes:
    - `by: string | number` - (optional) the key of the item attribute
    - `match: string | number | boolean` - (optional) a pattern to match
    - `compare: function` - (optional) a function for extended filtering. The function returns either *true* or *false* and takes three parameters:
      - `value: any` - the value to compare
      - `match: any` - a pattern to match
      - `item: any` - a data item the values of which should be compared (e.g. a shape)
  - `config` - (optional) an object which defines the parameters of filtering. The object may contain two properties:
    - `add: boolean` - (optional) defines whether each next filtering will be applied to the already filtered data (<i>true</i>), or to the initial data (<i>false</i>, default)
    - `smartFilter: boolean` - (optional) defines whether a filtering rule will be applied after adding and editing items of the collection

### Example

~~~js {7-9,12}
const diagram = new dhx.Diagram("diagram_container", {
    type: "default"
});
diagram.data.parse(data);

// filtering by the rule specified in the function
diagram.data.filter(function (shape) {
    return shape.id > 3;
});

// filtering by the key of the shape attribute
diagram.data.filter({ by: "text", match: "Read N" });
~~~

To revert the diagram to the initial state, call the **filter()** method without parameters.

~~~js
diagram.data.filter();
~~~

**Related articles**:  [Filtering items](../../../guides/manipulating_items/#filtering-items)

**Related sample**: [Diagram. Data. Filtering shapes](https://snippet.dhtmlx.com/tm43bsgn)