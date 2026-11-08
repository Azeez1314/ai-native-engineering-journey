# 02 Hoisting
## What

## Why

## When

## Example


# ROUGH WORK!

# 02 Hoisting
## What
This is the term used to indicate when a code is moved above. It does not indicate that the code is actually the first in line, but it is the first in memory.

Variable       Hoisted           Initial Value           Usable before line

var            Yes               undefined               Yes, undefined
let/const      TDZ               uninitialised           No, reference error (uninitialised)
function       Yes               function decl           Yes, function decl
function expression
(const f = f() {})
               TDZ.              uninitialised           No, Type Error (f is not declared)
function declaration
(f = () => {})
               Yes              function decl           Yes, function decl

## Why
It make it easy to maintain and read code.

## When
When it's good:

- [ ] It allow easy read of code. The declared function can be used by helper functions below. Top-bottom ease.
- [ ] It allows code that are no longer in ise to to released from memory

When it's bad:

- when var is used in block scope. It cannot be accessed

## Example
- [ var ]

console.log(name)
var name = "Azeez";

- [ let/const ]

console.log(age)      // Reference error. variable is uninitialised
let age = 10

console.log(school)      // Reference error. variable is uninitialised
const school = "Sheffield"

- [ function ]

test()        // function declaration

function(test) {
    let name = "Azeez"
    console.log(name)
}
test();

- [ function expression & arrow function]

newTest()        // Type error. uninitialised

const newTest = function() {
    let name = "Azeez"
    console.log(name)
}
newTest();  



anotherTest()        // yes. arrow function

const anotherTest = () => {
    let name = "Azeez"
    console.log(name)
}
anotherTest();  