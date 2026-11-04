# 01 Scope
## What

Scope as it relates to programming determines the extent or range of access to a code in a code base.

Global.         Script/text.                       let, const, var
Function.       Access is function level.          let, const, var
Block.          Access within the block.           let, const

An inner code can access outside code but not vice versa. This is the chain of the scope.

## Why

Name change: So that the same name can be used inside and outside of the code, and it will not affect each other
Memory optimisation: Once a scope is no longer needed it is closed.

## When

throughout the code.
at initialization

## Example

const appName = "Nanocrafts" // Global

function greet() {
    let emoji = "emoji sign"

    function greeting(name){
        let restricted = "not visible"
        let name  = "Welcome"
        return (name, appName, emoji)
    }  // block

} // Function

greet()



## Topics
- [ ] Types,  scope, closures, `this`
- [ ] Promises, async/await, event loop
- [ ] Modules, bundlers, npm
- [ ] Error handling and debugging
