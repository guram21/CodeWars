# CodeWars
#### [Multiply](https://www.codewars.com/kata//50654ddff44f800200000004)
```javascript
const multiply = (a, b) => a * b;
```
#### [Draw stairs](https://www.codewars.com/kata//5b4e779c578c6a898e0005c5)
```javascript
// Solution 1
const drawStairs = n => {
  let res = '';
  for (let i = 1; i <= n; i++) {
    res += i === n ? 'I' : 'I\n' + ' '.repeat(i);
  }
  return res;
};
// Solution 2
const drawStairs = n => {
  let stairs = '',
    space = ' ';
  for (let i = 0; i < n - 1; i++) {
    stairs += 'I\n' + space;
    space += ' ';
  }
  return stairs + 'I';
};
// Solution 3
const drawStairs = n =>
  [...Array(n)].map((_, i) => ' '.repeat(i) + 'I').join('\n');
```
#### [A wolf in sheep's clothing](https://www.codewars.com/kata//5c8bfa44b9d1192e1ebd3d15)
```javascript
const warnTheSheep = q => {
  const l = q.length,
    w = q.indexOf('wolf');
  return l === w + 1
    ? 'Pls go away and stop eating my sheep'
    : `Oi! Sheep number ${l - 1 - w}! You are about to be eaten by a wolf!`;
};
```
#### [I love you, a little, a lot, passionately ... not at all](https://www.codewars.com/kata//57f24e6a18e9fad8eb000296)
```javascript
const howMuchILoveYou = n => {
  const fl = [
    'I love you',
    'a little',
    'a lot',
    'passionately',
    'madly',
    'not at all'
  ];
  return fl[(n - 1) % 6];
};
```
#### [Complementary DNA](https://www.codewars.com/kata//554e4a2f232cdd87d9000038)
```javascript
// Solution 1
const DNAStrand = dna => {
  let r = '';
  for (let i = 0; i < dna.length; i++) {
    if (dna[i] === 'A') r += 'T';
    if (dna[i] === 'T') r += 'A';
    if (dna[i] === 'G') r += 'C';
    if (dna[i] === 'C') r += 'G';
  }
  return r;
};
// Solution 2
const pairs = { A: 'T', T: 'A', C: 'G', G: 'C' };
const DNAStrand = dna => dna.replace(/./g, c => pairs[c]);
// Solution 3
const DNAStrand = dna => {
  return dna.replace(/./g, function(c) {
    return DNAStrand.pairs[c];
  });
};

DNAStrand.pairs = {
  A: 'T',
  T: 'A',
  C: 'G',
  G: 'C'
};
```
#### [Count of positives / sum of negatives](https://www.codewars.com/kata//576bb71bbbcf0951d5000044)
```javascript
// Solution 1
const countPositivesSumNegatives = arr => {
  if (!arr || !arr.length) return [];
  let count = 0,
    sum = 0;
  for (let i = 0; i < arr.length; i++) {
    arr[i] > 0 ? count++ : sum += arr[i];
  }
  return [count, sum];
};
// Solution 2
const countPositivesSumNegatives = arr => {
  return arr !== null && arr.length > 0
    ? [
      arr.filter(el => el > 0).length,
      arr.filter(el => el < 0).reduce((a, b) => a + b, 0),
    ]
    : [];
};
```
#### [Sum of differences in array](https://www.codewars.com/kata//5b73fe9fb3d9776fbf00009e)
```javascript
// Solution 1
const sumOfDifferences = arr =>
  arr.length > 1 ? Math.max(...arr) - Math.min(...arr) : 0;
// Solution 2
const sumOfDifferences = arr => {
  const sorted = arr.sort((a, b) => b - a);
  let sum = 0;
  for (let i = 0; i < sorted.length - 1; i++) {
    sum += sorted[i] - sorted[i + 1];
  }
  return sum;
};
```
#### [Generate range of integers](https://www.codewars.com/kata//55eca815d0d20962e1000106)
```javascript
const generateRange = (min, max, step) => {
  const arr = [];
  for (let i = min; i <= max; i += step) {
    arr.push(i);
  }
  return arr;
};
```
#### [Keep Hydrated!](https://www.codewars.com/kata//582cb0224e56e068d800003c)
```javascript
const litres = time => Math.floor(time * 0.5);
```
#### [Training JS #1: create your first JS function and print "Helloworld!"](https://www.codewars.com/kata//571ec274b1c8d4a61c0000c8)
```javascript
function helloWorld() {
  const str = 'Hello World!';
  console.log(str);
  return str;
}
```
#### [Function 1 - hello world](https://www.codewars.com/kata//523b4ff7adca849afe000035)
```javascript
const greet = () => 'hello world!';
```
#### [Beginner Series #2 Clock](https://www.codewars.com/kata//55f9bca8ecaa9eac7100004a)
```javascript
const past = (h, m, s) => (h * 3600 + m * 60 + s) * 1000;
```
#### [Third Angle of a Triangle](https://www.codewars.com/kata//5a023c426975981341000014)
```javascript
const otherAngle = (a, b) => 180 - (a + b);
```
#### [Sum of angles](https://www.codewars.com/kata//5a03b3f6a1c9040084001765)
```javascript
const angle = n => 180 * (n - 2);
```
#### [Breaking chocolate problem](https://www.codewars.com/kata//534ea96ebb17181947000ada)
```javascript
const breakChocolate = (n, m) => (n * m > 0 ? n * m - 1 : 0);
```
#### [For Twins: 2. Math operations](https://www.codewars.com/kata//59c287b16bddd291c700009a)
```javascript
const iceBrickVolume = (radius, bottleLength, rimLength) =>
  2 * radius ** 2 * (bottleLength - rimLength);
```
#### [Simple multiplication](https://www.codewars.com/kata//583710ccaa6717322c000105)
```javascript
// Solution 1
const simpleMultiplication = number => number * (8 + (number % 2));
// Solution 2
const simpleMultiplication = number => number * (8 + (number & 1));
// Solution 3
const simpleMultiplication = number => number * (number % 2 ? 9 : 8);
// Solution 4
const simpleMultiplication = number => number * (8 + (number % 2 != 0));
// Solution 5
const simpleMultiplication = number => (number % 2 ? number * 9 : number * 8);
// Solution 6
const simpleMultiplication = number => (number << 3) + (number & 1) * number;
// Solution 7
const simpleMultiplication = number =>
  !(number % 2) ? number * 8 : number * 9;
```
#### [DNA to RNA Conversion](https://www.codewars.com/kata//5556282156230d0e5e000089)
```javascript
const DNAtoRNA = dna => dna.replace(/T/g, 'U');
```
#### [Convert boolean values to strings 'Yes' or 'No'](https://www.codewars.com/kata//53369039d7ab3ac506000467)
```javascript
const boolToWord = bool => (bool ? 'Yes' : 'No');
```
#### [Super Duper Easy](https://www.codewars.com/kata//55a5bfaa756cfede78000026)
```javascript
const problem = x => (x === +x ? x * 50 + 6 : 'Error');
```
#### [Chuck Norris VII - True or False? (Beginner)](https://www.codewars.com/kata//570669d8cb7293a2d1001473)
```javascript
const ifChuckSaysSo = () => !true;
```
#### [Type of sum](https://www.codewars.com/kata//5a2e9ae2b6cfd7692a0000ba)
```javascript
const typeOfSum = (a, b) => typeof (a + b);
```
#### [Convert a Number to a String!](https://www.codewars.com/kata//5265326f5fda8eb1160004c8)
```javascript
// Solution 1
var numberToString = num => num.toString();
// Solution 2
var numberToString = num => String(num);
// Solution 3
var numberToString = num => num + '';
// Solution 4
var numberToString = num => `${num}`;
```
#### [Number toString](https://www.codewars.com/kata//53934feec44762736c00044b)
```javascript
// Solution 1
const a = '123';
// Solution 2
const a = "123";
// Solution 3
const a = `123`;
// Solution 4
const a = 123 + '';
// Solution 5
const a = `${123}`;
// Solution 6
const a = String(123);
// Solution 7
const a = 123..toString();
// Solution 8
const a = 123 .toString();
// Solution 9
const a = (123).toString();
// Solution 10
const a = 123['toString']();
```
#### [Convert a String to a Number!](https://www.codewars.com/kata//544675c6f971f7399a000e79)
```javascript
// Solution 1
const stringToNumber = str => +str;
// Solution 2
const stringToNumber = str => Number(str);
// Solution 3
const stringToNumber = str => parseInt(str);
```
#### [Convert a Boolean to a String](https://www.codewars.com/kata//551b4501ac0447318f0009cd)
```javascript
// Solution 1
const booleanToString = String;
// Solution 2
const booleanToString = b => `${b}`;
// Solution 3
const booleanToString = b => b + '';
// Solution 4
const booleanToString = b => '' + b;
// Solution 5
const booleanToString = b => String(b);
// Solution 6
const booleanToString = b => b.toString();
// Solution 7
const booleanToString = b => Boolean(b) + '';
// Solution 8
const booleanToString = b => '' + Boolean(b);
// Solution 9
const booleanToString = b => (b ? 'true' : 'false');
// Solution 10
const booleanToString = b => (b ? 'false' : 'true');
// Solution 11
const booleanToString = b => (b === true ? 'true' : 'false');
// Solution 12
const booleanToString = b => (b === false ? 'false' : 'true');
```
#### [Sum The Strings](https://www.codewars.com/kata//5966e33c4e686b508700002d)
```javascript
const sumStr = (a, b) => String(+a + +b);
```
#### [Discover The Original Price](https://www.codewars.com/kata//552564a82142d701f5001228)
```javascript
//Solution 1
const discoverOriginalPrice = (discountedPrice, salePercentage) =>
  +((discountedPrice * 100) / (100 - salePercentage)).toFixed(2);
//Solution 2
const discoverOriginalPrice = (discountedPrice, salePercentage) =>
  +(discountedPrice / (1 - salePercentage / 100)).toFixed(2);
```
#### [Formatting decimal places #0](https://www.codewars.com/kata//5641a03210e973055a00000d)
```javascript
const twoDecimalPlaces = n => +n.toFixed(2);
```
#### [How many times should I go?](https://www.codewars.com/kata//57efcb78e77282f4790003d8)
```javascript
const howManyTimes = (annualPrice, individualPrice) =>
  Math.ceil(annualPrice / individualPrice);
```
#### [Return the closest number multiple of 10](https://www.codewars.com/kata//58249d08b81f70a2fc0001a4)
```javascript
const closestMultiple10 = num => Math.round(num / 10) * 10;
```
#### [Count Odd Numbers below n](https://www.codewars.com/kata//59342039eb450e39970000a6)
```javascript
const oddCount = n => Math.floor(n / 2);
```
#### [Century From Year](https://www.codewars.com/kata//5a3fe3dde1ce0e8ed6000097)
```javascript
const century = year => Math.ceil(year / 100);
```
#### [Area of a Square](https://www.codewars.com/kata//5748838ce2fab90b86001b1a)
```javascript
// Solution 1
const squareArea = A => +(((2 * A) / Math.PI) ** 2).toFixed(2);
// Solution 2
const squareArea = A => +Math.pow((2 * A) / Math.PI, 2).toFixed(2);
```
#### [Keep up the hoop](https://www.codewars.com/kata//55cb632c1a5d7b3ad0000145)
```javascript
const hoopCount = n => n >= 10 ? 'Great, now move on to tricks' : 'Keep at it until you get it';
```
#### [Simple Comparison?](https://www.codewars.com/kata//57f6ecdfcca6e045d2001207)
```javascript
// Solution 1
const add = (a, b) => a == b;
// Solution 2
const add = (a, b) => +a === +b;
// Solution 3
const add = (a, b) => +a - +b === 0;
// Solution 4
const add = (a, b) => eval(a - b) === 0;
// Solution 5
const add = (a, b) => a + '' === b + '';
// Solution 6
const add = (a, b) => `${a}` === `${b}`;
```
#### [Is he gonna survive?](https://www.codewars.com/kata//59ca8246d751df55cc00014c)
```javascript
// Solution 1
const hero = (bullets, dragons) => bullets >= dragons * 2;
// Solution 2
const hero = (bullets, dragons) => dragons * 2 <= bullets;
// Solution 3
const hero = (bullets, dragons) => bullets / dragons >= 2;
// Solution 4
const hero = (bullets, dragons) => bullets >> 1 >= dragons;
```
#### [Even or Odd](https://www.codewars.com/kata//53da3dbb4a5168369a0000fe)
```javascript
// Solution 1
const even_or_odd = number => ['Even', 'Odd'][number % 2];
// Solution 2
const even_or_odd = number => ['Even', 'Odd'][number & 1];
// Solution 3
const even_or_odd = number => (number % 2 ? 'Odd' : 'Even');
// Solution 4
const even_or_odd = number => (number & 1 ? 'Odd' : 'Even');
// Solution 5
const even_or_odd = number => ['Even', 'Odd'][!(number % 2)];
// Solution 6
const even_or_odd = number => (!(number % 2) ? 'Even' : 'Odd');
// Solution 7
const even_or_odd = number => ['Even', 'Odd'][Math.abs(number) % 2];
// Solution 8
const even_or_odd = number => (Math.abs(number) % 2 ? 'Odd' : 'Even');
```
#### [Calculate BMI](https://www.codewars.com/kata//57a429e253ba3381850000fb)
```javascript
// Solution 1
const bmi = (weight, height) => {
  let bmi = weight / height ** 2;
  if (bmi <= 18.5) return 'Underweight';
  if (bmi <= 25.0) return 'Normal';
  if (bmi <= 30.0) return 'Overweight';
  if (bmi > 30) return 'Obese';
};
// Solution 2
const bmi = (weight, height) =>
  (weight = weight / height / height) > 30
    ? 'Obese'
    : weight > 25
    ? 'Overweight'
    : weight > 18.5
    ? 'Normal'
    : 'Underweight';
// Solution 3
const bmi = (weight, height, bmi = weight / height ** 2) =>
  bmi <= 18.5
    ? 'Underweight'
    : bmi <= 25
    ? 'Normal'
    : bmi <= 30
    ? 'Overweight'
    : 'Obese';
```
#### [What's the real floor?](https://www.codewars.com/kata//574b3b1599d8f897470018f6)
```javascript
// Solution 1
const getRealFloor = n => (n <= 0 ? n : n - (n >= 13 ? 2 : 1));
// Solution 2
const getRealFloor = n => (n <= 0 ? n : n < 13 ? n - 1 : n - 2);
```
#### [Determine offspring sex based on genes XX and XY chromosomes](https://www.codewars.com/kata//56530b444e831334c0000020)
```javascript
// Solution 1
const chromosomeCheck = sperm =>
  sperm === 'XY'
    ? "Congratulations! You're going to have a son."
    : "Congratulations! You're going to have a daughter.";
// Solution 2
const chromosomeCheck = sperm =>
  sperm.indexOf('Y') >= 0
    ? "Congratulations! You're going to have a son."
    : "Congratulations! You're going to have a daughter.";
// Solution 3
const chromosomeCheck = sperm =>
  sperm.includes('Y')
    ? "Congratulations! You're going to have a son."
    : "Congratulations! You're going to have a daughter.";
// Solution 4
const chromosomeCheck = sperm =>
  sperm.match(/[Y]/gi)
    ? "Congratulations! You're going to have a son."
    : "Congratulations! You're going to have a daughter.";
// Solution 5
const chromosomeCheck = sperm => {
  let kid = sperm.includes('Y') ? 'son' : 'daughter';
  return `Congratulations! You're going to have a ${kid}.`;
};
// Solution 6
const chromosomeCheck = sperm =>
  `Congratulations! You're going to have a ${
    sperm.endsWith('X') ? 'daughter' : 'son'
  }.`;
