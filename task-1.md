### TASK 1 - SIMPLE DOM MANIPULATION 1

**Description**: This task will fetch post from a fake json server to your browser.

**Note**: _This task needs your computer to be connected to the internet._

#### Step 1: **Add Buttons**

Create 4 `button` elements within the `[role=pagination]` element. Every button should have a number from 1 to 4 respectively, and a class attribute that is equal to `rounded w-8 h-8 bg-gray-300`.

#### Step 2: **Adding the click event listener**

Complete the `activeButtons` function. Define a constant variable `buttons`. Fetch and assign all `buttons` from the document using `document.querySelectorAll()` to the `const buttons`.

Run a loop through every button in `const buttons`. For each `button` add a click event listener. The click event should call the `changePost` function with the `index` variable as an argument.

#### Step 3: **Fetching the post (XHR/AJAX)**

Add a parameter `post_id` to the `changePost` function, _that should complete the `postUrl`_ variable.

To make a request using the `fetch()`, pass the `postUrl` variable as an argument to `fetch()`. Convert the response to json using `res.json()`, then call the `replaceContent` function.

#### Step 4: **Adding the Post heading and paragraph**

To complete the `replaceContent()` you need to
fetch the `.heading` and `.para` elements from the DOM and assign them to their respective variables.
Set the `textContent` for both the `heading` and `para` variables to the `title` and `body` variables respectively.

#### Step 5: **Click the buttons**

Head to your browser click on buttons after the card, and the content should change for every button you click. If you can't find any button then something is wrong with your source code.

> Hint: Check the browsers console
