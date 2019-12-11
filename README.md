# solvedTasks
#### Draw stairs
```javascript
let user; 
user = 'Guram';
```function drawStairs(n) {
   
     let s = '';
   
     for (let i = 1; i <= n; i++) {
       s += i === n ? 'I' : 'I\n' + ' '.repeat(i)
     }
   
     console.log(s);
     return s;
   }
const sevenStepStairs = drawStairs(7);