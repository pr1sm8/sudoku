# Notes - implementation of B version

## Introduction

- select the number you want
- press the cell you want to fill the selected number
- right click on a filled cell to clear it

## Ideas implemented

- hinting when wrong moves are occuring
- what answer is updated -- sn{x} - v(t-1) -> v(t) v=value t=time
- custom events = cell_changed , conflicts

## Experimental Hypothesis

This version implements a hinting system that highlights the conflicting cells in red
for a quicker resolvement of the errors which improves the player's efficiency to view
errors on the board as it provides continual information

## New Logged Events

cell_changed - an event that fires when a cell's value is changed
{
    answerBefore - cell's answer before update
    answerAfter - cell's answer after update
    workBefore - cell's work before update
    workAfter - cell's work before update
}
conflicts - event that is fired when there are conflicts in the board state
{
    errors - contains an array of positions with conflicting values
}
