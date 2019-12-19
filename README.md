# CodeWars
#### Multiply
```javascript
const multiply = (a, b) => a * b;
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
#### Count of positives / sum of negatives
````javascript
function countPositivesSumNegatives(arr) {
if(arr === null || arr.length === 0) return [];
  
  let countPos = 0, summNeg = 0;
  
  for (let i = 0; i < arr.length; i++){
  if(arr[i] > 0){
  countPos++;
  }else{
  summNeg += arr[i];
}
}
  return [countPos, summNeg];
}
````
#### Sum of differences in array
````javascript
function sumOfDifferences(arr) {
  const sorted = arr.sort((a, b) => b - a);
  let summ = 0;

  for(let i = 0; i < sorted.length - 1; i++){
    summ += sorted[i] - sorted[i + 1];
  }
  
  return summ;
  
}
````
#### Generate range of integers
````javascript
function generateRange(min, max, step){
  const arr = [];
  for (let i = min; i <= max; i += step){
    arr.push(i);
  }
  return arr;
}
````
#### Keep Hydrated!
```javascript
const litres = time => Math.floor(time * 0.5);
```
#### Convert boolean values to strings 'Yes' or 'No'
````javascript
const boolToWord = bool => bool ? 'Yes' : 'No';
````
