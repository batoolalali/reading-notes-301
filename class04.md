## grid-column-start: 3;
move it to the 3rd vertical border from the left in the grid.
Typing both grid-column-start and grid-column-end every time can get tiring. Fortunately, grid-column is a shorthand property that can accept both values at once, separated by a slash.
columns and rows. grid-row-start works much like grid-column-start except along the vertical axis.
grid-area accepts four values separated by slashes: grid-row-start, grid-column-start, grid-row-end, followed by grid-column-end.
If grid items aren't explicitly placed with grid-area, grid-column, grid-row, etc., they are automatically placed according to their order in the source code. We can override this using the order property, which is one of the advantages of grid over table-based layout.
By default, all grid items have an order of 0, but this can be set to any positive or negative value, similar to z-index.

```CSS
{
grid-template-columns: 20% 20% 20% 20% 20%; and grid-template-rows: 20% 20% 20% 20% 20%;
}
```
- Specifying a bunch of columns with identical widths can get tedious. Luckily there's a repeat function to help with that.**

For example, we previously defined five 20% columns with the rule grid-template-columns: 20% 20% 20% 20% 20%;This can be simplified as grid-template-columns: repeat(5, 20%);

- grid-template-columns doesn't just accept values in percentages, but also length units like pixels and ems. You can even mix different units together.


- Grid gives us control over how wide or narrow each of the ‘grid cells’ get. This allows us to maintain a sensible aspect ratio to their height.

- The repeat() function takes two arguments, the first will define the number of column tracks and the second, what width the tracks should be.

### RegExr is an online tool to learn, build, & test Regular Expressions (RegEx / RegExp).
- Supports JavaScript & PHP/PCRE RegEx.
- Results update in real-time as you type.
- Roll over a match or expression for details.
- Validate patterns with suites of Tests.
- Save & share expressions with others.
- Use Tools to explore your results.
- Full RegEx Reference with help & examples.
- Undo & Redo with ctrl-Z / Y in editors.
- Search for & rate Community Patterns.
