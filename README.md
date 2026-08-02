Welcome to Code in Place 6

The mindset for Karel

Karel has limited functions, it is made so as to teach advanced functionality in programming.

Things to keep in mind
 
* imagine you are standing in a square box and your front, left and right is closed, your back side is not considered.
* Karel has the ability to extend hands to see if the front, left and right is open or closed, hence it is represented as conditions.
* ex: if front is clear, or front is blocked, though both have the same function they have different outputs, hence slightly different use cases in the same program.
* another ability of karel is to find out the direction it is facing: north, south, east, or west.
* it is important to remember to document and keep track of the change in direction. it helps later when writing code.

The mindset for typing code

the code that needs to be written requires a few things: Karel, a logic of how to solve the given challenge, what functions do we need to use, and if it is available pre-built or if one has to build it.

ex: turn left exists as `turn_left()`, but turn right doesn't exist. 
We create such a function by recreating its movement:
* the logic behind turning right being, if we turn left 4 times we reach the same place where we started, but if we only turn 3 times we can create a movement that is equivalent to a turn right.

```python
def turn_right():
    turn_left()
    turn_left()
    turn_left()

```

* now when we write the program, we can use `turn_right()` as a normal function like `turn_left()` and keep on writing the program.
* basically helper functions help make program writing less complex and easier. the more helper functions are used, the easier it is to understand the code.
* the advanced level of programming uses decomposition and helper functions together.

never forget to add the `:` colon when writing a helper function, it creates unnecessary errors.

Control flow: loops and decisions

* **decision making (`if`):** lets Karel choose what to do based on environment conditions.
* **repetition (`while`):** keeps an action running dynamically while a condition holds true.

```markdown

## Names of the conditions

### # karel conditions

* `front_is_clear()`
* `beepers_present()`
* `beepers_in_bag()`
* `left_is_clear()`
* `right_is_clear()`
* `facing_north()`
* `facing_south()`
* `facing_east()`
* `facing_west()`

### # opposites

* `front_is_blocked()`
* `no_beepers_present()`
* `no_beepers_in_bag()`
* `left_is_blocked()`
* `right_is_blocked()`
* `not_facing_north()`
* `not_facing_south()`
* `not_facing_east()`
* `not_facing_west()`

```