// Solution 7
const chromosomeCheck = sperm =>
  "Congratulations! You're going to have a " +
  (~sperm.indexOf('Y') ? 'son.' : 'daughter.');
// Solution 8
const chromosomeCheck = sperm =>
  `Congratulations! You're going to have a ${
    sperm === 'XY' ? 'son' : 'daughter'
  }.`;
// Solution 9
const chromosomeCheck = sperm =>
  "Congratulations! You're going to have a " +
  (sperm === 'XY' ? 'son' : 'daughter') +
  '.';
// Solution 10
const chromosomeCheck = sperm =>
  `Congratulations! You\'re going to have a ${
    sperm.includes('Y') ? 'son' : 'daughter'
  }.`;
// Solution 11
const chromosomeCheck = sperm => {
  const son = "Congratulations! You're going to have a son.";
  const daughter = "Congratulations! You're going to have a daughter.";
  return sperm.includes('Y') ? son : daughter;
};
// Solution 12
const chromosomeCheck = sperm => {
  const text = a => `Congratulations! You're going to have a ${a}.`;
  return sperm.search('Y') === -1 ? text('daughter') : text('son');
};
```
#### [Alan Partridge II - Apple Turnover](https://www.codewars.com/kata//580a094553bd9ec5d800007d)
```javascript
// Solution 1
const apple = x =>
  +x * +x > 1000
    ? "It's hotter than the sun!!"
    : 'Help yourself to a honeycomb Yorkie for the glovebox.';
