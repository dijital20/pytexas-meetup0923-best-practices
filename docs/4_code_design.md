# Design

The journey to obvious and familiar starts with design... how you portion up solutions into classes, functions, and 
variables. These patterns send signals to how your code should be used.

## Apply SOLID Principles where they make sense

When you do build classes and begin working with objects, it's best to follow the SOLID principles. Keep your classes focused on single responsibility, open for modification via subclassing, subclasses being able to stand in for parent classes, and defining consistent public interfaces are all good things to adopt and stay consistent with.

## Avoid classes where you don't need them

Unlike C# and Java, functions DON'T have to belong to classes in Python. This is fortunate in that, if a function doesn't change the state of a class, it doesn't necessarily mean that it needs to be a method on a class. Likewise, we don't have to create static classes just for the purpose of containing functions.

Start with simple, well-named functions, and consider building classes only when necessary.

## Name things appropriately

> There are only two hard things in Computer Science: cache invalidation, naming things, and off-by-one errors.

Naming is important in Python. Having good naming schemes can allow a user to have at-a-glance information on how something should be understood and used. Using case to indicate general type (classes vs instances, protected members, constant members, etc.) is a common trope in existing style guides. I generally like to add the following 2 additional rules:

1. Variables and fields (including class names) should have noun names. After all, these are **things that are**.
2. Functions and methods should have verb names. These are **things that do**.

This also has the side effect of notifying the user how they should address your variable... with or without parenthesis.

```python
grocery_list = grocery_service.get_list()
print(grocery_list)
grocery_service.order_groceries()
```

In the above example, `grocery_list` has a noun name, so parenthesis are not needed, and I know this is a piece of information. 

Meanwhile, `order_groceries` and `get_list` both have verb names, which signals that I need parenthesis, and potentially to pass some information. These are actions that do something.
