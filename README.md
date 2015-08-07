# Školení JS+DOM

## ~~JavaScript~~ ECMAScript 6

### Základní syntax
- podobá se Javě, C (...)
- Unicode
- case sensitive
- instrukce programu se nazývají výrazy (expression)

Výraz:
```js
expression;
```

Komentáře:
```js
// comment
/* 
	multiline
	comment
*/
```

Blok:
```js
if(condition) {
	// obsah bloku
}
```

Funkce:
```js
function example(argument, argument2) {
	// blok funkce
}
```

### Proměnné

#### Deklarace:
- klíčová slova: var, let, const

```js
var variable = value;
```

#### Obor působnosti - Variable scope:
```js
globalScope = smth;
var functionScope = smth;
let blockScope = smth;
const blockScope = 123;
```

### Datové typy
- dynamický jazyk = proměnné nemají pevně stanovený datový typ

#### Primitivní:

- boolean `true`, `false`
- null
- undefined
- number `123`, `10.05`
- string `'řetězec'`, `"druhý řetězec"`
- symbol `var id = Symbol()`

Proměnná je přímo daná hodnota...  

#### Referenční:

- Object `obj = { property: value, prop2: val2 }`
- function `function name(arguments) { body }`

Hodnota proměnné je odkaz do paměti na daný objekt...

#### Programové konstrukce

##### pole
```js
var array = [1, 2, 3, 4, 5];
var arrayOfArrays = [
	[ 1, 2, 3, 4, 5 ],
	[ 'cos', 'to', 'Honzo', 'cos', 'to', 'sněd' ],
	[ ]
];
// Přístup k hodnotě 
array[index];
arrayOfArrays[index][index2];
```

##### objekty
```js
var object = { jedna: 1, dve: 2, tri: 3 };
// Přístup k hodnotě
object.jedna;
object['dve'];
```

##### podmínky
```js
if (condition) { 
	// ...
}

if (...) { ... }
else { ... }

if (...) { ... }
else if (...) { ... }
```
Hodnoty vyhodnocené jako `false`: `undefined, null, 0, NaN, ""`

Porovnávací operátory:
- ekvivalence `==`
- neekvivalence `!=`
- striktní rovnost `===`
- striktní nerovnost `!==`
- větší než, menší než `>`, `<`
- větší anebo rovno, menší anebo rovno `>=`, `<=`

Logické operátory:
- NOT (negace) `!`
- OR (nebo) `one || two`
- AND (a zároveň) `one && two`

##### iterace a smyčky

```js
// Iterace
for ([initialExpression]; [condition]; [incrementExpression])
  statement

for (variable in object) {
  statements
}

// Cyklus 
do
  statement
while (condition);

while (condition)
  statement
```

##### funkce

```js
function add(first, second) {
	return first + second;
}

var result = add(1, 1);

// Arrow functions
var sum = (first, second) => first + second;

var result2 = sum(1, 2);
```