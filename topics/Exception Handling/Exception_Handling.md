# Exceptions & Exception Handling in JAVA

**Exceptions** — Kutilmagan holatda yoki qanaqadir actiondan keyin, Java exception otib loyihani terminate qilishiga aytiladi.  Java da exception "unwanted or unexpected event" deb ham ataladi.
- **Nega exception chiqadi** — Masalan: Internet muammosi, user tomonidan notog'ri kiritilgan ma'lumot yoki topilmagan fileni ochishga harakat qilganda exception chiqishi mumkin.

Exceptionlar projectimizni terminate qilib yubormasligi uchun, biz Exception handlerlardan foydalanamiz.

`try` - Exception sodir bo'lishi mumkin bo'lgan kodlarni o'zida saqlaydi.
`catch` - Exception sodir bo'lganda, uni handle qilish uchun ishlatiladi va doim try bilan birga keladi.
`throw` - Bu Exception otish uchun ishlatiladi.