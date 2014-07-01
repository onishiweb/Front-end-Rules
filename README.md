Front End Rules
===============

> [The Rules](http://www.velominati.com/the-rules/)

We have a growing Front End team here at Architect working on different projects all over the place all the time, in collaboration and in solitude. Yet we should all be able to pick up and work on any project at any time, regardless of the initial developer and be able to find our way around, understand what we're looking at and pick up where someone left off as easily if it were our own project to begin with.

The rules are here as our guide to all things Front End at Architect, they are created by us and for us*. By following these rules we ensure our code is well-written, well thought out, and easy to maintain.

## Rule 1: Obey the rules.
Where possible all of these rules should be followed to the letter. But, all rules are open to discussion and review. Obviously there are also times where a rule must be broken, but you should be able to explain why it was necessary and what benefit it gave you.

## Rule 2: Lead by example.
Your code should follow the rules and you should help others follow the rules when you can. Code reviews and pair programming are encouraged. Do your best to make yourself available for code reviews when possible and ask for code reviews when there's time on your project.

## Rule 3: It's all about the ~~bike~~ code.
None of these rules are personal, there is no agenda in the rules; it's all about the code. The rules are here to help us write good code and work together as a team. It's about learning as well, front end development is continually evolving with new techniques and new tools becoming available all the time, the rules will keep evolving with these best practices and be updated over time.

## Rule 4: Contribute.
The rules are not here to be written by one and followed by all, they are written by the team for the team. So contribute your ideas and best practices! See [How to Contribute](docs/rules-for-contributing.md).

## Rule 5: Doctype.
**Always** use the HTML5 Doctype:

	<!DOCTYPE html>

## Rule 10: SCSS Comments
Let's make our comments consistent and beautiful.

In SCSS, avoid using /* for single-line/inline comments - use // like in JS. It won't be exported to your CSS file, but it then allows you to comment out a whole block of SCSS with the standard CSS comments /*, without any interfearence.

Also, I use the following format for SCSS structuring:

// =============================================================================
// SCSS Header
// =============================================================================

It won't be processed into the raw CSS, which is probably a good thing, and it looks SEXY. I just love looking @ it.

## Rule 11: * { box-sizing: border-box; }
Border box is not default and required far more for resposive layouts than content-box. To save time worrying about when it's included, border-box everything. Use the compass mixin for backward compatibility upto and including IE8. Won't affect speed or anything - using * uses just as much memory as any other css.

## Rule 12: Use $variables for sizing
Keep a $spacing variable - it keeps your site's paddings, margins and gutterings consistent.
You can make more variables all relative to your main spacing variable too e.g $spacing-half: $spacing / 2
With fonts, this is also a good idea. $fnt-lrg; $fnt-med; $fnt-small; It's easy on big front-end's to end up with random font sizes.
Subtle consistency goes a long way.
