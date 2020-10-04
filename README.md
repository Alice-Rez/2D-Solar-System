# 2D Solar System

[Live Demo](https://alice-rez.github.io/2D-Solar-System/)

## Description

2D animation of the Solar System. This project was done after finishing CSS part of the course (before learning SCSS and JS). The proportions are not exact (it would make small planets not distinguishable), but the proportions between the time of orbit of individual planets (and Moon) corresponds to the reality. For the simplicity, just Moon of the Earth is displayed. Also there is no Pluto because Pluto is not a planet :grin:.

## Implementation

Images of the sun and planet surfaces taken from Wikipedia.

**Used technologies**: CSS variables, CSS animations, positioning, calculations, HTML,

For better manipulation with the whole system and for the better adjustments of responsiveness, the position and size of the sun were defined as a variables. Hence change of the position/size of the sun will lead to recalculation of the positions/sizes of the orbits/planets. using rems as a units then helps with changing size of the whole system at once in media queries just by redefinition of the root font size - the proportions will remain the same.

Divs in HTML corresponds to the orbits, planets are then added as the _::after_ pseudoelements. As a result, the whole orbiting animation is rotating of the orbit - the planet is glued on it and rotate together with orbit.

Orbits are positioned accordingly to the sun (position of sun minus difference in radiuses of sun and orbit of planet).

Planets are positioned accordingly to the orbit (in 50% of the orbit minus radius of the orbit, for the position in horizontal direction, probably from reason of the circular orbit the position had to be moved with 1px.... )

Creation of Moon's and Moon itself is same as for planet, only its position is relative to the earth position, because it is inside of earths div.
