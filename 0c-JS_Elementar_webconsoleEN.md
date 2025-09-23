# JavaScript Basics for the **Firefox Web Console**
_A compact, academically‑oriented primer with hands‑on commands and concise contrasts to Python and C++._  
**Context of use:** Open Firefox → Web Console (`Ctrl`+`Shift`+`K`). You can paste any of the code blocks directly and observe outputs.

---

## 0) Getting started in the browser console
- The Web Console evaluates code _in the page context_ (has access to `window`, DOM APIs, etc.).  
- Use `console.log(value)` to print results explicitly (the console also echoes the last expression’s value).  
- Clear the console with `Ctrl`+`L` (or the bin icon).  
- Multi‑line input: press `Shift`+`Enter` for a new line without executing.

> **Environment contrasts**
> - **JS (browser)**: event‑driven, single‑threaded with an event loop; DOM APIs available.  
> - **Python (REPL)**: multi‑paradigm, batteries‑included standard library; no DOM.  
> - **C++ (REPL via cling etc.)**: compiled/translated; no DOM; static typing and manual build ecosystem.

---

## 1) Declarations: `var`, `let`, `const`
**Essentials:**  
- `var` → function‑scoped; re‑declarable in the same scope; hoisted.  
- `let` → block‑scoped; **not** re‑declarable in the same block; temporal dead zone (TDZ) before initialisation.  
- `const` → block‑scoped constant binding (the binding is immutable, the object’s internals may still mutate).

```js
// 'var' — function-scoped and re-declarable
var a = 10;
console.log(a); // 10
var a = 20;     // re-declaration allowed
console.log(a); // 20

// 'let' — block-scoped, not re-declarable in the same block
let b = 5;
b = 7;          // reassignment allowed
console.log(b); // 7
// let b = 8;   // ❌ SyntaxError if uncommented: re-declaration in same scope

// 'const' — fixed binding (value can't be re-assigned)
const c = 3.14;
console.log(c); // 3.14
// c = 2.71;    // ❌ TypeError: Assignment to constant variable.

// 'const' with objects: binding fixed, internals can change
const cfg = { mode: "dev" };
cfg.mode = "prod";        // ✅ allowed (mutating the object, not rebinding)
console.log(cfg.mode);    // "prod"
```

**Common pitfall (hoisting & TDZ):**
```js
// Hoisting example:
console.log(x); // undefined (declaration hoisted, initialisation not)
var x = 1;

// Temporal Dead Zone (TDZ) with let/const:
try {
  console.log(y); // ReferenceError (TDZ)
} catch (e) { console.log(e.name); } // "ReferenceError"
let y = 1;
```

> **Contrasts**
> - **Python**: one declaration form; names are rebindable; scoping is block‑like (but `for` introduces its own semantics); no hoisting.  
> - **C++**: `auto`, explicit types; strict block scope; redefinition in the same scope is an error; no hoisting; `const` is deep (attempts to mutate cause compile‑time errors, modulo `mutable`/`const_cast`).

---

## 2) Types & `typeof`
Primitive types: `number`, `string`, `boolean`, `undefined`, `symbol`, `bigint`, and the special `null` (where `typeof null === "object"` is a historical quirk). Objects (arrays, functions, dates, etc.) are of type `"object"` (functions return `"function"`).

```js
let num = 42;
let text = "Hello";
let flag = true;
let nothing = null;
let notDefined;
let big = 10n;            // BigInt
let sym = Symbol("id");

console.log(typeof num);        // "number"
console.log(typeof text);       // "string"
console.log(typeof flag);       // "boolean"
console.log(typeof nothing);    // "object"  ← historical quirk
console.log(typeof notDefined); // "undefined"
console.log(typeof big);        // "bigint"
console.log(typeof sym);        // "symbol"
```

> **Contrasts**
> - **Python**: unlimited‑precision `int`, separate `float`, `bool`, `None`; `type(None)` distinct; dynamic duck typing.  
> - **C++**: static primitive types (`int`, `double`, `bool`, etc.); sizes/behaviour implementation‑dependent; `nullptr` for null pointers.

---

## 3) Numbers & arithmetic
JS uses IEEE‑754 **double precision** for `number` (integers and floats share one type). Use `BigInt` for huge integers; mixing `number` and `bigint` in the same operation is not allowed.

