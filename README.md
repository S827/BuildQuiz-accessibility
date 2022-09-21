# BuildQuiz-accessibility

We will learn accessibility by building a Quiz



Navigation is a core part of accessibility, and screen readers rely on you to provide the structure of your page. This is accomplished with semantic HTML elements.

Add header and main element, header will be used to introduce the page as well as provide navigation menu, 
main element will contain the core content of page.

Nest 1 img, h1 and nav element in header.
Add src in img element with id of logo, give h1 its content.

A useful property of an SVG (scalable vector graphics) is that it contains a path attribute which allows the image to be scaled without affecting the resolution of the resultant image.

Add background color in body selector.
Add color in body.
Add font-family and 0 margin on all sides.

Currently img is very large, we can scale it with width property, width: max(100px, 18vw).

Now use aspect-ratio property to set the desired aspect ratio to 35/4.
Also give padding of 0.4rem.

make header take its full-width, give background-color, height of 50px. And set display property to flex.

change the h1 font color with color property, set font-size to min(5vw, 1.2em).

To enable navigation on the page, add unorderered list with three items, items should be inside a tags to make it a link.

select nav element in css with nav selector, and give 50% width, max-width of 300px and height of 50px.

Now target nav ul element with nav > ul selector and set display property to flex, and justify-content to space-evenly.

Now in the main tag, add form element, and inside form element add 3 section element, with action attribute set to the provided link and method attribute set to post in form tag.

To increase the page accessibility, the role attribute can be used to indicate the purpose behind an element on the page to assistive technologies. The role attribute is a part of the Web Accessibility Initiative (WAI), and accepts preset values.
Give each section element the region role.

Every region role requires a visible label, which should be referenced by the aria-labelledby attribute.

To the section elements, give the following aria-labelledby attributes:

student-info
html-questions
css-questions
Then in each section, nest 1 h2 element with id of parent labelledby. Give each h2 its content.