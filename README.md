Front End Rules
===============

> [The Rules](http://www.velominati.com/the-rules/)

We have a growing Front End team here at Architect working on different projects all over the place all the time, in collaboration and in solitude. Yet we should all be able to pick up and work on any project at any time, regardless of the initial developer and be able to find our way around, understand what we're looking at and pick up where someone left off as easily if it were our own project to begin with.

The rules are here as our guide to all things Front End at Architect, they are created by us and for us*. By following these rules we ensure our code is well-written, well thought out, and easy to maintain.

> Every line of code should appear to be written by a single person, no matter the number of contributors.
[@mdo](https://twitter.com/mdo)

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

## Rule 6: It is what it is
Naming conventions for selectors should be based on what they are rather than what they look like. Class names like `bluetext`, or `redborder` become redundant if your colour scheme changes. A much better way to name your classes is with the role a certain HTML element is intended for in the document.

## Rule 7: Tabs are King in this castle.
Always use tabs, never spaces. Ensure everything nested is indented correctly by a single tab in all code including HTML, CSS/Sass and JavaScript.

## Rule 8: Do not use that which is unnecessary.
Code and Page bloat are easily avoidable, and serve both the developer and the audience to avoid. The more external frameworks we include in our JavaScript the longer each page takes to load, and the more code we have to trawl through when something goes wrong. Usually, there is a micro-library that will do the same thing, if VanillaJS won't.

This doesn't mean using micro-libraries over jQuery is always the correct option, but should be at least considered on a project specific basis.

## Rule 9: Comments (Sass)
Ensure comments are consistent and beautiful. In SCSS, avoid using `/* */` for single-line/inline comments - use `//` instead. 

To break up a section of CSS in a file use the following comment style:

	// ===================================
	// Header 
	// ===================================

This is a nice and clear method of introducing a new section in a CSS file and comes with the advantage that it won't be processed into the raw CSS.

## Rule 10: * { box-sizing: border-box; }
Border box is not default and required far more for responsive layouts than content-box. To save time worrying about when it's included, border-box everything. Use the compass mixin for backward compatibility up to and including IE8. Won't affect speed or anything - using `*` uses just as much memory as any other css.

See [Paul Irish's article](http://www.paulirish.com/2012/box-sizing-border-box-ftw/) for more information.

## Rule 11: Attribute order
HTML attributes should come in this particular order for easier reading of code.

- src, for, type, href
- title, alt, name
- id
- class
- data-*
- aria-*, role
- boolean attributes (required, checked, etc.)

To easily understand the markup you're writing, the main attribute of the element should be first, and for images and links, the title/alt attribute should follow immediately. Style and interaction attributes like classes, IDs, and data attributes should be towards the end of the elements, followed by a11y attributes.

	<input type="text" name="..." id="..." class="..." required>

	<img src="..." alt="..." class="...">

	<a href="..." title="..." id="..." class="..."></a>