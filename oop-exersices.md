# Object Oriented Programmingga oid masalalar


### 1-masala

`Person` nomli class yasang. Unda `name`, `age` va `country` maydonlari, `introduce` methodi bo'lsin. 

```js
class Person {
  // tadbiq eting
}

const person1 = new Person("John Doe", 21, "USA");
const person2 = new Person("Jane Doe", 20, "UK");

console.log(person1.name) // -> "John Doe"
console.log(person2.country) // -> "UK"

person1.introduce(); // -> "Mening ismim John Doe. Yoshim 21 da. USAda tug'ilganman."

```

> `class` syntax bilan topshiriqni bajargandan keyin `Contructor function` bilan ham topshiriqni bararishga harakat qiling.

### 2-masala

`Rectangle` nomli class yasang. Unda `height`, `width` maydonlari, `area` yuzani hisoblovchi, va `perimeter` perimeterni hsioblovchi metodlar bo'lsin.

```js
class Rectangle {
  // tadbiq eting
}

const rec1 = new Rectangle(10, 5);
console.log(rec1.area()); // -> 50
console.log(rec1.perimeter()); // -> 30
```

> `class` syntax bilan topshiriqni bajargandan keyin `Contructor function` bilan ham topshiriqni bararishga harakat qiling.

### 3-masala

`Televizor`, `ElektronChoynak`, `DoskaPardasiPulti`, `Eskalator`, `Lion`, `Cat`, `Dog` kabi obyektlar yasang, ularda qanday maydonlar va methodlar bo'lishi mumkinligi haqida o'ylang. Va ularni tadbiq eting. Yuqoridagilardan tashqari, yana 5 ta odatiy hayotda uchraydigan narsalar uchun class yozib ko'ring.

> Misol qilib `ElektronChoynak` ni tushuntirsam. Unda `model` maydoni bo'lishi mumkin.
> `openPPLib` - qopqoqni ochish
> `closePPLib` - qopqoqni yopish
> `plugIn` - taglikni manbaga ulash
> `attachToBase` - choynakni asosga ulash
> `detachFromBase` - choqnakni asosdan ajratish
> `powerOn` - choynakni One Touch Power bilan yoqish
> `powerOff` - choynakni One Touch Power bilan o'chirish  
> ![image](https://github.com/MirzayevOrzu/js-ninja-exercises/assets/72085156/e8d64edc-5612-4bad-9412-d8310e5fc861)





