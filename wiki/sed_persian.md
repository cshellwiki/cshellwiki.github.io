# [سیستم‌عامل] C Shell (csh) sed استفاده: ویرایش متن

## Overview
دستور `sed` یک ویرایشگر متن غیر تعاملی است که به شما این امکان را می‌دهد تا متن را به صورت خطی ویرایش کنید. این ابزار به ویژه برای پردازش و تغییر محتوای فایل‌ها و ورودی‌های متنی مفید است.

## Usage
سینتکس پایه دستور `sed` به صورت زیر است:

```bash
sed [options] [arguments]
```

## Common Options
- `-e`: برای مشخص کردن یک دستور ویرایش.
- `-f`: برای خواندن دستورات ویرایش از یک فایل.
- `-i`: برای ویرایش فایل‌ها به صورت درجا (بدون ایجاد فایل موقت).
- `-n`: برای خاموش کردن چاپ پیش‌فرض، فقط زمانی که دستور `p` استفاده می‌شود، خروجی چاپ می‌شود.

## Common Examples
- **جایگزینی یک کلمه در یک فایل:**
  ```bash
  sed 's/کلمه_قدیمی/کلمه_جدید/g' filename.txt
  ```

- **حذف خطوط خالی از یک فایل:**
  ```bash
  sed '/^$/d' filename.txt
  ```

- **چاپ فقط خطوطی که شامل یک کلمه خاص هستند:**
  ```bash
  sed -n '/کلمه/ p' filename.txt
  ```

- **ویرایش فایل به صورت درجا:**
  ```bash
  sed -i 's/کلمه_قدیمی/کلمه_جدید/g' filename.txt
  ```

## Tips
- همیشه قبل از استفاده از گزینه `-i` یک نسخه پشتیبان از فایل‌های خود تهیه کنید.
- از گزینه `-n` برای کنترل دقیق‌تر بر روی خروجی استفاده کنید.
- می‌توانید چندین دستور `sed` را با استفاده از `-e` به یکدیگر متصل کنید تا چندین ویرایش را در یک بار انجام دهید.