```js
let x = 10, y = 3;
console.log(x + y);   // 13
console.log(x - y);   // 7
console.log(x * y);   // 30
console.log(x / y);   // 3.333...
console.log(x % y);   // 1
console.log(x ** y);  // 1000

// Floating-point caveat:
console.log(0.1 + 0.2);       // 0.30000000000000004
console.log(Number.isInteger(3.0)); // true

// BigInt for exact big integer arithmetic:
console.log(2n ** 63n);       // 9223372036854775808n
// 1n + 1   // ❌ TypeError (cannot mix BigInt and Number)
```

> **Contrasts**
> - **Python**: `int` is arbitrary precision; `Decimal` for exact decimals; `/` is float division, `//` floor division.  
> - **C++**: distinct integer and floating types; integer division truncates; fixed widths and potential overflows; `long double` etc.

---

## 4) Equality, comparison & truthiness
Prefer **strict equality** `===`/`!==` to avoid implicit coercions.

```js
console.log(5 == "5");   // true  (loose equality with coercion)
console.log(5 === "5");  // false (strict equality)

console.log(null == undefined);   // true
console.log(null === undefined);  // false

// Truthiness
console.log(Boolean(""));     // false
console.log(Boolean(" "));    // true
console.log(Boolean(0));      // false
console.log(Boolean(NaN));    // false
console.log(Boolean([]));     // true (empty array is truthy)
console.log(Boolean({}));     // true
```

> **Contrasts**
> - **Python**: `==` value equality, `is` identity; empty containers are falsy; `None == 0` is `False`; no implicit string↔number coercion.  
> - **C++**: `==` compares values (or pointers); no automatic string↔number coercion; boolean contexts rely on implicit conversion operators.

---

## 5) Strings
Strings are immutable sequences of UTF‑16 code units. Template literals allow interpolation and multi‑line strings.

```js
let s = "JavaScript";
console.log(s.length);         // 10
console.log(s.toUpperCase());  // "JAVASCRIPT"
console.log(s.includes("Script")); // true

// Template literals
let who = "world";
console.log(`Hello, ${who}!`); // "Hello, world!"
```

> **Contrasts**
> - **Python**: immutable Unicode strings; f‑strings for interpolation.  
> - **C++**: `std::string` mutable; no built‑in interpolation (use streams/`fmt`).

---

## 6) Arrays (dynamic lists)
Arrays are objects with numeric indices; common methods: `push`, `pop`, `shift`, `unshift`, `slice`, `splice`, `map`, `filter`, `reduce`.

```js
let arr = [1, 2, 3];
arr.push(4);           // [1,2,3,4]
arr.pop();             // [1,2,3]
arr[0] = 99;           // [99,2,3]
console.log(arr.map(x => x * 2)); // [198,4,6]
```

> **Contrasts**
> - **Python**: `list` with rich slicing; list comprehensions.  
> - **C++**: `std::vector` (contiguous), `std::array` (fixed size), algorithms in `<algorithm>`; no first‑class higher‑order methods (use ranges/library).

---

## 7) Objects (records/dictionaries)
Plain objects are key–value maps; properties can be added/removed dynamically.

```js
let person = { name: "Alice", age: 25 };
console.log(person.name);        // "Alice"
person.age = 26;
person.city = "London";
console.log(Object.keys(person)); // ["name","age","city"]
```

> **Contrasts**
> - **Python**: `dict`; ordered insertion since 3.7.  
> - **C++**: `std::map`/`unordered_map`; types fixed at compile time; cannot add arbitrary fields to a `struct` instance at runtime.

---

## 8) Functions & arrows
Function declarations are hoisted; arrow functions capture `this` lexically and are concise.

```js
// Declaration (hoisted)
function greet(name) {
  return "Hello, " + name;
}
console.log(greet("Bob")); // "Hello, Bob"

// Arrow function
const square = n => n * n;
console.log(square(5)); // 25

// 'this' behaviour: arrows do NOT rebind 'this'
const obj = {
  x: 42,
  regular() { return function(){ return this.x; }; },
  arrow()   { return () => this.x; }
};
const r = obj.regular();
const a = obj.arrow();
console.log(r()); // undefined or window.x in sloppy mode
console.log(a()); // 42 (lexically captured 'this')
```

> **Contrasts**
> - **Python**: `def` defines functions; `lambda` for expressions; `self` is explicit in methods.  
> - **C++**: free functions and member functions; lambdas with capture lists; explicit `this` pointer in class methods.

---

