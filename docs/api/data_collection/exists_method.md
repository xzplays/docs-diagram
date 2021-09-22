---
sidebar_label: exists()
title: exists
description: text
---

# exists()

@short: checks whether the specified item exists in the diagram

@params:
- id 			string,number			the id of the item in question

@returns:
- result		boolean				true if the item exists, otherwise false


@example:
var shape = diagram.data.exists("1"); 


@template:	api_method
@descr:

@related:
common_guides/manipulating_shapes.md#checkingexistenceofshape