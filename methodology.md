# `metaL` is not a programming language

**metaL is a method of programming* in Python (or any other language you prefer:
JS, PHP,...)

`metaL` works over two key features:
* homoiconic self-modifying data structures
* metaprogramming via code generation

That's why DML/DDL syntax parser is not required and is the only an optional
feature: parser was left there just to be a demo of the third magic feature of
the `metaL`:
* custom user-defined syntax

All `metaL` structures can be defined directly in the **host language**
(Python), the syntax parser is only a way to do it more simplified and to work
in symbiosis with Python REPL + VSCode. VSCode has the ability to send selected
parts of code from a text editor to a terminal with running REPL. This sending
has some disadvantage: Python's `input()` function can input only a single
string, so when we send a text from a VSCode, we can't detect was it a single
line or multiple lines text block. So, the syntax was chosen single-lined. It
also points, that DML/DDL in metaL is not a programming language, it's a
language of CLI commands.

As we can use code generation for producing transformations in a host language,
**it is possible to leave metaL without interpreter `eval()/apply()` core**
(user-defined functions and continuations), which are complex to understand and
implement for the newbie language designer. User function (method, new user type
class) can be specified, translated into host language without its execution,
resulting code should be pasted into metaL.py, and finally system restarts with
this new working transformation. As `metaL` were primarily designed for work
with interactive code generation, such system redefinition method is suitable
for use, especially if we'll have metaL [metacircular implementation] in the
system release.
