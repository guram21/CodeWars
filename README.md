# solvedTasks
#### Draw stairs
```javascript
function drawStairs(n) {
   
     let s = '';
   
     for (let i = 1; i <= n; i++) {
       s += i === n ? 'I' : 'I\n' + ' '.repeat(i)
     }
   
     console.log(s);
     return s;
   }
```
#### A wolf in sheep's clothing
```javascript
function warnTheSheep(q) {
    const l = q.length, w = q.indexOf('wolf');
  return l === w + 1
    ? 'Pls go away and stop eating my sheep'
    : `Oi! Sheep number ${l - 1 - w}! You are about to be eaten by a wolf!`  
}
```
