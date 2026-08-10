# Method 2: The Ping-Pong (Shrinking Boundaries)

## Algorithm Overview

1. **Set the Boundaries (The two bookends):** 
   Karel starts at the West wall and immediately puts down a single beeper. He then walks forward across the completely empty world until he hits the East wall, where he puts down a second beeper. These two beepers mark his outermost boundaries.

2. **Step Inward (Preparing the loop):** 
   Karel turns around to face West and takes exactly one step forward. He is now standing in the empty space between his two boundary beepers, ready to start bouncing back and forth.

3. **Walk to the Boundary (Crossing the empty space):** 
   Karel walks forward as long as there are no beepers on the ground. Because the middle of the world is completely empty, he just walks straight ahead until he eventually bumps into the other boundary beeper on the far side.

4. **Move the Beeper (Shrinking the gap):** 
   Karel picks up the boundary beeper he just stepped on. He turns around, takes exactly one step inward toward the center, and puts the beeper back down. He then takes one more step forward so he is standing in the empty space again, ready for his next walk.

5. **Repeat Until They Meet (The bounce):** 
   Karel repeats Steps 3 and 4, ping-ponging back and forth. Every time he reaches a beeper, he picks it up and moves it one square inward. The two beepers get closer and closer together until they eventually meet in the middle. When Karel moves a beeper inward, steps forward, and instantly lands on the other beeper, the space has completely closed, and the loop ends.

6. **The Final Cleanup (The parity check):** 
   Because Karel brought two beepers to the middle, he has one extra. He picks up the extra beeper. Then, using the `if facing_east()` check you discovered, he adjusts his final position based on whether the world is even or odd. He takes his final steps and turns to ensure he lands perfectly on the true midpoint, facing the correct direction, and stops!

---

## Python Implementation

```python
from karel.stanfordkarel import *

"""
File: main.py
--------------------
Finds the midpoint of the world, defaulting to the left-middle
square in worlds with an even width.
"""

def main():
    if front_is_blocked():
        put_beeper()
    else:
        # Step 1: Set Boundaries
        put_beeper()
        while front_is_clear():
            move()
        put_beeper()
        
        turn_around()
        move()
        
        # Step 2: Bounce back and forth
        while no_beepers_present():
            while no_beepers_present():
                move()
            
            pick_beeper()
            turn_around()
            move()
            put_beeper()
            move()
            
        # Left-leaning parity branch
        if facing_east():
            pick_beeper()
            turn_around()
            move()
            turn_around()
        else:
            turn_around()
            move()
            pick_beeper()
            turn_around()
            move()
            turn_around()

def turn_around():
    turn_left()
    turn_left()

if __name__ == '__main__':
    main()
