# [سیستم‌عامل‌های یونیکس] C Shell (csh) unxz استفاده: [فشرده‌سازی فایل‌ها]

## Overview
دستور `unxz` برای استخراج فایل‌های فشرده‌شده با فرمت XZ استفاده می‌شود. این دستور به شما امکان می‌دهد تا فایل‌های فشرده را به حالت اولیه خود بازگردانید.

## Usage
سینتکس پایه این دستور به صورت زیر است:

```
unxz [options] [arguments]
```

## Common Options
- `-k`: این گزینه فایل فشرده اصلی را حفظ می‌کند و فقط نسخه استخراج‌شده را ایجاد می‌کند.
- `-v`: این گزینه اطلاعات بیشتری را در مورد فرآیند استخراج نمایش می‌دهد.

## Common Examples
در اینجا چند مثال عملی از استفاده از دستور `unxz` آورده شده است:

### مثال ۱: استخراج یک فایل
برای استخراج یک فایل فشرده با نام `file.xz`، می‌توانید از دستور زیر استفاده کنید:

```
unxz file.xz
```

### مثال ۲: حفظ فایل اصلی
اگر می‌خواهید فایل اصلی `file.xz` را پس از استخراج حفظ کنید، از گزینه `-k` استفاده کنید:

```
unxz -k file.xz
```

### مثال ۳: نمایش اطلاعات استخراج
برای مشاهده اطلاعات بیشتر در حین استخراج، از گزینه `-v` استفاده کنید:

```
unxz -v file.xz
```

## Tips
- همیشه قبل از استخراج، از فایل‌های مهم خود نسخه پشتیبان تهیه کنید.
- اگر با فایل‌های بزرگ کار می‌کنید، مطمئن شوید که فضای کافی در دیسک برای فایل استخراج‌شده وجود دارد.
- برای فشرده‌سازی مجدد فایل‌ها، می‌توانید از دستور `xz` استفاده کنید.