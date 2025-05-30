# [سیستم‌عامل] C Shell (csh) iconv استفاده: تبدیل کدگذاری متن

## Overview
دستور `iconv` در C Shell (csh) برای تبدیل کدگذاری متن استفاده می‌شود. این ابزار به شما این امکان را می‌دهد که فایل‌های متنی را از یک کدگذاری به کدگذاری دیگر تبدیل کنید، که برای کار با داده‌های متنی از منابع مختلف بسیار مفید است.

## Usage
سینتکس پایه دستور `iconv` به صورت زیر است:

```bash
iconv [options] [arguments]
```

## Common Options
- `-f` : مشخص کردن کدگذاری ورودی.
- `-t` : مشخص کردن کدگذاری خروجی.
- `-o` : تعیین نام فایل خروجی.
- `-c` : حذف کاراکترهای نامعتبر.

## Common Examples

### تبدیل فایل از UTF-8 به ISO-8859-1
```bash
iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
```

### تبدیل کدگذاری یک فایل و نمایش خروجی در ترمینال
```bash
iconv -f UTF-8 -t ASCII input.txt
```

### حذف کاراکترهای نامعتبر در حین تبدیل
```bash
iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
```

## Tips
- همیشه قبل از تبدیل، از فایل‌های اصلی خود پشتیبان بگیرید.
- برای بررسی کدگذاری فایل‌ها، می‌توانید از ابزارهایی مانند `file` استفاده کنید.
- اگر با کدگذاری‌های خاص کار می‌کنید، مستندات مربوط به آن‌ها را مطالعه کنید تا از سازگاری اطمینان حاصل کنید.