// Solution 2
const apple = x =>
  x ** 2 > 1000
    ? "It's hotter than the sun!!"
    : 'Help yourself to a honeycomb Yorkie for the glovebox.';
// Solution 3
const apple = x =>
  Math.pow(x, 2) > 1000
    ? "It's hotter than the sun!!"
    : 'Help yourself to a honeycomb Yorkie for the glovebox.';
```
#### [Sleigh Authentication](https://www.codewars.com/kata//52adc142b2651f25a8000643)
```javascript
// Solution 1
function Sleigh() {}
Sleigh.prototype.authenticate = function(name, password) {
  return name == 'Santa Claus' && password == 'Ho Ho Ho!';
}
// Solution 2
function Sleigh() {}
Sleigh.prototype.authenticate = function(name, password) {
  if (name === 'Santa Claus' && password === 'Ho Ho Ho!') return true;
  return false;
}
// Solution 3
function Sleigh() {}
Sleigh.prototype.authenticate = function(name, password) {
  return name === 'Santa Claus' && password === 'Ho Ho Ho!' ? true : false;
}
// Solution 4
function Sleigh() {
  this.name = 'Santa Claus';
  this.password = 'Ho Ho Ho!';
}
Sleigh.prototype.authenticate = function(name, password) {
  return this.name == name && this.password == password;
}
// Solution 5
class Sleigh {
  authenticate(name, password) {
    return name == 'Santa Claus' && password == 'Ho Ho Ho!';
  }
}
// Solution 6
class Sleigh {
  constructor() {
    this.users = {
      'Santa Claus': 'Ho Ho Ho!'
    }
  }
  authenticate(name, password) {
    return this.users[name] === password;
  }
}
// Solution 7
function Sleigh() {}
Sleigh.prototype.authenticate = function(name, password) {
  if (name !== 'Santa Claus' || password !== 'Ho Ho Ho!') {
    return false;
  } else {
    return true;
  }
}
```
#### [Is n divisible by x and y?](https://www.codewars.com/kata//5545f109004975ea66000086)
```javascript
// Solution 1
const isDivisible = (n, x, y) => n % x === 0 && n % y === 0;
// Solution 2
const isDivisible = (n, x, y) => (n % x) + (n % y) === 0;
// Solution 3
const isDivisible = (n, x, y) => !(n % x || n % y);
// Solution 4
const isDivisible = (n, x, y) => !(n % x | n % y);
```
#### [Rock Paper Scissors!](https://www.codewars.com/kata//5672a98bdbdd995fad00000f)
```javascript
// Solution 1
const rps = (p1, p2) => {
  if (
    (p1 === 'rock' && p2 === 'scissors') ||
    (p1 === 'scissors' && p2 === 'paper') ||
    (p1 === 'paper' && p2 === 'rock')
  )
    return 'Player 1 won!';
  if (
    (p1 === 'scissors' && p2 === 'rock') ||
    (p1 === 'paper' && p2 === 'scissors') ||
    (p1 === 'rock' && p2 === 'paper')
  )
    return 'Player 2 won!';
  return 'Draw!';
};
// Solution 2
const rps = (p1, p2) =>
  p1 === p2
    ? 'Draw!'
    : `Player ${
        /rockscissors|scissorspaper|paperrock/.test(p1 + p2) ? 1 : 2
      } won!`;
