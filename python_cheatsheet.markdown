# برگه تقلب جامع پایتون


| **موضوع** | **دستور/مفهوم** | **توضیح** | **مثال** |
|------------|------------------|------------|-----------|
| **مفاهیم پایه** | | | |
| تعریف متغیر | تخصیص مقدار | متغیرها بدون نیاز به تعریف نوع داده ایجاد می‌شوند. | ```python<br>x = 10  # عدد صحیح<br>y = 3.14  # اعشاری<br>name = "Ali"  # رشته<br>is_active = True  # بولین<br>print(x, y, name, is_active)<br>``` → `10 3.14 Ali True` |
| چاپ خروجی | `print()` | نمایش خروجی در کنسول با قابلیت قالب‌بندی. | ```python<br>print("Hello, World!")<br>num = 42<br>print(f"Number: {num}")<br>``` → `Hello, World!`<br>`Number: 42` |
| نظرات | `#`, `""" """` | توضیحات تک‌خطی یا چندخطی برای کد. | ```python<br># تک‌خطی<br>"""<br>چندخطی<br>برای توضیحات طولانی<br>"""<br>``` |
| بررسی نوع | `type()` | نمایش نوع داده یک متغیر. | ```python<br>x = "Hello"<br>print(type(x))<br>``` → `<class 'str'>` |
| تبدیل نوع | `int()`, `float()`, `str()` | تغییر نوع داده متغیر. | ```python<br>x = "5"<br>y = int(x)<br>print(y + 2)<br>``` → `7` |
| **ساختارهای کنترلی** | | | |
| شرط‌ها | `if`, `elif`, `else` | اجرای کد بر اساس شرط‌های منطقی. | ```python<br>age = 20<br>if age >= 18:<br>    print("Adult")<br>elif age >= 13:<br>    print("Teen")<br>else:<br>    print("Child")<br>``` → `Adult` |
| حلقه for | `for`, `range()` | تکرار روی دنباله‌ها یا محدوده اعداد. | ```python<br>for i in range(3):<br>    print(f"Iteration {i}")<br>``` → `Iteration 0`<br>`Iteration 1`<br>`Iteration 2` |
| حلقه while | `while` | تکرار تا زمانی که شرط برقرار باشد. | ```python<br>count = 0<br>while count < 3:<br>    print(f"Count: {count}")<br>    count += 1<br>``` → `Count: 0`<br>`Count: 1`<br>`Count: 2` |
| کنترل حلقه | `break`, `continue` | توقف یا پرش در حلقه. | ```python<br>for i in range(5):<br>    if i == 3:<br>        break<br>    print(i)<br>``` → `0 1 2` |
| **ساختارهای داده** | | | |
| لیست | `list` | مجموعه مرتب و تغییرپذیر. | ```python<br>numbers = [1, 2, 3]<br>numbers.append(4)<br>print(numbers[1])<br>print(numbers)<br>``` → `2`<br>`[1, 2, 3, 4]` |
| تاپل | `tuple` | مجموعه مرتب و غیرقابل‌تغییر. | ```python<br>coords = (10, 20)<br>print(coords[0])<br>``` → `10` |
| دیکشنری | `dict` | جفت‌های کلید-مقدار. | ```python<br>user = {"name": "Ali", "age": 25}<br>print(user["name"])<br>user["age"] = 26<br>print(user)<br>``` → `Ali`<br>`{'name': 'Ali', 'age': 26}` |
| مجموعه | `set` | مجموعه بدون تکرار و بدون ترتیب. | ```python<br>unique = {1, 2, 2, 3}<br>unique.add(4)<br>print(unique)<br>``` → `{1, 2, 3, 4}` |
| **توابع** | | | |
| تعریف تابع | `def` | ایجاد تابع با پارامتر و مقدار بازگشتی. | ```python<br>def square(num):<br>    return num * num<br>result = square(4)<br>print(result)<br>``` → `16` |
| پارامتر پیش‌فرض | `def` با مقدار پیش‌فرض | پارامترهای اختیاری با مقدار اولیه. | ```python<br>def greet(name="Guest"):<br>    return f"Hello, {name}!"<br>print(greet())<br>print(greet("Ali"))<br>``` → `Hello, Guest!`<br>`Hello, Ali!` |
| تابع بی‌نام | `lambda` | تابع کوتاه برای عملیات ساده. | ```python<br>double = lambda x: x * 2<br>print(double(5))<br>``` → `10` |
| **کار با رشته‌ها** | | | |
| الحاق رشته | `+`, `join()` | ترکیب رشته‌ها. | ```python<br>text = "Hello" + " World"<br>words = ["a", "b", "c"]<br>joined = "-".join(words)<br>print(text, joined)<br>``` → `Hello World a-b-c` |
| قالب‌بندی رشته | `f-string` | جایگذاری متغیرها در رشته. | ```python<br>name = "Ali"<br>age = 25<br>print(f"{name} is {age} years old")<br>``` → `Ali is 25 years old` |
| متدهای رشته | `upper()`, `lower()`, `strip()`, `split()` | تغییر یا پردازش رشته‌ها. | ```python<br>text = "  Hello World  "<br>print(text.strip().upper())<br>print(text.split())<br>``` → `HELLO WORLD`<br>`['Hello', 'World']` |
| **مدیریت خطاها** | | | |
| استثناها | `try`, `except`, `finally` | مدیریت خطاها و اجرای کد نهایی. | ```python<br>try:<br>    result = 10 / 0<br>except ZeroDivisionError:<br>    print("Cannot divide by zero")<br>finally:<br>    print("Done")<br>``` → `Cannot divide by zero`<br>`Done` |
| **ماژول‌ها و کتابخانه‌ها** | | | |
| وارد کردن ماژول | `import`, `from ... import` | استفاده از ماژول‌های داخلی یا خارجی. | ```python<br>import math<br>print(math.pi)<br>from random import randint<br>print(randint(1, 10))<br>``` → `3.141592653589793`<br>`(عدد تصادفی بین 1 تا 10)` |
| نصب بسته | `pip` | نصب کتابخانه‌های خارجی. | ```bash<br>pip install numpy<br>``` |
| **کار با فایل‌ها** | | | |
| خواندن فایل | `open("file", "r")` | خواندن محتوای فایل متنی. | ```python<br>with open("data.txt", "r") as file:<br>    content = file.read()<br>print(content)<br>``` |
| نوشتن در فایل | `open("file", "w")` | نوشتن یا بازنویسی در فایل. | ```python<br>with open("output.txt", "w") as file:<br>    file.write("Hello, Python!")<br>``` |
| اضافه کردن به فایل | `open("file", "a")` | افزودن به انتهای فایل. | ```python<br>with open("output.txt", "a") as file:<br>    file.write("\nNew line")<br>``` |
| **کتابخانه‌های پرکاربرد** | | | |
| کار با آرایه‌ها | `numpy` | عملیات سریع روی آرایه‌ها. | ```python<br>import numpy as np<br>arr = np.array([1, 2, 3])<br>print(arr * 2)<br>``` → `[2 4 6]` |
| کار با داده‌ها | `pandas` | مدیریت داده‌های جدولی. | ```python<br>import pandas as pd<br>df = pd.DataFrame({"name": ["Ali", "Sara"], "age": [25, 30]})<br>print(df)<br>``` → جدول با نام و سن |
| درخواست HTTP | `requests` | ارسال درخواست به وب. | ```python<br>import requests<br>response = requests.get("https://api.example.com")<br>print(response.status_code)<br>``` → `200` (در صورت موفقیت) |
| **مدیریت زمان** | | | |
| زمان و تاریخ | `datetime` | کار با تاریخ و زمان. | ```python<br>from datetime import datetime<br>now = datetime.now()<br>print(now.strftime("%Y-%m-%d %H:%M:%S"))<br>``` → `2025-09-04 22:33:00` |
| تأخیر | `time.sleep()` | توقف اجرای کد برای مدت مشخص. | ```python<br>import time<br>print("Start")<br>time.sleep(2)<br>print("End")<br>``` → بعد از 2 ثانیه |
| **برنامه‌نویسی پیشرفته** | | | |
| لیست‌ساز | List Comprehension | ساخت لیست به‌صورت فشرده. | ```python<br>evens = [x for x in range(10) if x % 2 == 0]<br>print(evens)<br>``` → `[0, 2, 4, 6, 8]` |
| ژنراتور | `yield` | تولید مقادیر به‌صورت تدریجی. | ```python<br>def fib(n):<br>    a, b = 0, 1<br>    for _ in range(n):<br>        yield a<br>        a, b = b, a + b<br>print(list(fib(5)))<br>``` → `[0, 1, 1, 2, 3]` |
| کلاس‌ها | `class` | برنامه‌نویسی شیءگرا. | ```python<br>class Person:<br>    def __init__(self, name, age):<br>        self.name = name<br>        self.age = age<br>    def introduce(self):<br>        return f"I'm {self.name}, {self.age} years old"<br>p = Person("Ali", 25)<br>print(p.introduce())<br>``` → `I'm Ali, 25 years old` |
| وراثت | `class Child(Parent)` | ارث‌بری از کلاس والد. | ```python<br>class Student(Person):<br>    def study(self):<br>        return f"{self.name} is studying"<br>s = Student("Sara", 20)<br>print(s.introduce())<br>print(s.study())<br>``` → `I'm Sara, 20 years old`<br>`Sara is studying` |