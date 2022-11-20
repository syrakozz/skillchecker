# Code Smells


## Bloaters
![Bloaters](/img/bloaters.png)

Bloaters are code, methods and classes that have increased to such gargantuan proportions that they are hard to work with. Usually these smells do not crop up right away, rather they accumulate over time as the program evolves (and especially when nobody makes an effort to eradicate them).

* Long Method
* Large Class
* Primitive Obsession
* Long Parameter List
* Data Clumps
  
  <br/>

## Object-Orientation Abusers
![Bloaters](/img/oo-abusers.png)

All these smells are incomplete or incorrect application of object-oriented programming principles.

* Alternative Classes with Different Interfaces
* Refused Bequest
* Switch Statements
* Temporary Field


<br/>

## Change Preventer
![Bloaters](/img/change-preventers.png)

These smells mean that if you need to change something in one place in your code, you have to make many changes in other places too. Program development becomes much more complicated and expensive as a result.

* Divergent Change
* Parallel Inheritance Hierarchies
* Shotgun Surgery


<br/>

## Dispensables
![Bloaters](/img/dispensables.png)

A dispensable is something pointless and unneeded whose absence would make the code cleaner, more efficient and easier to understand.

* Comments
* Duplicate Code
* Data Class
* Dead Code
* Lazy Class
* Speculative Generality

<br/>

## Couplers
![Bloaters](/img/couplers.png)

All the smells in this group contribute to excessive coupling between classes or show what happens if coupling is replaced by excessive delegation.

* Feature Envy
* Inappropriate Intimacy
* Incomplete Library Class
* Message Chains
* Middle Man

[Source](https://refactoring.guru/refactoring/smells)