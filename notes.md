# Notes - implementation of B version

## Introduction

- select the number you want
- press the cell you want to fill the selected number
- right click on a filled cell to clear it

## Ideas implemented

- hinting when wrong moves are occuring
- what answer is updated -- sn{x} - v(t-1) -> v(t) v=value t=time
- custom events = cell_changed , conflicts
