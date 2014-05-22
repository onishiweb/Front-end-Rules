Ordering CSS Properties
=======================

A suggested way to structure your css properties. I've found this very useful to do in the following order.

# Silent Classes and general mixins
%silent-class
@include mixin;

If the mixin is something like border radius, rem related or specific to just one property, I would normally add it in place of that property.

# Display
display: none/block/inline etc

# Positioning
float
position
left
right
top
bottom

# Dimensions
width
height
min-width
min-height
max-width
max-height
margin
padding
border
border-radius

(it's got a name - the box model convention - so it must be good - does your css structure have a name? no? oh...)

# Background
background
background-color
background-image
background-repeat
background-position

# fonts
color
font-family
font-size
font-weight
text-align
text-transform
text-decoration
text-shadow

# Misc
cursor
z-index ---->> it's got a Z in it of course it goes at the end ;-)

There's more I know, but let's discuss this for starters.