```
#### [Can we divide it?](https://www.codewars.com/kata//5a2b703dc5e2845c0900005a)
```javascript
const isDivideBy = (number, a, b) => number % a === 0 && number % b === 0;
```
#### [Student's Final Grade](https://www.codewars.com/kata//5ad0d8356165e63c140014d4)
```javascript
// Solution 1
const finalGrade = (exam, projects) => {
  if (exam > 90 || projects > 10) return 100;
  if (exam > 75 && projects >= 5) return 90;
  if (exam > 50 && projects >= 2) return 75;
  return 0;
};
// Solution 2
const final_Grade = (exam, projects) =>
  exam > 90 || projects > 10
    ? 100
    : exam > 75 && projects > 4
    ? 90
    : exam > 50 && projects > 1
    ? 75
    : 0;
```
#### [L1: Set Alarm](https://www.codewars.com/kata//568dcc3c7f12767a62000038)
```javascript
// Solution 1
const setAlarm = (employed, vacation) => {
  if (employed === true && vacation === false) return true;
  return false;
};
// Solution 2
const setAlarm = (employed, vacation) =>
  employed === true && vacation === false ? true : false;
// Solution 3
const setAlarm = (employed, vacation) => employed && !vacation;
```
#### [Is this a triangle?](https://www.codewars.com/kata//56606694ec01347ce800001b)
```javascript
// Solution 1
const isTriangle = (a, b, c) => a + b > c && a + c > b && c + b > a;
// Solution 2
const isTriangle = (a, b, c) => Math.max(a, b, c) < (a + b + c) / 2;
// Solution 3
const isTriangle = (a, b, c) => (a = [a, b, c].sort())[0] + a[1] > a[2];
```
#### [Calculate Two People's Individual Ages](https://www.codewars.com/kata//58e0bd6a79716b7fcf0013b1)
```javascript
// Solution 1
const getAges = (s, d) => {
  if (s < 0 || d < 0 || s < d) return null;
  return [(s + d) / 2, (s - d) / 2];
};
// Solution 2
const getAges = (s, d) => {
  return s < 0 || d < 0 || s < d ? null : [(s + d) / 2, (s - d) / 2];
};
```
#### [Do I get a bonus?](https://www.codewars.com/kata//56f6ad906b88de513f000d96)
```javascript
// Solution 1
const bonusTime = (salary, bonus) => `£${salary * (bonus ? 10 : 1)}`;
// Solution 2
const bonusTime = (salary, bonus) => '£' + salary * (bonus ? 10 : 1);
// Solution 3
const bonusTime = (salary, bonus) => '£' + (bonus ? salary * 10 : salary);
// Solution 4
const bonusTime = (salary, bonus) => (bonus ? `£${salary * 10}` : `£${salary}`);
// Solution 5
const bonusTime = (salary, bonus) =>
  bonus ? '£' + salary + '0' : '£' + salary;
