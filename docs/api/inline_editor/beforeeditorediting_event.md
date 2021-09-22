---
sidebar_label: beforeEditorEditing
title: beforeEditorEditing
description: text
---

# beforeEditorEditing

@short: fires before the text value of an item is edited via the inline editor 
    
@params:
- value         string              the new value of the item
- currentValue  string              the old value of the item
- id    	    string|number		the id of the item
- key 		    string				the name of the property to be edited
- subheaderId	string|undefined	optional, the id of the edited subheader of a swimlane

@returns:
- param     boolean     false - to block saving changes after editing an item via the inline editor, otherwise true

@example:
diagram.events.on("beforeEditorEditing", (value, id, key, subheaderId) => {
    console.log(value, id, key, subheaderId);
    return true;
});
// For diagram editor
editor.diagram.events.on("beforeEditorEditing", (value, id, key, subheaderId) => {
    console.log(value, id, key, subheaderId);
    return true;
});

@template: api_event
@descr:

**Related samples**:
- [Diagram. Events](https://snippet.dhtmlx.com/7h2hgb3g)
- [Diagram. Org chart events](https://snippet.dhtmlx.com/l38pct7c)

@changelog:
Added in v4.0