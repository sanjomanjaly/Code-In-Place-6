Here is your text fully converted into a clean `README.md` format, keeping your original tone, style, and flow while structuring it properly for GitHub:

```markdown
# Welcome to Code in Place 6[cite: 3]

## the mindset for Karel[cite: 3]

Karel has limited functions, it is made so as to teach advanced functionality in programming[cite: 3].

### things to keep in mind[cite: 3]
 
* imagine you are standing in a square box and your front, left and right is closed, your back side is not considered[cite: 3].
* Karel has the ability to extend hands to see if the front, left and right is open or closed, hence it is represented as conditions[cite: 3].
* ex: if front is clear, or front is blocked, though both have the same function they have different outputs, hence slightly different use cases in the same program[cite: 3].
* another ability of karel is to find out the direction it is facing: north, south, east, or west[cite: 3].
* it is important to remember to document and keep track of the change in direction[cite: 3]. it helps later when writing code[cite: 3].

## the mindset for typing code[cite: 3]

the code that needs to be written requires a few things: Karel, a logic of how to solve the given challenge, what functions do we need to use, and if it is available pre-built or if one has to build it[cite: 3].

ex: turn left exists as `turn_left()`[cite: 3], but turn right doesn't exist[cite: 3]. 
We create such a function by recreating its movement[cite: 3]:
* the logic behind turning right being, if we turn left 4 times we reach the same place where we started, but if we only turn 3 times we can create a movement that is equivalent to a turn right[cite: 3].

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

## control flow: loops and decisions



* **decision making (`if`):** lets Karel choose what to do based on environment conditions.


* **repetition (`while`):** keeps an action running dynamically while a condition holds true.



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

```
