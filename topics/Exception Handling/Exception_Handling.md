**Exceptions** — bu dastur bajarilishida kutilmagan holatlar yuz berganda sodir bo'ladigan xatoliklar bo‘lib, ular dastur ishini to‘xtatadi (terminate qiladi). Java tilida exceptionslarni "unwanted or unexpected event" deb ham atashadi.

### Exceptionlar nima sababdan kelib chiqadi?
Exceptionlar quyidagi holatlarda yuzaga kelishi mumkin:
- **Internet muammolari**: Dastur serverga ulanmoqchi bo‘lganda internet uzilib qolsa.
- **Notog‘ri foydalanuvchi ma’lumoti**: Foydalanuvchi raqam kiritishi kerak bo‘lgan joyga matn kiritsa.
- **Fayl topilmagan**: Fayl mavjud bo'lmaganda va dastur undan ma'lumot o'qimoqchi bo'lsa.

### Exceptionlarni qanday hal qilish mumkin?
Java exceptionlarni boshqarish uchun kuchli mexanizmni taqdim etadi. Bu mexanizm yordamida dasturni xatoliklardan keyin ham to'g'ri ishlashini ta'minlash yoki kerak bo‘lsa, dastur muammosiz to'xtatilishini amalga oshirish mumkin. Buning uchun Java'da **exception handling** (exceptionsni boshqarish) usullari mavjud. Asosiy kalit so'zlar: `try`, `catch`, `throw`, `throws`, va `finally`.

#### Exception Handling Kalit So‘zlari:
1. **try**: Exception sodir bo‘lishi mumkin bo‘lgan kodni `try` blokiga yozamiz. Agar exception yuz bersa, u `catch` bloki orqali "ushlanadi".
   ```java
   try {
       // Exception chiqishi mumkin bo'lgan kod
   }
   ```
   
2. **catch**: Ushbu blok exceptionlarni ushlaydi va ularni boshqaradi. Har xil exception turlari uchun bir nechta `catch` bloklari bo‘lishi mumkin.
   ```java
   catch (ExceptionType e) {
       // Exceptionni boshqarish uchun kod
   }
   ```

3. **throw**: Bu kalit so'z yordamida exceptionni qo'lda "otish" mumkin, ya'ni uni maxsus holatlarda sun’iy ravishda chaqirish mumkin.
   ```java
   throw new ExceptionType("Exception xabari");
   ```

4. **throws**: Bu metod imzosida ishlatiladi va metod qanday exceptionlarni otishi mumkinligini ko'rsatadi.
   ```java
   public void metodNomi() throws ExceptionType {
       // metodning kodlari
   }
   ```

5. **finally**: Ushbu blok har doim bajariladi, exception chiqsa ham, chiqmasa ham. Odatda fayllarni yopish yoki resurslarni bo'shatish uchun ishlatiladi.
   ```java
   finally {
       // Har doim bajariladigan kod
   }
   ```

### Exception Turlari:
Java’da exceptionlar ikkita asosiy kategoriya bo‘yicha ajratiladi:

1. **Checked Exceptions**: Bu turdagi exceptionlar dastur kompilyatsiya qilinayotgan paytda tekshiriladi. Kompilyator bunday xatolarni `catch` blokiga olish yoki metodda `throws` kalit so'zidan foydalanishni talab qiladi.
   - Misol: `IOException`, `SQLException`
   - `FileNotFoundException` uchun kod namunasi (bu `IOException`ning subclassi):
     ```java
     try {
         FileReader fayl = new FileReader("yoqfile.txt");
     } catch (FileNotFoundException e) {
         System.out.println("Fayl topilmadi!");
     }
     ```

2. **Unchecked Exceptions**: Bu exceptionlar kompilyatsiya paytida tekshirilmaydi, balki runtime (dastur bajarilayotganda) sodir bo‘ladi. Odatda, bu dasturdagi mantiqiy xatolarni bildiradi.
   - Misol: `NullPointerException`, `ArrayIndexOutOfBoundsException`
   - `NullPointerException` uchun kod namunasi:
     ```java
     String matn = null;
     try {
         System.out.println(matn.length());
     } catch (NullPointerException e) {
         System.out.println("NullPointerException topildi!");
     }
     ```

### Bir nechta exceptionlarni boshqarish misoli:
```java
try {
    int[] sonlar = {1, 2, 3};
    System.out.println(sonlar[5]); // ArrayIndexOutOfBoundsException
    int natija = 10 / 0; // ArithmeticException
} catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("Indeks chegaradan chiqdi!");
} catch (ArithmeticException e) {
    System.out.println("Nolga bo'lish mumkin emas!");
} finally {
    System.out.println("Bu blok har doim ishlaydi.");
}
```

Bu misol bir nechta exception turlarini boshqarishni va dasturning abrupt tarzda to‘xtab qolmasligini ta’minlaydi.

Exception handling orqali dasturlaringizni yanada barqaror va ishonchli qilish mumkin.
