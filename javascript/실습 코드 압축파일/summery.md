* BOM
```js
window.alert('hello world')
window.prompt('입력하세요!')
// 'hello world' (V)
// <!-- 주석 -->
// /* 주석 */ (V)
window.confirm('~~에 동의하십니까?')
// true, false
console.log('hello world')
// 터미널에 hello world
console.error('hello world')
console.table({'one':1, 'two':2})
```

* 변수
```js
let age = 30
let name = "Jun"

let x = 10
let y = x
let z = y

y = 20
console.log(z) // 10

// $, _ 를 제외한 공백, 특수문자, 구두점 등 을 사용할 수 없습니다.
// 변수 이름은 숫자로 시작할 수 없습니다. 숫자로 끝나는 것은 됩니다.
// 키워드(예: if, else, while 등)는 변수 이름으로 사용할 수 없습니다.
// 변수 이름은 대소문자를 구분합니다.

let x = 10
typeof(x)

let y = "Jun"
typeof(y)

// 변수의 값 변경
let x = 10
x

x = 20
x
```

* 원시타입
```js
function typeCheck(value) {
    const return_value = Object.prototype.toString.call(value);
    const type = return_value.substring(
        return_value.indexOf(" ") + 1,
        return_value.indexOf("]")
    );
    return type.toLowerCase();
}

typeCheck('hello')

// 타입은 단순한 데이터를 저장하는 원시타입, 그리고 객체로서 저장되는 참조타입으로 크게 구별할 수 있습니다. 

let str1 = 'hello';
str1[0] // 0번째 값을 불러옵니다.
str1[1] = 'w'

str1

str1 = 'world'

let text1 = 'hello "world"'
let text2 = "hello 'world'"
let text3 = `hello 'world'`
let text4 = `hello "world"`

console.log(text1, text2, text3, text4)

let name = 'hojun'
let age = 10
let text5 = `안녕하세요 저는 ${name}이라고 하빈다. 제 나이는 ${age}입니다`

let text6 = 'hello\nworld'
console.log(text6)
let text7 = 'hello\tworld'
console.log(text7)

let text8 = 'hello\'world'
console.log(text8)


let text = 'hello world'
text[0]
text.length // length는 0부터 시작하지 않습니다.

let 불멸자 = "immortal";
불멸자.toUpperCase();
console.log(불멸자);

let lyrics1 = '광야로 걸어가 ';
let lyrics2 = '알아 네 home ground';
'광야로 걸어가 알아 네 home ground' === lyrics1 + lyrics2;
// true


// indexOf
'hello world'.indexOf('world') // 6
'hello world'.indexOf('hi')
'hello world hello world'.indexOf('world', 10)


// replace
'hello world'.replace('hello', 'hi')
'hello world hello world'.replace('hello', 'hi')
'hello world hello world'.replace(/hello/g, 'hi')


// slice
'hello world'.slice(0, 5)
'hello world'.slice(0)
'hello world'.slice(6)
'hello world.png'.slice(-3)
'hello world.png'.slice(-3, 14)


// split
'hello world'.split(' ')
'hello world'.split(' ')[0]
'hello world'.split(' ')[1]
'hello world hi'.split(' ')[2]
'010-0000-1111'.split('-')


// toLowerCase, toUpperCase
'Hello World'.toLowerCase()
'Hello World'.toUpperCase()


// trim
"         abc  ".trim()


// 숫자형
// 산술연산
console.log(`10 + 3 = ${10 + 3}`)
console.log(`10 - 3 = ${10 - 3}`)
console.log(`10 / 3 = ${10 / 3}`)
console.log(`10 * 3 = ${10 * 3}`)
console.log(`10 ** 3 = ${10 ** 3}`) // 10의 3승
//console.log(`4 ** 0.5 = ${4 ** 0.5}`) // 4의 제곱근
console.log(`10 % 3 = ${10 % 3}`) // 나머지
console.log(`-10 % 3 = ${-10 % 3}`)


// 단항연산 
console.log(-2)
console.log(-(-2))
// console.log(--2) // error
console.log(+4)
console.log(+'4')


// 증감연산자
let num = 3; // 증감연산자는 할당연산자를 통해 할당된 값에만 사용 가능합니다.
console.log(`증감연산 : ${++num}`); // 4
num
console.log(`증감연산 : ${num++}`); // 5 (출력하고 나서 연산을 합니다!)
num
console.log(`증감연산 : ${--num}`); // 4
num
console.log(`증감연산 : ${num--}`); // 3 (출력하고 나서 연산을 합니다!)
num


// 비교연산자(값은 boolean으로 반환됩니다.)
console.log(`비교연산 : ${2 > 3}`);
console.log(`비교연산 : ${2 >= 3}`);
console.log(`비교연산 : ${2 < 3}`);
console.log(`비교연산 : ${2 <= 3}`);
console.log(`비교연산 : ${2 == 3}`); 
console.log(`비교연산 : ${2 != 3}`); 
console.log(`비교연산 : ${2 === 3}`); 
console.log(`비교연산 : ${2 !== 3}`);


// 등호 2개를 권하지 않습니다. 실무에서는 등호 3개를 사용하시길 권해드립니다.
console.log(`비교연산 : ${2 == '2'}`); // 다른 언어에서는 false, js에서는 true
console.log(`비교연산 : ${2 === '2'}`); // 다른 언어에서 이런 문법이 없고, js에서는 false

Infinity
-Infinity
1/0
30000000000
console.log("숫자가 아님" / 2); // NaN


// 관련 함수와 메서드
console.log(`parseInt('2') : ${parseInt('2')}`);
console.log(`parseInt('2asdf') : ${parseInt('2asdf')}`);
console.log(`parseInt('aa2') : ${parseInt('aa2')}`);
console.log(`parseInt('hello') : ${parseInt('hello')}`);
console.log(`parseInt('30b') : ${parseInt('30b')}`);
console.log(`parseInt('30.5') : ${parseInt('30.5')}`);
console.log(`parseFloat('45.4') : ${parseFloat('45.4')}`);

let test = 5;
console.log(`test.toString() : ${test.toString()}`);
console.log(`test.toString() : ${test.toString() + test.toString()}`);
console.log(`num.toString() : ${(3).toString()}`);

console.log(`isNaN('5') : ${isNaN('5')}`);
console.log(`isNaN(3) : ${isNaN(3)}`);
console.log(`isNaN('b3') : ${isNaN('b3')}`);
console.log(`isNaN('3b') : ${isNaN('3b')}`);
console.log(isNaN(undefined)); // true가 출력! 혼란 가중 => Number.isNaN 도입

console.log(Number.isNaN(undefined)); // false
console.log(Number.isNaN(null)); // false
console.log(Number.isNaN(NaN)); // true


// Math 
console.log(`Math.PI : ${Math.PI}`);
console.log(`Math.round(4.7) : ${Math.round(4.7)}`); // 반올림
console.log(`Math.pow(2, 8) : ${Math.pow(2, 8)}`);
console.log(`Math.sqrt(64) : ${Math.sqrt(64)}`);
console.log(`Math.abs(-5) : ${Math.abs(-5)}`);
console.log(`Math.random() : ${Math.random()}`);
console.log(`Math.max(10, 20, 30, 40, 50) : ${Math.max(10, 20, 30, 40, 50)}`);
console.log(`Math.min(10, 20, 30, 40, 50) : ${Math.min(10, 20, 30, 40, 50)}`);


// 논리 자료형
if (true) {
    console.log('true');
} else {
    console.log('false');
}

if (10 < 3) {
    console.log('true');
} else {
    console.log('false');
}

let x = 5;
let y = 10;
let z = 5;

console.log(x > y); // false
console.log(x < y); // true
console.log(x >= z); // true
console.log(x <= z); // true
console.log(x == z); // true
console.log(x != z); // false
console.log(x === y); // false
console.log(x !== y); // true

console.log('2' == 2) // true
console.log('2' != 2) // false
console.log('2' === 2) // false
console.log('2' !== 2) // true

let x = true // 1
let y = false // 0

console.log(true && true) // true
console.log(true && false) // false
console.log(false && true) // false
console.log(false && false) // false

console.log(true || true) // true
console.log(true || false) // true
console.log(false || true) // true
console.log(false || false) // false

for (let i = 0; i < 100; i++) {
    console.log(i);
}

for (let i = 0; i < 100; i++) {
    if (i % 3 === 0 && i % 5 === 0) {
        console.log(i);
    }
}

for (let i = 0; i < 100; i++) {
    if (i % 3 === 0 || i % 5 === 0) {
        console.log(i);
    }
}

!true // false
!false // true
!!'hello'
!!''
!!0
!!-10
console.log(!!true); // true
console.log(!!false); // false
console.log(!!undefined); // false
console.log(!!null); // false
console.log(!!NaN); // false

// undefined
let a;
console.log(a); // undefined


//null
let value1; // undefined
let value2 = null;
console.log(value2); //null


// 함수

function 나의시크릿라면레시피(){
	let 라면그릇;
	
	물 550ml를 끓인다;
	면과 분말 스프, 후레이크를 같이 넣는다;
	4분 40초간 더 끓인다;

	라면그릇 = 맛있는라면;

	return 라면그릇;
}

나의시크릿라면레시피();
나의시크릿라면레시피();
나의시크릿라면레시피();

function sum(x, y) { // 함수의 선언
    let z = x + y;
    return z
}

(sum(10, 20) + sum(10, 20)) * sum(1, 3) // 함수의 호출



function sum(x, y) { // 함수의 선언
    let z = x + y;
    console.log(z) // 함수의 기능
    return z
}

(sum(10, 20) + sum(10, 20)) * sum(1, 3) // 함수의 호출


function a(value){
    console.log(value);
    console.log('hello');
    return 100;
}

a(1000) + a(1000)


function b(){
    console.log('hello');
    return 100;
}

b() + b()


function c(){
    console.log('hello');
}

let test = c()
test


function d(){
    console.log('hello');
    return 'hello'
}

let test = d()
test


function e(){
    console.log('hello');
    return // return undefined
}

let test = e()
test


function f(){
    console.log('hello1');
    console.log('hello2');
    return // return undefined
    console.log('hello3');
    console.log('hello4');
}

f()



function sum(a, b, c){
    console.log(a, b, c)
    return a + b + c
}

sum(10, 20, 30)
sum(10, 20, 50)
sum(10, 20, 30, 40)
sum(10, 20)


// 함수 선언문
function sum1(x, y){
  return x + y;
}
console.log(sum1(10, 20));

// 함수 표현식
let sum2 = function(x, y){
  return x + y;
};
console.log(sum2(10, 20));


// 화살표 함수
let sum3 = (x, y) => x + y
console.log(sum3(10, 20));


// 화살표 함수
let sum4 = (x, y) => {
    x = x * 2
    y = y * 2
    return x + y
    }
console.log(sum4(10, 20));



// 객체 타입
// Array
let arr1 = [1, 2, 3, 4, 5]
arr1.push(6)

arr1



let arr1 = [1, 2, 3];
let arr2 = arr1; // 여기서 arr1과 arr2는 같은 [1, 2, 3]을 가리킵니다.
console.log(arr2);

arr1[0] = 10;
// arr1 = [10, 20];
console.log(arr2);



// 비교해보세요.
let arr1 = 'hello';
let arr2 = arr1;
console.log(arr2);

arr1[0] = 'w';
console.log(arr2);


// 배열 생성
const arr = [];
const arr = [1, 2, 3];
const arr2 = new Array(4, 5, 6);
const arr2 = new Array(3);
const arr3 = Array.from('hello');

// 배열의 호출
const arr = [1, 2, 3];
// 배열 안의 원소에 접근하기 위해서는 인덱스 번호를 이용합니다. 
console.log(arr[0]); // 1
console.log(arr[1]); // 2
console.log(arr[2]); // 3
console.log(arr[3]); // undefined


const arr1 = [1, 2, 3];
const arr2 = arr1

arr1[10] = 100
arr1.push(1000)


const myArray = [1, 2, 3, 4, 5];
console.log(myArray.length); // 5

// 상수, 백터([]), 메트릭스([[]]), 텐서(괄호 3개 이상)


// 100을 출력하고 싶다면!?
const arr2 = [
  [1, 2],
  [3, 4],
  [5, [10, 20, 30, [100, 200]]]
];
console.log(arr2[2]);
console.log(arr2[2][0]); // 5
console.log(arr2[2][1]); // [10, 20, 30, [100, 200]]
console.log(arr2[2][1][3]);
console.log(arr2[2][1][3][0]);


// 배열의 메서드
// push, pop

const arr = [1, 2, 3];
arr.push(4);
console.log(arr); // [1, 2, 3, 4]
arr.pop();

// shift, unshift
const myArray = ["사과", "바나나", "수박"];
myArray.shift();
console.log(myArray); 
myArray.unshift("오이", "배");
console.log(myArray);

// splice
const arr = [1, 2, 3];
arr.splice(1, 0, 4);

const arr = [1, 2, 3];
arr.splice(1, 1, 4);

const arr = [1, 2, 3, 4, 5];
arr.splice(1, 2, 100);

const arr = [1, 2, 3, 4, 5];
arr.splice(1, 3, 100, 200);

// slice
const arr = [10, 20, 30, 40, 50];
arr.slice(1, 3);


// sort
const avengers = ['아이언맨', '스파이더맨', '헐크', '토르'];
console.log(avengers.sort());

const avengers = ['나아이언맨', '가스파이더맨', '라헐크', '다토르'];
console.log(avengers.sort());


const nums = [23, 5, 1000, 42];
console.log(nums.sort());


let numbers = [4, 2, 5, 1, 3];
numbers.sort((a, b) => a - b); // 오름차순
console.log(numbers);


let numbers = [4, 2, 5, 1, 3];
numbers.sort((a, b) => b - a); // 내림차순
console.log(numbers);


let numbers = [4, 2, 5, 1, 3];
numbers.sort((a, b) => {
    console.log(a, b)
    return a - b
    }); // 내림차순
console.log(numbers);


// forEach
const arr = ['참외', '키위', '감귤'];
arr.forEach(function(item, index) {
    console.log(item, index);
    arr[index] = index+index;
});


const avengers = ['spiderman', 'ironman', 'hulk', 'thor'];

const newAvengers = [];
avengers.forEach(function (item) {
    newAvengers.push('💖' + item + '💖');
});


// map
const arr = [1, 2, 3];
const newArr = arr.map(function(item, index) {
  return item * index;
});

console.log(newArr);

///

const arr = [1, 2, 3];
const newArr = arr.map(item => item * 2);

console.log(newArr);

///

const arr = ['참외', '키위', '감귤'];
arr.forEach(item => item + '맛있어');


///

const arr = ['참외', '키위', '감귤'];
arr.map(item => item + '맛있어');


///

const data = [[10, 20, 30], [100, 200, 300], [1000, 2000, 3000]]
data.map(item => item[1])


let data = {
        "_id": "642ba3980785cecff3f39a8d",
        "index": 0,
        "age": 28,
        "eyeColor": "green",
        "name": "Annette Middleton",
        "gender": "female",
        "company": "KINETICA"
    }

data['age']



const data = [
    {
        "_id": "642ba3980785cecff3f39a8d",
        "index": 0,
        "age": 28,
        "eyeColor": "green",
        "name": "Annette Middleton",
        "gender": "female",
        "company": "KINETICA"
    },
    {
        "_id": "642ba398d0fed6e17f2f50c9",
        "index": 1,
        "age": 37,
        "eyeColor": "green",
        "name": "Kidd Roman",
        "gender": "male",
        "company": "AUSTECH"
    },
    {
        "_id": "642ba39827d809511d00dd8d",
        "index": 2,
        "age": 39,
        "eyeColor": "brown",
        "name": "Best Ratliff",
        "gender": "male",
        "company": "PRISMATIC"
    }
];

const ages = data.map(item => item['age']);

// includes
const arr1 = ['hello', 'world', 'hojun']
arr1.includes('world')

const arr1 = ['hello', 'world', 'hojun']
arr1.includes('hi')

// join
const arr1 = ['hello', 'world', 'hojun']
arr1.join('!') // hello!world!hojun

const arr2 = ['010', '1034', '1100']
arr2.join('-') // 010-1034-1100

const arr3 = [010, 1034, 1100]
arr3.join('-') // 이렇게 하시면 안됩니다. 0으로 시작하면 진수로 생각합니다.

// 메서드 체이닝
'010.0000.1111'.split('.').join('-')


// 객체
let obj = {
    name: 'hojun',
    age: 10,
    height: 180,
    weight: 70
}

obj.name
obj['name']
obj.name = "junho";
obj.name

delete obj.name;
obj

console.log('age' in obj);

let obj = {
    name: 'hojun',
    age: 10,
    height: 180,
    weight: 70
}
console.log(Object.keys(obj))
console.log(Object.values(obj))


// 조건문

if (true) {
    console.log('true');
}

if (false) {
    console.log('true');
}

if (10 > 3 && 10 > 5) {
    console.log('true');
}

let test = 5;
if(test < 10){
	console.log('참입니다!')
}


if (true) console.log("중괄호를 생략했습니다.");


if (true) {
    console.log('true');
} else {
    console.log('false');
}

let x = 3;
let y = 7;

if(x == y){
  console.log('if문으로 실행');
} else {
  console.log('else문으로 실행');
}


let x = 3;
let y = 7;

if(x == y){
  console.log('if문으로 실행');
} else {
  console.log('else문으로 실행');
}



let score = 95;
let money = 1000;

if (score > 90){
  console.log('참 잘했습니다!');
  money += 100000
} else if (score > 80){
  console.log('잘했습니다!');
  money += 10000
} else if (score > 70){
  console.log('했습니다!');
  money += 1000
} else {
  money = 0
}

console.log(money);


switch (new Date().getDay()) {
    case 1:
        console.log('월요일입니다.');
        break;
    case 2:
        console.log('화요일입니다.');
        break;
    case 3:
        console.log('수요일입니다.');
        break;
    case 4:
        console.log('목요일입니다.');
        break;
    case 5:
        console.log('금요일입니다.');
        break;
    default:
        console.log('금금요일입니다. 주말이 뭐죠?');
        break;
}

switch (new Date().getDay()) {
    case 1:
        console.log('월요일입니다.');
    case 2:
        console.log('화요일입니다.');
    case 3:
        console.log('수요일입니다.');
        break;
    case 4:
        console.log('목요일입니다.');
        break;
    case 5:
        console.log('금요일입니다.');
        break;
    default:
        console.log('금금요일입니다. 주말이 뭐죠?');
        break;
}

switch (new Date().getDay()) {
    case 1:
    case 2:
    case 3:
        console.log('수요일입니다.');
        break;
    case 4:
        console.log('목요일입니다.');
        break;
    case 5:
        console.log('금요일입니다.');
        break;
    default:
        console.log('금금요일입니다. 주말이 뭐죠?');
        break;
}

let price = 0;
let menu = '카페라떼'; // 메뉴를 바꿔보세요!

switch (menu) {
    case '아메리카노':
        price = 4000;
    case '카페라떼':
        price = 5000;
    case '바닐라라떼':
        price = 6000;
    case '콜드브루':
        price = 5500;
    case '딸기라떼':
        price = 7000;
    case '레몬에이드':
        price = 6500;
    case '에스프레소':
        price = 3500;
    case '루이보스':
        price = 4500;
    default:
        console.log('메뉴를 정확히 입력하세요.');
}

//반복문

for (let i = 0; i < 10; i++) {
    console.log(i);
}

for (let i = 0; i < 10; ++i) {
    console.log(i);
}

// 구조
for(초기화식; 조건식; 증감식) {
	//실행문;
}

for (let i = 0; i < 10; i = i + 3) {
    console.log(i);
}

for (let i = 0; i < 10; i += 3) {
    console.log(i);
}


const cars = ["BMW", "Volvo", "Saab", "Ford", "Flat", "Audi"];

let text = "";

text += '<section><h2>' + cars[0] + '</h2></section>'
text += '<section><h2>' + cars[1] + '</h2></section>'
text += '<section><h2>' + cars[2] + '</h2></section>'
text += '<section><h2>' + cars[3] + '</h2></section>'
text += '<section><h2>' + cars[4] + '</h2></section>'



const cars2 = ["BMW", "Volvo", "Saab", "Ford", "Flat", "Audi"];
let text2 = ''
for (let i = 0; i < cars2.length; i++) {
    text2 += '<section><h2>' + cars2[i] + '</h2></section>' 
}
text2

// 반복문
for(let i = 0; i <= 10; i += 2){
    console.log(i);
}

// 1부터 100까지의 짝수의 합
let s = 0;
for (let i = 0; i < 101; i+=2) {
    console.log(i);
    s += i;
}
console.log(s);

// 구구단
for (let i = 2; i < 10; i++) {
    for (let j = 1; j < 10; j++) {
        console.log(`${i} X ${j} = ${i*j}`);
    }
}

// i = 2, j = 1
// 출력값: 2 X 1 = 2
// i = 2, j = 2
// 출력값: 2 X 2 = 4
// i = 2, j = 3
// 출력값: 2 X 3 = 6
// i = 2, j = 4
// 출력값: 2 X 4 = 8
// i = 2, j = 5
// 출력값: 2 X 5 = 10
// i = 2, j = 6
// 출력값: 2 X 6 = 12
// i = 2, j = 7
// 출력값: 2 X 7 = 14
// i = 2, j = 8
// 출력값: 2 X 8 = 16
// i = 2, j = 9
// 출력값: 2 X 9 = 18
// i = 3, j = 1
// 출력값: 3 X 1 = 3
// i = 3, j = 2
// 출력값: 3 X 2 = 6


// 100보다 작은 3의 배수와 5의 배수의 합
s = 0;
for (let i = 0; i < 101; i++) {
    if(i % 3 == 0 || i % 5 == 0){
        console.log(i);
        s += i;
    }
}
console.log(s);


// while 문
let num = 0;

while (num < 11) {
    console.log(num);
    num += 1;
}


////

let num = 0;
let s = 0;

while (num < 101) {
    s += num;
    num += 1;
}

// 구구단
let i = 2;
let j = 1;
while (i < 10) {
    while (j < 10) {
        console.log(`${i} X ${j} = ${i*j}`);
        j++;
    }
    i++;
    j = 1;
}



// 예시 1
let num = 0;
while (num < 11) {
    num++;
    console.log(num);
    if(num > 5){
        break;
    }
}

// 예시 2
let i = 0;
while (i < 100) {
    i++;
    if (i === 14) {
        console.log(i + '살 부터 중학생이 됩니다.');
        break;
    }
}
console.log('중학교 입학을 축하합니다.');


for (let i = 0; i < 20; i++) {
    if (i < 13) continue;
    console.log(i + '살은 청소년입니다.');
}

for (let i = 0; i < 20; i++) {
    if (i < 13) {
        continue;
    }
    console.log(i + '살은 청소년입니다.');
}

// 전개구문
const 과일들 = ['사과', '파인애플', '수박'];
const 생선들 = ['조기', '갈치', '다금바리'];
const 합치면 = [...과일들, ...생선들];
const 합치면2 = [과일들, 생선들];


const 과일들 = ['사과', '파인애플', '수박'];
const 과일들2 = [...과일들]; 

과일들2.push('키위');


const 과일들3 = 과일들; 
과일들3.push('한라봉');

Math.max([10, 5, 4, 7, 21, 7, 4])
Math.max(...[10, 5, 4, 7, 21, 7, 4])


const 위니브1 = {개리: 1, 빙키: 2};
const 위니브2 = {라이캣: 3};
const 위니브3 = {...위니브1, ...위니브2};

console.log(위니브3);



// 디스트럭처링
let food1, food2, food3;

const categories = {food1 : '과일', food2 : '채소', food3 : '육류'};

food1 = categories.food1;
food2 = categories.food2;
food3 = categories.food3;

console.log(food1, food2, food3);





const {food1, food2, food3} = {food1 : '과일', food2 : '채소', food3 : '육류'};

console.log(food1, food2, food3);




const obj = {food1 : '과일', food2 : '채소', food3 : '육류'};

function objReturn(){
  return obj
}

// 반환값을 바로 디스트럭쳐링합니다.
const {food1, food3} = objReturn();

console.log(food1, food3);



const arr = [1, 2, 3];

const [a, b, c] = arr;

console.log(a); // 1
console.log(b); // 2
console.log(c); // 3

///


const arr = [1, 2, 3];

const [a, , c] = arr;

console.log(a); // 1
console.log(); // 2
console.log(c); // 3

//this

function a(){ console.log(this) } // window
a();

let myObj = {
    val1: 100,
    func1: function () {
        console.log(this); // myObj
    }
}

myObj.func1();


console.log(this) // window

// for - in 구문
const person = {
  name: 'John',
  age: 30,
  city: 'New York'
};

for (let key in person) {
  console.log(key + ': ' + person[key]);
}

const array = [10, 20, 30, 40, 50];

for (let index in array) {
  console.log(index + ': ' + array[index]);
}

// for - of 구문
const fruits = ['apple', 'banana', 'orange'];

for (let fruit of fruits) {
  console.log(fruit);
}

for (let s of 'hello world') {
  console.log(s);
}

for (let index in 'hello world') {
  console.log(index);
}

let text = 'hello world';
for (let i in text) {
  console.log(text[i]);
}


const person = {
  name: 'John',
  age: 30,
  city: 'New York'
};


for (let s of person) {
  console.log(s);
}

// Map
// object는 for of로 순회할 수 없습니다.
// keys와 values를 바로 사용할 수 없었습니다.
// 메서드가 제한적이었습니다.

let m = new Map();

m.set('name', 'hojun');
m.set('age', 10);
m.set('height', 180);
m.set('weight', 70);

console.log(m.get('name'));
console.log(m.get('age'));

m

m.delete('name');
// let mm = {'name' => 'hojun', 'age' => 10, 'height' => 180, 'weight' => 70}

m.size

for (const variable of m) {
  console.log(`m을 순회하고 있습니다. ${variable[0]}`)
  console.log(`m을 순회하고 있습니다. ${variable[1]}`)
}

for (const variable of m) {
  console.log(`m을 순회하고 있습니다. ${variable}`)
}

let [a, b, c] = [1, 2, 3]

for (const [key, val] of m) {
		console.log(`${key}: ${val}`);
}

console.log(m.keys());
console.log(m.values());

// object 자료형을 맵으로 변환하기
let temp2 = new Map(Object.entries({one:1, two:2}));
// 이 메서드는 객체의 키-값 쌍을 요소([key, value])로 가지는 배열을 반환합니다.
console.log(temp2);

// 반대의 경우
const temp3 = Object.fromEntries(temp2);
console.log(temp3);

// Set

let s = new Set('abcdeeeeeeeee');
console.log(s);

for (let variable of s) {
  console.log(variable);
}

let a = new Set('abc');
let b = new Set('cde');
// 교집합
let cro = [...a].filter(value => b.has(value));
// 합집합
let union = new Set([...a].concat([...b]));
// 차집합
let dif = [...a].filter(x => !b.has(x));


// JSON
let data = [
  {
    "_id": "e7cc9306-0853-43b6-Ac8c-6655b8497548",
    "index": "1",
    "name": "총솔",
    "email": "user-gi8krqo@Vehicula.co.kr",
    "phone": "010-5672-1076",
    "country": "페루",
    "address": "성수이로 60-1",
    "job": "아나운서"
  },
  {
    "_id": "9204771f-2206-4709-B9aa-f816725a0cd1",
    "index": "2",
    "name": "길하늘",
    "email": "user-ab4h756@mattis.org",
    "phone": "010-2313-1782",
    "country": "아루바",
    "address": "삼성로 85-3",
    "job": "방송연출가"
  }
]

data[0]['name']


const json = '{"result":true, "count":42}';
const obj = JSON.parse(json);
console.log(obj);

const obj = { "result": true, "count": 42 }
const json = JSON.stringify(obj);

let data = [
  {
    "_id": "f6901678-35e2-41f7-Ba74-929bc7dadca5",
    "index": "1",
    "name": "복세정",
    "email": "user-8zvjl65@Pulvinar.com",
    "phone": "010-4372-3348",
    "country": "세인트빈센트 그레나딘",
    "address": "양산로 11-4",
    "job": "화학연구원",
    "age": "49"
  },
  {
    "_id": "27caf754-dd27-40ae-A746-e9bc87075596",
    "index": "2",
    "name": "설기태",
    "email": "user-kk0afa8@diam.net",
    "phone": "010-3284-0552",
    "country": "괌",
    "address": "석촌호수로 70-1",
    "job": "기자",
    "age": "33"
  },
  {
    "_id": "51ef1986-7401-4a72-Cf15-1340b361d1f8",
    "index": "3",
    "name": "만호윤",
    "email": "user-bjea5w0@Volutpat.io",
    "phone": "010-2023-4818",
    "country": "키르기스스탄",
    "address": "공덕로 97-2",
    "job": "경찰관",
    "age": "31"
  },
  {
    "_id": "0950e357-353d-489e-C294-141fde6b2cb7",
    "index": "4",
    "name": "오윤찬",
    "email": "user-za2s6li@dolor.net",
    "phone": "010-2084-3157",
    "country": "미국",
    "address": "행운동 30-8",
    "job": "기자",
    "age": "24"
  },
  {
    "_id": "4630538d-096f-44e7-B870-a2d569930163",
    "index": "5",
    "name": "고유주",
    "email": "user-htadlwv@Elementum.org",
    "phone": "010-8412-9862",
    "country": "시에라리온",
    "address": "용두동 23-7",
    "job": "아나운서",
    "age": "41"
  }
]

let s = 0
data
.map(item => parseInt(item['age']))
.forEach(item => s += item);

s / data.length


// 다른 풀이
let s = 0;
for (let i = 0; i < data.length; i++) {
    s += parseInt(data[i]['age']);
}
s / data.length


// DOM
document.head
document.body
document.body.childNodes
document.body.childNodes[1]
document.body.childNodes[1].tagName
document.body.childNodes[1].innerText
document.body.childNodes[1]. //점만 찍어서 얼마나 많은 애트리뷰트가 있는지 확인해보세요.
document.body.childNodes[2]
document.body.childNodes[2].data

// (많이 사용) 해당하는 Id를 가진 요소에 접근하기
document.getElementById('one');

// 해당하는 모든 요소에 접근하기
document.getElementsByTagName('h2');

// 해당하는 클래스를 가진 모든 요소에 접근하기
document.getElementsByClassName('list-item');

// (많이 사용) css 선택자로 단일 요소에 접근하기
document.querySelector("selector");
// document.querySelector("h1");
// document.querySelector("h2");
// document.querySelector("#one");
// document.querySelector(".list-item");

// css 선택자로 여러 요소에 접근하기
document.querySelectorAll("selector");

// const item = document.querySelectorAll(".list-item");
// item.forEach(i => i.innerText = 'hi')

// https://caniuse.com/mdn-api_nodelist_foreach

class Robot {
    constructor(name, hp, mp) {
        this.name = name;
        this.hp = hp;
        this.mp = mp;
    }
}

let robot1 = new Robot('hojun', 100, 50);
let robot2 = new Robot('junho', 90, 50);
let robot3 = new Robot('hohojun', 80, 50);

// https://weniv.github.io/game-with-phaser/
// https://github.com/weniv/game-with-phaser?tab=readme-ov-file

class Character {
    constructor(name, hp, mp) {
        this.name = name;
        this.hp = hp;
        this.mp = mp;
    }
}

let hero = new Character('hojun', 100, 50);
let monster1 = new Character('monster', 90, 50);
let monster2 = new Character('monster', 90, 50);
let monster3 = new Character('monster', 90, 50);

// 생성자
function Character(name, hp, mp) {
    this.name = name;
    this.hp = hp;
    this.mp = mp;
    // return this;
}

let hero = new Character('hojun', 100, 50);
let monster1 = new Character('monster', 90, 50);

// 상속받기

class Character {
    constructor(name, hp, mp, x) {
        this.name = name;
        this.hp = hp;
        this.mp = mp;
        this.x = x;
    }
    move() {
        console.log('move');
        this.x += 10;
    }
}

let hero = new Character('hojun', 100, 50, 0);
hero.move();
hero.move();
hero.move();

class Mob extends Character {
    constructor(name, hp, mp, x, dropRate) {
        super(name, hp, mp, x);
        this.dropRate = dropRate;
    }
    die() {
        console.log('죽었음!');
        console.log('아이템 드랍함!')
    }
}

let monster1 = new Mob('monster', 100, 50, 0, 0.1);


/////

class Robot {
          
    constructor(name) {
        this.name = name;
    }

    sayYourName() {
        console.log(`삐리비리. 제 이름은 ${this.name}입니다. 주인님.`);
    }
}

const bot = new Robot('smith');

bot.name // smith
bot.name = 'jay';
bot.name



class Robot {
    #name;
          
    constructor(name) {
        this.name = name;
    }

    sayYourName() {
        console.log(`삐리비리. 제 이름은 ${this.name}입니다. 주인님.`);
    }
}

const bot = new Robot('smith');

bot.name // smith
bot.name = 'jay';
bot.name

// 비동기 프로그래밍
const one = '1';
const two = '2';
const three = '3';

console.log(one);
setTimeout(() => {
    console.log(two);
}, 1000);
console.log(three);

fetch('http://test.api.weniv.co.kr/mall')
.then(productData => productData.json())
.then(data => console.log(data))


// 쉬운 예제
let p = new Promise((resolve, reject) => {
    resolve('hello world');
}).then(메시지 => {
    alert(메시지);
    return 메시지.split(' ')[0]
}).then(메시지 => {
    alert(메시지);
    return 메시지[0]
}).then(메시지 => {
    alert(메시지);
});


let p = new Promise((resolve, reject) => {
    resolve('hello');
}).then(메시지 => {
    alert(메시지);
    return 1
}).then(메시지 => {
    alert(메시지);
    return 2
}).then(메시지 => {
    alert(메시지);
    return 3
}).then(메시지 => {
    alert(메시지);
});



new Promise((resolve, reject) => {
    // resolve('hello world');
    reject('hello world');
}).then(메시지 => {
    alert(메시지);
    throw Error("에러 발생!")
    return 메시지.split(' ')[0]
}).then(메시지 => {
    alert(메시지);
    return 메시지[0]
}).then(메시지 => {
    alert(메시지);
}).catch(메시지 => {
    alert('catch 실행!! :' + 메시지);
});


let data = []

fetch('http://test.api.weniv.co.kr/mall')
.then(productData => productData.json())
.then(productData => {
    data = productData
})

console.log(data)
```