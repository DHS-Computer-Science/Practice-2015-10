# Practice 2015 - 10: Important Puzzles

## Background
The Avengers are trying to catch Loki, but he’s trapped himself behind a series
of locked doors. Thor tried to smash through them, but they’re made of the same
material as the prison cell on the helicarrier. The doors can each be unlocked
by solving a puzzle consisting of a row of coins, some showing “heads” and some
showing “tails”. The Avengers need to figure out if each door can possibly be
unlocked given its initial configuration and a set of possible moves they can
make, or if they need to call Nick Fury and come up with a backup plan.

The puzzle consists of a row of coins that all start face-side up. There is
a “goal” configuration of the board, in which coins may be oriented as “heads”
or “tails.” There is also a set of allowed “moves” – a move consists of a list
of coins that all must be flipped when someone uses that move. The object of the
puzzle is to determine a sequence of moves that will take the board from the
starting configuration to the goal configuration.

For example, one instance of the puzzle could be described as follows:
Goal configuration: HTTHT. Possible moves:
1. Flip coin 5
2. Flip coins 1 and 4
3. Flip coins 1, 2, 3, 4, and 5
4. Flip coins 1, 4, and 5
To solve this puzzle, we could apply move 2 then move 3:
`HHHHH → move 2 → THHTH → move 3 → HTTHT`

There may be multiple ways to solve the puzzle; for instance, we could also
apply move 1, followed by 3, and then 4:
`HHHHH → move 1 → HHHHT → move 3 → TTTTH → move 4 → HTTHT`

However, there are also puzzles that cannot be solved. Your program, given a
goal configuration and list of moves, must determine whether or not it is
possible to solve the puzzle.

## Description

### Input
The first line of the file will have an integer, n, which is the number of test
cases in this file.

Each test case starts with a line containing two positive integers, l and m,
denoting the board length and number of possible moves, respectively.

The second line of each test case is a string of l characters (H’s and T’s)
describing the goal configuration.

After this, m lines follow, each describing a possible move. A move is given as
a string of S’s and F’s, representing coins that stay (for ‘S’)
or flip (for ‘F’) on that move.

Note that the first test case shown below is the puzzle given above.

Each board will have a length between 5 and 64, and between 1 and 64
possible moves.

### Output
If the puzzle can be solved, print “CAN BE SOLVED”. If not,
print “CANNOT BE SOLVED”.

## Sample
### Input
```
5
5 4
HTTHT
SSSSF
FSSFS
FFFFF
FSSFF
5 1
HTTHT
SSSSF
5 2
HTTHT
SSSSF
SFFSS
3 1
HTH
SFS
3 1
HTH
FSF
```

### Output
```
CAN BE SOLVED
CANNOT BE SOLVED
CAN BE SOLVED
CAN BE SOLVED
CANNOT BE SOLVED
```
