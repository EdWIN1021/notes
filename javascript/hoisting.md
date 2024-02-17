## Hoisting

Hoisting is a behavior in JavaScript where variable and function declarations are moved to the top of their containing scope during the compilation phase, before the code is executed.

### undefined vs not defined
```js
// undefined 
console.log(a);
var a = "qwe";

// Cannot access 'a' before initialization const a = "qwe";
console.log(a); 
var a = "qwe"; 
```

### TDZ (Temporal Dead Zone)