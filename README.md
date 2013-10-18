# John Conway's Game of Life

The game of life is a simulation of cellular automaton.  Each cell is arranged in a 2-D grid and has 8 neighboring
cells.  The life cycle of a cell is dictated by a simple set of rules.

* If a cell is alive and has fewer than 2 neighbors, it dies as if by loneliness.
* If a cell is alive and has more than 3 neighbors, it dies as if by starvation due to over-crowding.
* If a cell is alive and has 2 or 3 neighbors it remains alive.
* If a cell is dead and has exactly 3 neighbors it spawns, as if by reproduction.

A further description of the game of life can be found at [Wikipedia](http://en.wikipedia.org/wiki/Conway%27s_Game_of_Life).

## Build Instructions
Requires GHC 7.6 and Haskell Platform 2013.  Additional dependencies are listed in gameoflife.cabal.

* cabal install -j

## Instructions
Instructions for using the life program once installed.

```
The life program
  
life [OPTIONS]
  
Common flags:
  -w --width=INT      The number of cells across the game board.
  -h --height=INT     The number of cells tall.
  -c --cellwidth=INT  The number of pixels across a single cell.
  -g --genpersec=INT  The number of generations per second.
  -? --help           Display help message
  -V --version        Print version information
```

For example, if you wanted a game of life where the board was 100x100 and the 20 generations occurred every
second, you would enter `life -w 100 -h 100 -g 20` in the command line.  The cell with modifier allows you 
to change the scale of each cell in pixels so that you can keep the whole game board on screen.
