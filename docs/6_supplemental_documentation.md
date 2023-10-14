# Supplemental Documentation

Additional documentation can be useful for your project depending on the type of project.

## Text/Markdown Docs

Markdown is a great format for producing additional documentation. It is easy to write, easy to read without rendering,
renders into basic HTML, and easily supported by GitHub, GitLab, Bitbucket, etc. Good markdown documentation can be the
manual and FAQ for your project, giving users a readable reference.

Here are some recommended documents:

### README.md

This document should outline what your project does, how to install it, basic usage, and how to get help/support.

### CONTRIBUTING.md and DEVELOPING.md

If you are allowing people to contribute features to your project, then these documents should outline how to setup a 
development environment, considerations for code editing, and how to submit features or fixes.

### STYLE.md

As stated earlier, if you have standards on code style, this is a great place to put them. This is useful for readers
to know how to read your code, and writes to know what code style you expect.

### Any other documents

Create other docs as you need to. Most projects stick these additional docs into a `docs/` folder. Make sure that these
documents are linked from your `README.md`.

## Unit Tests

Well-written (and well documented) unit tests not only help ensure that the code works where it is deployed, but can 
also be a wonderful reference in how your project works (or doesn't work). Consider shipping your unit tests, and 
documenting how to run them in your markdown documentation. If you are using a third party unit test framework, like
`pytest` or `nose`, make sure you include something like a `requirements-dev.txt` with the dependencies for your unit
tests, so that your users can run them.

## Sample Code

Sample scripts using your project can also be useful for demonstrating how your project can work. Be sure to be more
verbose in your documentation of this code, both with docstrings and line comments. Make sure that your scripts focus 
on common usage patterns and scenarios. Consider placing these scripts in a folder, like `sample/`, and include a
`README.md` explaining each sample script.