```
#### [101 Dalmatians - squash the bugs, not the dogs!](https://www.codewars.com/kata//56f6919a6b88de18ff000b36)
```javascript
// Solution 1
const dogs = [
  'Hardly any',
  'More than a handful!',
  "Woah that's a lot of dogs!",
  '101 DALMATIANS!!!'
];
// Solution 2
const howManyDalmatians = number =>
  number <= 10
    ? dogs[0]
    : number <= 50
    ? dogs[1]
    : number <= 100
    ? dogs[2]
    : dogs[3];
```
#### [Training JS #7: if..else and ternary operator](https://www.codewars.com/kata//57202aefe8d6c514300001fd)
```javascript
// Solution 1
const saleHotdogs = n => (n < 5 ? n * 100 : n >= 5 && n < 10 ? n * 95 : n * 90);
// Solution 2
const saleHotdogs = n => n * (n < 5 ? 100 : n < 10 ? 95 : 90);
```
#### [Be Concise I - The Ternary Operator](https://www.codewars.com/kata//56f3f6a82010832b02000f38)
```javascript
const describeAge = age => `You're a(n) ${age <= 12 ? 'kid' : age >= 13 && age <= 17 ? 'teenager' : age >= 18 && age <= 64 ? 'adult' : 'elderly'}`;
```
#### [Basic Mathematical Operations](https://www.codewars.com/kata//57356c55867b9b7a60000bd7)
```javascript
// Solution 1
const basicOp = (operation, value1, value2) => eval(value1 + operation + value2);
// Solution 2
const basicOp = (operation, value1, value2) => {
    switch (operation) {
        case '+': return value1 + value2;
        case '-': return value1 - value2;
        case '*': return value1 * value2;
        case '/': return value1 / value2;
    }
};
// Solution 2
const basicOp = (operation, value1, value2) => {
  var cases = {
    '+': value1 + value2,
    '-': value1 - value2,
    '*': value1 * value2,
    '/': value1 / value2
  };
  return cases[operation]
};
```
#### [simple calculator](https://www.codewars.com/kata//5810085c533d69f4980001cf)
```javascript
// Solution 1
const calculator = (a, b, sign) =>
  !isNaN(a + b) && /[\+\-\*\/]/.test(sign)
    ? eval(a + sign + b)
    : 'unknown value';
// Solution 2
const calculator = (a, b, sign) => {
  if (typeof a === 'number' && typeof b === 'number')
    switch (sign) {
      case '+':
        return a + b;
      case '-':
        return a - b;
      case '*':
        return a * b;
      case '/':
        return a / b;
      default:
        return 'unknown value';
    }
};
// Solution 3
const calculator = (a, b, sign) => {
  let operation = {
    '+': a + b,
    '-': a - b,
    '*': a * b,
    '/': a / b
  };
  return operation[sign] ? operation[sign] : 'unknown value';
};
```
#### [Switch it Up!](https://www.codewars.com/kata//5808dcb8f0ed42ae34000031)
```javascript
// Solution 1
const switchItUp = number =>
  [
    'Zero',
    'One',
    'Two',
    'Three',
    'Four',
    'Five',
    'Six',
    'Seven',
    'Eight',
    'Nine'
  ][number];
// Solution 2
const switchItUp = number =>
  'Zero One Two Three Four Five Six Seven Eight Nine'.split(' ')[number];
// Solution 2
const switchItUp = number => {
  const words = [
    'Zero',
    'One',
    'Two',
    'Three',
    'Four',
    'Five',
    'Six',
    'Seven',
    'Eight',
    'Nine'
  ];
  return words[number];
};
// Solution 3
const switchItUp = number => {
  switch (number) {
    case 0:
      return 'Zero';
    case 1:
      return 'One';
    case 2:
      return 'Two';
    case 3:
      return 'Three';
    case 4:
      return 'Four';
    case 5:
      return 'Five';
    case 6:
      return 'Six';
    case 7:
      return 'Seven';
    case 8:
      return 'Eight';
    case 9:
      return 'Nine';
  }
};
// Solution 4
const switchItUp = number => {
  return {
    0: 'Zero',
    1: 'One',
    2: 'Two',
    3: 'Three',
    4: 'Four',
    5: 'Five',
    6: 'Six',
    7: 'Seven',
    8: 'Eight',
    9: 'Nine'
  }[number];
};
// Solution 5
const switchItUp = number =>
  number === 1
    ? 'One'
    : number === 2
    ? 'Two'
    : number === 3
    ? 'Three'
    : number === 4
    ? 'Four'
    : number === 5
    ? 'Five'
    : number === 6
    ? 'Six'
    : number === 7
    ? 'Seven'
    : number === 8
    ? 'Eight'
    : number === 9
    ? 'Nine'
    : number === 0
    ? 'Zero'
    : '0-9 only!';
