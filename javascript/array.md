## Arrays
```javascript
l = [a, b, c]
copy = l.slice()      // clone array
```

#### Create
```javascript
l.splice(1, 0, X);                  // add item at specific index   -> [_, X, _, _]
l.splice(1, 0, X, Y);               // add items at specific index  -> [_, X, Y, _, _]
l.splice(l.indexOf(REF), 0, X);    	// add item before REF          -> [_, X, REF, _, _]
l.splice(l.indexOf(REF) + 1, 0, X);	// add item after REF           -> [_, REF, X, _, _]
l.unshift(X);                       // add item to beginning        -> [X, _, _, _]
l.unshift(X, Y);                    // add items to beginning       -> [X, Y, _, _, _]
l.push(X);                          // add item to end              -> [_, _, _, X]
l.push(X, Y);                       // add items to end             -> [_, _, _, X, Y]
```

#### Get
```javascript
l[1]            // get by index   -> b
l.indexOf(b)    // get index      -> 0
```

#### Update
```javascript
l[1] = X            // replace at index     -> [a, X, c]
l.map(() => X)      // replace all          -> [X, X, X]
```

#### Remove
```javascript
l[1] = X                // replace at index     -> [a, X, c]
l.map(() => X)          // replace all          -> [X, X, X]
l.pop()                 // -> c     l == [a, b]
l.shift()               // -> a     l == [b, c]
l.splice(1, 1)          // -> b     l == [a, c]
l.filter((e) => e != b)     // -> [a, c]
```

#### Set Theory
```javascript
arrA.filter(x => arrB.includes(x))  // intersection
arrA.filter(x => !arrB.includes(x)) // difference
arrA.filter(x => !arrB.includes(x)).concat(arrB.filter(x => !arrA.includes(x))) // symmetrical difference
[...arrA, ...arrB]              // union with duplicates
[...new Set([...arrA, ...arrB)] // union without duplicates
```

#### Sort
```javascript
l.sort((a,b) => a-b)     // sort ascending
l.sort((a,b) => b-a)     // sort descending
```

#### Iterables
```javascript
.find(n => ...)  // es6
.findIndex(...)  // es6

.every(n => ...)    // -> boolean
.some(n => ..)      //  -> boolean

.filter(n => ...)
.map(n => ...)
.reduce((total, n) => total)
.reduceRight(...)
```