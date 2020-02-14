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
  const str = 'Hello World!';
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
const simpleMultiplication = number => number * (8 + number % 2)

const simpleMultiplication = number => number * (8 + (number & 1));

const simpleMultiplication = number => number * (number % 2 ? 9 : 8);

const simpleMultiplication = number => number * (8 + (number % 2 != 0));

const simpleMultiplication = number => number % 2 ? number * 9 : number * 8;

const simpleMultiplication = number => (number << 3) + (number & 1) * number;

const simpleMultiplication = number => !(number % 2) ? number * 8 : number * 9;
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
const booleanToString = String;

const booleanToString = b => String;

const booleanToString = b => String(b);

const booleanToString = b => ( b === true) ? "true" : "false";

const booleanToString = b => ( b === false) ? "false" : "true";

const booleanToString = b => b ? 'true' : 'false';

const booleanToString = b => b ? 'false' : 'true';

const booleanToString = b => b + '';

const booleanToString = b => '' + b;

const booleanToString = b => Boolean(b) + '';

const booleanToString = b => '' + Boolean(b);

const booleanToString = b => b.toString();

const booleanToString = b => `${b}`;
```
#### Sum The Strings
````javascript
const sumStr = (a, b) => String(+a + +b);
````
#### Discover The Original Price
````javascript
const discoverOriginalPrice = (discountedPrice, salePercentage) => +(discountedPrice * 100 / (100 - salePercentage)).toFixed(2);

const discoverOriginalPrice = (discountedPrice, salePercentage) => +(discountedPrice / (1 - salePercentage / 100)).toFixed(2);
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
#### Count Odd Numbers below n
```javascript
const oddCount = n => Math.floor(n / 2);
```
#### Century From Year
```javascript
const century = year => Math.ceil(year / 100);
```
#### Area of a Square
```javascript
const squareArea = A => +Math.pow((2 * A / Math.PI), 2).toFixed(2);

const squareArea = A => +((2 * A / Math.PI) ** 2).toFixed(2);
```
#### Keep up the hoop
```javascript
const hoopCount = n => n >= 10 ? 'Great, now move on to tricks': 'Keep at it until you get it';
```
#### Simple Comparison?
```javascript
const add = (a, b) => a == b;

const add = (a, b) => +a == +b;

const add = (a, b) => +a - +b == 0;

const add = (a, b) => eval(a - b) == 0;

const add = (a, b) => a + "" == b + "";

const add = (a, b) => (`${a}`) == (`${b}`); 
```
#### Is he gonna survive?
```javascript
const hero = (bullets, dragons) => bullets >= dragons * 2;

const hero = (bullets, dragons) => dragons * 2 <= bullets;

const hero = (bullets, dragons) => bullets / dragons >= 2;

const hero = (bullets, dragons) => bullets >> 1 >= dragons;
```
#### Even or Odd
```javascript
const even_or_odd = number =>  number % 2 ? 'Odd' : 'Even';

const even_or_odd = number =>  number & 1 ? 'Odd' : 'Even';

const even_or_odd = number => !(number % 2) ? 'Even' : 'Odd';

const even_or_odd = number => Math.abs(number) % 2 ? "Odd" : "Even";

const even_or_odd = number => ['Even', 'Odd'][number % 2];

const even_or_odd = number => ['Even', 'Odd'][number & 1];

const even_or_odd = number => ['Even', 'Odd'][!(number % 2)];

const even_or_odd = number => ["Even", "Odd"][Math.abs(number) % 2];
```
#### Calculate BMI
```javascript
function bmi(weight, height) {
  let bmi = weight / height ** 2;
  if (bmi <= 18.5) return 'Underweight';
  if (bmi <= 25.0) return 'Normal';
  if (bmi <= 30.0) return 'Overweight';
  if (bmi > 30) return 'Obese';
}

const bmi = (weight, height) => (weight = weight / height / height) > 30 ? 'Obese' : weight > 25 ? 'Overweight' : weight > 18.5 ? 'Normal' : 'Underweight';

const bmi = (weight, height, bmi = weight / height ** 2) => bmi <= 18.5 ? "Underweight" :
                                                            bmi <= 25 ? "Normal" :
                                                            bmi <= 30 ? "Overweight" : "Obese";
```
#### What's the real floor?
```javascript
const getRealFloor = n => n <= 0 ? n : n < 13 ? n - 1 : n - 2;

const getRealFloor = n => n <= 0 ? n : n - (n >= 13 ? 2 : 1);
```
#### Determine offspring sex based on genes XX and XY chromosomes
```javascript
const chromosomeCheck = sperm => sperm == 'XY' 
? "Congratulations! You're going to have a son."
: "Congratulations! You're going to have a daughter.";

const chromosomeCheck = sperm => sperm.indexOf('Y') >= 0
? "Congratulations! You're going to have a son."
: "Congratulations! You're going to have a daughter.";

const chromosomeCheck = sperm => sperm.includes("Y")
? "Congratulations! You're going to have a son."
: "Congratulations! You're going to have a daughter.";

const chromosomeCheck = sperm => sperm.match(/[Y]/gi) 
? "Congratulations! You're going to have a son." 
: "Congratulations! You're going to have a daughter.";

const chromosomeCheck = sperm => {
  let kid = sperm.includes('Y') ? 'son' : 'daughter'
  return `Congratulations! You're going to have a ${kid}.`
}

const chromosomeCheck = sperm => `Congratulations! You're going to have a ${sperm.endsWith('X') ? 'daughter' : 'son'}.`;

const chromosomeCheck = sperm => "Congratulations! You're going to have a " + (~sperm.indexOf('Y')? "son." : "daughter.");

const chromosomeCheck = sperm => `Congratulations! You're going to have a ${sperm === 'XY' ? 'son' : 'daughter'}.`;

const chromosomeCheck = sperm => "Congratulations! You're going to have a " + (sperm === 'XY' ? 'son' : 'daughter') + '.';

const chromosomeCheck = sperm => `Congratulations! You\'re going to have a ${sperm.includes('Y') ? 'son' : 'daughter'}.`;

function chromosomeCheck(sperm) {
  const son = 'Congratulations! You\'re going to have a son.';
  const daughter = 'Congratulations! You\'re going to have a daughter.'
  
  return sperm.includes('Y') ? son: daughter; 
}

function chromosomeCheck(sperm) {
  const text = a => `Congratulations! You're going to have a ${a}.`
  return sperm.search('Y') === -1 ? text('daughter') : text('son');
}
```