```
#### [No zeros for heros](https://www.codewars.com/kata//570a6a46455d08ff8d001002)
```javascript
// Solution 1
const noBoringZeros = n => {
  while (n % 10 === 0 && n !== 0) {
    n = n / 10;
  }
  return n;
};
// Solution 2
const noBoringZeros = n => +`${n}`.replace(/0+$/, '');
// Solution 3
const noBoringZeros = n => +(n + '').replace(/0*$/, '');
// Solution 4
const noBoringZeros = n => +String(n).replace(/[0]+$/g, '');
// Solution 5
const noBoringZeros = n => Number(n.toString().replace(/0+$/g, ''));
// Solution 6
const noBoringZeros = n => (!n || n % 10 ? n : noBoringZeros(n / 10));
// Solution 7
const noBoringZeros = n => (n % 10 || n === 0 ? n : noBoringZeros(n / 10));
```
#### [Power of two](https://www.codewars.com/kata//534d0a229345375d520006a0)
```javascript
// Solution 1
const isPowerOfTwo = n => {
  while (n % 2 === 0 && n != 0) {
    n /= 2;
  }
  return n == 1;
};
// Solution 2
const isPowerOfTwo = n => !(n & (n - 1));
// Solution 3
const isPowerOfTwo = n => (n & (n - 1)) === 0;
// Solution 4
const isPowerOfTwo = n => (n & (~n + 1)) == n;
// Solution 5
const isPowerOfTwo = n => Math.log2(n) % 1 === 0;
// Solution 6
const isPowerOfTwo = n => /^10*$/.test(n.toString(2));
// Solution 7
const isPowerOfTwo = n => Number.isInteger(Math.log2(n));
// Solution 8
const isPowerOfTwo = n => (n === 0 ? false : (n & (n - 1)) === 0);
// Solution 9
const isPowerOfTwo = n => (n === 1 ? true : n < 1 ? false : isPowerOfTwo(n / 2));
```
#### [Difference Of Squares](https://www.codewars.com/kata//558f9f51e85b46e9fa000025)
```javascript
// Solution 1
const differenceOfSquares = x => x * (x * x - 1) * (3 * x + 2) / 12;
// Solution 2
const differenceOfSquares = x => Math.pow(x * (x + 1) / 2, 2) - x * (x + 1) * (2 * x + 1) / 6;
// Solution 
const differenceOfSquares = n => n * n * (n + 1) * (n + 1) / 4 - n * (n + 1) * (2 * n + 1) / 6;
// Solution 4
const differenceOfSquares = n => {
  let sum = 0, sumSquares = 0;
    while (n > 0) {
    sum += n;
    sumSquares += Math.pow(n, 2);
    n--;
  }
  let squareSum = Math.pow(sum, 2)
  return squareSum - sumSquares;
};
```
#### [Factorial](https://www.codewars.com/kata//57a049e253ba33ac5e000212)
```javascript
const factorial = n => n > 1 ? n * factorial(--n) : 1;
```
#### [Powers of 3](https://www.codewars.com/kata//57be674b93687de78c0001d9)
```javascript
// Solution 1
const largestPower = num => {
  let k = 0;
  while (3 ** k < num) ++k;
  return --k;
};
// Solution 2
const largestPower = num => {
  for (let i = 0; i < 999; i++) if (Math.pow(3, i) >= num) return --i;
};
// Solution 3
const largestPower = num => {
  for (let i = -1, k = 1; ; i++, k *= 3) if (k >= num) return i;
};
// Solution 4
const largestPower = num => Math.ceil(Math.log10(num) / Math.log10(3)) - 1;
// Solution 5
const largestPower = (num, a = -1) =>
  Math.pow(3, a) >= num ? --a : largestPower(num, a + 1);
```
#### [The wheat/rice and chessboard problem](https://www.codewars.com/kata//5b0d67c1cb35dfa10b0022c7)
```javascript
// Solution 1
const squaresNeeded = grains => {
  let i = 0;
  while (2 ** i - 1 < grains) {
    i++;
  }
  return i;
};
// Solution 2
const squaresNeeded = grains => (1 + Math.log2(grains)) | 0;
// Solution 3
const squaresNeeded = grains => Math.ceil(Math.log2(++grains));
// Solution 4
const squaresNeeded = grains => (grains ? grains.toString(2).length : 0);
// Solution 5
const squaresNeeded = grains => (!grains ? 0 : grains.toString(2).length);
// Solution 6
const squaresNeeded = grains =>
  grains > 0 ? grains.toString(2).split('').length : 0;
// Solution 7
const squaresNeeded = grains =>
  grains === 0 ? 0 : 1 + squaresNeeded(Math.floor(grains / 2));
```
#### [Sum of Multiples](https://www.codewars.com/kata//57241e0f440cd279b5000829)
```javascript
// Solution 1
const sumMul = (n, m) => {
  if (n >= m) return 'INVALID';
  let sum = 0;
  for (let i = n; i < m; i += n) {
    sum += i;
  }
  return sum;
};
// Solution 2
const sumMul = (n, m, k = Math.floor(m / n)) =>
  n >= m || m <= 0
    ? 'INVALID'
    : m % n !== 0
    ? (n * k * (k + 1)) / 2
    : (n * k * (k - 1)) / 2;
