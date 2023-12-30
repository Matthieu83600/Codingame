## Solution

```Javascript
/**
 * Auto-generated code below aims at helping you parse
 * the standard input according to the problem statement.
 **/

const n = parseInt(readline()); // the number of temperatures to analyse
var inputs = readline().split(' ');
let result = inputs[0] || 0;
for (let i = 0; i < inputs.length; i++) {
    const t = parseInt(inputs[i]); // a temperature expressed as an integer ranging from -273 to 5526
    if (t**2 < result**2 || (t**2 === result**2 && t > result)) {
        result = t;
    }
}

// Write an answer using console.log()
// To debug: console.error('Debug messages...');

console.log(result);
```