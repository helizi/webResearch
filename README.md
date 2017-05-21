
<h1 dir="rtl">شمارنده در پایتون</h1>
<p dir = "rtl">   شمارنده یک قابلیت در پایتون است که از نسخه‌ی ۳.۴ به بعد به آن اضافه شده است. شمارنده فواید بسیار زیادی دارد و در مواقعی که میخواهیم کلاسی با تعداد محدودی شی از آن بسازیم از شمارنده استفاده میکنیم. بدین‌ترتیب مقادیر شمارنده اشتباها با مقادیر عدد صحیح مقایسه نشده و میتوان برای نحوه‌ی رفتار آن‌ها را تعیین کرد، برای مثال نحوه‌ی چاپ شدن آن‌ها و یا اضافه کردن تعدادی متد به شمارنده‌ها. علاوه بر پیاده‌سازی داخلی شمارنده در پایتون، روش‌های متعددی هم برای پیاده‌سازی دستی توسط خود شخص باتوجه به کاربردهای او وجود دارد. </p>
<p dir = "rtl">در تکه کدهای زیر یک پیاده‌سازی مرسوم و ناسازگار را مشاهده میکنید. برای استفاده از این پیاده‌سازی ابتدا باید کتاب‌خانه‌ی enum34 را با استفاده از دستور زیر نصب کنید </p>
To use enum34, do $ pip install enum34



```markdown
from enum import Enum     # for enum34, or the stdlib version
# from aenum import Enum  # for the aenum version
Animal = Enum('Animal', 'ant bee cat dog')

Animal.ant  # returns <Animal.ant: 1>
Animal['ant']  # returns <Animal.ant: 1> (string lookup)
Animal.ant.name  # returns 'ant' (inverse lookup)


```
<p dir= "rtl">یا به طور مشابه</p>

```markdown

class Animal(Enum):
    ant = 1
    bee = 2
    cat = 3
    dog = 4
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/helizi/webResearch/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text
You can use the [editor on GitHub](https://github.com/helizi/webResearch/edit/master/README.md) to maintain and preview the content for your website in Markdown files.
[Link](url) and ![Image](src)
