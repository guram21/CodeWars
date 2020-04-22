# CodeWars
#### Multiply
```javascript
const multiply = (a, b) => a * b;
```
#### Draw stairs
```javascript

```
#### A wolf in sheep's clothing
```javascript
const warnTheSheep = q => {
  const l = q.length,
    w = q.indexOf('wolf');
  return l === w + 1
    ? 'Pls go away and stop eating my sheep'
    : `Oi! Sheep number ${l - 1 - w}! You are about to be eaten by a wolf!`;
};
```
#### I love you, a little, a lot, passionately ... not at all
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
#### Complementary DNA
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
#### Count of positives / sum of negatives
```javascript
const countPositivesSumNegatives = arr => {
  if (arr === null || arr.length === 0) return [];
  let countPos = 0,
    sumNeg = 0;
  for (let i = 0; i < arr.length; i++) {
    arr[i] > 0 ? countPos++ : (sumNeg += arr[i]);
  }
  return [countPos, sumNeg];
};
```
#### Sum of differences in array
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
#### Generate range of integers
```javascript
const generateRange = (min, max, step) => {
  const arr = [];
  for (let i = min; i <= max; i += step) {
    arr.push(i);
  }
  return arr;
};
```
#### Keep Hydrated!
```javascript
const litres = time => Math.floor(time * 0.5);
```
#### Training JS #1: create your first JS function and print "Helloworld!"
```javascript
function helloWorld() {
  const str = 'Hello World!';
  console.log(str);
  return str;
}
```
#### Function 1 - hello world
```javascript
const greet = () => 'hello world!';
```
#### Beginner Series #2 Clock
```javascript
const past = (h, m, s) => (h * 3600 + m * 60 + s) * 1000;
```
#### Third Angle of a Triangle
```javascript
const otherAngle = (a, b) => 180 - (a + b);
```
#### Sum of angles
```javascript
const angle = n => 180 * (n - 2);
```
#### Breaking chocolate problem
```javascript
const breakChocolate = (n, m) => (n * m > 0 ? n * m - 1 : 0);
```
#### For Twins: 2. Math operations
```javascript
const iceBrickVolume = (radius, bottleLength, rimLength) =>
  2 * radius ** 2 * (bottleLength - rimLength);
```
#### Simple multiplication
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
#### DNA to RNA Conversion
```javascript
const DNAtoRNA = dna => dna.replace(/T/g, 'U');
```
#### Convert boolean values to strings 'Yes' or 'No'
```javascript
const boolToWord = bool => (bool ? 'Yes' : 'No');
```
#### Super Duper Easy
```javascript
const problem = x => (x === +x ? x * 50 + 6 : 'Error');
```
#### Chuck Norris VII - True or False? (Beginner)
```javascript
const ifChuckSaysSo = () => !true;
```
#### Type of sum
```javascript
const typeOfSum = (a, b) => typeof (a + b);
```
#### Convert a Number to a String!
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
#### Number toString
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
#### Convert a String to a Number!
```javascript
// Solution 1
const stringToNumber = str => +str;
// Solution 2
const stringToNumber = str => Number(str);
// Solution 3
const stringToNumber = str => parseInt(str);
```
#### Convert a Boolean to a String
```javascript
// Solution 1
const booleanToString = String;
// Solution 2
const booleanToString = b => String;
// Solution 3
const booleanToString = b => `${b}`;
// Solution 4
const booleanToString = b => b + '';
// Solution 5
const booleanToString = b => '' + b;
// Solution 6
const booleanToString = b => String(b);
// Solution 7
const booleanToString = b => b.toString();
// Solution 8
const booleanToString = b => Boolean(b) + '';
// Solution 9
const booleanToString = b => '' + Boolean(b);
// Solution 10
const booleanToString = b => (b ? 'true' : 'false');
// Solution 11
const booleanToString = b => (b ? 'false' : 'true');
// Solution 12
const booleanToString = b => (b === true ? 'true' : 'false');
// Solution 13
const booleanToString = b => (b === false ? 'false' : 'true');
```
#### Sum The Strings
```javascript
const sumStr = (a, b) => String(+a + +b);
```
#### Discover The Original Price
```javascript
//Solution 1
const discoverOriginalPrice = (discountedPrice, salePercentage) =>
  +((discountedPrice * 100) / (100 - salePercentage)).toFixed(2);
//Solution 2
const discoverOriginalPrice = (discountedPrice, salePercentage) =>
  +(discountedPrice / (1 - salePercentage / 100)).toFixed(2);
```
#### Formatting decimal places #0
```javascript
const twoDecimalPlaces = n => +n.toFixed(2);
```
#### How many times should I go?
```javascript
const howManyTimes = (annualPrice, individualPrice) =>
  Math.ceil(annualPrice / individualPrice);
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
// Solution 1
const squareArea = A => +(((2 * A) / Math.PI) ** 2).toFixed(2);
// Solution 2
const squareArea = A => +Math.pow((2 * A) / Math.PI, 2).toFixed(2);
```
#### Keep up the hoop
```javascript
const hoopCount = n => n >= 10 ? 'Great, now move on to tricks' : 'Keep at it until you get it';
```
#### Simple Comparison?
```javascript
// Solution 1
const add = (a, b) => a == b;
// Solution 2
const add = (a, b) => +a == +b;
// Solution 3
const add = (a, b) => +a - +b == 0;
// Solution 4
const add = (a, b) => eval(a - b) == 0;
// Solution 5
const add = (a, b) => a + '' == b + '';
// Solution 6
const add = (a, b) => `${a}` == `${b}`;
```
#### Is he gonna survive?
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
#### Even or Odd
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
#### Calculate BMI
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
#### What's the real floor?
```javascript
// Solution 1
const getRealFloor = n => (n <= 0 ? n : n - (n >= 13 ? 2 : 1));
// Solution 2
const getRealFloor = n => (n <= 0 ? n : n < 13 ? n - 1 : n - 2);
```
#### Determine offspring sex based on genes XX and XY chromosomes
```javascript
// Solution 1
const chromosomeCheck = sperm =>
  sperm == 'XY'
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
#### Alan Partridge II - Apple Turnover
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
#### Sleigh Authentication
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
#### Is n divisible by x and y?
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
#### Rock Paper Scissors!
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
#### Can we divide it?
```javascript
const isDivideBy = (number, a, b) => number % a === 0 && number % b === 0;
```
#### Student's Final Grade
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
#### L1: Set Alarm
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
#### Is this a triangle?
```javascript
// Solution 1
const isTriangle = (a, b, c) => a + b > c && a + c > b && c + b > a;
// Solution 2
const isTriangle = (a, b, c) => Math.max(a, b, c) < (a + b + c) / 2;
// Solution 3
const isTriangle = (a, b, c) => (a = [a, b, c].sort())[0] + a[1] > a[2];
```
#### Calculate Two People's Individual Ages
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
#### Do I get a bonus?
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
#### 101 Dalmatians - squash the bugs, not the dogs!
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
#### Training JS #7: if..else and ternary operator
```javascript
// Solution 1
const saleHotdogs = n => (n < 5 ? n * 100 : n >= 5 && n < 10 ? n * 95 : n * 90);
// Solution 2
const saleHotdogs = n => n * (n < 5 ? 100 : n < 10 ? 95 : 90);
```
#### Be Concise I - The Ternary Operator
```javascript
const describeAge = age => `You're a(n) ${age <= 12 ? 'kid' : age >= 13 && age <= 17 ? 'teenager' : age >= 18 && age <= 64 ? 'adult' : 'elderly'}`;
```
#### Basic Mathematical Operations
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
#### simple calculator
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
#### Switch it Up!
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
#### No zeros for heros
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
#### Power of two
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
#### Difference Of Squares
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
#### Factorial
```javascript
const factorial = n => n > 1 ? n * factorial(--n) : 1;
```
