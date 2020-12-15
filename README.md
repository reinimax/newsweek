This project is a clone of https://www.newsweek.com/ using Bootstrap.

Already in the planning phase I ran into a problem: The original site reorders content on the top of the page at the lowest screen size. The problem here is, that content from different columns (that appear at greater sreen size) is mixed together. This cannot be solved using Bootstrap as it is.

Marking the content up in columns, as the greater screen sizes require, makes the reordering impossible (you can only reorder content inside the same column, that is: siblings. You cannot move content from one column to another).

Not grouping the items together in columns makes it possible to reorder them, but breaks the layout at bigger screen sizes.

This could be solved using a little "hack":
1) Add the stuff that is out of order separately to the html and hide it.
2) At the lowest sreen size, hide everything in the central column except the top story, that goes ... uhm ... to the top and show the hidden stuff at the right spot.
However, this adds a bunch of redundant html and seems not very elegant.

And of course, simply using the standard CSS Grid would take care of this problem. However, this project is about practicing Bootstrap, so building it without Bootstrap shouldn't be the goal here... So I decided not to replicate the reordering of the original site here

This time, I decided not to copy the images from the original site, but to use https://picsum.photos to add in a bunch of random pictures. If you don't know it, check it out. It's awesome.


So far, I found Bootstrap to be quite tedious. Here's what I don't like about it:

1) It adds an extra layer to the project, that is, an extra layer where things can go wrong and break and have to be debugged.
2) You really add a bunch of classes, which bloats the markup. And you have to adjust the html so that certain Bootstrap-classes work correctly. Of course, also without Bootstrap it is sometimes necessary to change the html (eg. adding a wrapper to something), but generally I try to avoid it as much as possible.
3) Similar to point 2: Since you're styling stuff by adding/changing classes in the html, when you're making a stylistic change, you have to change ALL the html elements to which the change applies. And if you have a lot of content this is a lot of tedious work. Of course, you could simply overwrite or extend an already existing class, but this is likely to be considered a bad practice if the same effect can be reached using the original Bootstrap-classes.
4) Point 3 leads to an interesting dilemma: I could
  a) fill in all the stuff and then style it. This is "easy" but tedious, since after filling all elements, I have to go back to each single item and apply the same classes over and over again.
  b) fully style each element and then copy-pasting it as a basis for the rest of the corresponding content. This works well if the finished site is very similar to vanilla Bootstrap. Otherwise, one would style stuff with Bootstrap and overwrite these styles at the same moment and possibly creating problems further down the road.

What I found positive about Bootstrap is above all the amazing "grid"-System that allows you to set up a responsive layout in no time without any work up-front. Just add in a few col-*-* classes and you're ready to go. As noted above, you cannot do everything with it and I would have probably preferred a system based on a real grid instead of something that calls itself "grid", but is really flexbox under the hood. Anyway, in most cases the Bootstrap "grid" will suffice and it is fast and easy.


