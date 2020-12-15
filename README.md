This project is a clone of https://www.newsweek.com/ using Bootstrap.

Already in the planning phase I ran into a problem: The original site reorders content on the top of the page at the lowest screen size. The problem here is, that content from different columns (that appear at greater sreen size) is mixed together. This cannot be solved using Bootstrap as it is.

Marking the content up in columns, as the greater screen sizes require, makes the reordering impossible (you can only reorder content inside the same column, that is: siblings. You cannot move content from one column to another).

Not grouping the items together in columns makes it possible to reorder them, but breaks the layout at bigger screen sizes.

This could be solved using a little "hack":
1) Add the stuff that is out of order separately to the html and hide it.
2) At the lowest sreen size, hide everything in the central column except the top story, that goes ... uhm ... to the top and show the hidden stuff at the right spot.
However, this adds a bunch of redundant html and seems not very elegant.

And of course, simply using the standard CSS Grid would take care of this problem. However, this project is about practicing Bootstrap, so building it without Bootstrap shouldn't be the goal here... So I decided not to replicate the reordering of the original site here
