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
  return s;
}
```
#### A wolf in sheep's clothing
```javascript
function warnTheSheep(q) {
  const l = q.length,
    w = q.indexOf('wolf');
  return l === w + 1 ? 'Pls go away and stop eating my sheep' : `Oi! Sheep number ${l - 1 - w}! You are about to be eaten by a wolf!`
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
function DNAStrand(dna) {
  let r = '';
  for (let i = 0; i < dna.length; i++) {
    if (dna[i] === 'A') r += 'T';
    if (dna[i] === 'T') r += 'A';
    if (dna[i] === 'G') r += 'C';
    if (dna[i] === 'C') r += 'G';
  }
  return r;
}
````
#### Count of positives / sum of negatives
````javascript
function countPositivesSumNegatives(arr) {
  if (arr === null || arr.length === 0) return [];
  let countPos = 0,
    summNeg = 0;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > 0) {
      countPos++;
    } else {
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
  for (let i = 0; i < sorted.length - 1; i++) {
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
#### Training JS #1: create your first JS function and print "Helloworld!"
````javascript
function helloWorld() {
  var str = 'Hello World!';
  console.log(str);
  return str;
}
````
#### Function 1 - hello world
```javascript
const greet = () => 'hello world!';
```
#### Beginner Series #2 Clock
```javascript
const past = (h, m, s) => (h * 3600 + m * 60 + s) * 1000;
```
#### Third Angle of a Triangle
````javascript
const otherAngle = (a, b) => 180 - (a + b);
````
#### Sum of angles
````javascript
const angle = n => 180 * (n - 2);
````
#### Breaking chocolate problem
````javascript
const breakChocolate = (n,m) => n * m > 0 ? n * m - 1 : 0;
````
#### For Twins: 2. Math operations
```javascript
const iceBrickVolume = (radius, bottleLength, rimLength) => 2 * radius ** 2 * (bottleLength - rimLength);
```
#### Simple multiplication
```javascript
var simpleMultiplication = number => number * (8 + number % 2)

var simpleMultiplication = number => number * (8 + (number & 1));

var simpleMultiplication = number => number * (number % 2 ? 9 : 8);

var simpleMultiplication = number => number * (8 + (number % 2 != 0));

var simpleMultiplication = number => number % 2 ? number * 9 : number * 8;

var simpleMultiplication = number => (number << 3) + (number & 1) * number;

var simpleMultiplication = number => !(number % 2) ? number * 8 : number * 9;
```
#### DNA to RNA Conversion
```javascript
const DNAtoRNA = dna => dna.replace(/T/g, 'U');
```
#### Convert boolean values to strings 'Yes' or 'No'
````javascript
const boolToWord = bool => bool ? 'Yes' : 'No';
````
#### Super Duper Easy
```javascript
const problem = x => x === +x ? x * 50 + 6 : 'Error';
```
#### Chuck Norris VII - True or False? (Beginner)
````javascript
const ifChuckSaysSo = () => !true;
````
#### Type of sum
````javascript
const typeOfSum = (a, b) => typeof (a + b);
````
#### Convert a Number to a String!
````javascript
const numberToString = (num) => String(num);
````
#### Convert a Boolean to a String
```javascript
var booleanToString = String;

var booleanToString = b => String;

var booleanToString = b => String(b);

var booleanToString = b => ( b === true) ? "true" : "false";

var booleanToString = b => ( b === false) ? "false" : "true";

var booleanToString = b => b ? 'true' : 'false';

var booleanToString = b => b ? 'false' : 'true';

var booleanToString = b => b + '';

var booleanToString = b => '' + b;

var booleanToString = b => Boolean(b) + '';

var booleanToString = b => '' + Boolean(b);

var booleanToString = b => b.toString();

var booleanToString = b => `${b}`;
```
#### Sum The Strings
````javascript
const sumStr = (a, b) => String(+a + +b);
````
#### Discover The Original Price
````javascript
var discoverOriginalPrice = (discountedPrice, salePercentage) => +(discountedPrice * 100 / (100 - salePercentage)).toFixed(2);

var discoverOriginalPrice = (discountedPrice, salePercentage) => +(discountedPrice / (1 - salePercentage / 100)).toFixed(2);
````
#### Formatting decimal places #0
```javascript
const twoDecimalPlaces = n => +n.toFixed(2);
```
#### How many times should I go?
```javascript
const howManyTimes = (annualPrice, individualPrice) => Math.ceil(annualPrice / individualPrice);
```
#### Return the closest number multiple of 10
```javascript
const closestMultiple10 = num => Math.round(num / 10) * 10;
```