```
#### [Grasshopper - Summation](https://www.codewars.com/kata//55d24f55d7dd296eb9000030)
```javascript
// Solution 1
const summation = num => {
  let sum = 0;
  for (let i = 0; i <= num; i++) {
    sum += i;
  }
  return sum;
};
// Solution 2
const summation = num => (num * (num + 1)) / 2;
// Solution 3
const summation = function f(num) {
  return num ? num + f(num - 1) : 0;
};
```
#### [Beginner Series #3 Sum of Numbers](https://www.codewars.com/kata//55f2b110f61eb01779000053)
```javascript
const getSum = (a, b) => {
  const min = Math.min(a, b),
    max = Math.max(a, b);
  return ((max - min + 1) * (min + max)) / 2;
};
```
#### [Sum of the first nth term of Series](https://www.codewars.com/kata//555eded1ad94b00403000071)
```javascript
const SeriesSum = n => {
  let sum = 0;
  for (let i = 0; i < n; i++) {
    sum += 1 / (1 + i * 3);
  }
  return sum.toFixed(2);
};
```
#### [Miles per gallon to kilometers per liter](https://www.codewars.com/kata//557b5e0bddf29d861400005d)
```javascript
// Solution 1
const converter = mpg => +(mpg * 0.354006043538214).toFixed(2);
// Solution 2
const converter = mpg => +(mpg / 2.82481053).toFixed(2);
```
#### [Find the Slope](https://www.codewars.com/kata//55a75e2d0803fea18f00009d)
```javascript
// Solution 1
const slope = points =>
  points[2] === points[0]
    ? 'undefined'
    : `${(points[3] - points[1]) / (points[2] - points[0])}`;
// Solution 2
const slope = points =>
  String(
    points[2] !== points[0]
      ? (points[3] - points[1]) / (points[2] - points[0])
      : undefined
  );
// Solution 3
const slope = ([a, b, c, d]) => (a === c ? 'undefined' : `${(b - d) / (a - c)}`);
```
#### [Grasshopper - Make change](https://www.codewars.com/kata//560dab9f8b50f89fd6000070)
```javascript
// Solution 1
const money = 10,
  candy = 1.42,
  chips = 2.4,
  soda = 1,
  change = money - candy - chips - soda;
// Solution 2
const change = (money = 10) - (candy = 1.42) - (chips = 2.4) - (soda = 1);
// Solution 3
const [money, candy, chips, soda, change] = '10$1.42$2.40$1.00$5.18'
  .split('$')
  .map(Number);
```
#### [Grasshopper - Basic Function Fixer](https://www.codewars.com/kata//56200d610758762fb0000002)
```javascript
const addFive = num => num + 5;
``` 
#### [Training JS #2: Basic data types--Number](https://www.codewars.com/kata//571edd157e8954bab500032d)
```javascript
let v1 = 50,
  v2 = 100,
  v3 = 150,
  v4 = 200,
  v5 = 2,
  v6 = 250;
const equal1 = () => v1 + v1;
const equal2 = () => v6 - v3;
const equal3 = () => v1 * v5;
const equal4 = () => v4 / v5;
const equal5 = () => v2 % v4;
```
#### [Fix the Bugs (Syntax) - My First Kata](https://www.codewars.com/kata//56aed32a154d33a1f3000018)
```javascript
// Solution 1
const myFirstKata = (a, b) =>
  typeof a !== 'number' || typeof b !== 'number' ? false : (a % b) + (b % a);
// Solution 2
const myFirstKata = (a, b) =>
  typeof a === 'number' && typeof b === 'number' ? (a % b) + (b % a) : false;
// Solution 3
const myFirstKata = (a, b) => (+a === a && +b === b ? (a % b) + (b % a) : false);
// Solution 4
const myFirstKata = (a, b) => (a % b) + (b % a) || !!0;
```
#### [Training JS #6: Basic data types--Boolean and conditional statements if..else](https://www.codewars.com/kata//571f832f07363d295d001ba8)
```javascript
// Solution 1
const trueOrFalse = val => Boolean(val).toString();
// Solution 2
const trueOrFalse = val => String(Boolean(val));
// Solution 3
const trueOrFalse = val => (!!val).toString();
// Solution 4
const trueOrFalse = val => Boolean(val) + '';
// Solution 5
const trueOrFalse = val => String(!!val);
// Solution 6
const trueOrFalse = val => !!val + '';
```
#### [Get Planet Name By ID](https://www.codewars.com/kata//515e188a311df01cba000003)
```javascript
const getPlanetName = id => {
  switch (id) {
    case 1:
      return 'Mercury';
    case 2:
      return 'Venus';
    case 3:
      return 'Earth';
    case 4:
      return 'Mars';
    case 5:
      return 'Jupiter';
    case 6:
      return 'Saturn';
    case 7:
      return 'Uranus';
    case 8:
      return 'Neptune';
  }
};
```
#### [Power](https://www.codewars.com/kata//562926c855ca9fdc4800005b)
```javascript
// Solution 1
const numberToPower = (number, power) => {
  let sum = 1;
  for (let i = 1; i <= power; i++) sum *= number;
  return sum;
};
// Solution 2
const numberToPower = (number, power) =>
  power > 0 ? number * numberToPower(number, power - 1) : 1;
// Solution 3
const numberToPower = (number, power) =>
  Array(power)
    .fill(number)
    .reduce((res, n) => res * n, 1);
