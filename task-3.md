
#### TASK 3 - DELETE A LIST ITEM (DOM MANIPULATION) :fire:

**Description**: In this task we will write the code to delete a list from the DOM. At first we will look at: 

* How to hide a List from view while still existing in the DOM
* How to remove a List from the DOM after hiding from the view
* How to modify the List from the Array directly. 

#### Step 1: Creating the StartApp function
Create a function `startApp`. Inside the function get the refresh button from the DOM using the CSS attribute selector `document.querySelector('[role=refresh]')`. Add a click event to the `refreshButton` that fires the `refreshList` function already provided for you. After that line add `refreshButton.click()` - *That function should click the button automatically*.

#### Step 2: Creating the Delete function
Create a function `activeDeleteButton` that takes in 2 parameters, `listEl` and `doAfterDelete` where the dataTypes are `Node` and `Function` respectively.  
Create a `deleteButton` variable, get the `button` inside of `listEl` with the selector `button[role=delete]` (Attribute Selector) and assign it to `deleteButton`. 

Add a click event listener to `deleteButton`. Inside the listener function do the following: 
* Added add a class of `hide__self` to the `listEl`. 

Head back to the `createList` function, invoke the `activeDeleteButton` with the `listEl` as the first argument and `onDelete` function as the second argument.

> At this point the list should hide when the (x) button is clicked. To remove it from the DOM you can continue from `Step 3`.

#### Step 3: Removing the List from the DOM
Continue from the `deleteButton` click listener function:
* Call `setTimeout()` with a delay of`1000` (which means 1000 miliseconds or 1 second). 
> Having issues with setTimeout? [Guide](https://javascript.info/settimeout-setinterval)
* Inside setTimeout, set `listEl.outerHTML = ''`.
> Setting the `outerHTML` property of a Node/Element to an empty string `''` deletes that element from the DOM. 
> You can confirm this by seeing the mutation from the inspector, when you click the delete button 


> At this point if you click the refresh button the item you deleted shoulld reappear. That's because it still exist in the PhoneHolder.phones Array. The next step should fix that. :wink:

#### Step 4: Updating the List of Phones
Inside the `setTimeout` function
> Reminder: `doAfterDelete` is a function parameter. So that's why we can invoke it.
* Invoke the `doAfterDelete()` function after the `listEl.outerHTML = ''` statement.

#### Finally: Study `callbacks`.
Visit [Link](https://suhas.org/javascript-callbacks/ 'Understanding JS Callbacks') to understand `callbacks`. And then try to understand the code.