## 9) Control flow
```js
let score = 80;
if (score >= 90)       console.log("A");
else if (score >= 70)  console.log("B");  // "B"
else                   console.log("C");

for (let i = 1; i <= 3; i++) console.log(i); // 1,2,3

let n = 0;
while (n < 3) { console.log(n); n++; }
```

> **Contrasts**
> - **Python**: indentation‑based blocks; `for ... in ...` over iterables; `range`.  
> - **C++**: braces for blocks; classic `for(;;)` and range‑for (`for(auto& v: vec)`).

---

## 10) Errors & exceptions
```js
try {
  JSON.parse("{bad json}");
} catch (e) {
  console.log(e.name); // "SyntaxError"
} finally {
  console.log("Always runs");
}
```

> **Contrasts**
> - **Python**: `try/except/finally`; rich exception hierarchy.  
> - **C++**: exceptions are optional in practice; many libraries prefer error codes/`std::expected` patterns.

---

## 11) Modules (ES Modules in browsers)
Modern browsers support `<script type="module">` and `import`/`export`. In the console, you can use dynamic `import()` to load modules from URLs (subject to CORS).

```js
// Dynamic import (demo; needs a valid URL and CORS allowance):
// const lib = await import('https://example.com/path/to/module.js');
// console.log(lib.someExport);
```

> **Contrasts**
> - **Python**: `import` system with modules/packages; virtual environments (`venv`).  
> - **C++**: headers/libraries; C++20 modules (toolchain support varies).

---

## 12) DOM touchpoint (browser‑specific)
Since you are in the Web Console, you can interact with the document:

```js
document.title;                    // read title
document.querySelectorAll("a").length; // count links
const el = document.createElement("div");
el.textContent = "Hello DOM";
document.body.appendChild(el);
```

> **Contrasts**
> - **Python / C++**: No DOM in standard environments; need bindings/frameworks (e.g., PyQt, WebKit, CEF).

---

## 13) Quick self‑check (copy‑paste and predict outputs)
```js
// 1) What logs?
let p = [];
console.log(Boolean(p), p.length); // ?

// 2) Equality?
console.log(0 == false, 0 === false); // ?, ?

// 3) Hoisting?
try { d++; } catch (e) { console.log("err"); }
var d = 1;
console.log(d); // ?

// 4) BigInt?
try { console.log(1n + 1); } catch (e) { console.log(e.name); } // ?

// 5) this-binding?
const ctx = { v: 7, f: () => this.v, g(){ return this.v; } };
console.log(ctx.f(), ctx.g()); // ?, ?
```

**Expected insights (no spoilers):**  
1) Empty arrays are **truthy**; length is 0. 2) `0 == false` is `true`, `0 === false` is `false`. 3) `var` is hoisted (read is `undefined` before init, increment throws earlier); final `d` is 1. 4) Mixing `BigInt` and `Number` throws `TypeError`. 5) Arrow keeps outer `this` (likely `undefined`/`window`), method `g` binds to `ctx` → `7`.

---

## 14) Good practice checklist
- Prefer `const` and `let`; avoid `var`.  
- Prefer strict equality `===`/`!==`.  
- Beware floating‑point rounding; use `BigInt`/`Decimal` libraries when needed.  
- Treat objects as mutable references; copy with structuredClone or spread.  
- Keep browser vs server contexts distinct (DOM vs Node.js APIs).

---

### Appendix: Copy‑ready “lab block”
Paste this whole block once, then scroll the console to observe outputs in order.
```js
// LAB BLOCK — quick tour
(function(){
  console.log("== Declarations ==");
  var a = 1; let b = 2; const c = 3;
  console.log(a,b,c);
  try { let b = 9; } catch(e){ console.log("shadowing ok in new block"); }
  console.log("== Types ==");
  console.log(typeof 42, typeof "x", typeof true, typeof null, typeof 10n);
  console.log("== Numbers ==");
  console.log(0.1 + 0.2, 2n ** 10n);
  console.log("== Equality ==");
  console.log(5 == "5", 5 === "5");
  console.log("== Arrays ==");
  let arr = [1,2,3]; console.log(arr.map(x=>x*2));
  console.log("== Objects ==");
  let o = {x:1}; o.y=2; console.log(Object.keys(o));
  console.log("== Functions ==");
  function f(n){return n*n} const g=n=>n*n; console.log(f(4), g(4));
  console.log("== Control ==");
  for (let i=0;i<3;i++) console.log(i);
  console.log("== DOM ==");
  const el=document.createElement("div"); el.textContent="Lab OK"; document.body.appendChild(el);
})();
```
