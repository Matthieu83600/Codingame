## Solution

```Javascript
/**
 * Auto-generated code below aims at helping you parse
 * the standard input according to the problem statement.
 **/

const N = parseInt(readline());
// stocker les chevaux
const horses = [];
for (let i = 0; i < N; i++) {
    const pi = parseInt(readline());
    // envoi des puissances des chevaux dans le tableau
    horses.push(pi);
}

// tri des chevaux
sortedHorses = horses.sort((a,b) => a-b);

const diffPowerHorses = horses
                            // verifie la différence entre la valeur courante et la valeur précédente
                            .map((current, index, array) => current - array[index-1])
                            // enlève 1ere valeur
                            .slice(1)
                            // tri de la différence de puissance
                            .sort((a,b) => a-b);
console.error(diffPowerHorses);
// Write an answer using console.log()
// To debug: console.error('Debug messages...');

console.log(diffPowerHorses[0]);
```