# [לינוקס] C Shell (csh) psql שימוש: הפעלת לקוח PostgreSQL

## Overview
הפקודה `psql` היא לקוח שורת פקודה עבור PostgreSQL, המאפשר למשתמשים להתחבר למסדי נתונים, להריץ שאילתות SQL ולבצע פעולות ניהול שונות.

## Usage
התחביר הבסיסי של הפקודה `psql` הוא:

```bash
psql [options] [arguments]
```

## Common Options
- `-h` : מציין את הכתובת של השרת.
- `-p` : מציין את מספר הפורט להתחברות.
- `-U` : מציין את שם המשתמש להתחברות למסד הנתונים.
- `-d` : מציין את שם מסד הנתונים להתחברות.
- `-c` : מריץ פקודת SQL אחת ומסיים את החיבור.

## Common Examples
להלן מספר דוגמאות שימוש נפוצות ב-`psql`:

1. להתחבר למסד נתונים מקומי בשם `mydb` עם שם משתמש `user`:
    ```bash
    psql -U user -d mydb
    ```

2. להריץ שאילתת SQL ישירות מהשורת פקודה:
    ```bash
    psql -U user -d mydb -c "SELECT * FROM my_table;"
    ```

3. להתחבר לשרת מרוחק בכתובת `192.168.1.100` על פורט `5432`:
    ```bash
    psql -h 192.168.1.100 -p 5432 -U user -d mydb
    ```

4. לייבא קובץ SQL למסד הנתונים:
    ```bash
    psql -U user -d mydb -f my_script.sql
    ```

## Tips
- תמיד כדאי לבדוק את הגרסה של `psql` באמצעות הפקודה `psql --version` כדי לוודא שאתה משתמש בגרסה הנכונה.
- השתמש באופציה `-W` כדי להכריח את `psql` לבקש סיסמה, אם אתה מעדיף לא להכניס אותה בשורת הפקודה.
- ניתן להשתמש בפקודת `\?` לאחר הכניסה ל-`psql` כדי לקבל רשימה של פקודות עזר זמינות.