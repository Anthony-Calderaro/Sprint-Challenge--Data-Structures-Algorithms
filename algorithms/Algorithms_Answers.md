Add your answers to the Algorithms exercises here.

Exercise (1)
(a) o(1)
(b) o(n)
(c) o(n)
(d) o(n^2)
(e) o(n^3)
(f) o(1)
(g) o(n)

Exercise (2)
(a) 
Step 1: Make a function that sorts the array numerically.
Step 2: Return the value of the last index less the zero-th index

const n = [1, 2, 3, 4, 5];
function maxDiff (n) {
    n.sort();
    return n[n.length - 1] - n[0];
}

(b)
Step 1: Start at floor n. Drop egg function.
Step 2: If Egg breaks, go down 1 floor, set breakfloor to n. If it stays safe, set the safeFloor to n, then go up 1 floor.
Step 3: Repeat until safe floor is exactly 1 below break floor, then return the safefloor.

let safeFloor = 0;
let breakFloor = 0;

function (n) {
    if (breakEggFunction(n) === 'break') {
        let breakFloor = n; 
        breakEggFunction(breakFloor - 1);
    } 
    if (breakEggFunction(n) === 'safe') {
        let safeFloor = n;
        breakEggFunction(safeFloor + 1);
    }
    if (safeFloor = breakFloor -1) return safeFloor;
}

Exercise (3)
(a) o(n^2) - because the runtime runs the same operation over the entire length of the array, and has to hit each index.
(b) o(n) - because the runtime splits the array into fewer operations by moving the pivot to the middle.  