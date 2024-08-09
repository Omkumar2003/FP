# Functional Programming  

- Functional programming is more about declaring what you want to happen, rather than how you want it to happen.
- Imperative (or procedural) programming declares both the what and the how.

Imperative code 
```
car = create_car()
car.add_gas(10)
car.clean_windows()
```

this is functional thing , see in just one line ..how obscure amount of mutation we are doing which can make debugging tough
```
return clean_windows(add_gas(create_car()))
```

The important distinction is that in the functional example, we never change the value of the car variable, we just compose functions that return new values, with the outermost function, clean_windows in this case, returning the final result.



## we are doing in js 

Frankly, js  is not the best language for functional programming. Reasons include:

- No static typing.
- Everything is mutable.
- No tail call optimization.
- Side effects are common.
- Imperative and OOP styles abound in popular libraries.
- Purity is not enforced (and sometimes not even encouraged).
- Sum Types are hard to define.
- Pattern matching is weak at best.



## Immutability


In FP, we strive to make data immutable. Once a value is created, it cannot be changed. Mutable data, on the other hand, can be changed after it's created.

Who cares?
Immutable data is easier to think about and work with. When 10 different functions have access to the same variable, and you're debugging a problem with that variable, you have to consider the possibility that any of those functions could have changed the value.

When a variable is immutable, you can be sure that it hasn't changed since it was created. It's a helluva lot easier to work with.

Generally speaking, immutability means fewer bugs and more maintainable code.
