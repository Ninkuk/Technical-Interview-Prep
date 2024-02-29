#technical 

## General Tips
- 

---
## Basic Data Types

| Type      | Description                                 |
| --------- | ------------------------------------------- |
| `Number`  | includes both int and float                 |
| `String`  | "hello world"                               |
| `Boolean` | true / false                                |
| `Array`   | `number[]` or `string[]`                    |
| `Any`     | removes the typescript-ness                 |
| `Unknown` | Similar to `Any` but forces you to typecast |

#### Union Types `|`
You can set a variable's type to multiple types

```ts
// age can be both number and string
let age: Number | String = 20;
age = "twenty";
```


---
## Custom Data Types

### Type Alias

```ts
type Point = {
    x: Number;
    y: Number;
};

let pt: Point = {x: 0, y: 5};
```

#### Optional Property `?`
In an object, a property can be defined of optional type. If accessed without setting, it will give the value of `undefined`.

```ts
type Point = {
    x: Number;
    y: Number;
    z?: Number; // z is an optional property
};
```

### Interface
Veeeeeery similar to a type alias

```ts
interface Point {
    x: Number;
    y: Number;
};

let pt: Point = {x: 0, y: 5};
```