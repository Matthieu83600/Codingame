## Solution

```Javascript
/**
 * Auto-generated code below aims at helping you parse
 * the standard input according to the problem statement.
 * ---
 * Hint: You can use the debug stream to print initialTX and initialTY, if Thor seems not follow your orders.
 **/

var inputs = readline().split(' ');
const lightX = parseInt(inputs[0]); // the X position of the light of power
const lightY = parseInt(inputs[1]); // the Y position of the light of power
let initialTx = parseInt(inputs[2]); // Thor's starting X position
let initialTy = parseInt(inputs[3]); // Thor's starting Y position

// game loop
while (true) {
    const remainingTurns = parseInt(readline()); // The remaining amount of turns Thor can move. Do not remove this line.
    
    let move = "";

    if (lightY == initialTy) {
        if (lightX > initialTx) {
            move = "E";
            initialTx++;
        } else {
            move = "W";
            initialTx--;
        }
    } else if (lightX == initialTx) {
        if (lightY > initialTy) {
            move = "S";
            initialTy++;
        } else {
            move = "N";
            initialTy--;
        }
    } else if (lightY > initialTy) {
        if (lightX > initialTx) {
            move = "SE";
            initialTx++;
            initialTy++;
        } else {
            move = "SW";
            initialTx--;
            initialTy++;
        }
    } else if (lightX > initialTx) {
        if (lightY > initialTy) {
            move = "NE";
            initialTx++;
            initialTy--;
        } else {
            move = "NW";
            initialTx--;
            initialTy--;
        }
    }
    console.log(move);
}
```