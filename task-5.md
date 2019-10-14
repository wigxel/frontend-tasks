## XHR/AJAX REQUEST :guitar: 

In this task we will be making an AJAX Request to the an endpoint. The endpoint is a JSON file containing a list of phones.  
After that we will render the list of phones from the data received from the endpoint. With that we should have other information, not just the name of the phone anymore.

### STEP 1: **Fetching Phones**
 - Create a `fetchPhones()` function  
 - Call the `fetch()` function with the constant `PHONE_ENDPOINT` variable as an argument.
 > That is the endpoint where the phones data reside.  
 - Convert the response to JSON using `res.json()` e.g 
 ```javascript
fetch(PHONE_ENDPOINT)
    .then(res => res.json())
    .then((response) => {
        // we'll get the converted response from here!
    })
```
> Activate your developer tools in the browser enviroment and locate the `Network` tab. You should find the `endpoint` among the logs there. Click on that log to see the response or payload.  

- Log the response variable to the console to see the data structure.
> You'll observe that it's an `Object` with 2 keys. We will be needing just the `phones` key in this task. The value of the `phones` key is an `Array`.

### STEP 2: **Rendering List**

- Store the response using `PhoneHolder.set()` function.  
- Call the `refreshList()` function (same function from the previous task)
> You'll notice the list renders but instead of the name, we get `[object Object]`. So we need to modify the structure of the List next.

### STEP 3: **Modifying the LIST structure**
- Locate the `createList()` function definition. 
- Change the `phone_name` parameter to to `phoneObject` because the parameter represents an `Object`, no longer a `String`.
- Rename all `phone_name` variable in the `createList()` function to `phoneObject.name`. That way we should get the name.  
> You should be getting the phone names now. 

### STEP 4: **Adding Preloader**
I think preloaders are cool. It's a way of telling the user that something's coming. We really need it here. So let's add that feature.
- In the `fetchPhones()` function
    - Before `fetch()` function, invoke the `showPreloader()` function.
    - Before the `refreshList()` function, invoke the `hidePreloader()` function.
> That's how we control when we want to show or hide the preloader.

 ### Try Out!
- Try adding the `quantity` of the `phone` to the List element.

### That's all. :sparkle: 
:smiley: :thinking: *Please if you are having any issue, don't forget to state them in the `issues` tab [Here](github.com/wigxel/frontend-tasks "See Repo")*