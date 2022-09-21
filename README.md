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

change font for h1 and h2, set to verdana and fall back to sans-serif. also give border-bottom of 4px solid colorname to h2 element.

To be able to navigate within the page, give each anchor element an href corresponding to the id of the h2 elements.

Below #student-info, need to add quiz content, so add 3 div element below it with class "info", then in each divs, add label and input elements.

It is important to link each input to the corresponding label element. This provides assistive techology users with visual reference to the input.

add ids to the input element, we need to take input of name, email address and date of birth, and add corresponding label element with for attribute whose value should match with the corresponding input element's id.
Also add Content of the label of name, email address and date of birth.

In input, always add type and name attribute, for name type will be text, for email type will be email, for dob type will be date.
Also add palceholder to display the applicable text.

Even though after adding placeholder for 1st input, it not actually best practice for accessibility, users confuse with the placeholder text and the actual value, so remove the placeholder, it is best practice to rely on the label.

DOB is not descriptive enough, especially for visually impaired users, without having to add visible text to the label, is to add text only a screen reader can read, we can do this by appending span element of class "sr-only" to the label element.
In span element, add text "(Date of Birth)".
But notice, (Date of Birth) is still visible, to make it invisible we need to add css rules in .sr-only element.
set position absolute
set width, height to 1px
set 0 padding, margin of -1px, oveflow hidden, clip: rect(0, 0, 0, 0), white-space to nowrap, 0 border.

Now lets add question, within 2nd section element, add 2 div element, with class name question-block, add in each div element, add 1 p element with text of question number and a fieldset element with class question.

Each fieldset will contain true false question, withing each fieldset element, add 1 legend element, and 1 ul element, give 2 options in ul element.

Give each fieldset an adequate name attribute, give both ul classes of answers-list, also in legend element add the question for true false, also add true false in li items.

Now, we are unable to select any answer as it is only text, so in order to make it function add radio type in input element within the label element which should be in each li element.

Also link the label with its input element.
Also add the answer with value attribute in input.

Now check that, both options can be selected at once, we dont want that, so group the answers with name attribute in input element.

Now question numbering is just 1, 2 etc, we want to add Question # in fron of the number to avoid unnecessary repition.
we can do this with psuedo before element with p. p::before{content: "Question #}

Now that we have added 2 true false questions, now we will add 2 more questions which will contain dropdown and a text box.

In last section, add div element of class formrow and nest 4 div elements of class question-block and answer.

in 1st div, nest a label element with question.
In 3rd div, nest a label element with question.

Now that question is ready, need to add options for answer, here we are using dropdown to select the answer,
so add select element in the 2nd div which is required, and add 3 option elements with value 
"" Select an option
"yes" Yes
"no" No
 Link the label element with select element, for and id set as customer. and give name attribute in select element, as customer.

 So now 3rd ques and ans is set, in the 4th question, we have do you have any questions, so need to give user a textarea where user can write their queries, so in 4th div with answer class, nest textarea element with rows and cols defined, and with a placeholder attribute.

 Link 3rd div label with 4th div textarea also give name attribute in textarea.

 Add submit button in the form element.

 Now the only thing left is footer element and address.
 footer element is container for collection of content that is related to the page, and address element is container for contact information for the author of the page.
 Add a footer element after main element, and add a address element inside footer.
 Within address element add the address
 e.g:
 freeCodeCamp<br />
 San Francisco<br />
 California<br />
 USA 

 wrap a link around text freeCodeCamp.

 Now in css, target li items of nav bar with nav > ul > li.
 and set color: #dfdfe2;
 margin 0 on top and bottom, left-right margin of 0.2rem.
 padding of 0.2rem
 set display to block.

 On the topic of visual accessibility, contrast between elements is a key factor. eg: the contrast between elements is a keyfactor. contrast between text and background of heading should be 4.5:1.
 Change the font color of a elements within li, by setting  color to inherit.

 now remove the underlines of nav items. with text-decoration set to none will remove the underlines.

 Now what we want is whenever user hover over the nav items, it should change the color and background color, also cursor should change to pointer, so to select it, use nav > ul > li:hover{}.

 Now usng flex properties in header element, set justify-content to space-between to make the space between flex items.
 and set align-items to center to vertically align it.

 Then fix the header to the top of the viewport. position: fixed, and set top: 0.

 Notice that, student info is invisible, so set the padding-top to make it visible, target main element.

 Set width of section element to 80% of the parent element, set margin to center the content, and set bottom margin of 10px, also set max-width to 600px;

 set 0 top margin and 60px top padding of h2 element.

 Add padding to top and left of .info element.

 Give .formrow element a top margin and left, right padding, also set font-size of all input elements to 13px.