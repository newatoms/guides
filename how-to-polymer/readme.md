> Goal of this guide: Explain the basics of Polymer using analogies

# How to Polymer

![Castle](https://upload.wikimedia.org/wikipedia/commons/a/a2/Inveraray_Castle,_Argyll_and_Bute,_Scotland-31May2010.jpg)

Imagine writing the building manual for this castle. You would quite quickly devide the castle up into certain elements. You have the drawbridge, the towers, the walls, etc.. These all are themselves made out of elements: windows, stone, ventilation shafts, etc. At the lowest level you might have elements like a single stone.

However, you wouldn't write a manual for each different stone you'd need, for example if you need a smaller stone. So you'd like the manuals to be somewhat flexible but specific enough to be able to quickly understand what you have to do.

Polymer is a coding language in which you can write manuals for all levels of these elements. Each element fulfills a unique purpose in a flexible way. In an element you often make use of other, smaller, elements. For a wall you'd use stones and both a specific, dynamic elements.

## Dynamic elements

The element should fulfill a unique function but remain flexible. You must be able to create a wall of 10 by 5 meters in the same way as you would create one of 50 by 5m. So the element 'above' the wall, a bastion for example, should be able to specify the size of the wall. When receiving instructions on it's size, the wall should update the amount of stones it's made out of.

![A bastion](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c5/Bastion_%28PSF%29.jpg/440px-Bastion_%28PSF%29.jpg)

It therefore wouldn't make sense to write the size of the wall inside the wall manual. What might be in the wall manual, is the size and type of stone that it use for a certain type of wall.

## Structure

As you might have notices, there is a hierarchy in the elements. Elements call upon other elements and might also be called upon themselves. Stone -> wall -> bastion -> side of the outer wall -> total outer wall -> castle -> province -> country -> continent -> world .. etc.

## Non dynamic parts

The element should be dynamic but fulfill a certain purpose. A stone will always be able to cary this much weight, survive for this long, etc.


## The advantages of Polymer

You've been building your castle for the past few weeks and it's now almost completed but you forgot to build the towers. Lucky for you, there's this Hans from Helsinky that really enjoys bumping into his towers while walking through other countries. So he gave the manuals to build the tower away for free. Since you both use the same manual for stone and since he gave the manual for the flag away as well, you can easily incorporate the tower into your castle now––lucky for us the castle is rebuild from scratch each time ;).

You've did since research and improved the weight a stone can carry by changing a fundamental chemical compount. Awesome, but now you'd need to go to walk through the whole castle to replase all the stones right? Nope! Since every element that uses the stone element uses the same manual, you can just alter the manual and build the castle from scratch again. So one element change can have huge effects throughout a castle.




styling: class, Id, structure
