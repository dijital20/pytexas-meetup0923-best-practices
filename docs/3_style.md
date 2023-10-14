# Style

<div style="text-align: center; font-size: 125%; margin: 2.5% 5%; padding: 2.5% 5%; font-style: italic; border: 1px dotted black; border-radius: 1em; box-shadow: gray 0 5px 20px;">
"I don't care what you believe in, just believe in it."
<br/>-- Shepherd Book, "Serenity"
</div>

Style is one of those subjects where every Python developer has a different notion. Whether you are a die-hard Black or YAPF user, PEP8 stalwart, Google Style Guide follower, or anything else in between, everyone has an opinion. Readability is in the eye of the beholder, and no one can read your mind.

Whatever you believe, do 2 things with your style:

1. Document it
2. Follow it consistently

## Document it

Consider creating a `STYLE.md` file in the root of your project, and listing off your style rules.

* If you are using tools - Document the tools you are using, ensure they are in your `requirements.txt` or other dependency management solution, and consider adding text on how to run the tools.
* If you are using an existing style guide (PEP8, Google) - Link to the style guide you use, and make sure to document any deviations.
* If you are using your own style - Document the things you care about and conventions you use.

Consider documenting everything that is of consequence of differs from other common code.

### Naming schemes

*Do you name your variables based on type, use, or something else? What does the case of a name say about the object behind that name?*

This may be helpful in your code, and give your users signals to what you want as input or are passing out as output. Consider defining how naming relates to the inputs, outputs, and objects that the user has to deal with.

Case can be useful for at-a-glance signals of what things are and how they are used. I'm a fan of the naming rules in PEP8, and usually extend them with rules we'll talk about in [Code Design](4_code_design.md).

### Spacing

*How long can lines be? How do you prefer long lines be handled?*

Consider how and where users will read code. 

The PEP8 standard of 79 characters seems small, but makes sense for users reading code in an 80 column terminal. If that's too short, then giving yourself some extra room can be a good thing.

How do you handle long lines? Do you prefer to move items like collection elements and function arguments onto separate lines? How do you feel about hanging indents or the line continuation marker (`\`)?

Likewise, how do you handle indentation? Do you use tabs, spaces, or both. How many spaces are in a block? Consider sticking to the PEP8 standard of 4 spaces, bu

### Docstring format

What docstring format do you subscribe to, and how should it be interpreted? Most tools understand Sphinx, ReStructured Text, and the Google Docstring style. Consider using one of these established standards.

### Definition ordering/distribution

How do you break up objects along different packages and modules, and do you have a specific scheme for ordering of items in a module? Listing elements in syntactic order, alphabetical order, or some other order (static methods, class methods/fields, dunder methods, public methods, private methods) might aid in finding things. Consider adopting xn order and defining it.

Same with imports. Tools like `isort` or `ruff` can manage this for you.

## Apply it consistently

Once your style is defined, review your code to make sure it adheres to your own role. If you find exceptions to the rule in your code, consider documenting these deviations with line comments.

## Why?

Style affects consistency, and consistency, I feel, is a key to readability. Code that is consistent in style takes less cognitive load to read, which aids in understanding and retention.
