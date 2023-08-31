# "this" kalit so'ziga oid masalalar | JavaScript

Barcha masalalarni browser muhitida yechish kerak bo'ladi. Chunki node.js muhitida ba'zi masalarni ishlashni imkoni yo'q.

### 1-masala

Yozilgan kodni shunday o'zgartiringki, natijada `foo` funksiyasini ko'rsatilgandek chaqirilganda, aytilgan natijani chiqarsin.

```js
function foo() {

    console.log(`Assalomu alaykum, mening ismim ${this.fullName}. Mazkur oliygohda ${this.subject} fanidan dars beraman.`);

}

foo(); // -> "Assalomu alaykum, mening ismim Doniyorov Bektosh. Mazkur oliygohda Matematika fanidan dars beraman."
```

### 2-masala

Kod shu xolida yuritilsa, hozir `bar` funksiyasi ikki marta chaqirilganda ham `12` qiymati konsolga ikki marta chiqadi. Yozilgan kodni shunday o'zgartiringki natijada `bar` funksiyasi ikkinchi marta chaqirilganda `13` qiymati konsolega chiqsin.

```js
var x = 12

function bar() {
    console.log(this.x);
}

bar(); // -> 12


bar(); // -> 13
```

### 3-masala. Consolega qanday natija chiqadi?

```js
const object = {
     message: "Hello, World!",

    getMessage() {
        const message = "Hello, Earth!";
        return this.message;
    },
};

console.log(object.getMessage()); // What is logged?
```

### 4-masala. Consolega qanday natija chiqadi?

```js
const object = {
    who: "World",

    greet() {
        return `Hello, ${this.who}!`;
    },

    farewell: () => {
        return `Goodbye, ${this.who}!`;
    },
};

console.log(object.greet()); // What is logged?
console.log(object.farewell()); // What is logged?

```

### 5-masala. Consolega qanday natija chiqadi?

```js
var length = 4;
function callback() {
    console.log(this.length); // What is logged?
}

const object = {
    length: 5,
    method(callback) {
        callback();
    },
};

object.method(callback, 1, 2);
```

### 6-masala. Consolega qanday natija chiqadi?

```js
const object = {
    who: "World",

    greet() {
        return `Hello, ${this.who}!`;
    },

    farewell: () => {
        return `Goodbye, ${this.who}!`;
    },
};

console.log(object.greet()); // What is logged?
console.log(object.farewell()); // What is logged?
```

### 7-masala

`call` funksiyasini shunday 3 turli xil usullarda chaqiringki, natijada barcha chaqirishlar bir xil qiymat chiqarsin.

```js
var num1 = 1;

function foo(num2) {

    console.log(this.num1 + num2);

}

foo(2); // -> 3

foo.call() // -> 10
foo.call() // -> 10
foo.call() // -> 10
```

### 8-masala

```js
let ismlar = ["FOO", "BAR", "BAZ"]
var myName = "ABC"

function salomlash(names) {

    names.forEach(name => console.log(`Salom ${name}, mening ismim, ${this.myName}`))

}

logNames(ismlar);
// -> "Salom FOO, mening ismim ABC"
// -> "Salom BAR, mening ismim ABC"
// -> "Salom BAZ, mening ismim ABC"

logNames.call(/* ? */)
// -> "Salom FOO, mening ismim 113"
// -> "Salom BAR, mening ismim 123"
// -> "Salom BAZ, mening ismim 123"

logNames.apply(/* ? */)
// -> "Salom FOO, mening ismim 113"
// -> "Salom BAR, mening ismim 123"
// -> "Salom BAZ, mening ismim 123"
```
