# 02 Hoisting
## What

## Why

## When

## Example


# ROUGH WORK!

# 01 Classes
## What
Class is a blueprint/template for making objects that follow a structure or behaviour. 

For example, classes are similar to cookie cutter.
  And each cookie will be an object. It may have different colours but it will be the same shape

Without class, if you want to create a user as an example, it will be:

const user1 = { name: "Alice", greet: function() { "Hi, I 'm Alice"}}
const user2 = { name: "Sam", greet: function() { "Hi, I 'm Sam"}}

With class:

class User {
    Constructor(name) {
        this.name = name
    }

    greet() { `Hi, I'm + " this.name"` }
}

const user1 = new User("Alice")
const user2 = new User("Sam")

console.log(user1.greet())
console.log(user2.greet())

- [ class User ] creates a blueprint for users
- [ Constructor ] creates a new name using this blueprint
- [ this.name ] each name created will be stored as this
- [ greet() ] accessed by all names created with the blueprint
- [ new User] creates an instance of a new user

## Why
Less memory is used.

## When
- [ ] When code reuse is important
- [ ] Ease of organization
- [ ] It makes update easy

## Brief about Inheritance
It allows extension without the need to create a new class.

class Admin extend User {
    deleteUser(){
      `this.name  + " deleted a user"`
    }
}



