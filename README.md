<style type="text/css">
@font-face {
    font-family: font;
    src: url('BNazanin.ttf')
}
p {
    font-family: font;
}
</style>
<h1 dir="rtl">شمارنده در پایتون</h1>
<p dir = "rtl">   شمارنده یک قابلیت در پایتون است که از نسخه‌ی ۳.۴ به بعد به آن اضافه شده است. شمارنده فواید بسیار زیادی دارد و در مواقعی که میخواهیم کلاسی با تعداد محدودی شی از آن بسازیم از شمارنده استفاده میکنیم. بدین‌ترتیب مقادیر شمارنده اشتباها با مقادیر عدد صحیح مقایسه نشده و میتوان برای نحوه‌ی رفتار آن‌ها را تعیین کرد، برای مثال نحوه‌ی چاپ شدن آن‌ها و یا اضافه کردن تعدادی متد به شمارنده‌ها. علاوه بر پیاده‌سازی داخلی شمارنده در پایتون، روش‌های متعددی هم برای پیاده‌سازی دستی توسط خود شخص باتوجه به کاربردهای او وجود دارد. </p>
<p dir = "rtl">در تکه کدهای زیر یک پیاده‌سازی مرسوم و ناسازگار را مشاهده میکنید. برای استفاده از این پیاده‌سازی ابتدا باید کتاب‌خانه‌ی  enum34   یا aenum را با استفاده از دستورات زیر نصب کنید. </p>

- **To use enum34: $ pip install enum34**
- **To use aenum: $ pip install aenum**



```markdown
from enum import Enum    #for enum34, or the stdlib version
#from aenum import Enum   #for the aenum version 
Animal = Enum('Animal', 'ant bee cat dog')
Animal.ant  #returns <Animal.ant: 1>
Animal['ant']  #returns <Animal.ant: 1> (string lookup)
Animal.ant.name  #returns 'ant' (inverse lookup)


```
<p dir= "rtl">یا به طور مشابه:</p>

```markdown
class Animal(Enum):
    ant = 1
    bee = 2
    cat = 3
    dog = 4
```

<p dir = "rtl"> هم‌چنین شمارنده را می‌توان به صورت دستی با استفاده از تعریف یک کلاس پیاده‌سازی کرد:</p>

```markdown
class Animal:
    DOG = 1
    CAT = 2

x = Animal.DOG 
```
<p dir = "rtl"> یک روش دیگر برای پیاده‌سازی شمارنده در کد زیر معرفی شده‌است:</p>


```markdown
class Enum(set):
    def __getattr__(self, name):
        if name in self:
            return name
        raise AttributeError
```
<p dir = "rtl"> این روش در مقایسه با روش‌های معرفی شده در قبل پیچیده‌تر و کندتر است اما فوایدی دارد از جمله اینکه اگر کاربر .شمارنده‌ای مانند زیر تعریف کند</p>

```markdown
Animals = Enum(["DOG", "CAT", "HORSE"])
```
<p dir = "rtl">و سپس کدهای زیر را اجرا کنیم داریم:</p>

```markdown
print(Animals.DOG) #print DOG
print(Animals.SNAKE) #AtrributeError
```
<p dir = "rtl">یعنی در صورت صدا زدن شمارنده روی شی که قبلا اسم آن در شمارنده وارد نشده‌است، با پیغام خطا روبه‌رو خواهیم شد.</p>
