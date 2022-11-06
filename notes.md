# Notes - implementation of B version

## Introduction

- select the number you want
- press the cell you want to fill the selected number
- right click on a filled cell to clear it

## Ideas implemented

- right click - erase instead of a button - remove the option selection menu from appearing
- keyboard interaction - partial with only setting numbers

## Experimental Hypothesis

This version also accepts keyboard input events to control the movement of the focus indicator
and allow state changes on the board for faster movement as keyboard is faster to type on rather
than having to aim with a mouse

## New Logged Events

keyboard_move - is fired if a keyboard event is corresponding to the movement of the focus indicator

```JSON
{
    prevPos - previous position of the focus indicator
    curPos - current position of the focus indicator
    direction - direction of movement of focus indicator
}
```

keyboard_move_illegal - is fired instead of keyboard_move when a keyboard press is detected to move the focus indicator outside the available cells

```JSON
{
    prevPos - previous position of the focus indicator
    curPos - current position of the focus indicator
    direction - direction of movement of focus indicator
}
```
