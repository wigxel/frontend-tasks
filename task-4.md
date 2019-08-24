
#### TASK 4 - ADD A NEW PHONE MODEL / MOVE PHONE MODELS TO SOLD SECTION

**Description**:  In this task you add a new phone model to the phones array, and also move a phone models to the _sold phones_ box
You'll learn the followings from this task:
* Adding an item to the start of an array using reverse method.
* Using `preventDefault` to prevent the default action for an event. 

### ADDING A NEW PHONE MODEL
#### Step 1: Add the input and button
In the HTML, add a `form` element before the `.list-holder` element and set the class attribute to `flex`. Inside the `form` element:
1. Create an input element with a placeholder `Add a phone model` and set the class attribute to `flex-1 border border-gray-500 p-2 pl-5`
2. Create a button element after the input, set the text to `INSERT` and the class attribute to `px-4 appearance-none hover:bg-gray-200 border border-gray-900`. 

#### Step 2: Add event listeners and functionality
1. Create an `activeInsertForm()` function.  
2. Get the `<form>` and `<input>` elements from the DOM  and assign them to their respective variables.  
3. Add a `submit` event to the `<form>` element *(this event is __triggered before__ the form submits)*. Inside the event `closure`, get the value of the `<input>` element from it's variable. Copy and paste the code below next.
```javascript 
const phones = PhoneHolder.get();
```
> The `phones` above variable is simple an `Array`.  

4. You are expected to `push` the value of the `<input>` element to the `phones` array. Copy and paste the code below next.
```javascript 
PhoneHolder.set(phones);
```
5. Clear the `<input>` elements value by settings it's `value` property to an empty string. 
```javascript 
formInput.value = ''
```

6. Still in the `closure` invoke the `refreshList()` function to render the list to the DOM. 

> Head to your browser to see what the code does for now.

#### Noticed a Bug in the code?
> Am sure you must have noticed that whenever the form is submitted it reloads the page(Form elements behaviour by default). We'll have to stop that from happening. 

### Using `preventDefault()` function
1. Back to the `submit` event `closure` which looks something like this:
```javascript
formElement.addEventListener('submit', function() {
    ...
```
2. You have to access the `event` parameter. This parameter is passed to the `closure` when an event is fired. So we get:
```javascript
formElement.addEventListener('submit', function(event) {
    event.preventDefault();
    ...
```
> At this point, we should be able to insert a new phone model even if the input field is empty. The input will be added to the end of the list. 
3. Ask google _how to insert an item to the start of an array in javascript_. 

### Moving an item to Sold Phones
1. Create an activateAddButton function before the `activeInsertForm` function. This function has two parameters, `listEl` and `model` which are `Node` and `String` datatypes respectively. 
2. In the `activateAddButton()` function, query select the `add button` with `[role=add-to-sold]` from the `listEl`. 
3. In the click event `closure` invoke the `movePhoneToSold()` with an argument of `model`. 
4. Head to the `createList()` function to uncomment the `activateAddButton` statement.

#### Creating the `movePhoneToSold()` function. :sparkle:
1. Create the `movePhoneToSold()` function above the `activateAddButton()` function. This function should have a parameter `phone_name` which will be of `String` datatype.
2. Create `filterPhones` variable. Set the variable to an empty array.
3. Run a `for` loop through the `PhoneHolder.get()`
4. Inside the loop block, write a code that pushes the item that isn't equal to the `phone_name` parameter.
5. Invoke `PhoneHolder.set()` function with the `filterPhones` variable as the argument.
6. Create a `soldList` variable and assign it to `PhoneHolder.getSold()` function, which returns an `Array`. 
7. Push the `phone_name` variable to the `soldList` variable. 
8. Invoke the `PhoneHolder.setSold()` function with `soldList` as the argument.
9. Invoke the `refreshList()` function. 

> Some changes where made to the `refreshList()` and the `addToList()` function. Do well to understand them. 

> The next task should have some AJAX. :thinking:
