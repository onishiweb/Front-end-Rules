Sass / Scss Structuring
=================

A good way to structure your sass files.

Include the following folders:
Settings (all colour/fonts/spacing etc variables)
Tools (helpers and mixins)
Base (normalize)
Globals (global site styles - layout, header, nav, footer and content section generic styles)
Objects (e.g. media blocks, buttons - common design objects)
Components (Site partials, specific object styles)

# Settings

## Breakpoints
Set the breakpoints, tweakpoints of the site

## Spacing
VERY useful to set a $spacing variable, to control the spacing of your site. This way spacing is ALWAYS consistent and the site looks great with less effort.

So example we set variables like this:
$spacing: 20px;
$spacing-double: $spacing * 2;
$spacing-half: $spacing / 2;
$spacing-quarter: $spacing / 4;

This way our spacing is always relevant to a base size. It really makes the difference.

Keep a second variable for $gutter if you're using grids, allow for greater flexibility, you can always set:
$gutter = $spacing;

## Colours
Setting colour variables throughout the site. It's useful not to write:

$blue: blue;

instead:

$c-text: blue;
$c-header-text: red;

I use c- are a prefix for colour variables

## Fonts

Include your google font imports here.
Set font variables, again not to the font name itself, but something site-relevant.

$font-header: 'Wingdings, sans-serif';
or $f-header: 'SteelTongs, sans-serif';

# Tools

Include Retina functions, grids, and any custom mixins or helpers

## Mixins
These should only be used when the output is dynamic, based on an optional input. Example is my very own responsive margin mixin:

@mixin responsive-margin($spacing, $direction:bottom) {
	margin-#{$direction}: $spacing / 2;
	@include breakpoint(medium) {
		margin-#{$direction}: $spacing;
	}
}

It always halves the height for mobile devices, using the breakpoints mixin, so you won't forget to decrease spacing for mobile sizes. Defaults to margin-bottom.

## Helpers
These are less input based and are there to avoid repitition and reduce classes in your markup - can include clearfix, visually-hidden, hide-mobile.

# Base

## base styles
Set base styles for html, body, h1-h6 sizes, button resets. Anything you want site elements to default to.

## Normalize
Include if that's what you prefer to use

# Globals

layout - include all your widths at certain breakpoints (set in settings). A good idea to set a silent class e.g. %wrapper
header - all styles for .global-header
nav - all styles for .global-nav
footer - you get the idea
content - this is a good place to include silent classes for generic site content stuff. For example, displaying lists in a certain way.

# Objects

Include common design objects e.g. general button styles or media blocks (an image/video accompanied by a picture is quite common)

# Partials

All specific site partials. Normally all the stuff that's in .global-content, everything should be specific to the _partial.scss file.

E.g. if you have a page about Gangsters

_gangsters.scss

and put everything specific under your class .gangsters

REMEMBER: no id's in css wherever possible ;-)

# Themes

One scss file for each colour e.g. _blue.scss with your colours labelled:

$color1-med: red
$color1-light: lightred
$color1-lighter:
$color1-dark:

$color2:

etc

and one _colour-variables.scss to hold all your colour variables e.g. $c-bg-header for background header colour e.g.

$c-bg-header: $color1-lighter;
