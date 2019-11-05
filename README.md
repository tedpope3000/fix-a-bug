# 🛠 fix-a-bug

## Setup

Clone this repo.

```bash
git clone https://github.com/datamade/fix-a-bug.git && cd fix-a-bug
```

Install the requirements. (Feel free to use a virtual environment!)

```bash
pip install -r requirements.txt
```

Run the tests.

```bash
pytest -sv
```

## Challenge

The code in `fix_me.py` contains four errors that are preventing the test from
passing. Debug and correct each error. As you identify the errors, fill out
a description of the problem and an explanation of the root cause and your fix
in the section below.

### Error 1

**Description:**
`value` and `index` objects were confusingly named in the `enumerate` for loop.

**Explanation:**
The enumerate object iterates with a tuple of (index, value), but the object
names were flipped.

### Error 2

**Description:**
`sum` function needs an iterable as an argument.

**Explanation:**
The sum function, `help(sum)`, shows that it accepts an iterable of values to 
be summed; creating a list of the 2 arguments solves the problem.

### Error 3

**Description:**
The assertion error shows that the list of values will be made correctly with
the `DATA` atttribute from the ParentB class.

**Explanation:**
Switching the order of inheritance will override the DATA attribute from class
ParentA and use the list of values that we need.

### Error 4

**Description:**
The name 'previous_value' is not defined.

**Explanation:**
The index 0 of a list will return it's first element, but in the `get_previous`
method it will return `[0 -1]` and -1 would be the last item in the list.
