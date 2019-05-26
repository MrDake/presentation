Hello my name is Daulet.
And I'll talk about the most powerful layout system currently available in CSS.<br>
THE GRIIID

These are parts of my speach
1. What is a GRID?
2. Browser support
3. Basic terms
4. Container properties
5. Properties of items

What is a GRID?

CSS Grid Layout (aka "Grid") is a TWO-DIMENSIONAL GRID-BASED LAYOUT SYSTEM, 

the purpose of which is to completely change the way that web-based user interfaces are designed. 

CSS was always used to layout web pages, 

but it never did a that job good. 

At first we used tables, 

then wrap (floats), 

positioning and inline blocks (inline-block), 

but all of these methods are essentially just hacks and omit many important functionalities 

(for example, vertical alignment). 

Flexbox helped, but it is designed for simpler one-dimensional layouts, not for complex two-dimensional ones 

(in fact, Flexbox and Grid work very well together). 

CSS Grid - this is the first module created specifically to solve layout problems, which we have solved using hacks when creating websites until now.


Browser support

Here we see the table that shows current browsers and the numbers of their stable versions that work with Grid. 

As we can see the full coverage is: 
without prefix - around 89.78% 
global - around 92.36% 

that maens we can use grid almost in any browser today

Basic terms

Here we see the basic elements of the grid which we will discuss in the next slides

Grid container the element to which the display: grid applies. This is the direct parent for all grid elements. In this example, container is a div with class container . 
Grid item the child elements of the container. Here item is a grid item, but not a sub-item. 
Sub-item the child of grid item. And it does not inherit the grid.

Grid lines is the horizontal and vertical grid container delimiters. These lines are on either side of a column or row. They have direct and reverse numbering.

Grid track is the space between two adjacent grid lines, vertical (Column) or horizontal (Row).

A grid cell is the smallest indivisible unit of a grid container that can be referenced when positioning grid elements. Formed at the intersection of the grid row and grid column.

A grid area is the space inside the grid of a container into which one or more grid elements can be placed. This element can consist of one or more grid cells.

Container properties

Let's talk about the container properties

display 
Defines the element as a container and sets a new mesh formatting context for its content. 

grid-template-columns & grid-template-rows 
Defines the columns and rows of the grid using a list of values separated by spaces. Values represent the size of the track, and the spaces between them represent the grid lines. 

When you leave empty space between track values, the grid lines are automatically assigned numeric names

We can see what our previous code would do.

If your definition contains duplicate parts, you can use the repeat() notation:

The fr (fraction) unit allows you to customize the size of the tracks as part of the free space in the container. Here is an example that sets each element one third the width of the container.

grid-template-areas Defines a grid pattern referring to the names of areas that are set using the grid-area property. Repetition of the name of the region leads to the fact that the content covers these cells. 
Dot means empty cell. 

Here we see how this code works. 
Notice 
that you don’t name the lines, just the areas. 
If you use this syntax, it will be automatically named.

grid-column-gap grid-row-gap 
Specifies the size of the width of the lines. 
You can think of this as setting the width of indentations between columns and rows.

Here we can see how this code works.

You can use a shortend variant of gap property like on this slide

justify-items 
Aligns the content along the line axis. This value applies to all grid elements within the container. 

on this slide you can see how it works

align-items 
Aligns the content along the column axis.
This value applies to all grid elements within the container. 

You can see it here.

justify-content Sometimes the total mesh size may be smaller than the size of the container. This can happen if all grid elements have fixed units, for example, px. 
In this case, you can set the alignment of the grid inside the container. 
This property aligns the grid along the row axis. 

Here we can see how this code works.

In this case, you can set the alignment of the grid inside the container. This property aligns the grid along the column axis. 

You can see it here.

Properties of 
the child elements 
(Grid item)

Let's talk about the grid item properties

grid-column-start grid-column-end grid-row-start grid-row-end 
Determine the location in the grid referring to specific lines. grid-column-start / grid-row-start is the line from which the element starts, and grid-column-end / grid-row-end is the line on which the element ends. 

This code works like this.

Another example to better understand how this works. 
You can view this in more detail by opening the presentation later. make sure to pause video to do it

An example of how this can be written shortly

grid-area Gives the name of the element so that it can be referenced using the property created through the grid-template-areas. 
Alternatively, this property can be used as a shorthand for grid-row-start + grid-column-start + grid-row-end + grid-column-end. 

Here is an example

So. In the end we will talk about justify-self and align-self 

justify-self 
Aligns the content of the element along the axis of the string. 
This value applies to content within a single item.

You can see it here.

align-self 
Aligns the contents of the element along the axis of the column.

This code works like this.

That's all i wanted to tell you about grid layout for today. 
Thx for watchig.
take care, CU