@ https://typescript-exercises.github.io/#exercise=5&file=%2Findex.ts

# Basic concepts
### Type inference
TS automatically infer the variable even if it's no set to any type.

##  Type ASSERTION
Type assertion allows you to set the type of a value and tell the compiler not to infer it. 

```
let code: any = 123; 
let employeeCode = <number> code; 
console.log(typeof(employeeCode)); //Output: number
```
 Can also be used by using 'as' key word, due to tsx 
```
ar x = <any> foo; 
// is equivalent to:
var x = foo as any;
```

# Interface vs types
## Types
- Types allows us to use unions
```
type Jobs = 'salary worker' | 'retired';
```

- Let use use primitives
## Interface
- ### Interfaces can be merged

```
interface Client { 
    name: string; 
}

interface Client {
    age: number;
}
```
-  By using the `extends` keyword, a new interface can inherit all the properties and methods of an existing interface, while also adding new properties.
```
interface VIPClient extends Client {
    benefits: string[]
}
```
` While extending in Types can be done `

```
type VIPClient = Client & {benefits: string[]}; // Client is a type
```

## Omit & Partial in TS?

# Questions



- ` What is TypeScript, and what are its key features?`
        TypeScript extends JavaScript by adding data types, classes, and other object-oriented features with type-checking. It checks the data type on compile time
- ` How does TypeScript differ from JavaScript?`
- ` How do you define a variable with a specific type in TypeScript?`
- ` What are the benefits of using TypeScript over JavaScript?`
` Explain the concept of type annotations and type inference in - `TypeScript.
` How do you declare an interface in TypeScript? Provide an - `example.
` What is the difference between interfaces and classes in - `TypeScript?
- ` How do you implement inheritance in TypeScript classes?`
` What are generics in TypeScript? Provide an example of using - `generics.
` How can you ensure that a variable can have multiple types in - `TypeScript?
` What are modules in TypeScript? How do you export and import - `modules?
- ` How do you handle asynchronous operations in TypeScript?`
` What are decorators in TypeScript? Provide an example of using a - `decorator.
` How can you configure the TypeScript compiler and specify its - `options?
- ` Explain the concept of ambient declarations in TypeScript.`
` What is the "any" type in TypeScript? When and why would you use - `it?
` What are the different types of modules in TypeScript? How do - `they differ?
` How can you enforce that a function parameter must be of a - `specific type in TypeScript?
` Explain the concept of union types and intersection types in - `TypeScript.
- ` How do you handle nullable or optional types in TypeScript?`
` What is a type assertion in TypeScript? How do you perform type - `assertions?
` How do you handle error handling in TypeScript, especially in - `asynchronous code?
` What are the key differences between "interface" and "type" - `declarations in TypeScript?
` How can you enforce immutability in TypeScript objects and - `arrays?
- ` What is the purpose of the "readonly" modifier in TypeScript?`
` How do you use the "namespace" keyword in TypeScript? Provide an - `example.
` What are the differences between "declare var," "declare let," - `and "declare const" in TypeScript?
` How do you use the "keyof" keyword and index types in TypeScript?- `
- ` Explain the concept of conditional types in TypeScript.`
` What is the "never" type in TypeScript? When and why would you - `use it?
