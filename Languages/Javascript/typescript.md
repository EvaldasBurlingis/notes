# Typescript

TypeScript is a superset of JavaScript which primarily provides optional static typing, classes and interfaces. One of the big benefits is to enable IDEs to provide a richer environment for spotting common errors as you type the code.

[Typescript website](https://www.typescriptlang.org/)

## Why to use typescript

* Provide an optional type system for JavaScript.
* Provide planned features from future JavaScript editions to current JavaScript engines

## Type system

As mentioned before Types are annotated using `:TypeAnnotation` syntax. Anything that is available in the type declaration space can be used as a Type Annotation.

### Types

```typescript

//Primitive types
var num: number;
var str: string;
var bool: boolean;

// Arrays
var strArray: string[];
var boolArray: boolean[];

// Special types
var canBeAnything: any;

// Void shows that function does not return type
function returnNothing: void {
    console.log('I print things to console');
}

// Union type allows property to be one of multiple types
var numOrStr: number | string;

// Intersection type combines multiple types into one
function extend<T, U>(first: T, second: U): T & U {
  return { ...first, ...second };
}

const x = extend({ a: "hello" }, { b: 42 });

const a = x.a;
const b = x.b;

// Tuple types allow to express array with fixed num of elements and types
let myArray: [string, string, number];

// Type alias 
type StrOrNum = string|number;
let item: StrOrNum = 'item';

```

#### `null` and `undefined`
How they are treated by the type system depends on the `strictNullChecks` compiler flag. When in `strictNullCheck:false`, the null and undefined JavaScript literals are effectively treated by the type system the same as something of type any. These literals can be assigned to any other type.

```typescript
var num: number;
var str: string;

// These literals can be assigned to anything
num = null;
str = undefined;
```

### Interfaces and inline type annotations

Interfaces are the core way in TypeScript to compose multiple type annotations into a single named annotation.

* Interface
```typescript
interface Motorcycle {
    make: string;
    model: string;
    color: string;
    topSpeed: number;
}

var moto: Motorcycle;

moto = {
    make: 'Honda',
    model: 'CB1000RR',
    color: 'Red',
    topSpeed: 300
};
```

* Inline type annotation
```typescript
var moto {
    make: string;
    model: string;
    color: string;
    topSpeed: number;
};

moto = {
    make: 'Honda',
    model: 'CB1000RR',
    color: 'Red',
    topSpeed: 300
};
```



