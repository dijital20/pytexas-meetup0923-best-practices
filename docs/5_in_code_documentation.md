# In-Code Documentation

Documentation in code can also make a huge difference, especially in today's era of modern development tools. VSCode, 
PyCharm, and others can easily use in-code documentation to help guide users.

## Type hints

Type hints are great. Well written type hints let your users know what data types you expect for inputs and outputs. 
Coupled with a tool like `mypy`, type hints can also help find bugs in your own code, by helping to ensure consistent 
usage.

## Docstrings

Every module, class, and function/method should have a docstring. Regardless of which format you use (Sphinx, 
RestructuredText, Google, etc.), good, descriptive docstrings can be a lifesaver for development or documentation tool.

Docstrings should ideally have 3 parts...

### Summary

Keep this short and simple. What does the thing do/contain? Resist the urge to give deep implementation details (that's 
what `Notes` is for in a moment), and instead focus on the elevator pitch for the object.

### Arguments

For functions and methods, define the input arguments. Generally, I recommend that people using type hints avoid putting
types in the docstrings, as they can get out of sync (or at least double your maintenance if you change types). 

Description for each argument should define what the argument is in relation to the function. If you have a keyword 
argument with a default that is a sentinel value (like `None`), make sure to describe what behavior that means, like 
this example:

```python
def get_machine_information(serial_number: str | None = None) -> dict[str, str]:
    """Get information for a machine given its serial number.

    Args:
        serial_number: Serial number of the machine. Defaults to None, which will look up the serial of the current 
            machine.
    
    Returns:
        Dictionary of information on the maching. Keys include `model`, `manufacturer`, and `cpu`.

    Raises:
        ValueError: If the serial number cannot be looked up for the current machine.
        FileNotFoundError: If the serial number is not found in the database of machines.
    """
    ...
```

### Returns, Yields, and Raises

Define what the function will return. If your function doesn't return anything, feel free to omit this section. If your 
function raises any exceptions explicitly, be sure to define what type is raised and the conditions that would 
precipitate the exception.

### Notes and other sections

Other sections are optional, but helpful.

- **Examples**: Show off examples of your code in use. If you put these in REPL format, then you might be able to use the 
  `doctest` module to use them as unit tests.
- **Notes**: Give details on implementation behavior here. Be as detailed as you feel you need to be.
- **See Also**: Use this section to redirect users to other objects, or to other documents in your codebase.

## Line comments

Line comments should provide context or justification to your code. Admittedly, these are usually geared more to 
maintainers than users, but can be useful to both audiences. 

The other 2 useful uses for line comments are signposts and regions. A signpost is a short comment that helps you find 
a place in the code. Signposts give you easily searchable statements you can use to get to a specific area of code.

```python
class Order:
    # Modify orders
    def add_product(product: Product) -> Order:
        ...

    ...  # A few lines later...

    # Transition orders
    def execute() -> PlacedOrder:
        ...
```

Regions are like signpost comments, but there are comments at the beginning and end of the region which help draw 
borders around the code. Most modern editors can detect these comments and allow code folding. Even without that, it 
helps you group objects by usage. Regions can be nested.

```python
# region Public classes
class Order:
    # region Magic Methods
    def __init__():
        ...
    # endregion

    # region Public functions
    def add_product(product: Product) -> Order:
        ...
    
    ...
    # endregion

...
# endregion
```
