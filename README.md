![General Assembly Logo](http://i.imgur.com/ke8USTq.png)

# Ruby Lab Day: Code Retreat

## Objectives

By the end of this, students should be able to:

-   Pair with other developers under a variety of constraints.
-   Explain the value of team communication in their own words.
-   Solve a problem in multiple ways by "spiking".
-   Choose an implementation strategy for a problem using lessons learned from
    spikes.

## Instructions

This code retreat will consist of several pairing rounds. Try to pair with
someone new each time. For each round, you and your pair will work on
implementing Conway's Game of Life in ruby (see below). After each round we will
hold a quick retrospective to share our experiences with each other.

<!--
Instructor note: Code should be deleted between each round. It's fun to watch
the looks on student faces when they hear this the first time.

For more ideas on challenges, check out
http://coderetreat.org/facilitating/activity-catalog
-->

After a brief introduction, we will whiteboard the rules. Then, we'll complete
the following activities. Each activity will be followed by a retro and a break.

These times are subject to, and most likely __will__ change.

1.  Caveman Coder (45 minutes)
1.  Navigator-Driver (30 mintues)
1.  Silent Coder (15 mintues)
1.  Flat Files (30 mintues)
1.  Sandi's Rules (30 minutes)
1.  Git Happens (30 minutes)
1.  Hot Potato (30 minutes)
1.  Free-for-all (60 minutes)
1.  Retro of the Day (15 minutes)

<!--
1.  Caveman Coder: whiteboard only, switch with another team after 30 minutes
1.  Navigator-Driver: One types, the other dictates; switch every 15 minutes
1.  Silent Coder: no talking allowed in pair
1.  Flat Files: no nested conditionals
1.  Sandi's Rules: https://robots.thoughtbot.com/sandi-metz-rules-for-developers
1.  Git Happens: randomly during the exercise, lose any uncommitted code (git reset --hard HEAD~1)
1.  Hot Potato: only one can work at a time, switch 5 minutes, no communication,
    delete uncommitted code
1.  Free-for-all: no constraints
-->

Before we get started, let's review the purpose of a code retreat and understand
the problem we'll be solving.

## Code Retreat

A code retreat is a day-long intensive practice, focusing on fundamentals. Pairs
of programmers tackle the same problem multiple times under different
constraints. The constraints are chosen to emphasize the value of modern
development practices like test-driven development, pair programming, patterns,
and iterative development.

Corey Haines expalins the goals of a code retreat in [Cleveland Code Retreat
Introduction on Vimeo](http://vimeo.com/18955165).

## Conway's Game of Life

The Game of Life, also known simply as Life, is a cellular automaton devised by
the British mathematician John Horton Conway in 1970.

Visualization of the Game of Life:

![Alt Conway's Game of Life](http://upload.wikimedia.org/wikipedia/commons/e/e5/Gospers_glider_gun.gif)

<!--
Image from Population Dynamics(http://www.slideshare.net/pelikan/stars2012-finalpresentation)

-->

The "game" is a zero-player game, meaning that its evolution is determined by
its initial state, requiring no further input. One interacts with the Game of
Life by creating an initial configuration and observing how it evolves.

The universe of the Game of Life is an **infinite two-dimensional orthogonal
grid** of square cells, each of which is in one of two possible states, live or
dead. Every cell interacts with its eight neighbors, which are the cells that
are directly horizontally, vertically, or diagonally adjacent.

### Rules

At each step in time, the following transitions occur:

1.  Any live cell with fewer than two live neighbours dies, as if caused by
    underpopulation.
1.  Any live cell with more than three live neighbours dies, as if by
    overcrowding.
1.  Any live cell with two or three live neighbours lives on to the next
    generation.
1.  Any dead cell with exactly three live neighbours becomes a live cell.

The initial pattern constitutes the seed of the system. The first generation is
created by applying the above rules simultaneously to every cell in the seed.
**Births and deaths happen simultaneously**, and the discrete moment at which
this happens is sometimes called a `tick` (in other words, each generation is a
pure function of the one before). The rules continue to be applied repeatedly to
create further generations.

Here is a visual representation of what is happening:

![population-dynamics-in-conways-game-of-life-and-its-variants-9-728](https://cloud.githubusercontent.com/assets/10408784/17438008/b3013c1a-5aee-11e6-888c-65946800ebcd.jpg)

### Tips & Tricks

You are **not** expected to finish the exercise in any particular round.

Even though your solution should work with an infinite grid, it can be
beneficial to start with a large, finite grid. Your solution should work for a
grid of at least 80x80 cells.

You may want to solve the problem for an infinite grid, but initialize the game
with a finite grid so it can be displayed on screen.

Your solution should work with any arbitrary starting arrangement of dead and
alive cells. Try initializing each tile randomly with either an alive or a dead
cell.

The hardest part might be getting started. Decide what class you want to use to
represent cells or tiles. Then, start adding small features to your class one
at a time.

For pairing exercises, try using one computer, and pass it between yourself and
your pair. Work together and in sequence. You and pair should not be working in
separate files at the same time.

## Bonus

If you're looking for extra challenge or practice once you've completed the
above, try pairing with someone using the following constraints:

-   Small methods. No methods longer than four lines.
-   No mutation of state allowed. Once a variable is assigned, it cannot change.
-   No conditionals. Do not use `if/else` and friends.
-   No loops.

If you have a working solution you like, post it to GitHub. It's great for
employers to see you tackling such a classic problem. Work with a classmate to
refactor your code using
[SOLID](http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod) and [The Rules
of Simple Design](http://xprogramming.com/classics/expemergentdesign/).

## Additional Resources

-   [Screencast: Coding Conway’s Game of Life in Ruby the TDD Way with RSpec](http://www.rubyinside.com/screencast-coding-conways-game-of-life-in-ruby-the-tdd-way-with-rspec-5564.html)
-   [A few git tips you didn't know about](http://mislav.uniqpath.com/2010/07/git-tips/)
-   [Fork A Repo - User Documentation](https://help.github.com/articles/fork-a-repo/)
-   [Syncing a fork - User Documentation](https://help.github.com/articles/syncing-a-fork/)
s
## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or alternative
licensing, please contact legal@ga.co.
