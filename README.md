# exercise-vampires-werewolves-and-hybrids-using-ES6-classes

## Learning Goals

Upon completing this exercise, you will be able to:

- Create classes using ES6 syntax
- Implement inheritance using the extends keyword
- Define and use constructors in parent and child classes
- Utilize public and private class fields
- Create and use instance methods
- Practice class instantiation and object creation

## Introduction

Welcome to the sleepy town of Shadowville, where nothing ever happens... or so the residents thought. Lately, the town has been plagued by mysterious occurrences and sightings of supernatural beings. Vampires lurk in the shadows, werewolves howl at the moon, and rumors of hybrid creatures spread like wildfire.

As a skilled programmer, you've been called upon to create a simulation of these supernatural entities using ES6 classes, inheritance and basic OOP concepts.

Your mission is to bring these creatures to life and create a system where they can interact with the unsuspecting townspeople…

Are you ready to dive into the world of vampires, werewolves, and hybrids? 
Let's begin our supernatural adventure! 🧛‍♂️🐺🧪

## Getting Started

1. Fork the repository
2. Clone the repository to your computer
3. Open the repository in VS Code
4. Start the Live Server in VS Code
5. Follow instructions

## **Instructions**

Create a file named `supernatural.js` and implement the following classes:

### **Task 1: Supernatural**

Create a base `Supernatural` class with the following:

- Public field `name` and private field `#powerLevel`
- Constructor that receives `name` and `powerLevel`
- Getter method `powerLevel()` that returns the value of `#powerLevel`
- Method `introduceSelf()` that returns "I am `name`, a supernatural being."

### **Task 2: Vampire**

Create a `Vampire` class that extends `Supernatural`:

- Add a new public field `bloodThirst`
- In the constructor:
    - Call the `super` constructor with `name` and `powerLevel`
    - Initialize the `bloodThirst` field
- Create a method `drinkBlood()` that increases `#powerLevel` by 10 and returns the string: "`name` drinks blood and feels stronger!"
- Override `introduceSelf()` to return "I am `name`, a vampire."

### **Task 3: Werewolf**

Create a `Werewolf` class that extends `Supernatural`:

- Add a new public field `furColor`
- In the constructor:
    - Call the `super` constructor with `name` and `powerLevel`
    - Initialize the `furColor` field
- Create a method `howl()` that increases `#powerLevel` by 5 and returns the string: 
"`name` howls at the moon!"
- Override `introduceSelf()` to return "I am `name`, a werewolf with `furColor` fur."

### **Task 4: Hybrid**

Create a `Hybrid` class that extends `Supernatural`:

- Add new public fields `bloodThirst` and `furColor`
- In the constructor:
    - Call the `super` constructor with `name` and `powerLevel`
    - Initialize the `bloodThirst` and `furColor` fields
- Implement both `drinkBlood()` from `Vampire` and `howl()` from `Werewolf`
- Create a method `useHybridPower()` that calls both `drinkBlood()` and `howl()`, then returns the combined strings: "[Result of drinkBlood()] [Result of howl()]"
- Override `introduceSelf()` to return "I am `name`, a hybrid with vampire and werewolf powers."

1. Override the `speak()` method:
- Return a string: "I am `name`, a hybrid with vampire and werewolf powers."

### **Task 5: Create the Townsperson Class**

1. Create a `Townsperson` class with public fields for `name` and `fear` 
(number from 0 to 10)

2. Add a method `scream()` that returns a string based on their fear level. 
Implement conditional logic so that:
    1. If their fear level is 0, return “scream”
    2. If their fear level is 1, return “scream!”
    3. If their fear level is 2, return “scream!!”
    4. Depending on their fear level, append the corresponding number of exclamation marks to “scream”, where the fear level can be a maximum of 10.  For example, if fear level is 10, return “scream!!!!!!!!!!” (10 exclamation marks).

### **Task 6: Encounter**

Create an `encounter()` function that simulates an encounter between a supernatural being (Vampire, Werewolf, or Hybrid) and a Townsperson:

1. The function should accept two parameters:
    - `supernaturalBeing`: an instance of either Vampire, Werewolf, or Hybrid
    - `townsperson`: an instance of Townsperson
2. Implement the following logic within the function:
    - If the supernatural being's power level is greater than the townsperson's fear level, return a string: "[Townsperson's name] encounters [Supernatural Being's name] and runs away screaming!"
    - If the supernatural being's power level is less than or equal to the townsperson's fear level, return a string: "[Townsperson's name] encounters [Supernatural Being's name] and stands their ground bravely!"

