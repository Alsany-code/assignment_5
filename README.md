1. Difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll

"getElementById" is used to select a single element with a specific ID. For example, if there is a unique header element on a webpage with an ID of main-header, using getElementById will directly select that header. "getElementsByClassName" selects all elements with a certain class. For instance, if multiple buttons share the class "submit-btn", this method will select all of them at once. "querySelector" allows selecting the first element that matches any CSS selector, such as the first paragraph inside a div, while "querySelectorAll" selects all elements that match a given CSS selector, like all items in a list.
While getElementsByClassName/getElementById will only give html collection, querySelector/querySelectorAll gives nodelist.

2. How to create and insert a new element into the DOM
3. 
To create a new element and insert it to the DOM rrequires 3 steps:
First, Create the element: document.createElement("tagName")
Set content or attributes: textContent, innerText, etc.
Insert it into the DOM: appendChild, prepend.

3. Event Bubbling

Event bubbling is when an action starts from the innermost element and moves outward to its parent elements. For example, if you click a button inside a card, the click event first activates the button's own behavior, then the card’s behavior, and then any container that holds the card. Each ancestor element has a chance to respond to the event as it bubbles up through the DOM hierarchy.

4. Event Delegation

Event delegation is when you attach a single listener to a parent element instead of multiple listeners on child elements. For example, instead of adding a click listener to every individual button in a list, you attach one listener to the list itself. When a button is clicked, the parent listener identifies which specific button was clicked and handles it. This saves memory and works even for buttons added to the list dynamically after the page loads.

5. Difference between preventDefault() and stopPropagation()

preventDefault() is used to stop the browser’s default behavior. For example, clicking a link normally navigates to another page, but using preventDefault() stops that navigation. stopPropagation() stops the event from moving to parent elements. For instance, if you click a button inside a form, the click might normally trigger both the button and the form's click behavior. Using stopPropagation() prevents the form from reacting to the button click.
