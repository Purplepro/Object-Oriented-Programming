# Object-Oriented-Programming

/ Classes
class Person {
    constructor(name) {
        this.name = name;
    }
    greet() {
        return "Hello, my name is " + this.name;
    }
}
class Student extends Person {
    constructor(name, course) {
      super(name); // inherited from Person
      this.course = course;
    }
    /*
    greet() {
        return "Hello, my name is " + this.name;
    }
    */
    doHomework(assignment) {
        console.log(`Deliverable: ${assignment}`); // temperate literal
    }
}
const bob = new Person('Bob');
console.log(bob.name);
console.log(bob.greet());
const john = new Student('John', 'SEI');
console.log(bob);
console.log(john);
class Parent {
    constructor(name, location) {
        this.name = name;
        this.location = location;
    }
    drive(car) {
        console.log(`${this.name} is driving ${car}`);
    }
}
class Child extends Parent {
    constructor(name, location, school) {
        super(name, location);
        this.school = school;
    }
    doHomework(assignment) {
        console.log(`Deliverable: ${assignment}`); // temperate literal
    }
}
const parentOne = new Parent('Sarah', 'LA');
parentOne.name; // console.log
parentOne.location;
parentOne.drive('Mercedes');
const childOne = new Child('Robert', 'LA', 'Private School');
childOne.name;
childOne.location;
childOne.school;
childOne.drive('Honda') // method that comes from Parent
childOne.doHomework('Physics'); // method is on the class Child