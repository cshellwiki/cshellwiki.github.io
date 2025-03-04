# [لینوکس] C Shell (csh) iotop استفاده: نمایش استفاده از دیسک توسط پروسه‌ها

## Overview
دستور `iotop` ابزاری است که به شما این امکان را می‌دهد تا استفاده از دیسک توسط پروسه‌های در حال اجرا را مشاهده کنید. این ابزار به ویژه برای شناسایی پروسه‌هایی که بار زیادی بر روی دیسک ایجاد می‌کنند، مفید است.

## Usage
سینتکس پایه دستور `iotop` به صورت زیر است:

```csh
iotop [options] [arguments]
```

## Common Options
- `-o` : فقط پروسه‌هایی را نمایش می‌دهد که در حال حاضر از دیسک استفاده می‌کنند.
- `-b` : خروجی را به صورت غیر تعاملی (batch) نمایش می‌دهد که برای ذخیره در فایل مناسب است.
- `-n NUM` : تعداد دفعاتی که خروجی باید نمایش داده شود را مشخص می‌کند.
- `-d SEC` : زمان تأخیر بین نمایش‌ها را به ثانیه تعیین می‌کند.

## Common Examples
- نمایش پروسه‌هایی که در حال حاضر از دیسک استفاده می‌کنند:
  ```csh
  iotop -o
  ```

- اجرای `iotop` به صورت غیر تعاملی و ذخیره خروجی در یک فایل:
  ```csh
  iotop -b -n 5 > output.txt
  ```

- مشاهده استفاده از دیسک با تأخیر ۲ ثانیه:
  ```csh
  iotop -d 2
  ```

## Tips
- برای مشاهده پروسه‌های با بار بالا، از گزینه `-o` استفاده کنید تا فقط پروسه‌های فعال را ببینید.
- برای تجزیه و تحلیل بهتر، خروجی را به یک فایل متنی هدایت کنید و بعداً آن را بررسی کنید.
- اگر با استفاده از `iotop` در محیط‌های گرافیکی مشکل دارید، از حالت غیر تعاملی (`-b`) استفاده کنید.