
### Question
```js
var Employee = {
  company: 'xyz'
}
var emp1 = Object.create(Employee);
delete emp1.company
console.log(emp1.company);
```
### Output: 
`xyz`
### Explanation

Lets do a code walkthrough to understand this.

```js
var Employee = {
  company: 'xyz'
}
```
An object `Employee` is created with a property `company` with a value `xyz`.
```js
var emp1 = Object.create(Employee);
```
`Object.create()` method creates a new object, using an existing object as the prototype of the newly created object.

So `Object.create()` method creates a new object, using an existing object as the prototype of the newly created object. So  `emp1` would not have a direct property called `company` . Instead it's `prototype` would have `company` property which can be accessed as `emp1.__proto__.company`.
```js
delete emp1.company
```
Here we deleted an non-existent property. Nothing changes in the object.

```js
console.log(emp1.company);
```
JS runtime first tries to find property `company` on object `emp1`. But it's not found. Then JS runtime searches for it in it's prototype at path `emp1.__proto__.company` which is found and value `xyz` is returned.
