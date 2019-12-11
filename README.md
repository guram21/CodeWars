# solvedTasks
#### Draw stairs
given a number n, draw stairs with 'I' n tall and n wide, with the tallest in the top left. 
Example (with - to represent spaces; DO NOT USE THEM IN THE SOLUTIONS! USE SPACES IN SOLUTION! 
the "-"s are for clarity.): draw_stairs(3) == '''I\n_I\n__I'''
```javascript
function drawStairs(n) {
   
     let s = '';
   
     for (let i = 1; i <= n; i++) {
       s += i === n ? 'I' : 'I\n' + ' '.repeat(i)
     }
   
     console.log(s);
     return s;
   }
const sevenStepStairs = drawStairs(7);
```