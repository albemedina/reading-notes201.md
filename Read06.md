# HTML/JavaScript Book Reading

# Class-06 Readings: Problem Domain, Objects, and the DOM

*Resource: Duckett JavsScript and JQuery interactive Front End Web Development* - Various parts cited from this resource

## Chapter 3 - Object Literals (pp.100-105)

- Objects are a grouping of variables and functions to represent a real world model.
- In an object variables become properties and functions become mehtods. Just different term used to define what they are but they are still created the same way. Just means the variables and functions and now part of an object.
- Variables in the object have a pairing of a key and a value. Same applies to functions where they have a key (the function name) then the function definition.
- The value of a property can be a string, number, boolean, array and another object. Methods are always functions but that function belowing to the object model.
- Defining an object is just about the same was a variable. The example below created a car object that contains the keys/value shown which are the properties and the method called detailedName.

```javascript
bjects gropu together a set of vairables and functions to create a model of a something you would recognize in the real world. In an object, variables and fuctions take on new names.

- In an object: variables become known as properties
- In an object: functions become known as methods

The object in the book represents a hotel. It has 5 properites and 1 method. The object is in curly bracess, it is stored in a variable calle hotel.

`var gym = {
  name: 'planet fitness',
  cardio room: 1,
  equipment: 100,
  gym: true,
  roomTypes: ['free weights', 'cardio', 'swimming'],
  '
  The above are properties--the variables.
  'checkAvailability: function() {
    return this.rooms - this.booked;
  }
}`
