# Programming Paradigm

## Hybrid Approach: OOP Backend with Functional Frontend

At this stage of our application's development we are planning to use a hybrid approach of programming paradigms, choosing the most appropriate for different layers of the application:

- **Backend (Node.js, Express, Mongoose):** Object-Oriented Programming
- **Frontend (React):** Functional Programming with Hooks

For the purposes of this assessment, we will provide a thorough explanation of Object-Oriented Programming (OOP) as it is the foundation of our data models and application logic.

---

## Object Oriented Programming

Object Oriented Programming is a paradigm which structures code into objects rather than functions and logic. An object or class (these terms are often interchangable) bundles related data (attributes) and behaviours (methods) into modular units, aligning with real world entities and their relationships. OOP promotes code organisation, reusability and maintainability through abstraction, encapsulation, inheritance and polymorphism (more on those terms below!)

---

## The Four Pillars of OOP

The four key principles of OOP are referred to as _The Four Pillars_. They are a set of rules to follow when creating an application, in order to help write clean, efficient and maintainable codebases. Let's discuss The Four Pillars in detail below.

---

### Abstraction

Essentially, this is ensuring that overcomplicated details of your code are "hidden away" behind simple interfaces. Abstraction focuses on only exposing essential features, keeping your code DRY and readable. Without abstraction your code can will be full of repeated and complex function code, and with several complicated functions can be difficult to understand.

For example, if you have a coffee making application:

- Processes abstracted from the user in hidden methods:
  - "Boil water"
  - "Measure cofee beans"
  - "Adjust grind setting to coarse"
  - "Grind coffee"
  - "Add boiling water to coffee pot"
  - "Wait five minutes"
  - "Stir coffee"
  - "Wait three minutes"
  - "Press coffee plunger"
- After abstraction, the simple interface becomes:
  - "Make a French Press Coffee"

As a practical coding example, the below is **abstracted** complex logic hidden from the user inside a method:

```js
class CoffeeMaker {
  constructor(type, size) {
    this.type = type;
    this.size = size;
    this.isBrewing = false;
  }

  makeCoffee() {
    // Complex coffee-making logic hidden from the user
    this.boilWater();
    this.grindBeans();
    this.bloomCoffee();
    this.pourWater();
    this.isBrewing = true;
    return "Your coffee is ready!";
  }

  // Private methods (implementation details)
  boilWater() {
    /* complex temperature control logic */
  }
  grindBeans() {
    /* complex grinding settings logic */
  }
  bloomCoffee() {
    /* complex timing and pouring logic */
  }
  pourWater() {
    /* complex water flow control logic */
  }
}
```

Below is the **simple interface** that abstraction creates for the user:

```js
// Simple usage - the user just calls makeCoffee()
const myCoffee = new CoffeeMaker("French Press", "Large");
myCoffee.makeCoffee(); // All complexity hidden!
```

Abstraction is the design pattern, not the end result. Meaning that the class design _is_ the abstraction that hides complexity from the user.

---

### Encapsulation

Encapsulation bundles data and methods which operate on the data within a single class or object, while restricting access to some of the objects components. This is achieved through the implementation of private properties and other modifiers.

Please see the diagram below to illustrate this concept:

!"[DIAGRAM HERE"]

An example of this is a user object which has a password as an attribute:

- A user must enter a password when registering or logging in
- The password is interacted with but **should never be stored as plain text, or directly accessible**
- Encapsulation ensures that password hashing occurs _within_ the `User` class, while only exposing safe methods such as `validatePassword()`

A practical coding example is below:

**Without Encapsulation:**

```js
// Dangerous - password exposed
user.password = "plaintext123";
console.log(user.password); // Anyone can read it!
```

**With Encapsulation:**

```js
class User {
  #passwordHash; // Private field

  setPassword(plainTextPassword) {
    this.#passwordHash = bcrypt.hash(plainTextPassword);
  }

  validatePassword(attempt) {
    return bcrypt.compare(attempt, this.#passwordHash);
  }
}

// Safe - password internally managed
user.setPassword("plaintext123");
user.validatePassword("guess"); // Returns true/false
// user.#passwordHash → Error: private field inaccessible
```

Encapsulation protects sensitive data through access and modification controls.

---

### Inheritance

Inheritance is the passing of properties and methods from an existing _parent_ object to a new related _child_ object. This is helpful for almost all programming projects, as it promotes code re-use, keeping codeblocks DRY, and forms logical heirarchy for related objects.

Please see the below diagram to illustrate the concept of inheritance:

![DIAGRAM HERE]

As an example, let's think use these objects: `Animal`, `Cat` and `Dog`.

- `Animal` is a parent class, as both `Dog` and `Cat` are animals.
- `Animal` has the properties: `name` and `age`
- `Dog` is an animal, so it inherits the properties `name` and `age` from the `Animal` object, but has the new properties `breed` and a new method `bark()`
- `Cat` is an animal, so it inherits the properties `name` and `age` from the `Animal` object, but has the new properties `breed` and `purr()`

A practical coding example is below:

```js
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}

class Dog extends Animal {
  constructor(name, age, breed) {
    super(name, age); // Inherit from Animal
    this.breed = breed;
  }

  bark() {
    return "Woof!";
  }
}

class Cat extends Animal {
  constructor(name, age, breed) {
    super(name, age); // Inherit from Animal
    this.breed = breed;
  }

  purr() {
    return "Purrrr...";
  }
}

// Usage
const myDog = new Dog("Rex", 3, "Labrador");
console.log(myDog.name); // "Rex" (inherited from Animal)
console.log(myDog.bark()); // "Woof!" (Dog's own method)
const myCat = new Cat("Fluffy", 7, "Devon Rex");
console.log(myCat.age); // 7 (inherited from Animal)
console.log(myCat.purr()); // "Purrr..." (Cat's own method)
```

Inheritance eliminates the need for repeated code, as the parent-child relationship allows objects to inherit properties without needing to redefine them.

---

### Polymorphism

Polymorphism is an incredibly versatile tool in OOP. It allows objects of different classes to be treated as one larger class, with the same method behaving differently depending on the object which has called it.

To follow on from our animal example:

- An `Animal` object has the method `speak()`
- A `Dog` object returns "Woof!" when speak is called on it
- A `Cat` object returns "Meow!" when speak is called on it

What this looks like in code:

```javascript
class Animal {
  speak() {
    return "Some animal sound";
  }
}

class Dog extends Animal {
  speak() {
    return "Woof!";
  }
}

class Cat extends Animal {
  speak() {
    return "Meow!";
  }
}

// Polymorphism in action - create a new Dog and Cat object
const animals = [new Dog(), new Cat()];

// Loop through the array of new objects, and call the speak() method for each
animals.forEach((animal) => console.log(animal.speak())); // Output: "Woof!" then "Meow!" - same method, different behavior
```

Polymorphism ensures that your code is flexible, and extendible, so new animals can be added without changing existing logic.

---

## Conclusion

Overall, OOP allows developers to create scalable, secure, and versatile applications through creating classes. Abstraction allows users to interface with methods simply, encapsulation ensures access to data related to objects is secure and controlled, inheritance allows code to stay DRY, and polymorphism allows developers to apply methods to multiple objects to ensure maintainable and scalable code.
