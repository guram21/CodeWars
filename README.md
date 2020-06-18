# CodeWars
#### [Multiply](https://www.codewars.com/kata//50654ddff44f800200000004)
```javascript
const multiply = (a, b) => a * b;
```
#### [Draw stairs](https://www.codewars.com/kata//5b4e779c578c6a898e0005c5)
```javascript
// Solution 1
const drawStairs = num => {
  let res = '';
  for (let i = 1; i <= num; i++) {
    res += i === num ? 'I' : 'I\n' + ' '.repeat(i);
  }
  return res;
};
// Solution 2
const drawStairs = num => {
  let stairs = '',
    space = ' ';
  for (let i = 0; i < num - 1; i++) {
    stairs += 'I\n' + space;
    space += ' ';
  }
  return stairs + 'I';
};
// Solution 3
const drawStairs = num =>
  [...Array(num)].map((_, i) => ' '.repeat(i) + 'I').join('\n');
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
const howMuchILoveYou = num => {
  const fl = [
    'I love you',
    'a little',
    'a lot',
    'passionately',
    'madly',
    'not at all'
  ];
  return fl[(num - 1) % 6];
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
const angle = num => 180 * (num - 2);
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
const simpleMultiplication = num => num * (8 + num % 2);
// Solution 2
const simpleMultiplication = num => num * (8 + (num & 1));
// Solution 3
const simpleMultiplication = num => num * (num % 2 ? 9 : 8);
// Solution 4
const simpleMultiplication = num => num * (8 + (num % 2 !== 0));
// Solution 5
const simpleMultiplication = num => num % 2 ? num * 9 : num * 8;
// Solution 6
const simpleMultiplication = num => (num << 3) + (num & 1) * num;
// Solution 7
const simpleMultiplication = num => !(num % 2) ? num * 8 : num * 9;
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
const numberToString = num => num.toString();
// Solution 2
const numberToString = num => String(num);
// Solution 3
const numberToString = num => num + '';
// Solution 4
const numberToString = num => `${num}`;
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
const twoDecimalPlaces = num => +num.toFixed(2);
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
const oddCount = num => Math.floor(num / 2);
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
const hoopCount = num => num >= 10 ? 'Great, now move on to tricks' : 'Keep at it until you get it';
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
const even_or_odd = num => ['Even', 'Odd'][num % 2];
// Solution 2
const even_or_odd = num => ['Even', 'Odd'][num & 1];
// Solution 3
const even_or_odd = num => (num % 2 ? 'Odd' : 'Even');
// Solution 4
const even_or_odd = num => (num & 1 ? 'Odd' : 'Even');
// Solution 5
const even_or_odd = num => ['Even', 'Odd'][!(num % 2)];
// Solution 6
const even_or_odd = num => (!(num % 2) ? 'Even' : 'Odd');
// Solution 7
const even_or_odd = num => ['Even', 'Odd'][Math.abs(num) % 2];
// Solution 8
const even_or_odd = num => (Math.abs(num) % 2 ? 'Odd' : 'Even');
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
const getRealFloor = num => (num <= 0 ? num : num - (num >= 13 ? 2 : 1));
// Solution 2
const getRealFloor = num => (num <= 0 ? num : num < 13 ? num - 1 : num - 2);
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
  return name === 'Santa Claus' && password === 'Ho Ho Ho!';
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
  return name === 'Santa Claus' && password === 'Ho Ho Ho!';
}
// Solution 4
function Sleigh() {
  this.name = 'Santa Claus';
  this.password = 'Ho Ho Ho!';
}
Sleigh.prototype.authenticate = function(name, password) {
  return this.name === name && this.password === password;
}
// Solution 5
class Sleigh {
  authenticate(name, password) {
    return name === 'Santa Claus' && password === 'Ho Ho Ho!';
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
const isDivideBy = (num, a, b) => num % a === 0 && num % b === 0;
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
const setAlarm = (employed, vacation) =>
  employed === true && vacation === false;
// Solution 2
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
const howManyDalmatians = num =>
  num <= 10
    ? dogs[0]
    : num <= 50
    ? dogs[1]
    : num <= 100
    ? dogs[2]
    : dogs[3];
```
#### [Training JS #7: if..else and ternary operator](https://www.codewars.com/kata//57202aefe8d6c514300001fd)
```javascript
// Solution 1
const saleHotdogs = num => (num < 5 ? num * 100 : num >= 5 && num < 10 ? num * 95 : num * 90);
// Solution 2
const saleHotdogs = num => num * (num < 5 ? 100 : num < 10 ? 95 : 90);
```
#### [Be Concise I - The Ternary Operator](https://www.codewars.com/kata//56f3f6a82010832b02000f38)
```javascript
const describeAge = a => `You're a(n) ${a < 13 ? 'kid' : a < 18 ? 'teenager' : a < 65 ? 'adult' : 'elderly'}`;
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
  const cases = {
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
const switchItUp = num =>
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
  ][num];
// Solution 2
const switchItUp = num =>
  'Zero One Two Three Four Five Six Seven Eight Nine'.split(' ')[num];
