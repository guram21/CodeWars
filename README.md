# CodeWars
#### Multiply
```javascript
function multiply(a, b) {
  return a * b;
}
```
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
#### I love you, a little , a lot, passionately ... not at all
````javascript
function howMuchILoveYou(n) {
  const fl = ['I love you', 'a little', 'a lot', 'passionately', 'madly', 'not at all'];
  return fl[(n - 1) % 6]
}
````
#### Complementary DNA
````javascript
function DNAStrand(dna){
  let r = '';
  
  for (let i = 0; i < dna.length; i++){
    if(dna[i] === 'A') r += 'T';
    if(dna[i] === 'T') r += 'A';
    if(dna[i] === 'G') r += 'C';
    if(dna[i] === 'C') r += 'G';
  }
  
  return r;
}
````