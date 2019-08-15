
#### TASK 2 - CREATING LIST ITEMS - DOM MANIPULATION

**Description**: A List of Highend Phones with a collapse button that reveals the options on click event  - *when the user clicks on the button*.

> Hint: Make the console your _**friend**_

#### Step 1: Start the App
Call the `startApp` function before the closing script tag (`</script>`).

Create a new variable `phoneList` inside the `startApp` function, the value should be an empty Array `[]`. 

#### Step 2: Create the List Elements

Inside the `for` loop, çall the `createList` function with the `model` variable as the argument. 

 > *The `createList` function returns a `Node`*   

Assign the `createList` function to the `listEl` variable, and push the variable to `phoneList` array.  

After the `for` loop invoke the `addToList` function with the `phoneList` variable as an argument. 

#### Step 3: Create List Element
In the `createList` function, set a parameter `phone_name`. Using `document.createElement`, create a `li` element, assign it to a `listEl` variable, add a class of `fancy__list` to the `listEl`.  
Before the `return` statement, invoke the `activeToggleButton` function with the `listEl` as an argument .

 > *`activeToggleButton` adds the click event listener to the `.toggle-btn` inside the `listEl`. The `activeToggleButton` doesn't have a return value.*
 
> *At this point you should see a list of all the phones in the `PHONE_MODELS` array. But the toggle `button` won't work.*

#### Step 4: Add the click event to the Buttons
In the `activeToggleButton` function,  add a click event to `arrowButton` variable. On click of the `arrowButton` the `toggleAction` function should be called.

#### Final Step: Add More Phone Models
Add some models to the `PHONE_MODELS` array, to see if it's dynamic.
