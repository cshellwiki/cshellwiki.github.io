# [לינוקס] C Shell (csh) chgrp שימוש: שינוי בעלות קבוצתית על קבצים

## Overview
הפקודה `chgrp` משמשת לשינוי קבוצת הבעלות על קבצים או תיקיות במערכת הקבצים. זה מאפשר למשתמשים לנהל את ההרשאות והגישה לקבצים על פי קבוצות.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
chgrp [אפשרויות] [ארגומנטים]
```

## Common Options
- `-R`: משנה את קבוצת הבעלות באופן רקורסיבי לכל הקבצים והתיקיות בתיקייה הנתונה.
- `-v`: מציג מידע על כל שינוי שנעשה.
- `-c`: מציג מידע רק על שינויים שבוצעו.

## Common Examples
- שינוי קבוצת הבעלות על קובץ ספציפי:
  ```csh
  chgrp users myfile.txt
  ```

- שינוי קבוצת הבעלות על תיקייה וכל הקבצים בתוכה באופן רקורסיבי:
  ```csh
  chgrp -R users mydirectory
  ```

- שינוי קבוצת הבעלות על קובץ והצגת השינוי:
  ```csh
  chgrp -v users myfile.txt
  ```

- שינוי קבוצת הבעלות על מספר קבצים:
  ```csh
  chgrp users file1.txt file2.txt file3.txt
  ```

## Tips
- תמיד בדוק את קבוצת הבעלות הנוכחית של הקבצים לפני ביצוע שינויים באמצעות הפקודה `ls -l`.
- השתמש באופציה `-R` בזהירות, כדי לא לשנות קבוצות בעלות על קבצים לא רצויים.
- זכור שדרושים לך הרשאות מתאימות כדי לשנות קבוצת בעלות על קבצים.