// Solution 2
const switchItUp = num => {
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
  return words[num];
};
// Solution 3
const switchItUp = num => {
  switch (num) {
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
const switchItUp = num => {
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
  }[num];
};
// Solution 5
const switchItUp = num =>
  num === 1
    ? 'One'
    : num === 2
    ? 'Two'
    : num === 3
    ? 'Three'
    : num === 4
    ? 'Four'
    : num === 5
    ? 'Five'
    : num === 6
    ? 'Six'
    : num === 7
    ? 'Seven'
    : num === 8
    ? 'Eight'
    : num === 9
    ? 'Nine'
    : num === 0
    ? 'Zero'
    : '0-9 only!';
```
#### [No zeros for heros](https://www.codewars.com/kata//570a6a46455d08ff8d001002)
```javascript
// Solution 1
const noBoringZeros = num => {
  while (num % 10 === 0 && num !== 0) {
    num = num / 10;
  }
  return num;
};
// Solution 2
const noBoringZeros = num => +`${num}`.replace(/0+$/, '');
// Solution 3
const noBoringZeros = num => +(num + '').replace(/0*$/, '');
// Solution 4
const noBoringZeros = num => +String(num).replace(/[0]+$/g, '');
// Solution 5
const noBoringZeros = num => Number(num.toString().replace(/0+$/g, ''));
// Solution 6
const noBoringZeros = num => (!num || num % 10 ? num : noBoringZeros(num / 10));
// Solution 7
const noBoringZeros = num => (num % 10 || num === 0 ? num : noBoringZeros(num / 10));
```
#### [Power of two](https://www.codewars.com/kata//534d0a229345375d520006a0)
```javascript
// Solution 1
const isPowerOfTwo = num => {
  while (num % 2 === 0 && num !== 0) {
    num /= 2;
  }
  return num === 1;
};
// Solution 2
const isPowerOfTwo = num => !(num & num - 1);
// Solution 3
const isPowerOfTwo = num => (num & num - 1) === 0;
// Solution 4
const isPowerOfTwo = num => (num & ~num + 1) === num;
// Solution 5
const isPowerOfTwo = num => Math.log2(num) % 1 === 0;
// Solution 6
const isPowerOfTwo = num => /^10*$/.test(num.toString(2));
// Solution 7
const isPowerOfTwo = num => Number.isInteger(Math.log2(num));
// Solution 8
const isPowerOfTwo = num => num === 0 ? false : (num & num - 1) === 0;
// Solution 9
const isPowerOfTwo = num => num === 1 ? true : num < 1 ? false : isPowerOfTwo(num / 2);
```
#### [Difference Of Squares](https://www.codewars.com/kata//558f9f51e85b46e9fa000025)
```javascript
// Solution 1
const differenceOfSquares = num => num * (num * num - 1) * (3 * num + 2) / 12;
// Solution 2
const differenceOfSquares = num => Math.pow(num * (num + 1) / 2, 2) - num * (num + 1) * (2 * num + 1) / 6;
// Solution 
const differenceOfSquares = num => num * num * (num + 1) * (num + 1) / 4 - num * (num + 1) * (2 * num + 1) / 6;
// Solution 4
const differenceOfSquares = num => {
  let sum = 0, sumSquares = 0;
    while (num > 0) {
    sum += num;
    sumSquares += Math.pow(num, 2);
    num--;
  }
  let squareSum = Math.pow(sum, 2)
  return squareSum - sumSquares;
};
```
#### [Factorial](https://www.codewars.com/kata//57a049e253ba33ac5e000212)
```javascript
const factorial = num => num > 1 ? num * factorial(--num) : 1;
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
const SeriesSum = num => {
  let sum = 0;
  for (let i = 0; i < num; i++) {
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
const money = 10,
  candy = 1.42,
  chips = 2.4,
  soda = 1,
  change = money - candy - chips - soda;
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
const numberToPower = (num, pow) => {
  let sum = 1;
  for (let i = 1; i <= pow; i++) sum *= num;
  return sum;
};
// Solution 2
const numberToPower = (num, pow) =>
  pow > 0 ? num * numberToPower(num, pow - 1) : 1;
// Solution 3
const numberToPower = (num, pow) =>
  Array(pow)
    .fill(num)
    .reduce((acc, curr) => acc * curr, 1);
```
#### [Is it a palindrome?](https://www.codewars.com/kata//57a1fd2ce298a731b20006a4)
```javascript
const isPalindrome = str => (str = str.toLowerCase()) === str.split('').reverse().join('');
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
const SafeInteger = num => Number.isSafeInteger(num);
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
const opposite = num => -num;
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
// Solution 1
const findChildren = (santasList, children) => [
  ...new Set(children.filter(el => santasList.includes(el)).sort()),
];
// Solution 2
const findChildren = (santasList, children) =>
  children
    .filter((el, i, arr) => santasList.includes(el) && i === arr.indexOf(el))
    .sort();
// Solution 3
const findChildren = (santasList, children) => {
  const arr = [];
  for (let item of santasList) {
    for (let child of children) {
      if (item === child && !arr.includes(item)) arr.push(item);
    }
  }
  return arr.sort();
};
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
#### [Holiday VIII - Duty Free](https://www.codewars.com/kata//57e92e91b63b6cbac20001e5)
```javascript
// Solution 1
const dutyFree = (normPrice, discount, hol) =>
  Math.floor((hol * 100) / (normPrice * discount));
// Solution 2
const dutyFree = (normPrice, discount, hol) =>
  Math.floor(hol / ((normPrice * discount) / 100));
// Solution 3
const dutyFree = (normPrice, discount, hol) =>
  Math.floor((hol / normPrice / discount) * 100);
// Solution 4
const dutyFree = (normPrice, discount, hol) =>
  hol / ((normPrice * discount) / 100) ^ 0;
// Solution 5
const dutyFree = (normPrice, discount, hol) =>
  ~~((100 * hol) / normPrice / discount);
// Solution 6
const dutyFree = (normPrice, discount, hol) =>
  (hol / normPrice / discount) * 100 | 0;
```
#### [All Star Code Challenge #22]()
```javascript
// Solution 1
const toTime = (seconds, hr = seconds / 3600, min = (hr - parseInt(hr)) * 60) =>
  `${Math.floor(hr)} hour(s) and ${Math.floor(min)} minute(s)`;
// Solution 2
const toTime = (seconds, hr = seconds / 3600, min = (seconds % 3600) / 60) =>
  `${Math.floor(hr)} hour(s) and ${Math.floor(min)} minute(s)`;
// Solution 3
const toTime = (seconds, hr = seconds / 3600, min = (seconds % 3600) / 60) =>
  `${Math.trunc(hr)} hour(s) and ${Math.trunc(min)} minute(s)`;
// Solution 4
const toTime = (seconds, min = seconds / 60 | 0, hr = min / 60 | 0) =>
  `${hr} hour(s) and ${min - hr * 60} minute(s)`;
// Solution 5
const toTime = seconds =>
  `${Math.floor(seconds / 3600)} hour(s) and ${Math.floor(
    (seconds % 3600) / 60
  )} minute(s)`;
// Solution 6
const toTime = seconds =>
  `${seconds / 3600 | 0} hour(s) and ${
    (seconds % 3600) / 60 | 0
  } minute(s)`;
// Solution 7
const toTime = seconds =>
  `${seconds / 3600 | 0} hour(s) and ${(seconds / 60) % 60 | 0} minute(s)`;
```
#### [Formatting decimal places #1](https://www.codewars.com/kata//5641c3f809bf31f008000042)
```javascript
// Solution 1
const twoDecimalPlaces = num => +num.toFixed(4).slice(0, -2);
// Solution 2
const twoDecimalPlaces = num => Math.trunc(num * 100) / 100;
// Solution 3
const twoDecimalPlaces = num => parseInt(num * 100) / 100;
// Solution 4
const twoDecimalPlaces = num => (num * 100 | 0) / 100;
// Solution 5
const twoDecimalPlaces = num => ~~(num * 100) / 100;
```
#### [Tortoise racing](https://www.codewars.com/kata//55e2adece53b4cdcb900006c)
```javascript
// Solution 1
const race = (v1, v2, g, t) =>
  v1 >= v2
    ? null
    : ((t = new Date((g / (v2 - v1)) * 3600 * 1000)),
    [t.getHours(), t.getMinutes(), t.getSeconds()]);
// Solution 2
const race = (v1, v2, g, t = g / (v2 - v1)) =>
  v1 >= v2 ? null : [t | 0, (t * 60) % 60 | 0, Math.trunc(t * 3600) % 60];
// Solution 3
const race = (v1, v2, g, t = g / (v2 - v1)) =>
  t >= 0 ? [t, (t * 60) % 60, (t * 3600) % 60].map(Math.floor) : null;
// Solution 4
const race = (v1, v2, g, t = g / (v2 - v1)) =>
  t >= 0 ? [~~t, ~~((t * 60) % 60), ~~((t * 60 ** 2) % 60)] : null;
// Solution 5
const race = (v1, v2, g, t = g / (v2 - v1)) =>
  t >= 0 ? [t | 0, (t * 60 | 0) % 60, (t * 3600 | 0) % 60] : null;
```
#### [Lario and Muigi Pipe Problem](https://www.codewars.com/kata//56b29582461215098d00000f)
```javascript
// Solution 1
const pipeFix = num => {
  const arr = [];
  for (let i = Math.min(...num); i <= Math.max(...num); i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const pipeFix = num => {
  const arr = [];
  for (let i = num[0]; i <= Math.max(...num); i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 3
const pipeFix = num => {
  const arr = [];
  for (let i = num[0]; i <= num[num.length - 1]; i++) {
    arr.push(i);
  }
  return arr;
};
```
#### [Expressions Matter](https://www.codewars.com/kata//5ae62fcf252e66d44d00008e)
```javascript
const expressionMatter = (a, b, c) =>
  Math.max(
    a + b + c,
    a * b * c,
    a + b * c,
    (a + b) * c,
    a * b + c,
    a * (b + c)
  );
```
#### [Convert to Binary](https://www.codewars.com/kata//59fca81a5712f9fa4700159a)
```javascript
const toBinary = num => +num.toString(2);
```
#### [Binary Addition](https://www.codewars.com/kata//551f37452ff852b7bd000139)
```javascript
const addBinary = (a, b) => (a + b).toString(2);
```
#### [Calculate Price Excluding VAT](https://www.codewars.com/kata//5890d8bc9f0f422cf200006b)
```javascript
// Solution 1
const excludingVatPrice = price =>
  price === null ? -1 : +(price / 1.15).toFixed(2);
// Solution 2
const excludingVatPrice = price =>
  price !== null ? +(price / 1.15).toFixed(2) : -1;
```
#### [Parse nice int from char problem](https://www.codewars.com/kata//557cd6882bfa3c8a9f0000c1)
```javascript
const getAge = inputString => parseInt(inputString, 10);
```
#### [Hex to Decimal](https://www.codewars.com/kata//57a4d500e298a7952100035d)
```javascript
const hexToDec = h => parseInt(h, 16);
```
#### [Bin to Decimal](https://www.codewars.com/kata//57a5c31ce298a7e6b7000334)
```javascript
const binToDec = bin => parseInt(bin, 2);
```
#### [Parse float](https://www.codewars.com/kata//57a386117cb1f31890000039)
```javascript
// Soliution 1
const parseF = s => !isNaN(parseFloat(s)) ? parseFloat(s) : null;
// Soliution 2
const parseF = s => isNaN(parseFloat(s)) ? null : parseFloat(s);
// Soliution 3
const parseF = s => !isNaN(s = parseFloat(s)) ? s : null;
// Soliution 4
const parseF = s => isNaN(s = parseFloat(s)) ? null : s;
```
#### [Sum Arrays](https://www.codewars.com/kata//53dc54212259ed3d4f00071c)
```javascript
// Solution 1
const sum = num => {
  'use strict';
  let sum = 0;
  for (let i = 0; i < num.length; i++) {
    sum += num[i];
  }
  return sum;
};
// Solution 2
const sum = num => num.reduce((acc, curr) => acc + curr, 0);
```
#### [Count the Monkeys!](https://www.codewars.com/kata//56f69d9f9400f508fb000ba7)
```javascript
// Solution 1
const monkeyCount = num => {
  const arr = [];
  for (let i = 1; i <= num; i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const monkeyCount = num => [...Array(++num).keys()].slice(1);
// Solution 3
const monkeyCount = num => [...Array(num)].map((_, i) => ++i);
// Solution 4
const monkeyCount = num => [...Array(num).keys()].map(i => ++i);
// Solution 5
const monkeyCount = num => Array(num).fill().map((_, i) => ++i);
// Solution 6
const monkeyCount = num => Array.from(Array(++num).keys()).slice(1);
// Solution 7
const monkeyCount = num => [...new Array(++num).keys()].filter(i => i > 0);
```
#### [Filling an array (part 1)](https://www.codewars.com/kata//571d42206414b103dc0006a1)
```javascript
// Solution 1
const arr = num => {
  const arr = [];
  for (let i = 0; i < num; i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const arr = num => [...Array(num || 0).keys()];
// Solution 3
const arr = (num = 0) => [...Array(num).keys()];
// Solution 4
const arr = num => num ? [...Array(num).keys()] : [];
// Solution 5
const arr = num => Array.from({ length: num }, (_, i) => i);
```
#### [What is type of variable?](https://www.codewars.com/kata//57293671c98f77e84b000065)
```javascript
//Solution 1
const type = value => ({}).toString.call(value).slice(8, -1).toLowerCase();
//Solution 2
const type = value =>
  Object.prototype.toString.call(value).slice(8, -1).toLowerCase();
//Solution 3
const type = value =>
  ({}).toString
    .call(value)
    .match(/\s([a-zA-Z]+)/)[1]
    .toLowerCase();
//Solution 4
const type = value =>
  ({}).toString
    .call(value)
    .match(/(\w+)]/)[1]
    .toLowerCase();
```
#### [Is every value in the array an array?](https://www.codewars.com/kata//582c81d982a0a65424000201)
```javascript
const arrCheck = value => value.every(Array.isArray);
```
#### [Enumerable Magic #3 - Does My List Include This?](https://www.codewars.com/kata//545991b4cbae2a5fda000158)
```javascript
// Solution 1
const include = (arr, item) => {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === item) return true;
  }
  return false;
};
// Solution 2
const include = Array.includes;
// Solution 3
const include = (arr, item) => arr.includes(item);
// Solution 4
const include = (arr, item) => new Set(arr).has(item);
// Solution 5
const include = (arr, item) => arr.indexOf(item) > -1;
// Solution 6
const include = (arr, item) => arr.indexOf(item) >= 0;
// Solution 7
const include = (arr, item) => arr.indexOf(item) !== -1;
// Solution 8
const include = (arr, item) => arr.some(el => el === item);
// Solution 9
const include = (arr, item) => Boolean(~arr.indexOf(item));
// Solution 10
const include = (arr, item) => arr.find(el => el === item) === item;
```
#### [Counting sheep...](https://www.codewars.com/kata//54edbc7200b811e956000556)
```javascript
// Solution 1
const countSheeps = (arrayOfSheep, count = 0) => {
  for (let i = 0; i < arrayOfSheep.length; i++)
    if (arrayOfSheep[i] === true) count++;
  return count;
};
// Solution 2
const countSheeps = (arrayOfSheep, count = 0) => {
  for (let i in arrayOfSheeps) {
    arrayOfSheeps[i] ? count++ : null;
  }
  return count;
};
// Solution 3
const countSheeps = arrayOfSheeps => arrayOfSheeps.filter(Boolean).length;
// Solution 4
const countSheeps = arrayOfSheeps => arrayOfSheeps.filter(el => el).length;
// Solution 5
const countSheeps = arrayOfSheeps =>
  !arrayOfSheeps ? 0 : arrayOfSheeps.reduce((acc, curr) => curr ? ++acc : acc, 0);
```
#### [A Needle in the Haystack](https://www.codewars.com/kata//56676e8fabd2d1ff3000000c)
```javascript
// Solution 1
const findNeedle = haystack =>
  `found the needle at position ${haystack.indexOf('needle')}`;
// Solution 2
const findNeedle = haystack => {
  for (let i = 0; i < haystack.length; i++) {
    if (haystack[i] === 'needle') return `found the needle at position ${i}`;
  }
};
```
#### [Difference of Volumes of Cuboids](https://www.codewars.com/kata//58cb43f4256836ed95000f97)
```javascript
// Solution 1
const findDifference = (a, b) =>
  Math.abs(
    a.reduce((acc, curr) => acc * curr) - b.reduce((acc, curr) => acc * curr)
  );
// Solution 2
const findDifference = (a, b) =>
  Math.abs(a[0] * a[1] * a[2] - b[0] * b[1] * b[2]);
// Solution 3
const findDifference = (a, b) => (
  (c = (a, b) => a * b), Math.abs(a.reduce(c) - b.reduce(c))
);
// Solution 3
const findDifference = (a, b) =>
  Math.abs(
    a.reduce((acc, curr) => acc * curr) - b.reduce((acc, curr) => acc * curr)
  );
// Solution 4
const findDifference = (a, b, A = 1, B = 1) => {
  a.map(el => A *= el);
  b.map(el => B *= el);
  return Math.abs(A - B);
};
// Solution 5
const findDifference = (a, b) => {
  let A = a.reduce((acc, curr) => acc * curr);
  let B = b.reduce((acc, curr) => acc * curr);
  return Math.abs(A - B);
};
// Solution 6
const findDifference = (a, b, A = 1, B = 1) => {
  for (let i = 0; i < 3; i++) {
    A *= a[i];
    B *= b[i];
  }
  return Math.abs(A - B);
};
```
#### [Find the smallest integer in the array](https://www.codewars.com/kata//55a2d7ebe362935a210000b2)
```javascript
class SmallestIntegerFinder {
  findSmallestInt(args) {
    return Math.min(...args);
  }
}
```
#### [Find the first non-consecutive number](https://www.codewars.com/kata//58f8a3a27a5c28d92e000144)
```javascript
// Solution 1
const firstNonConsecutive = arr => {
  for (let i = 0; i < arr.length - 1; ++i) {
    if (arr[i] + 1 !== arr[i + 1]) return arr[i + 1];
  }
  return null;
};
// Solution 2
const firstNonConsecutive = arr => {
  const res = arr.find((el, i) => el !== i + arr[0]);
  return Number.isInteger(res) ? res : null;
};
// Solution 3
const firstNonConsecutive = arr =>
  arr.length === 1
    ? null
    : arr[0] + 1 !== arr[1]
      ? arr[1]
      : firstNonConsecutive(arr.slice(1));
```
#### [Total amount of points](https://www.codewars.com/kata//5bb904724c47249b10000131)
```javascript
// Solution 1
const points = games => {
  let count = 0;
  games.forEach(item => {
    if (item[0] > item[2]) count += 3;
    if (item[0] === item[2]) count++;
  });
  return count;
};
// Solution 2
const points = games => {
  let count = 0;
  for (let i = 0; i < games.length; i++) {
    if (games[i][0] > games[i][2]) count += 3;
    if (games[i][0] === games[i][2]) count++;
  }
  return count;
};
// Solution 3
const points = games =>
  games.reduce((acc, curr) => {
    return acc += curr[0] > curr[2] ? 3 : curr[0] === curr[2] ? 1 : 0;
  }, 0);
```
#### [Enumerable Magic #2 - True for Any?](https://www.codewars.com/kata//54598e89cbae2ac001001135)
```javascript
const any = (arr, fun) => arr.some(fun);
```
#### [Square(n) Sum](https://www.codewars.com/kata//515e271a311df0350d00000f)
```javascript
// Solution 1
const squareSum = num => {
  let sum = 0;
  for (let i = 0; i < num.length; i++) {
    sum += Math.pow(num[i], 2);
  }
  return sum;
};
// Solution 2
const squareSum = num => {
  let sum = 0;
  num.forEach(el => sum += el ** 2);
  return sum;
};
// Solution 3
const squareSum = num =>
  num.reduce((acc, curr) => acc + curr * curr, 0);
```
#### [How good are you really?](https://www.codewars.com/kata//5601409514fc93442500010b)
```javascript
// Solution 1
const betterThanAverage = (classPoints, yourPoints) => {
  let sum = 0;
  for (let i = 0; i < classPoints.length; i++) {
    sum += classPoints[i];
  }
  return sum / classPoints.length < yourPoints;
};
//2 Solution
const betterThanAverage = (classPoints, yourPoints) => {
  let sum = 0;
  classPoints.forEach(el => sum += el);
  return sum / classPoints.length < yourPoints;
};
// Solution 3
const betterThanAverage = (classPoints, yourPoints) =>
  classPoints.reduce((acc, curr) => acc + curr, 0) / classPoints.length < yourPoints;
```
#### [Sum of positive](https://www.codewars.com/kata//5715eaedb436cf5606000381)
```javascript
// Solution 1
const positiveSum = arr => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > 0) sum += arr[i];
  }
  return sum;
};
// Solution 2
const positiveSum = arr => {
  let sum = 0;
  arr.forEach(el => el > 0 ? sum += el : 0);
  return sum;
};
// Solution 3
const positiveSum = arr => arr.reduce((acc, curr) => acc + (curr > 0 && curr), 0);
```
#### [Calculate average](https://www.codewars.com/kata//57a2013acf1fa5bfc4000921)
```javascript
// Solution 1
const find_average = arr => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum / arr.length;
};
// Solution 2
const find_average = arr => {
  let sum = 0;
  arr.forEach(el => sum += el);
  return sum / arr.length;
};
// Solution 3
const find_average = arr => arr.reduce((acc, curr) => acc + curr, 0) / arr.length;
```
#### [Divide and Conquer](https://www.codewars.com/kata//57eaec5608fed543d6000021)
```javascript
// Solution 1
const divCon = arr => {
  let sumNum = 0;
  let sumStr = 0;
  for (let i = 0; i < arr.length; i++) {
    +arr[i] === arr[i] ? sumNum += arr[i] : sumStr += +arr[i];
  }
  return sumNum - sumStr;
};
// Solution 2
const divCon = arr => {
  let sumNum = 0;
  let sumStr = 0;
  arr.forEach(el => +el === el ? sumNum += el : sumStr += +el);
  return sumNum - sumStr;
};
// Solution 3
const divCon = arr =>
  arr.reduce((acc, curr) => +curr === curr ? acc + curr : acc - +curr, 0);
```
#### [Sum of Odd Cubed Numbers](https://www.codewars.com/kata//580dda86c40fa6c45f00028a)
```javascript
// Solution 1
const cubeOdd = arr => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    if (typeof arr[i] !== 'number') return undefined;
  }
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] % 2) sum += arr[i] ** 3;
  }
  return sum;
};
// Solution 2
const cubeOdd = arr => {
  let sum = 0;
  let cubed = arr.map(item => item ** 3);
  cubed.forEach(el => el % 2 ? (sum += el) : (sum += 0));
  return cubed.includes(NaN) ? undefined : sum;
};
// Solution 3
const cubeOdd = arr => {
  arr = arr
    .filter(el => el % 2 !== 0)
    .reduce((acc, curr) => acc + curr ** 3, 0);
  return isNaN(arr) ? undefined : arr;
};
// Solution 4
const cubeOdd = arr =>
  !arr.some(isNaN)
    ? arr
      .map(el => el ** 3)
      .filter(el => el % 2)
      .reduce((acc, curr) => acc + curr, 0)
    : undefined;
```
#### [Odd or Even?](https://www.codewars.com/kata//5949481f86420f59480000e7)
```javascript
// Solution 1
const oddOrEven = arr => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum % 2 ? 'odd' : 'even';
};
// Solution 2
const oddOrEven = arr => {
  let sum = 0;
  arr.forEach(el => sum += el);
  return sum % 2 ? 'odd' : 'even';
};
// Solution 3
const oddOrEven = arr =>
  arr.reduce((acc, curr) => acc + curr, 0) % 2 ? 'odd' : 'even';
```
#### [Sum without highest and lowest number](https://www.codewars.com/kata//576b93db1129fcf2200001e6)
```javascript
// Solution 1
const sumArray = arr => {
  if (!arr || arr.length <= 1) return 0;
  let min = arr[0],
    max = arr[0],
    sum = arr[0];
  for (let i = 1; i < arr.length; i++) {
    if (arr[i] < min) min = arr[i];
    if (arr[i] > max) max = arr[i];
    sum += arr[i];
  }
  return sum - min - max;
};
// Solution 2
const sumArray = arr => {
  if (!arr || arr.length <= 1) return 0;
  let min = arr[0],
    max = arr[0],
    sum = 0;
  arr.forEach(el => {
    if (el < min) min = el;
    if (el > max) max = el;
    sum += el;
  });
  return sum - min - max;
};
// Solution 3
const sumArray = arr => {
  return Array.isArray(arr) && arr.length > 1
    ? arr.reduce((s, n) => s + n, 0) - Math.min(...arr) - Math.max(...arr)
    : 0;
};
// Solution 4
const sumArray = arr =>
  arr
    ? arr
      .sort((a, b) => a - b)
      .slice(1, -1)
      .reduce((acc, curr) => acc + curr, 0)
    : 0;
```
#### [Find Maximum and Minimum Values of a List](https://www.codewars.com/kata//577a98a6ae28071780000989)
```javascript
// Solution 1
const min = arr => Math.min(...arr),
  max = arr => Math.max(...arr);
// Solution 2
const min = arr => arr.sort((a, b) => a - b)[0],
  max = arr => arr.sort((a, b) => b - a)[0];
// Solution 3
const min = arr => {
  let min = arr[0];
  for (let i = 1; i < arr.length; i++) {
    if (arr[i] < min) min = arr[i];
  }
  return min;
};
const max = arr => {
  let max = arr[0];
  for (let i = 0; i < arr.length; i++) {
    if (max < arr[i]) max = arr[i];
  }
  return max;
};
```
#### [Remove the minimum](https://www.codewars.com/kata//563cf89eb4747c5fb100001b)
```javascript
// Solution 1
const removeSmallest = num => {
  let arr = [];
  let min = Math.min(...num);
  let index = num.indexOf(min);
  for (let i = 0; i < num.length; i++) {
    if (i !== index) arr.push(num[i]);
  }
  return arr;
};
// Solution 2
const removeSmallest = num => {
  let arr = [...num];
  let min = Math.min.apply(null, arr);
  arr.splice(arr.indexOf(min), 1);
  return arr;
};
// Solution 3
const removeSmallest = num => {
  let arr = num.concat();
  arr.splice(num.indexOf(Math.min(...num)), 1);
  return arr;
};
```
#### [Find the divisors!](https://www.codewars.com/kata//544aed4c4a30184e960010f4)
```javascript
// Solution 1
const divisors = num => {
  let arr = [];
  for (let i = 2; i < num; i++) {
    if (num % i === 0) arr.push(i);
  }
  return arr.length ? arr : `${num} is prime`;
};
// Solution 2
const divisors = num => {
  let arr = [...Array(num).keys()].slice(2, num).filter(el => num % el === 0);
  return arr.length > 0 ? arr : `${num} is prime`;
};
```
#### [Count by X](https://www.codewars.com/kata//5513795bd3fafb56c200049e)
```javascript
// Solution 1
const countBy = (x, n) => {
  let arr = [];
  for (let i = x, t = n; t > 0; i += x) {
    arr.push(i);
    t--;
  }
  return arr;
};
// Solution 2
const countBy = (x, n) => {
  let arr = [];
  for (let i = 1; i <= n; i++) {
    arr.push(x * i);
  }
  return arr;
};
// Solution 3
const countBy = (x, n) => {
  let arr = [];
  while (arr.length < n) arr.push(x * (arr.length + 1));
  return arr;
};
```
#### [Unfinished Loop - Bug Fixing #1](https://www.codewars.com/kata//55c28f7304e3eaebef0000da)
```javascript
// Solution 1
const createArray = num => {
  let arr = [];
  for (let i = 1; i <= num; i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const createArray = num =>
  Array(num)
    .fill(1)
    .map((el, i) => el + i);
// Solution 3
const createArray = num => Array(...Array(num)).map((el, i) => i + 1);
// Solution 4
const createArray = num => Array.from({ length: num }, (el, i) => i + 1);
```
#### [Training JS #10: loop statement --for](https://www.codewars.com/kata//5721a78c283129e416000999)
```javascript
// Solution 1
const pickIt = arr => {
  const odd = [],
    even = [];
  for (let i = 0; i < arr.length; i++) {
    arr[i] % 2 ? odd.push(arr[i]) : even.push(arr[i]);
  }
  return [odd, even];
};
// Solution 2
const pickIt = arr => {
  const odd = [],
    even = [];
  for (let el of arr) (el % 2 ? odd : even).push(el);
  return [odd, even];
};
// Solution 3
const pickIt = arr => {
  const oddEven = [[], []];
  for (let el of arr) oddEven[~el & 1].push(el);
  return oddEven;
};
/*
const pickIt = arr => {
  const odd = [],
    even = [];
  arr.forEach(el => el % 2 ? odd.push(el) : even.push(el));
  return [odd, even];
};

const pickIt = arr => [
  arr.filter(el => el % 2),
  arr.filter(el => !(el % 2)),
];
*/
```
#### [Pre-FizzBuzz Workout #1](https://www.codewars.com/kata//569e09850a8e371ab200000b)
```javascript
// Solution 1
const preFizz = num => {
  let arr = [];
  for (let i = 1; i <= num; i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const preFizz = num =>
  Array(num)
    .fill(1)
    .map((el, i) => el + i);
// Solution 3
const preFizz = num => Array(...Array(num)).map((el, i) => ++i);
// Solution 4
const preFizz = num => Array.from({ length: num }, (el, i) => ++i);
```
#### [Powers of 2](https://www.codewars.com/kata//57a083a57cb1f31db7000028)
```javascript
// Solution 1
const powersOfTwo = num => {
  const arr = [];
  for (let i = 0; i <= num; i++) {
    arr.push(2 ** i);
  }
  return arr;
};
// Solution 2
const powersOfTwo = num => [...Array(++num)].map((_, i) => 2 ** i);
// Solution 3
const powersOfTwo = num =>
  Array(++num)
    .fill(0)
    .map((_, i) => 2 ** i);
// Solution 4
const powersOfTwo = num => Array.from({ length: ++num }, (_, i) => 2 ** i);
```
#### [Reversed sequence](https://www.codewars.com/kata//5a00e05cc374cb34d100000d)
```javascript
// Solution 1
const reverseSeq = num => {
  let arr = [];
  for (let i = num; i > 0; i--) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const reverseSeq = num =>
  Array(num)
    .fill(0)
    .map(() => num--);
// Solution 3
const reverseSeq = num => Array.from({ length: num }, () => num--);
// Solution 4
const reverseSeq = num => Array.from({ length: num }, (_, i) => ++i).reverse();
// Solution 5
const reverseSeq = num => [...Array(num)].map(() => num--);
// Solution 6
const reverseSeq = num => [...Array(num).keys()].map(() => num--);
// Solution 7
const reverseSeq = num => [...Array(num).keys()].map(el => ++el).reverse();
// Solution 8
const reverseSeq = num => num < 2 ? [num] : [num].concat(reverseSeq(--num));
```
#### [Training JS #4: Basic data types--Array](https://www.codewars.com/kata//571effabb625ed9b0600107a)
```javascript
const getLength = arr => arr.length;

const getFirst = arr => arr.shift();
// const getFirst = arr => arr[0];

const getLast = arr => arr.pop();
// const getLast = arr => arr.slice(-1)[0];
// const getLast = arr => arr[arr.length - 1];

const pushElement = arr => (arr.push(0), arr);
// const pushElement = arr => arr.concat(0);

const popElement = arr => (arr.pop(), arr);
// const popElement = arr => arr.slice(0, -1);
```
#### [No Loops 2 - You only need one](https://www.codewars.com/kata//57cc40b2f8392dbf2a0003ce)
```javascript
const check = (arr, el) => arr.includes(el);
```
#### [You only need one - Beginner](https://www.codewars.com/kata//57cc975ed542d3148f00015b)
```javascript
const check = (arr, el) => arr.includes(el);
```
#### [Be Concise IV - Index of an element in an array](https://www.codewars.com/kata//5703c093022cd1aae90012c9)
```javascript
// Solution 1
const find = (arr, el, i = arr.indexOf(el)) => i < 0 ? 'Not found' : i;
// Solution 2
const find = (arr, el, i = arr.indexOf(el)) => i >= 0 ? i : 'Not found';
// Solution 3
const find = (arr, el) => (el = arr.indexOf(el)) >= 0 ? el : 'Not found';
// Solution 4
const find = (arr, el) => arr.includes(el) ? arr.indexOf(el) : 'Not found';
// Solution 5
const find = (arr, el) => (el => el >= 0 ? el : 'Not found')(arr.indexOf(el));
```
#### [Find numbers which are divisible by given number](https://www.codewars.com/kata//55edaba99da3a9c84000003b)
```javascript
// Solution 1
const divisibleBy = (num, div) => num.filter(el => el % div === 0);
// Solution 2
const divisibleBy = (num, div) => num.filter(el => !(el % div));
```
# CodeWars
#### [Multiply](https://www.codewars.com/kata//50654ddff44f800200000004)
```javascript
const multiply = (a, b) => a * b;
```
#### [Draw stairs](https://www.codewars.com/kata//5b4e779c578c6a898e0005c5)
```javascript
// Solution 1
const drawStairs = num => {
  let res = '';
  for (let i = 1; i <= num; i++) {
    res += i === num ? 'I' : 'I\n' + ' '.repeat(i);
  }
  return res;
};
// Solution 2
const drawStairs = num => {
  let stairs = '',
    space = ' ';
  for (let i = 0; i < num - 1; i++) {
    stairs += 'I\n' + space;
    space += ' ';
  }
  return stairs + 'I';
};
// Solution 3
const drawStairs = num =>
  [...Array(num)].map((_, i) => ' '.repeat(i) + 'I').join('\n');
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
const howMuchILoveYou = num => {
  const fl = [
    'I love you',
    'a little',
    'a lot',
    'passionately',
    'madly',
    'not at all'
  ];
  return fl[(num - 1) % 6];
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
const angle = num => 180 * (num - 2);
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
const simpleMultiplication = num => num * (8 + num % 2);
// Solution 2
const simpleMultiplication = num => num * (8 + (num & 1));
// Solution 3
const simpleMultiplication = num => num * (num % 2 ? 9 : 8);
// Solution 4
const simpleMultiplication = num => num * (8 + (num % 2 !== 0));
// Solution 5
const simpleMultiplication = num => num % 2 ? num * 9 : num * 8;
// Solution 6
const simpleMultiplication = num => (num << 3) + (num & 1) * num;
// Solution 7
const simpleMultiplication = num => !(num % 2) ? num * 8 : num * 9;
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
const numberToString = num => num.toString();
// Solution 2
const numberToString = num => String(num);
// Solution 3
const numberToString = num => num + '';
// Solution 4
const numberToString = num => `${num}`;
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
const twoDecimalPlaces = num => +num.toFixed(2);
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
const oddCount = num => Math.floor(num / 2);
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
const hoopCount = num => num >= 10 ? 'Great, now move on to tricks' : 'Keep at it until you get it';
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
const even_or_odd = num => ['Even', 'Odd'][num % 2];
// Solution 2
const even_or_odd = num => ['Even', 'Odd'][num & 1];
// Solution 3
const even_or_odd = num => (num % 2 ? 'Odd' : 'Even');
// Solution 4
const even_or_odd = num => (num & 1 ? 'Odd' : 'Even');
// Solution 5
const even_or_odd = num => ['Even', 'Odd'][!(num % 2)];
// Solution 6
const even_or_odd = num => (!(num % 2) ? 'Even' : 'Odd');
// Solution 7
const even_or_odd = num => ['Even', 'Odd'][Math.abs(num) % 2];
// Solution 8
const even_or_odd = num => (Math.abs(num) % 2 ? 'Odd' : 'Even');
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
const getRealFloor = num => (num <= 0 ? num : num - (num >= 13 ? 2 : 1));
// Solution 2
const getRealFloor = num => (num <= 0 ? num : num < 13 ? num - 1 : num - 2);
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
  return name === 'Santa Claus' && password === 'Ho Ho Ho!';
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
  return name === 'Santa Claus' && password === 'Ho Ho Ho!';
}
// Solution 4
function Sleigh() {
  this.name = 'Santa Claus';
  this.password = 'Ho Ho Ho!';
}
Sleigh.prototype.authenticate = function(name, password) {
  return this.name === name && this.password === password;
}
// Solution 5
class Sleigh {
  authenticate(name, password) {
    return name === 'Santa Claus' && password === 'Ho Ho Ho!';
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
const isDivideBy = (num, a, b) => num % a === 0 && num % b === 0;
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
const setAlarm = (employed, vacation) =>
  employed === true && vacation === false;
// Solution 2
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
const howManyDalmatians = num =>
  num <= 10
    ? dogs[0]
    : num <= 50
    ? dogs[1]
    : num <= 100
    ? dogs[2]
    : dogs[3];
```
#### [Training JS #7: if..else and ternary operator](https://www.codewars.com/kata//57202aefe8d6c514300001fd)
```javascript
// Solution 1
const saleHotdogs = num => (num < 5 ? num * 100 : num >= 5 && num < 10 ? num * 95 : num * 90);
// Solution 2
const saleHotdogs = num => num * (num < 5 ? 100 : num < 10 ? 95 : 90);
```
#### [Be Concise I - The Ternary Operator](https://www.codewars.com/kata//56f3f6a82010832b02000f38)
```javascript
const describeAge = a => `You're a(n) ${a < 13 ? 'kid' : a < 18 ? 'teenager' : a < 65 ? 'adult' : 'elderly'}`;
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
  const cases = {
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
const switchItUp = num =>
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
  ][num];
// Solution 2
const switchItUp = num =>
  'Zero One Two Three Four Five Six Seven Eight Nine'.split(' ')[num];
// Solution 2
const switchItUp = num => {
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
  return words[num];
};
// Solution 3
const switchItUp = num => {
  switch (num) {
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
const switchItUp = num => {
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
  }[num];
};
// Solution 5
const switchItUp = num =>
  num === 1
    ? 'One'
    : num === 2
    ? 'Two'
    : num === 3
    ? 'Three'
    : num === 4
    ? 'Four'
    : num === 5
    ? 'Five'
    : num === 6
    ? 'Six'
    : num === 7
    ? 'Seven'
    : num === 8
    ? 'Eight'
    : num === 9
    ? 'Nine'
    : num === 0
    ? 'Zero'
    : '0-9 only!';
```
#### [No zeros for heros](https://www.codewars.com/kata//570a6a46455d08ff8d001002)
```javascript
// Solution 1
const noBoringZeros = num => {
  while (num % 10 === 0 && num !== 0) {
    num = num / 10;
  }
  return num;
};
// Solution 2
const noBoringZeros = num => +`${num}`.replace(/0+$/, '');
// Solution 3
const noBoringZeros = num => +(num + '').replace(/0*$/, '');
// Solution 4
const noBoringZeros = num => +String(num).replace(/[0]+$/g, '');
// Solution 5
const noBoringZeros = num => Number(num.toString().replace(/0+$/g, ''));
// Solution 6
const noBoringZeros = num => (!num || num % 10 ? num : noBoringZeros(num / 10));
// Solution 7
const noBoringZeros = num => (num % 10 || num === 0 ? num : noBoringZeros(num / 10));
```
#### [Power of two](https://www.codewars.com/kata//534d0a229345375d520006a0)
```javascript
// Solution 1
const isPowerOfTwo = num => {
  while (num % 2 === 0 && num !== 0) {
    num /= 2;
  }
  return num === 1;
};
// Solution 2
const isPowerOfTwo = num => !(num & num - 1);
// Solution 3
const isPowerOfTwo = num => (num & num - 1) === 0;
// Solution 4
const isPowerOfTwo = num => (num & ~num + 1) === num;
// Solution 5
const isPowerOfTwo = num => Math.log2(num) % 1 === 0;
// Solution 6
const isPowerOfTwo = num => /^10*$/.test(num.toString(2));
// Solution 7
const isPowerOfTwo = num => Number.isInteger(Math.log2(num));
// Solution 8
const isPowerOfTwo = num => num === 0 ? false : (num & num - 1) === 0;
// Solution 9
const isPowerOfTwo = num => num === 1 ? true : num < 1 ? false : isPowerOfTwo(num / 2);
```
#### [Difference Of Squares](https://www.codewars.com/kata//558f9f51e85b46e9fa000025)
```javascript
// Solution 1
const differenceOfSquares = num => num * (num * num - 1) * (3 * num + 2) / 12;
// Solution 2
const differenceOfSquares = num => Math.pow(num * (num + 1) / 2, 2) - num * (num + 1) * (2 * num + 1) / 6;
// Solution 
const differenceOfSquares = num => num * num * (num + 1) * (num + 1) / 4 - num * (num + 1) * (2 * num + 1) / 6;
// Solution 4
const differenceOfSquares = num => {
  let sum = 0, sumSquares = 0;
    while (num > 0) {
    sum += num;
    sumSquares += Math.pow(num, 2);
    num--;
  }
  let squareSum = Math.pow(sum, 2)
  return squareSum - sumSquares;
};
```
#### [Factorial](https://www.codewars.com/kata//57a049e253ba33ac5e000212)
```javascript
const factorial = num => num > 1 ? num * factorial(--num) : 1;
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
const SeriesSum = num => {
  let sum = 0;
  for (let i = 0; i < num; i++) {
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
const money = 10,
  candy = 1.42,
  chips = 2.4,
  soda = 1,
  change = money - candy - chips - soda;
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
const numberToPower = (num, pow) => {
  let sum = 1;
  for (let i = 1; i <= pow; i++) sum *= num;
  return sum;
};
// Solution 2
const numberToPower = (num, pow) =>
  pow > 0 ? num * numberToPower(num, pow - 1) : 1;
// Solution 3
const numberToPower = (num, pow) =>
  Array(pow)
    .fill(num)
    .reduce((acc, curr) => acc * curr, 1);
```
#### [Is it a palindrome?](https://www.codewars.com/kata//57a1fd2ce298a731b20006a4)
```javascript
const isPalindrome = str => (str = str.toLowerCase()) === str.split('').reverse().join('');
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
const SafeInteger = num => Number.isSafeInteger(num);
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
const opposite = num => -num;
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
// Solution 1
const findChildren = (santasList, children) => [
  ...new Set(children.filter(el => santasList.includes(el)).sort()),
];
// Solution 2
const findChildren = (santasList, children) =>
  children
    .filter((el, i, arr) => santasList.includes(el) && i === arr.indexOf(el))
    .sort();
// Solution 3
const findChildren = (santasList, children) => {
  const arr = [];
  for (let item of santasList) {
    for (let child of children) {
      if (item === child && !arr.includes(item)) arr.push(item);
    }
  }
  return arr.sort();
};
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
#### [Holiday VIII - Duty Free](https://www.codewars.com/kata//57e92e91b63b6cbac20001e5)
```javascript
// Solution 1
const dutyFree = (normPrice, discount, hol) =>
  Math.floor((hol * 100) / (normPrice * discount));
// Solution 2
const dutyFree = (normPrice, discount, hol) =>
  Math.floor(hol / ((normPrice * discount) / 100));
// Solution 3
const dutyFree = (normPrice, discount, hol) =>
  Math.floor((hol / normPrice / discount) * 100);
// Solution 4
const dutyFree = (normPrice, discount, hol) =>
  hol / ((normPrice * discount) / 100) ^ 0;
// Solution 5
const dutyFree = (normPrice, discount, hol) =>
  ~~((100 * hol) / normPrice / discount);
// Solution 6
const dutyFree = (normPrice, discount, hol) =>
  (hol / normPrice / discount) * 100 | 0;
```
#### [All Star Code Challenge #22]()
```javascript
// Solution 1
const toTime = (seconds, hr = seconds / 3600, min = (hr - parseInt(hr)) * 60) =>
  `${Math.floor(hr)} hour(s) and ${Math.floor(min)} minute(s)`;
// Solution 2
const toTime = (seconds, hr = seconds / 3600, min = (seconds % 3600) / 60) =>
  `${Math.floor(hr)} hour(s) and ${Math.floor(min)} minute(s)`;
// Solution 3
const toTime = (seconds, hr = seconds / 3600, min = (seconds % 3600) / 60) =>
  `${Math.trunc(hr)} hour(s) and ${Math.trunc(min)} minute(s)`;
// Solution 4
const toTime = (seconds, min = seconds / 60 | 0, hr = min / 60 | 0) =>
  `${hr} hour(s) and ${min - hr * 60} minute(s)`;
// Solution 5
const toTime = seconds =>
  `${Math.floor(seconds / 3600)} hour(s) and ${Math.floor(
    (seconds % 3600) / 60
  )} minute(s)`;
// Solution 6
const toTime = seconds =>
  `${seconds / 3600 | 0} hour(s) and ${
    (seconds % 3600) / 60 | 0
  } minute(s)`;
// Solution 7
const toTime = seconds =>
  `${seconds / 3600 | 0} hour(s) and ${(seconds / 60) % 60 | 0} minute(s)`;
```
#### [Formatting decimal places #1](https://www.codewars.com/kata//5641c3f809bf31f008000042)
```javascript
// Solution 1
const twoDecimalPlaces = num => +num.toFixed(4).slice(0, -2);
// Solution 2
const twoDecimalPlaces = num => Math.trunc(num * 100) / 100;
// Solution 3
const twoDecimalPlaces = num => parseInt(num * 100) / 100;
// Solution 4
const twoDecimalPlaces = num => (num * 100 | 0) / 100;
// Solution 5
const twoDecimalPlaces = num => ~~(num * 100) / 100;
```
#### [Tortoise racing](https://www.codewars.com/kata//55e2adece53b4cdcb900006c)
```javascript
// Solution 1
const race = (v1, v2, g, t) =>
  v1 >= v2
    ? null
    : ((t = new Date((g / (v2 - v1)) * 3600 * 1000)),
    [t.getHours(), t.getMinutes(), t.getSeconds()]);
// Solution 2
const race = (v1, v2, g, t = g / (v2 - v1)) =>
  v1 >= v2 ? null : [t | 0, (t * 60) % 60 | 0, Math.trunc(t * 3600) % 60];
// Solution 3
const race = (v1, v2, g, t = g / (v2 - v1)) =>
  t >= 0 ? [t, (t * 60) % 60, (t * 3600) % 60].map(Math.floor) : null;
// Solution 4
const race = (v1, v2, g, t = g / (v2 - v1)) =>
  t >= 0 ? [~~t, ~~((t * 60) % 60), ~~((t * 60 ** 2) % 60)] : null;
// Solution 5
const race = (v1, v2, g, t = g / (v2 - v1)) =>
  t >= 0 ? [t | 0, (t * 60 | 0) % 60, (t * 3600 | 0) % 60] : null;
```
#### [Lario and Muigi Pipe Problem](https://www.codewars.com/kata//56b29582461215098d00000f)
```javascript
// Solution 1
const pipeFix = num => {
  const arr = [];
  for (let i = Math.min(...num); i <= Math.max(...num); i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const pipeFix = num => {
  const arr = [];
  for (let i = num[0]; i <= Math.max(...num); i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 3
const pipeFix = num => {
  const arr = [];
  for (let i = num[0]; i <= num[num.length - 1]; i++) {
    arr.push(i);
  }
  return arr;
};
```
#### [Expressions Matter](https://www.codewars.com/kata//5ae62fcf252e66d44d00008e)
```javascript
const expressionMatter = (a, b, c) =>
  Math.max(
    a + b + c,
    a * b * c,
    a + b * c,
    (a + b) * c,
    a * b + c,
    a * (b + c)
  );
```
#### [Convert to Binary](https://www.codewars.com/kata//59fca81a5712f9fa4700159a)
```javascript
const toBinary = num => +num.toString(2);
```
#### [Binary Addition](https://www.codewars.com/kata//551f37452ff852b7bd000139)
```javascript
const addBinary = (a, b) => (a + b).toString(2);
```
#### [Calculate Price Excluding VAT](https://www.codewars.com/kata//5890d8bc9f0f422cf200006b)
```javascript
// Solution 1
const excludingVatPrice = price =>
  price === null ? -1 : +(price / 1.15).toFixed(2);
// Solution 2
const excludingVatPrice = price =>
  price !== null ? +(price / 1.15).toFixed(2) : -1;
```
#### [Parse nice int from char problem](https://www.codewars.com/kata//557cd6882bfa3c8a9f0000c1)
```javascript
const getAge = inputString => parseInt(inputString, 10);
```
#### [Hex to Decimal](https://www.codewars.com/kata//57a4d500e298a7952100035d)
```javascript
const hexToDec = h => parseInt(h, 16);
```
#### [Bin to Decimal](https://www.codewars.com/kata//57a5c31ce298a7e6b7000334)
```javascript
const binToDec = bin => parseInt(bin, 2);
```
#### [Parse float](https://www.codewars.com/kata//57a386117cb1f31890000039)
```javascript
// Soliution 1
const parseF = s => !isNaN(parseFloat(s)) ? parseFloat(s) : null;
// Soliution 2
const parseF = s => isNaN(parseFloat(s)) ? null : parseFloat(s);
// Soliution 3
const parseF = s => !isNaN(s = parseFloat(s)) ? s : null;
// Soliution 4
const parseF = s => isNaN(s = parseFloat(s)) ? null : s;
```
#### [Sum Arrays](https://www.codewars.com/kata//53dc54212259ed3d4f00071c)
```javascript
// Solution 1
const sum = num => {
  'use strict';
  let sum = 0;
  for (let i = 0; i < num.length; i++) {
    sum += num[i];
  }
  return sum;
};
// Solution 2
const sum = num => num.reduce((acc, curr) => acc + curr, 0);
```
#### [Count the Monkeys!](https://www.codewars.com/kata//56f69d9f9400f508fb000ba7)
```javascript
// Solution 1
const monkeyCount = num => {
  const arr = [];
  for (let i = 1; i <= num; i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const monkeyCount = num => [...Array(++num).keys()].slice(1);
// Solution 3
const monkeyCount = num => [...Array(num)].map((_, i) => ++i);
// Solution 4
const monkeyCount = num => [...Array(num).keys()].map(i => ++i);
// Solution 5
const monkeyCount = num => Array(num).fill().map((_, i) => ++i);
// Solution 6
const monkeyCount = num => Array.from(Array(++num).keys()).slice(1);
// Solution 7
const monkeyCount = num => [...new Array(++num).keys()].filter(i => i > 0);
```
#### [Filling an array (part 1)](https://www.codewars.com/kata//571d42206414b103dc0006a1)
```javascript
// Solution 1
const arr = num => {
  const arr = [];
  for (let i = 0; i < num; i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const arr = num => [...Array(num || 0).keys()];
// Solution 3
const arr = (num = 0) => [...Array(num).keys()];
// Solution 4
const arr = num => num ? [...Array(num).keys()] : [];
// Solution 5
const arr = num => Array.from({ length: num }, (_, i) => i);
```
#### [What is type of variable?](https://www.codewars.com/kata//57293671c98f77e84b000065)
```javascript
//Solution 1
const type = value => ({}).toString.call(value).slice(8, -1).toLowerCase();
//Solution 2
const type = value =>
  Object.prototype.toString.call(value).slice(8, -1).toLowerCase();
//Solution 3
const type = value =>
  ({}).toString
    .call(value)
    .match(/\s([a-zA-Z]+)/)[1]
    .toLowerCase();
//Solution 4
const type = value =>
  ({}).toString
    .call(value)
    .match(/(\w+)]/)[1]
    .toLowerCase();
```
#### [Is every value in the array an array?](https://www.codewars.com/kata//582c81d982a0a65424000201)
```javascript
const arrCheck = value => value.every(Array.isArray);
```
#### [Enumerable Magic #3 - Does My List Include This?](https://www.codewars.com/kata//545991b4cbae2a5fda000158)
```javascript
// Solution 1
const include = (arr, item) => {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === item) return true;
  }
  return false;
};
// Solution 2
const include = Array.includes;
// Solution 3
const include = (arr, item) => arr.includes(item);
// Solution 4
const include = (arr, item) => new Set(arr).has(item);
// Solution 5
const include = (arr, item) => arr.indexOf(item) > -1;
// Solution 6
const include = (arr, item) => arr.indexOf(item) >= 0;
// Solution 7
const include = (arr, item) => arr.indexOf(item) !== -1;
// Solution 8
const include = (arr, item) => arr.some(el => el === item);
// Solution 9
const include = (arr, item) => Boolean(~arr.indexOf(item));
// Solution 10
const include = (arr, item) => arr.find(el => el === item) === item;
```
#### [Counting sheep...](https://www.codewars.com/kata//54edbc7200b811e956000556)
```javascript
// Solution 1
const countSheeps = (arrayOfSheep, count = 0) => {
  for (let i = 0; i < arrayOfSheep.length; i++)
    if (arrayOfSheep[i] === true) count++;
  return count;
};
// Solution 2
const countSheeps = (arrayOfSheep, count = 0) => {
  for (let i in arrayOfSheeps) {
    arrayOfSheeps[i] ? count++ : null;
  }
  return count;
};
// Solution 3
const countSheeps = arrayOfSheeps => arrayOfSheeps.filter(Boolean).length;
// Solution 4
const countSheeps = arrayOfSheeps => arrayOfSheeps.filter(el => el).length;
// Solution 5
const countSheeps = arrayOfSheeps =>
  !arrayOfSheeps ? 0 : arrayOfSheeps.reduce((acc, curr) => curr ? ++acc : acc, 0);
```
#### [A Needle in the Haystack](https://www.codewars.com/kata//56676e8fabd2d1ff3000000c)
```javascript
// Solution 1
const findNeedle = haystack =>
  `found the needle at position ${haystack.indexOf('needle')}`;
// Solution 2
const findNeedle = haystack => {
  for (let i = 0; i < haystack.length; i++) {
    if (haystack[i] === 'needle') return `found the needle at position ${i}`;
  }
};
```
#### [Difference of Volumes of Cuboids](https://www.codewars.com/kata//58cb43f4256836ed95000f97)
```javascript
// Solution 1
const findDifference = (a, b) =>
  Math.abs(
    a.reduce((acc, curr) => acc * curr) - b.reduce((acc, curr) => acc * curr)
  );
// Solution 2
const findDifference = (a, b) =>
  Math.abs(a[0] * a[1] * a[2] - b[0] * b[1] * b[2]);
// Solution 3
const findDifference = (a, b) => (
  (c = (a, b) => a * b), Math.abs(a.reduce(c) - b.reduce(c))
);
// Solution 3
const findDifference = (a, b) =>
  Math.abs(
    a.reduce((acc, curr) => acc * curr) - b.reduce((acc, curr) => acc * curr)
  );
// Solution 4
const findDifference = (a, b, A = 1, B = 1) => {
  a.map(el => A *= el);
  b.map(el => B *= el);
  return Math.abs(A - B);
};
// Solution 5
const findDifference = (a, b) => {
  let A = a.reduce((acc, curr) => acc * curr);
  let B = b.reduce((acc, curr) => acc * curr);
  return Math.abs(A - B);
};
// Solution 6
const findDifference = (a, b, A = 1, B = 1) => {
  for (let i = 0; i < 3; i++) {
    A *= a[i];
    B *= b[i];
  }
  return Math.abs(A - B);
};
```
#### [Find the smallest integer in the array](https://www.codewars.com/kata//55a2d7ebe362935a210000b2)
```javascript
class SmallestIntegerFinder {
  findSmallestInt(args) {
    return Math.min(...args);
  }
}
```
#### [Find the first non-consecutive number](https://www.codewars.com/kata//58f8a3a27a5c28d92e000144)
```javascript
// Solution 1
const firstNonConsecutive = arr => {
  for (let i = 0; i < arr.length - 1; ++i) {
    if (arr[i] + 1 !== arr[i + 1]) return arr[i + 1];
  }
  return null;
};
// Solution 2
const firstNonConsecutive = arr => {
  const res = arr.find((el, i) => el !== i + arr[0]);
  return Number.isInteger(res) ? res : null;
};
// Solution 3
const firstNonConsecutive = arr =>
  arr.length === 1
    ? null
    : arr[0] + 1 !== arr[1]
      ? arr[1]
      : firstNonConsecutive(arr.slice(1));
```
#### [Total amount of points](https://www.codewars.com/kata//5bb904724c47249b10000131)
```javascript
// Solution 1
const points = games => {
  let count = 0;
  games.forEach(item => {
    if (item[0] > item[2]) count += 3;
    if (item[0] === item[2]) count++;
  });
  return count;
};
// Solution 2
const points = games => {
  let count = 0;
  for (let i = 0; i < games.length; i++) {
    if (games[i][0] > games[i][2]) count += 3;
    if (games[i][0] === games[i][2]) count++;
  }
  return count;
};
// Solution 3
const points = games =>
  games.reduce((acc, curr) => {
    return acc += curr[0] > curr[2] ? 3 : curr[0] === curr[2] ? 1 : 0;
  }, 0);
```
#### [Enumerable Magic #2 - True for Any?](https://www.codewars.com/kata//54598e89cbae2ac001001135)
```javascript
const any = (arr, fun) => arr.some(fun);
```
#### [Square(n) Sum](https://www.codewars.com/kata//515e271a311df0350d00000f)
```javascript
// Solution 1
const squareSum = num => {
  let sum = 0;
  for (let i = 0; i < num.length; i++) {
    sum += Math.pow(num[i], 2);
  }
  return sum;
};
// Solution 2
const squareSum = num => {
  let sum = 0;
  num.forEach(el => sum += el ** 2);
  return sum;
};
// Solution 3
const squareSum = num =>
  num.reduce((acc, curr) => acc + curr * curr, 0);
```
#### [How good are you really?](https://www.codewars.com/kata//5601409514fc93442500010b)
```javascript
// Solution 1
const betterThanAverage = (classPoints, yourPoints) => {
  let sum = 0;
  for (let i = 0; i < classPoints.length; i++) {
    sum += classPoints[i];
  }
  return sum / classPoints.length < yourPoints;
};
//2 Solution
const betterThanAverage = (classPoints, yourPoints) => {
  let sum = 0;
  classPoints.forEach(el => sum += el);
  return sum / classPoints.length < yourPoints;
};
// Solution 3
const betterThanAverage = (classPoints, yourPoints) =>
  classPoints.reduce((acc, curr) => acc + curr, 0) / classPoints.length < yourPoints;
```
#### [Sum of positive](https://www.codewars.com/kata//5715eaedb436cf5606000381)
```javascript
// Solution 1
const positiveSum = arr => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > 0) sum += arr[i];
  }
  return sum;
};
// Solution 2
const positiveSum = arr => {
  let sum = 0;
  arr.forEach(el => el > 0 ? sum += el : 0);
  return sum;
};
// Solution 3
const positiveSum = arr => arr.reduce((acc, curr) => acc + (curr > 0 && curr), 0);
```
#### [Calculate average](https://www.codewars.com/kata//57a2013acf1fa5bfc4000921)
```javascript
// Solution 1
const find_average = arr => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum / arr.length;
};
// Solution 2
const find_average = arr => {
  let sum = 0;
  arr.forEach(el => sum += el);
  return sum / arr.length;
};
// Solution 3
const find_average = arr => arr.reduce((acc, curr) => acc + curr, 0) / arr.length;
```
#### [Divide and Conquer](https://www.codewars.com/kata//57eaec5608fed543d6000021)
```javascript
// Solution 1
const divCon = arr => {
  let sumNum = 0;
  let sumStr = 0;
  for (let i = 0; i < arr.length; i++) {
    +arr[i] === arr[i] ? sumNum += arr[i] : sumStr += +arr[i];
  }
  return sumNum - sumStr;
};
// Solution 2
const divCon = arr => {
  let sumNum = 0;
  let sumStr = 0;
  arr.forEach(el => +el === el ? sumNum += el : sumStr += +el);
  return sumNum - sumStr;
};
// Solution 3
const divCon = arr =>
  arr.reduce((acc, curr) => +curr === curr ? acc + curr : acc - +curr, 0);
```
#### [Sum of Odd Cubed Numbers](https://www.codewars.com/kata//580dda86c40fa6c45f00028a)
```javascript
// Solution 1
const cubeOdd = arr => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    if (typeof arr[i] !== 'number') return undefined;
  }
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] % 2) sum += arr[i] ** 3;
  }
  return sum;
};
// Solution 2
const cubeOdd = arr => {
  let sum = 0;
  let cubed = arr.map(item => item ** 3);
  cubed.forEach(el => el % 2 ? (sum += el) : (sum += 0));
  return cubed.includes(NaN) ? undefined : sum;
};
// Solution 3
const cubeOdd = arr => {
  arr = arr
    .filter(el => el % 2 !== 0)
    .reduce((acc, curr) => acc + curr ** 3, 0);
  return isNaN(arr) ? undefined : arr;
};
// Solution 4
const cubeOdd = arr =>
  !arr.some(isNaN)
    ? arr
      .map(el => el ** 3)
      .filter(el => el % 2)
      .reduce((acc, curr) => acc + curr, 0)
    : undefined;
```
#### [Odd or Even?](https://www.codewars.com/kata//5949481f86420f59480000e7)
```javascript
// Solution 1
const oddOrEven = arr => {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum % 2 ? 'odd' : 'even';
};
// Solution 2
const oddOrEven = arr => {
  let sum = 0;
  arr.forEach(el => sum += el);
  return sum % 2 ? 'odd' : 'even';
};
// Solution 3
const oddOrEven = arr =>
  arr.reduce((acc, curr) => acc + curr, 0) % 2 ? 'odd' : 'even';
```
#### [Sum without highest and lowest number](https://www.codewars.com/kata//576b93db1129fcf2200001e6)
```javascript
// Solution 1
const sumArray = arr => {
  if (!arr || arr.length <= 1) return 0;
  let min = arr[0],
    max = arr[0],
    sum = arr[0];
  for (let i = 1; i < arr.length; i++) {
    if (arr[i] < min) min = arr[i];
    if (arr[i] > max) max = arr[i];
    sum += arr[i];
  }
  return sum - min - max;
};
// Solution 2
const sumArray = arr => {
  if (!arr || arr.length <= 1) return 0;
  let min = arr[0],
    max = arr[0],
    sum = 0;
  arr.forEach(el => {
    if (el < min) min = el;
    if (el > max) max = el;
    sum += el;
  });
  return sum - min - max;
};
// Solution 3
const sumArray = arr => {
  return Array.isArray(arr) && arr.length > 1
    ? arr.reduce((s, n) => s + n, 0) - Math.min(...arr) - Math.max(...arr)
    : 0;
};
// Solution 4
const sumArray = arr =>
  arr
    ? arr
      .sort((a, b) => a - b)
      .slice(1, -1)
      .reduce((acc, curr) => acc + curr, 0)
    : 0;
```
#### [Find Maximum and Minimum Values of a List](https://www.codewars.com/kata//577a98a6ae28071780000989)
```javascript
// Solution 1
const min = arr => Math.min(...arr),
  max = arr => Math.max(...arr);
// Solution 2
const min = arr => arr.sort((a, b) => a - b)[0],
  max = arr => arr.sort((a, b) => b - a)[0];
// Solution 3
const min = arr => {
  let min = arr[0];
  for (let i = 1; i < arr.length; i++) {
    if (arr[i] < min) min = arr[i];
  }
  return min;
};
const max = arr => {
  let max = arr[0];
  for (let i = 0; i < arr.length; i++) {
    if (max < arr[i]) max = arr[i];
  }
  return max;
};
```
#### [Remove the minimum](https://www.codewars.com/kata//563cf89eb4747c5fb100001b)
```javascript
// Solution 1
const removeSmallest = num => {
  let arr = [];
  let min = Math.min(...num);
  let index = num.indexOf(min);
  for (let i = 0; i < num.length; i++) {
    if (i !== index) arr.push(num[i]);
  }
  return arr;
};
// Solution 2
const removeSmallest = num => {
  let arr = [...num];
  let min = Math.min.apply(null, arr);
  arr.splice(arr.indexOf(min), 1);
  return arr;
};
// Solution 3
const removeSmallest = num => {
  let arr = num.concat();
  arr.splice(num.indexOf(Math.min(...num)), 1);
  return arr;
};
```
#### [Find the divisors!](https://www.codewars.com/kata//544aed4c4a30184e960010f4)
```javascript
// Solution 1
const divisors = num => {
  let arr = [];
  for (let i = 2; i < num; i++) {
    if (num % i === 0) arr.push(i);
  }
  return arr.length ? arr : `${num} is prime`;
};
// Solution 2
const divisors = num => {
  let arr = [...Array(num).keys()].slice(2, num).filter(el => num % el === 0);
  return arr.length > 0 ? arr : `${num} is prime`;
};
```
#### [Count by X](https://www.codewars.com/kata//5513795bd3fafb56c200049e)
```javascript
// Solution 1
const countBy = (x, n) => {
  let arr = [];
  for (let i = x, t = n; t > 0; i += x) {
    arr.push(i);
    t--;
  }
  return arr;
};
// Solution 2
const countBy = (x, n) => {
  let arr = [];
  for (let i = 1; i <= n; i++) {
    arr.push(x * i);
  }
  return arr;
};
// Solution 3
const countBy = (x, n) => {
  let arr = [];
  while (arr.length < n) arr.push(x * (arr.length + 1));
  return arr;
};
```
#### [Unfinished Loop - Bug Fixing #1](https://www.codewars.com/kata//55c28f7304e3eaebef0000da)
```javascript
// Solution 1
const createArray = num => {
  let arr = [];
  for (let i = 1; i <= num; i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const createArray = num =>
  Array(num)
    .fill(1)
    .map((el, i) => el + i);
// Solution 3
const createArray = num => Array(...Array(num)).map((el, i) => i + 1);
// Solution 4
const createArray = num => Array.from({ length: num }, (el, i) => i + 1);
```
#### [Training JS #10: loop statement --for](https://www.codewars.com/kata//5721a78c283129e416000999)
```javascript
// Solution 1
const pickIt = arr => {
  const odd = [],
    even = [];
  for (let i = 0; i < arr.length; i++) {
    arr[i] % 2 ? odd.push(arr[i]) : even.push(arr[i]);
  }
  return [odd, even];
};
// Solution 2
const pickIt = arr => {
  const odd = [],
    even = [];
  for (let el of arr) (el % 2 ? odd : even).push(el);
  return [odd, even];
};
// Solution 3
const pickIt = arr => {
  const oddEven = [[], []];
  for (let el of arr) oddEven[~el & 1].push(el);
  return oddEven;
};
/*
const pickIt = arr => {
  const odd = [],
    even = [];
  arr.forEach(el => el % 2 ? odd.push(el) : even.push(el));
  return [odd, even];
};

const pickIt = arr => [
  arr.filter(el => el % 2),
  arr.filter(el => !(el % 2)),
];
*/
```
#### [Pre-FizzBuzz Workout #1](https://www.codewars.com/kata//569e09850a8e371ab200000b)
```javascript
// Solution 1
const preFizz = num => {
  let arr = [];
  for (let i = 1; i <= num; i++) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const preFizz = num =>
  Array(num)
    .fill(1)
    .map((el, i) => el + i);
// Solution 3
const preFizz = num => Array(...Array(num)).map((el, i) => ++i);
// Solution 4
const preFizz = num => Array.from({ length: num }, (el, i) => ++i);
```
#### [Powers of 2](https://www.codewars.com/kata//57a083a57cb1f31db7000028)
```javascript
// Solution 1
const powersOfTwo = num => {
  const arr = [];
  for (let i = 0; i <= num; i++) {
    arr.push(2 ** i);
  }
  return arr;
};
// Solution 2
const powersOfTwo = num => [...Array(++num)].map((_, i) => 2 ** i);
// Solution 3
const powersOfTwo = num =>
  Array(++num)
    .fill(0)
    .map((_, i) => 2 ** i);
// Solution 4
const powersOfTwo = num => Array.from({ length: ++num }, (_, i) => 2 ** i);
```
#### [Reversed sequence](https://www.codewars.com/kata//5a00e05cc374cb34d100000d)
```javascript
// Solution 1
const reverseSeq = num => {
  let arr = [];
  for (let i = num; i > 0; i--) {
    arr.push(i);
  }
  return arr;
};
// Solution 2
const reverseSeq = num =>
  Array(num)
    .fill(0)
    .map(() => num--);
// Solution 3
const reverseSeq = num => Array.from({ length: num }, () => num--);
// Solution 4
const reverseSeq = num => Array.from({ length: num }, (_, i) => ++i).reverse();
// Solution 5
const reverseSeq = num => [...Array(num)].map(() => num--);
// Solution 6
const reverseSeq = num => [...Array(num).keys()].map(() => num--);
// Solution 7
const reverseSeq = num => [...Array(num).keys()].map(el => ++el).reverse();
// Solution 8
const reverseSeq = num => num < 2 ? [num] : [num].concat(reverseSeq(--num));
```
#### [Training JS #4: Basic data types--Array](https://www.codewars.com/kata//571effabb625ed9b0600107a)
```javascript
const getLength = arr => arr.length;

const getFirst = arr => arr.shift();
// const getFirst = arr => arr[0];

const getLast = arr => arr.pop();
// const getLast = arr => arr.slice(-1)[0];
// const getLast = arr => arr[arr.length - 1];

const pushElement = arr => (arr.push(0), arr);
// const pushElement = arr => arr.concat(0);

const popElement = arr => (arr.pop(), arr);
// const popElement = arr => arr.slice(0, -1);
```
#### [No Loops 2 - You only need one](https://www.codewars.com/kata//57cc40b2f8392dbf2a0003ce)
```javascript
const check = (arr, el) => arr.includes(el);
```
#### [You only need one - Beginner](https://www.codewars.com/kata//57cc975ed542d3148f00015b)
```javascript
const check = (arr, el) => arr.includes(el);
```
#### [Be Concise IV - Index of an element in an array](https://www.codewars.com/kata//5703c093022cd1aae90012c9)
```javascript
// Solution 1
const find = (arr, el, i = arr.indexOf(el)) => i < 0 ? 'Not found' : i;
// Solution 2
const find = (arr, el, i = arr.indexOf(el)) => i >= 0 ? i : 'Not found';
// Solution 3
const find = (arr, el) => (el = arr.indexOf(el)) >= 0 ? el : 'Not found';
// Solution 4
const find = (arr, el) => arr.includes(el) ? arr.indexOf(el) : 'Not found';
// Solution 5
const find = (arr, el) => (el => el >= 0 ? el : 'Not found')(arr.indexOf(el));
```
#### [Find numbers which are divisible by given number](https://www.codewars.com/kata//55edaba99da3a9c84000003b)
```javascript
// Solution 1
const divisibleBy = (num, div) => num.filter(el => el % div === 0);
// Solution 2
const divisibleBy = (num, div) => num.filter(el => !(el % div));
```
#### [Removing Elements](https://www.codewars.com/kata//5703c093022cd1aae90012c9)
```javascript
// Solution 1
const removeEveryOther = arr => arr.filter((el, i) => i % 2 === 0);
// Solution 2
const removeEveryOther = arr => arr.filter((el, i) => !(i % 2));
```
#### [Well of Ideas - Easy Version](https://www.codewars.com/kata//57f222ce69e09c3630000212)
```javascript
// Solution 1
const well = arr => {
  const good = arr.filter(el => el === 'good').length;
  return good < 1 ? 'Fail!' : good < 3 ? 'Publish!' : 'I smell a series!';
};
// Solution 2
const well = arr => (
  (good = arr.filter(el => el === 'good').length),
  good < 1 ? 'Fail!' : good < 3 ? 'Publish!' : 'I smell a series!'
);
// Solution 3
const well = arr => {
  let good = 0;
  for (let i = 0; i < arr.length; ++i)
    if (arr[i] === 'good' && ++good > 2) return 'I smell a series!';
  return good ? 'Publish!' : 'Fail!';
};
// Solution 4
const well = arr => {
  let good = 0;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === 'good') {
      good++;
      if (good === 3) break;
    }
  }
  return ['Fail!', 'Publish!', 'Publish!', 'I smell a series!'][good];
};
// Solution 5
const well = arr => {
  const good = arr.reduce((a, b) => a + (b === 'good'), 0);
  return good ? (good > 2 ? 'I smell a series!' : 'Publish!') : 'Fail!';
};
// Solution 6
const well = arr =>
  arr.includes('good')
    ? arr.filter(el => el === 'good').length < 3
      ? 'Publish!'
      : 'I smell a series!'
    : 'Fail!';
// Solution 7
const well = (arr, good = 'good') => {
  let a = 0;
  arr.map(el => el === good ? a++ : null);
  return !a ? 'Fail!' : a <= 2 ? 'Publish!' : 'I smell a series!';
};
```
#### [JavaScript Array Filter](https://www.codewars.com/kata//514a6336889283a3d2000001)
```javascript
// Solution 1
const getEvenNumbers = arr => arr.filter(el => !(el % 2));
// Solution 2
const getEvenNumbers = arr => arr.filter(el => el % 2 === 0);
```
#### [Find how many times did a team from a given country win the Champions League?](https://www.codewars.com/kata//581b30af1ef8ee6aea0015b9)
```javascript
// Solution 1
const countWins = (winnerList, country) =>
  winnerList.filter(el => el.country === country).length;
// Solution 2
const countWins = (winnerList, country) =>
  winnerList.reduce((a, b) => a + (b['country'] === country ? 1 : 0), 0);
// Solution 3
const countWins = (winnerList, country) => {
  let count = 0;
  for (let i = 0; i < winnerList.length; i++) {
    if (winnerList[i].country === country) count += 1;
  }
  return count;
};
```
#### [filterEvenLengthWords](https://www.codewars.com/kata//59564f3bcc15b5591a00004a)
```javascript
// Solution 1
const filterEvenLengthWords = words => words.filter(el => !(el.length % 2));
// Solution 2
const filterEvenLengthWords = words => words.filter(el => el.length % 2 === 0);
```
#### [Array.diff](https://www.codewars.com/kata//523f5d21c841566fde000009)
```javascript
// Solution 1
const arrayDiff = (a, b) => a.filter(el => !b.includes(el));
// Solution 2
const arrayDiff = (a, b) => {
  const arr = [];
  for (let i = 0; i < a.length; i++) {
    if (b.indexOf(a[i]) < 0) arr.push(a[i]);
  }
  return arr;
};
```
#### [Find Duplicates](https://www.codewars.com/kata//5558cc216a7a231ac9000022)
```javascript
const duplicates = arr =>
  arr.filter((el, i) => i !== arr.indexOf(el) && i === arr.lastIndexOf(el));
```
#### [Train to remove duplicates from an array with filter()](https://www.codewars.com/kata//58308360aeb69a460b0002b2)
```javascript
const unique = arr => arr.filter((el, i) => i === arr.indexOf(el));
```
#### [My head is at the wrong end!](https://www.codewars.com/kata//56f699cd9400f5b7d8000b55)
```javascript
const fixTheMeerkat = arr => arr.reverse();
```
#### [Convert number to reversed array of digits](https://www.codewars.com/kata//5583090cbe83f4fd8c000051)
```javascript
// Solution 1
const digitize = num => num.toString().split('').map(Number).reverse();
// Solution 2
const digitize = num => String(num).split('').map(Number).reverse();
// Solution 3
const digitize = num => (num + '').split('').map(Number).reverse();
// Solution 4
const digitize = num => Array.from(String(num), Number).reverse();
// Solution 5
const digitize = num => [...String(num)].map(Number).reverse();
// Solution 6
const digitize = num =>
  `${num}`
    .split('')
    .reverse()
    .map(el => +el);
// Solution 7
const digitize = num => {
  const str = num + '',
    res = [];
  for (let i = str.length - 1; i >= 0; i--) {
    res.push(+str[i]);
  }
  return res;
};
```
#### [Two Oldest Ages](https://www.codewars.com/kata//511f11d355fe575d2c000001)
```javascript
const twoOldestAges = ages => ages.sort((a, b) => a - b).slice(-2);
```
#### [Sum of two lowest positive integers](https://www.codewars.com/kata//558fc85d8fd1938afb000014)
```javascript
// Solution 1
const sumTwoSmallestNumbers = num => {
  num = num.sort((a, b) => a - b);
  return num[0] + num[1];
};
// Solution 2
const sumTwoSmallestNumbers = num => {
  const [a, b] = num.sort((a, b) => a - b);
  return a + b;
};
```
#### [Simple parenthesis removal](https://www.codewars.com/kata//5a3bedd38f27f246c200005f)
```javascript
// Solution 1
const solve = s => {
  let k = 1,
    x = 1,
    t = 0,
    chars = '';
  for (let char of s)
    if (char === '(') {
      t === 1 && k === -1 ? (k *= x) : (k = x);
      if (t === 1) x = 1;
    } else if (char === ')') {
      k = 1;
      x = 1;
    } else if (char === '+') x = 1;
    else if (char === '-') x *= -1;
    else {
      if (t === 0 && x === -1) chars += '-';
      if (t === 1) {
        x *= k;
        if (x === 1) chars += '+';
        else if (x === -1) chars += '-';
      }
      x = 1;
      t = 1;
      chars += char;
    }
  return chars;
};
// Solution 2
const solve = (s) => {
  let arr = [],
    num = 1,
    str = '';
  for (let i of s) {
    switch (i) {
    case '(':
      arr.push(num);
      num = 1;
      break;
    case ')':
      arr.pop();
      num = 1;
      break;
    case '-':
      num = -1;
      break;
    case '+':
      num = 1;
      break;
    default:
      str +=
          (arr.reduce((acc, curr) => acc * curr, 1) * num === 1 ? '+' : '-') +
          i;
    }
  }
  return str[0] === '+' ? str.slice(1) : str;
};
// Solution 3
const solve = s => {
  let arr = [],
    str = '',
    num = 1;
  for (let i of s) {
    if (i === '(') {
      arr.push(num);
      num = 1;
    } else if (i === ')') {
      arr.pop();
      num = 1;
    } else if (i === '-') {
      num = -1;
    } else if (i === '+') {
      num = 1;
    } else
      str +=
        (arr.reduce((acc, curr) => acc * curr, 1) * num === 1 ? '+' : '-') + i;
  }
  return str[0] === '-' ? str : str.slice(1);
};
```
#### [Sentence Smash](https://www.codewars.com/kata//53dc23c68a0c93699800041d)
```javascript
// Solution 1
const smash = str => {
  'use strict';
  let res = '';
  for (let i = 0; i < str.length; i++) {
    res += str[i];
    if (i !== str.length - 1) res += ' ';
  }
  return res;
};
// Solution 2
const smash = words => words.join(' ');
// Solution 3
const smash = str => str.toString().replace(/,/g, ' ');
```
#### [String Templates - Bug Fixing #5](https://www.codewars.com/kata//55c90cad4b0fe31a7200001f)
```javascript
const buildString = (...template) => `I like ${template.join(', ')}!`;
```
#### [Printing Array elements with Comma delimiters](https://www.codewars.com/kata//56e2f59fb2ed128081001328)
```javascript
const printArray = arr => arr.join(',')
```
#### [CSV representation of array](https://www.codewars.com/kata//5a34af40e1ce0eb1f5000036)
```javascript
const toCsvText = arr => arr.join('\n');
```
#### [Enumerable Magic #1 - True for All?](https://www.codewars.com/kata//54598d1fcbae2ae05200112c)
```javascript
const all = (arr, fun) => arr.every(fun);
```
#### [Grasshopper - Array Mean](https://www.codewars.com/kata//55d277882e139d0b6000005d)
```javascript
const findAverage = num =>
  num.reduce((acc, curr) => acc + curr, 0) / num.length;
```
#### [Be Concise III - Sum Squares](https://www.codewars.com/kata//56f8fe6a2e6c0dc83b0008a7)
```javascript
const sumSquares = arr => arr.reduce((acc, curr) => acc + curr ** 2, 0);
```
#### [SpeedCode #2 - Array Madness](https://www.codewars.com/kata//56ff6a70e1a63ccdfa0001b1)
```javascript
const arrayMadness = (a, b) =>
  a.reduce((acc, curr) => acc + curr ** 2, 0) >
  b.reduce((acc, curr) => acc + curr ** 3, 0);
```
#### [Beginner - Reduce but Grow](https://www.codewars.com/kata//57f780909f7e8e3183000078)
```javascript
const grow = arr => arr.reduce((acc, curr) => acc * curr, 1);
```
#### [Array plus array](https://www.codewars.com/kata//5a2be17aee1aaefe2a000151)
```javascript
const arrayPlusArray = (arr1, arr2) =>
  arr1.reduce((acc, curr) => acc + curr, 0) +
  arr2.reduce((acc, curr) => acc + curr, 0);
```
#### [Freudian translator](https://www.codewars.com/kata//5713bc89c82eff33c60009f7)
```javascript
// Solution 1
const toFreud = str =>
  str
    ? str
      .split(' ')
      .map(el => 'sex')
      .join(' ')
    : '';
// Solution 2
const toFreud = str => str.replace(/\S+/g, 'sex');
// Solution 3
const toFreud = str => str.replace(/[^ ]+/g, 'sex');
```
#### [Training JS #16: Methods of String object--slice(), substring() and substr()](https://www.codewars.com/kata//57274562c8dcebe77e001012)
```javascript
const cutIt = arr => {
  const minLength = Math.min(...arr.map(str => str.length));
  return arr.map(str => str.slice(0, minLength));
};
```
#### [Beginner - Lost Without a Map](https://www.codewars.com/kata//57f781872e3d8ca2a000007e)
```javascript
// Solution 1
const maps = arr => arr.map(el => el * 2);
// Solution 2
const maps = arr => arr.map(el => el + el);
// Solution 3
const maps = arr => {
  const res = [];
  for (let i = 0; i < arr.length; i++) {
    res[i] = arr[i] * 2;
  }
  return res;
};
```
#### [Enumerable Magic #25 - Take the First N Elements](https://www.codewars.com/kata//545afd0761aa4c3055001386)
```javascript
const take = (arr, n) => arr.splice(0, n);
```
#### [Remove First and Last Character Part Two](https://www.codewars.com/kata//570597e258b58f6edc00230d)
```javascript
const array = arr => arr.split(',').slice(1, -1).join(' ') || null;
```
#### [Vasya - Clerk](https://www.codewars.com/kata//555615a77ebc7c2c8a0000b8)
```javascript
// Solution 1
const tickets = peopleInLine => {
  let twentyFive = [], fifty = [], message = '';
  for (let i = 0; i < peopleInLine.length; i++) if (peopleInLine[i] === 25) {
    twentyFive.push(25);
    message = 'YES';
  } else if (peopleInLine[i] === 50) if (twentyFive.length === 0) {
    i = peopleInLine.length;
    message = 'NO';
  } else {
    fifty.push(50);
    twentyFive.pop(25);
    message = 'YES';
  } else if (peopleInLine[i] === 100) {
    if (fifty.length === 0 && twentyFive.length < 3) {
      i = peopleInLine.length;
      message = 'NO';
    }
    if (fifty.length > 0 && twentyFive.length === 0) {
      i = peopleInLine.length;
      message = 'NO';
    }
    if (fifty.length === 0 && twentyFive.length > 2) {
      twentyFive.pop(25);
      twentyFive.pop(25);
      twentyFive.pop(25);
      message = 'YES';
    }
    if (fifty.length > 0 && twentyFive.length > 0) {
      fifty.pop(50);
      twentyFive.pop(25);
      message = 'YES';
    }
  }
  return message;
};
// Solution 2
const tickets = peopleInLine => {
  let [c25, c50, c100] = [0, 0, 0];
  for (let v of peopleInLine) {
    if (v === 25) c25++;
    if (v === 50) {
      c50++;
      c25--;
    }
    if (v === 100) {
      c25--;
      c50 > 0 ? c50-- : (c25 -= 2);
    }
    if (c25 < 0 || c50 < 0) return 'NO';
  }
  return 'YES';
};
// Solution 3
const tickets = peopleInLine => {
  let m25 = 0,
    m50 = 0;
  for (let i = 0; i < peopleInLine.length; i++) {
    switch (peopleInLine[i]) {
    case 25:
      m25++;
      break;
    case 50:
      m25 > 0 ? m25-- : (m25 = -1);
      m50++;
      break;
    case 100:
      m25 > 0 && m50 > 0 ? m50-- : m25 > 2 ? (m25 -= 2) : (m25 = -1);
      m25--;
      break;
    }
  }
  return m25 < 0 ? 'NO' : 'YES';
};
```
#### [Jenny's secret message](https://www.codewars.com/kata//55225023e1be1ec8bc000390)
```javascript
const greet = name => name === 'Johnny' ? 'Hello, my love!' : `Hello, ${name}!`;
```
#### [Template Strings](https://www.codewars.com/kata//55a14f75ceda999ced000048)
```javascript
const TempleStrings = (obj, feature) => `${obj} are ${feature}`;
```
#### [Returning Strings](https://www.codewars.com/kata//55a70521798b14d4750000a4)
```javascript
const greet = name => `Hello, ${name} how are you doing today?`;
```
#### [Grasshopper - Combine strings](https://www.codewars.com/kata//55f73f66d160f1f1db000059)
```javascript
// Solution 1
const combineNames = (firstName, lastName) => `${firstName} ${lastName}`;
// Solution 2
const combineNames = (firstName, lastName) => firstName + ' ' + lastName;
// Solution 3
const combineNames = (...names) => names.join(' ');
```
#### [Grasshopper - Variable Assignment Debug](https://www.codewars.com/kata//5612e743cab69fec6d000077)
```javascript
let a = 'dev';
let b = 'Lab';
let name = a + b;
```
#### [Grasshopper - Debug sayHello](https://www.codewars.com/kata//5625618b1fe21ab49f00001f)
```javascript
const sayHello = name => `Hello, ${name}`;
```
#### [Take the Derivative](https://www.codewars.com/kata//5963c18ecb97be020b0000a2)
```javascript
const derive = (coefficient,exponent) => `${coefficient * exponent}x^${--exponent}`;
```
#### [If you can't sleep, just count sheep!!](https://www.codewars.com/kata//5b077ebdaf15be5c7f000077)
```javascript
const countSheep = num => {
  let str = '';
  for (let i = 1; i <= num; i++) {
    str += `${i} sheep...`;
  }
  return str;
};
```
#### [get character from ASCII Value](https://www.codewars.com/kata//55ad04714f0b468e8200001c)
```javascript
const getChar = c => String.fromCodePoint(c);
```