```
#### [Is it a palindrome?](https://www.codewars.com/kata//57a1fd2ce298a731b20006a4)
```javascript
const isPalindrome = x => (x = x.toLowerCase()) === x.split('').reverse().join('');
```
#### [isReallyNaN](https://www.codewars.com/kata//56c24c58e0c0f741d4001aef)
```javascript
// Solution 1
const isReallyNaN = val => Number.isNaN;
// Solution 2
const isReallyNaN = val => val !== val;
// Solution 3
const { isNaN: isReallyNaN } = Number;
```
#### [Filter the number](https://www.codewars.com/kata//55b051fac50a3292a9000025)
```javascript
// Solution 1
const FilterString = value => +value.replace(/[a-z]/gi, '');
// Solution 2
const FilterString = value => +value.replace(/[^0-9]/g, '');
// Solution 3
const FilterString = value => +value.replace(/[^\d]/g, '');
// Solution 4
const FilterString = value => +value.replace(/\D+/g, '');
// Solution 5
const FilterString = value => +value.replace(/\D/g, '');
```
#### [Is integer safe to use?](https://www.codewars.com/kata//55a4f9afeffe4231090000d6)
```javascript
const SafeInteger = n => Number.isSafeInteger(n);
```
#### [Return Negative](https://www.codewars.com/kata//55685cd7ad70877c23000102)
```javascript
// Solution 1
const makeNegative = num => num < 0 ? num : -num;
// Solution 2
const makeNegative = num => -Math.abs(num);
```
#### [Opposite number](https://www.codewars.com/kata//56dec885c54a926dcd001095)
```javascript
const opposite = number => -number;
```
#### [Invert values](https://www.codewars.com/kata//5899dc03bc95b1bf1b0000ad)
```javascript
// Solution1
const invert = arr => arr.map(el => el === 0 ? el : -el);
// Solution 2
const invert = arr => arr.map(el => 0 - el);
// Solution 3
const invert = arr => {
  const newArr = [];
  for (let i = 0; i < arr.length; i++) newArr.push(-arr[i]);
  return newArr;
};
```
#### [BASIC: Making Six Toast.](BASIC: Making Six Toast.)
```javascript
// Solution 1
const sixToast = num => num >= 6 ? num - 6 : 6 - num;
// Solution 2
const sixToast = num => Math.abs(num - 6);
```
#### [Closest elevator](https://www.codewars.com/kata//5c374b346a5d0f77af500a5a)
```javascript
// Solution 1
const elevator = (left, right, call) =>
  Math.abs(call - left) < Math.abs(call - right) ? 'left' : 'right';
// Solution 2
const elevator = (left, right, call) =>
  (call - left) ** 2 < (call - right) ** 2 ? 'left' : 'right';
```
#### [To square(root) or not to square(root)](https://www.codewars.com/kata//57f6ad55cca6e045d2000627)
```javascript
const squareOrSquareRoot = arr =>
  arr.map(el => el ** 0.5 % 1 ? el * el : el ** 0.5);
```
#### [Squares sequence](https://www.codewars.com/kata//5546180ca783b6d2d5000062)
```javascript
// Solution 1
const squares = (x, n) =>
  Array.from({ length: n }, (_, i) => Math.pow(x, Math.pow(2, i)));
// Solution 2
const squares = (x, n) => {
  const arr = [];
  for (let i = 0; i < n; i++){
    arr.push(x);
    x = Math.pow(x, 2);
  }
  return arr;
};
```
#### [Square Every Digit](https://www.codewars.com/kata//546e2562b03326a88e000020)
```javascript
// Solution 1
const squareDigits = num =>
  +(num + '')
    .split('')
    .map(el => el * el)
    .join('');
// Solution 2
const squareDigits = num => {
  const str = num + '',
    res = [];
  for (let i = 0; i < str.length; i++) {
    res[i] = str[i] * str[i];
  }
  return +res.join('');
};
```
#### [Find the next perfect square!](https://www.codewars.com/kata//56269eb78ad2e4ced1000013)
```javascript
// Solution 1
const findNextSquare = (n, sq = n ** 0.5) => sq % 1 ? -1 : ++sq * sq;
// Solution 2
const findNextSquare = sq => sq ** 0.5 % 1 ? -1 : (sq ** 0.5 + 1) ** 2;
// Solution 3
const findNextSquare = sq => (sq = Math.sqrt(sq)) % 1 ? -1 : ++sq ** 2;
// Solution 4
const findNextSquare = sq =>
  Math.round(sq = Math.sqrt(sq)) === sq ? ++sq ** 2 : -1;
// Solution 5
const findNextSquare = sq =>
  Math.sqrt(sq) % 1 ? -1 : Math.pow(Math.sqrt(sq) + 1, 2);
// Solution 6
const findNextSquare = sq =>
  Math.round(Math.sqrt(sq)) === Math.sqrt(sq)
    ? Math.pow(Math.sqrt(sq) + 1, 2)
    : -1;
```
#### [Santa's Naughty List](https://www.codewars.com/kata//5a0b4dc2ffe75f72f70000ef)
```javascript
const findChildren = (santasList, children) => [
  ...new Set(children.filter(el => santasList.includes(el)).sort()),
];
```
#### [You're a square!](https://www.codewars.com/kata//54c27a33fb7da0db0100040e)
```javascript
// Solution 1
const isSquare = num => Math.sqrt(num) % 1 === 0;
// Solution 2
const isSquare = (num, n = Math.sqrt(num)) => ~~n === n;
// Solution 3
const isSquare = num => /^[0-9]+$/.test(Math.sqrt(num));
// Solution 4
const isSquare = num => Number.isInteger(Math.sqrt(num));
// Solution 5
const isSquare = (num, n = Math.sqrt(num)) => n === (n | 0);
// Solution 6
const isSquare = (num, n = Math.sqrt(num)) => n === Math.floor(n);
```
#### [Beginner Series #4 Cockroach](https://www.codewars.com/kata//55fab1ffda3e2e44f00000c6)
```javascript
// Solution 1
const cockroachSpeed = s => Math.floor(s * 27.778);
// Solution 2
const cockroachSpeed = s => Math.floor(s / .036);
// Solution 3
const cockroachSpeed = s => s * 27.778 | 0;
// Solution 4
const cockroachSpeed = s => s / .036 | 0;
```
#### [Price of Mangoes](https://www.codewars.com/kata//57a77726bb9944d000000b06)
```javascript
// Solution 1
const mango = (quantity, price) => price * (quantity - Math.floor(quantity / 3));
// Solution 2
const mango = (quantity, price) => price * (quantity - (quantity / 3 | 0));
```
