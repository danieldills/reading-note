## JS Object Literals; The DOM

### Object Literals Chapter 3
What is an object?
***Objects group together a set of variables and functions to create a model of something you would recognize from the real world. In an object, variables and functions take on new names.***

***pg. 101 Duckett JS book***
```
var hotel = {
    name: 'Quay',
    rooms: 40,
    booked: 25,
    gym: true,
    roomTypes: ['twin', 'double', 'suite'],

    checkAvailability: function() {
        return this.rooms - this.booked;
    }
};
```
Above you can see a hotel object. The object contains the following key/value pairs:

|Properties: |Key               |Value    |
|---         |---               |---      |
|            |name              | string  |
|            |rooms             |number   |
|            |booked            |number   |
|            |gym               |Boolean  |
|            |roomTypes         |array    |
|Methods     |checkAvailability |functions|

**Creating an object: Literal Notation**
- Literal notation is the easiest and most popular way to create object.
    - Object is curly braces and their contents. The object is stored in variable called hotel, so you would refer to it as the hotel object. 
    - Separate each key from its value using a colon. 
    - Separate each property and method with a comma.

**Accessing an object and Dot Notation**
- You access the properties or methods of an object using dot notation. You can also access properties using square brackets.
    - To access a property or method of an object you use the name of the object, followed by a period, then the name of the property or method you want to access. This is known as dot notation.
    - The period is known as the member operator. The property or method on its right is a member of the object on its left. Here, two variable are created to hold the hotel name and number of vacant rooms.

    ``` 
    var hotelName = hotel.name;
    var roomsFree = hotel.checkavailability();
    ```

    ### Document Object Model Chapter 5
    The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.
    - The DOM Tree is a model of a web page

    Access and updating the DOM tree involves two steps
    1. Step 1: Access the elements
        - select an individual element node
        - select multiple elements (nodelists)
        - traversing between elements nodes
    1. Step 2: Work with those elements
        - access/update text nodes
        - work with HTML content
        - access or update attribute values
    
[<== Back](README.md)