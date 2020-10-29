# JavaScript Prerequisites 7%

## Language fundamentals

### Datatypes

- Null: null
  - the absense of an object
- Undefined: undefined
  - lack of a defined value
- Number: 1, 1.5, -1e4, NaN
- BigInt: 1n, 9007199254740993n
- String: 'str', "str", `str ${var}`
  - single quotes and double quotes work
- Boolean: true, false
- Symbol: Symbol('description'), Symbol.for('namespace')

### Functions

functions are objects, meaning a function can return another function

### Prototypal Inheritance (Functional)

- functional
- constructor functions
- class-syntax constructors

#### functional

``` javascript
const wolf = {
  howl: function () { console.log(this.name + ': awoooooooo') }
}

const dog = Object.create(wolf, {
  woof: { value: function() { console.log(this.name + ': woof') } }
})

const rufus = Object.create(dog, {
  name: {value: 'Rufus the dog'}
})

rufus.woof() // prints "Rufus the dog: woof"
rufus.howl() // prints "Rufus the dog: awoooooooo"
```

## Scoped to core language features introduced since EcmaScript 1 and still heavily used today
