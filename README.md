# python-rules

These rules were adapted from the PEP 8 style guidelines.

## Naming Conventions
| Type | Example |
|---|---|
| Function | function, my_fun­ction                     |
| Variable | x, var, my_var­iable                       |
| Class    | Model, MyClass                             |
| Method   | class_­method, method                      |
| Constant | CONSTANT, MY_CON­STANT, MY_LON­G_C­ONSTANT |
| Module   | module.py, my_mod­ule.py                   |
| Package  | package, mypackage                         |

## Imports
- All imports at top of file
- No unnecesarry imports, use specific imports
- No duplicate sources for imports. Use:
```py
from datetime import datetime, date
```

## Line Limits and Line Breaking
- We limit the number of lines to a respectable 79 characters.
- This is to ensure that we can have two files open adjacent to one another (Or an equivalent single file on a 800x600 monitor).
- If it is impossible to use implied continuation, then you can use backslashes to break lines instead:
```py
from mypkg import example1, \
    example2, example3
```

## Indentation
- Use 4 consec­utive spaces to indicate indent­ation.
- Prefer spaces over tabs.

## Comments
- Limit the line length of comments and docstrings to 72 charac­ters.
- Use complete sentences, starting with a capital letter.
- Make sure to update comments if you change your code.
- Start each line with a # followed by a single space.

## Block Comments
- Indent block comments to the same level as the code they describe.
- Separate paragraphs by a line containing a single #.

## Inline Comments
- Use inline comments sparingly.
- Write inline comments on the same line as the statement they refer to.
- Separate inline comments by two or more spaces from the statement.
- Don’t use them to explain the obvious.

## When to Avoid Adding Whitespace
- No trailing whitespace.
- Immedi­ately inside parent­heses, brackets, or braces.
- Before a comma, semicolon, or colon.
- Before the open parent­hesis that starts the argument list of a function call.
- Before the open bracket that starts an index or slice.
- Between a trailing comma and a closing parent­hesis.
- To align assignment operators.
- Immedi­ately inside brackets, as well as before commas and colons.

## Progra­mming Recomm­end­ations
- Don’t compare boolean values to True or False using the equiva­lence operator.
- Use the fact that empty sequences are falsy in if statem­ents.
- Use `is not` rather than `not ... is` in if statem­ents.
- Don’t use `if x:` when you mean `if x is not None:`

## Code Layout
- Surround top-level functions and classes with two blank lines.
- Surround method defini­tions inside classes with a single blank line.
- Use blank lines sparingly inside functions to show clear steps.
- Always specify the following when code is run as a script:
```py
if __name__ == "__main__":
```

## Indentation Following Line Breaks
- We align the indented block with the opening delimiter

```py
def function(arg_one, arg_two,
             arg_three, arg_four):
    return arg_one
```

## Where to Put the Closing Brace
- Line up the closing brace with the first character of the line that starts the construct:

```py
list_of_numbers = [
    1, 2, 3,
    4, 5, 6,
    7, 8, 9
]
```

## Documentation Strings
- Surround docstrings with three double quotes on either side, as in `"­"­"This is a docstr­ing­"­"­"`.
- Write them for all public modules and classes.
- Write them for non-obvious functions and methods.
- Put the "­"­" that ends a multiline docstring on a line by itself.
```py
"""
Multiline
Docstring
"""
```
- For one-line docstr­ings, keep the "­"­" on the same line.

## Whitespace Around Binary Operators
- Surround the following binary operators with a single space on either side:
    - Assignment operators (`=`, `+=`, `-=`, and so forth)
    - Compar­isons (`==`, `!=`, `>`, `<`, `>=`, `<=`) and (`is`, `is not`, `in`, `not in`)
    - Booleans (and, not, or)
- When = is used to assign a default value to a function argument, do not surround it with spaces:
    - `def functi­on(­def­aul­t_p­ara­met­er=5):`
- Normal assignment will be surrounded by spaces:
    - `y = x**2 + 5`
    - `z = (x+y) * (x-y)`
    - `if x>5 and x%2==0:`
- Treat the colon as the operator with lowest priority:
    - `list[x+1 : x+2]`
- In an extended slice, both colons must be surrounded by the same amount of whitespace:
    - `list[3­:4:5]`
    - `list[x+1 : x+2 : x+3]`
- If a slice parameter is omitted, a space is still required:
    - `list[x+1 : x+2 : ]`

## Because We're Geeks
- We only make use of Yoda conditions where the two parts of an expression are reversed from the typical order in a conditional statement.
- NO EXCEPTIONS!

```py
if (0 >= timer):
    return "Initiate Order 66"
```

## When to ignore this style guide
- If complying with the style guide would break compatibility with existing software.
- If you don't get the Yoda reference.
