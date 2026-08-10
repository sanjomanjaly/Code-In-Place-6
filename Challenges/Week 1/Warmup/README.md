
### Beginner (The "Make It Work" Level)

*   **The Goal:** Just get to the finish line.
*   **How it works:** You write a straight list of commands from top to bottom.
*   **The Downside:** It gets the job done, but it is very rigid. If you ask a beginner script to walk forward 100 times, you have to write the `move` command 100 times. It also assumes the world is perfect and nothing will go wrong.

**Code**

```python
def main():
    move()
    pick_beeper()
    move()

```



### Intermediate (The "Storyteller" Level)

* **The Goal:** Make the code easy for humans to read and update.
* **How it works:** Instead of a massive list of commands, you group actions into custom, clearly named steps (like `approach_target` or `retrieve_item`).
* **The Upgrade:** The main part of the code now reads like a short story. If a bug happens, you know exactly which "chapter" of the code to fix without reading every single line.

**Code (Without Comments)**

```python
def main():
    approach_target()
    retrieve_item()
    approach_target()

def approach_target():
    move()

def retrieve_item():
    pick_beeper()

```

**Code (With Comments)**

```python
def main():
    approach_target()
    retrieve_item()
    approach_target()

def approach_target():
    # Groups movement logic
    move()

def retrieve_item():
    # Groups interaction logic
    pick_beeper()

```

### Advanced (The "Defensive & Documented" Approach)

This is where you deploy the master template. An advanced programmer does not just write code that works when the world is perfect; they write defensive code that prevents crashes. Here, you use conditions (`if`) to ensure Karel does not walk into a wall or try to pick up a beeper that isn't there.

**Code**

```python
"""
=========================================================
OBJECTIVE: 
Safely navigate Karel to pick up a single beeper and advance, 
accounting for potential world errors.

CORE LOGIC:
1. Safe Movement: Check if the path is clear before stepping.
2. Safe Retrieval: Check if a beeper actually exists before picking it up.

CODE QUALITY CHECK:
- Implemented defensive programming (pre-condition checks).
- Used the master documentation template.
=========================================================
"""

def main():
    safe_move()
    safe_pick()
    safe_move()

def safe_move():
    # Prevents Karel from crashing into a wall
    if front_is_clear():
        move()

def safe_pick():
    # Prevents a crash if the beeper is missing
    if beepers_present():
        pick_beeper()

```
