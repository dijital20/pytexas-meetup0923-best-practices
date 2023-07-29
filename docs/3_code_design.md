# Design

The journey to obvious and familiar starts with design... how you portion up solutions into classes, functions, and 
variables. These patterns send signals to how your code should be used.

## Avoid classes where you don't need them

Unlike C# and Java, functions DON'T have to belong to classes in Python. This is fortunate in that, if a function doesn't change the state of a class, it doesn't necessarily mean that it needs to be a method on a class. Likewise, we don't have to create static classes just for the purpose of containing functions.

Start with simple, well-named functions, and consider building classes only when necessary.

## Apply SOLID Principles where they make sense

When you do build classes and begin working with objects, it's best to follow the SOLID principles. Keep your classes focused on single responsibility, open for modification via subclassing, 

## Name things appropriately

## Consider including unit tests

## Sample code
