# JavaScript

## Data types
### Primitives
number
string
boolean
bigint
symbol
### Non-Primitives
object
array
function

Everything is an object (stored in heap memory) except primitive values. Primitives (stored in faster memory regions like stack, though not the concern of JS programmer) are immutable, they cannot be modified. Though, the variables pointing to immutable primitives can be reassigned to get the illusion of modification. JS uses 'autoboxing' when methods are called on primitive values, which wraps them in objects temporarily.

Only an object is a non-primitive, functions and arrays are actually objects with key-value pairs under the hood. Object is mutable, and variables only store reference to them. The primitives are also available in object form, but note that their underlying raw values are still immutable

All variables are hoisted by the JS Engine before the code execution actually starts:
- 'var' ones are initialized with 'undefined' type, irrespective of the scope.
- 'let' ones are not initialized.
- 'const' are just like 'let' except that they cannot be reassigned once assigned with declaration
- functions declared with 'function' keyword and a name are initialized properly with their bodies
- anonymous functions with no name (arrow notation or 'function' kw) that are assigned to variables are initialized (assigned) accordingly with the 'var', 'let', or 'const' keyword of the variable   