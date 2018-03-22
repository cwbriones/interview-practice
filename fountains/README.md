Fountains
=========

# Overview

Consider a series of hills and valleys.

```
Height
  3        _
  2       / \   _             _
  1      /   \_/ \   _   ____/ \
  0     /         \_/ \_/
```

We'll place fountains at various locations. A fountain floods areas around it, until the water level reaches the height of the fountain.

```
* - Fountain Placement
. - Water level

Height
  3        _
  2       / \   _             _
  1      /   \_/ \...*......./ \
  0     /         \_/ \_/
```

As you can see in the above diagram, the fountain has flooded at its height of two but cannot climb the hills at the ends of the valley.

Another example:

```
* - Fountain Placement
. - Water level

Height
  3        _
  2       / \.................*
  1      /   \_/ \   _   ____/ \
  0     /         \_/ \_/
```

Note if we placed a fountain at the top of the starting mountain, the whole map would flood.

# Problem

You are given two inputs:
* An array of heights
* An array of fountain placements, where 1s are fountains and 0s are empty.

Your job is to compute the flooded areas.
* Output: An array of flooded areas, where 1 means it is flooded and 0 means it is dry.

Each entry in the height array differs by at most 1 from the adjacent entries. Both arrays are the same size.

A rough example corresponding to the above would be
```js
area      = [0, 1, 2, 3, 2, 1, 2, 1, 0, 1, 0, 1, 1, 1, 2]
fountains = [0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0]
flooded   = [0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 0]
```