### **Testing the Instantiation and Encounters**

To test your implementation, create instances of the classes and simulate encounters:

1. Create instances of `Vampire`, `Werewolf`, and `Hybrid` with different names, power levels, blood thirst, and fur colors.
2. Create instances of `Townsperson` with different names and fear levels.
3. Call the `introduceSelf()` method on each supernatural being instance and log the results to the console.
4. Call the `scream()` method on each `Townsperson` instance and log the results to the console.
5. Test the `encounter()` function by passing in different combinations of supernatural beings and townspeople. Log the results of each encounter to the console.

### **Bonus Task: Refactoring and ES6 Modules**

In this bonus task, you'll refactor your code to use ES6 modules and separate your classes into individual files. This will make your code more modular, reusable, and easier to maintain.

**Step 1: Create separate files for each class**

1. Create a new file for each class:
    - `Supernatural.js` for the `Supernatural` class
    - `Vampire.js` for the `Vampire` class
    - `Werewolf.js` for the `Werewolf` class
    - `Hybrid.js` for the `Hybrid` class
    - `Townsperson.js` for the `Townsperson` class
2. Move the respective class code from `supernatural.js` into each corresponding file.

**Step 2: Export the classes**

To make the classes available for use in other files, you need to export them. Add an export statement at the end of each class file.

Example (`Vampire.js`):

```jsx
class Vampire extends Supernatural {

// ... (Vampire class code remains the same)

}

export default Vampire;
```

Repeat this for each class file, exporting the class as the default export.

**Step 3: Create an** `index.js` **file**

1. Create a new file named index.js in the same directory as your other files.
2. Import the classes into index.js using the import statement.

Example (`index.js`):

```jsx
import Supernatural from './Supernatural.js';

import Vampire from './Vampire.js';

import Werewolf from './Werewolf.js';

import Hybrid from './Hybrid.js';

import Townsperson from './Townsperson.js';
```

3. Move the `encounter()` function & your testing code from `supernatural.js` into `index.js`.

**Step 4: Run your refactored code**

1. Open your terminal or command prompt and navigate to the directory containing your JavaScript files.
2. Run the `index.js` file using the Live Server.
3. Verify that the console outputs match the expected results from the testing code in `index.js`

## **Submission**

When you've completed the exercise:

1. Run the following commands:

```jsx
git add .
git commit -m "Completed Vampires, Werewolves and Hybrids exercise"
git push origin main
```

1. Create a Pull Request and submit your assignment.

Happy coding! May your supernatural beings be both terrifying and bug-free! 🧛‍♂️🐺🧪

## Frequently Asked Questions (FAQs)

<details>
<summary>What is the purpose of the `Supernatural` class?</summary>

The `Supernatural` class serves as a base class for all supernatural beings in this exercise. It defines common properties and methods that are shared by vampires, werewolves, and hybrids. By creating a base class, we can avoid code duplication and establish a consistent structure for the derived classes.

</details>

<details>
<summary>How do I create a subclass that inherits from a base class?</summary>

To create a subclass that inherits from a base class, you can use the `extends` keyword followed by the name of the base class.

</details>

<details>
<summary>What is the purpose of the `super` keyword in the constructor of a subclass?</summary>

The `super` keyword is used in the constructor of a subclass to call the constructor of its parent class. It allows you to pass arguments to the parent constructor and initialize any inherited properties. In this exercise, you'll use `super` to pass the `name` and `powerLevel` arguments to the `Supernatural` constructor.

</details>

<details>
<summary>How can I access the private field `#powerLevel` from within a class method?</summary>

Private fields, denoted by the # symbol, can only be accessed from within the class where they are defined. To access the `#powerLevel` field in a class method, you can simply use `this.#powerLevel`. Keep in mind that private fields are not accessible from outside the class or from subclasses.

</details>
    
<details>
<summary>How do I override a method from a parent class in a subclass?</summary>

To override a method from a parent class in a subclass, you simply define a method with the same name in the subclass. When an instance of the subclass calls the method, the overridden version in the subclass will be executed instead of the parent class's version. In this exercise, you'll override the `introduceSelf()` method in the `Vampire`, `Werewolf`, and `Hybrid` classes.

</details>
