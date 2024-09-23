# OOP in Java

## Object-Oriented Programming (OOP) in Java

**Object** — har qanday predmet yoki buyumlar `Object` deb ataladi.  
`Object`ning xususiyatlari (`properties`) va metodlari mavjud bo'ladi.  
- **Property** — bu jism yoki narsaga mos belgilar.  
- **Method** — uning qobiliyatlari.

### Misol:
Masalan, odamni `Object` deb olsak, uning ismi, yoshi — `property`, gapirishi, yurishi — `method` hisoblanadi.

`Object` — OOPda fundamental tushunchadir.

---

## OOP Principles

OOP bilan ishlashda asosiy 4ta tamoyil (`principles`) mavjud:

1. **Encapsulation**
2. **Inheritance** (meros olish)
3. **Polymorphism**
4. **Abstraction**

---

## Class

`Class` — tasavvur qilaylik, mushuklar bor. Har bir mushukning o'ziga xos xususiyatlari mavjud:  
- rang  
- hajm  
- meowlashi

Ushbu `Object`ning umumiy xususiyatlari va metodlarini Shablon qilib saqlash uchun classlar ishlatiladi.  
`Class`lar `Object`ning `property` va `method`larini saqlaydi.

---

## Constructors

1. **Constructor** bu yangi `Object`larni e'lon qilish uchun ishlatiladigan maxsus `method`.
2. Constructor `Object`ning boshlang'ich qiymatlarini (`initial values`) belgilash imkonini beradi.
3. Constructor orqali yangi `Object`larning qiymatlarini o'zgartirish mumkin.
4. Constructor chaqirilganda yangi `Object` uchun yangi joy (`memory`) ajratiladi.

---

## Constructor Turlari

1. **Default Constructor** — Bu har qanday `Object` yaratilganda avtomatik chaqiriladigan Constructor. Agar `class`da `Constructor` ko'rsatilmagan bo'lsa, `default constructor` avtomatik tarzda yaratiladi.
2. **Parametrized Constructor** — Bu Constructor, `Object` yaratish vaqtida specific parametrlarni qabul qilish imkoniyatini beradi.
3. **Copy Constructor** — Bu Constructor boshqa `Object`ning `property`larini yangi `Object`ga o'tkazish imkonini beradi.

---

## Keywords

### `this` Keyword

`this` keywords — `Object`ning o'ziga tegishli qiymatlarni ko'rsatishda,  
name conflictlarni hal qilishda va `class` ichidagi `Constructor` holatlarda ishlatiladi.

---
