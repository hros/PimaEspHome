<div dir="rtl">

**** ראשוני מאוד ולא בשל אבל ....
לינק להודעה #114  08/09/2020 15:42

החלטתי שלשים RPI (גם זירו) זה overkill
בנוסף החלטתי ללמוד משהו חדש

בשורה התחתונה כרגע יש לי esp8266 - כרטיס שקניתי ב ali
https://www.aliexpress.com/item/32995506222.html?spm=a2g0s.9042311.0.0.27424c4depAp9s

הכרטיס מקבל 5v ויש לו מייצב
ולפי מה שרשום כנראה מתמודד עם 5V בממשק ה UART
הוספתי ממיר חיצוני כדי שיוכל לקבל את ה 12V של האזעקה
(יש תמונה של מה שמורכב כרגע)

לכאורה הוא מגיע עם תוכנה שמאפשרת להעביר UART על הרשת
אבל צריך לפקד ב AT דרך ה UART - לא רלוונטי שמחובר לאזעקה

בהתחלה חשבתי להוריד קוד דוגמא שעושה בדיוק העברה של uart על הרשת
לקנפג hardcoded את הקצבים וחיבור ל wifi הביתי
ואז להשתמש בסקריפט פייתון ולהריץ אותו באיזה rpi - אולי אפילו על אותו rpi של HA

אבל זה סתר את הרצון שלי ללמוד משהו חדש
אז החלטתי לממש את הפרוטוקול כבר על ה ESP ואפילו זה עבד
אפילו הוספתי עדכון OTA (אבל רק דרך סביבת הפיתוח) והודעת debug שלחתי ברשת כי ה uart היה תפוס
כבר חשבתי להוסיף ספרייה של mqtt ולסיים
אבל הרגשתי שיש חיסרון בלנהל דבר כזה
חיפשתי framework פשוט - אבל לא מצאתי משהו (האמת מצאתי - סגרתי את החלון ולא מוצא שוב)

בסוף החלטתי לשבת על esphome
בשונה מ tasmota שמגיע עם הרבה אלמנטים ורק מורידים לו קונפיגורצה
ב esphome הקונפיגרציה משפיעה על הקימפול ומורידים לרכיב קוד מותאם
גיליתי שיש לו אופציה להוספת קוד חיצוני
בנוסף יש לו ממשק סגור מול HA (מתבסס על תוסף שלהם) ולא חייבים mqtt למרות שזה פחות גנרי

מודה שאני עדיין לא מבין לגמרי את הפרוטוקול - לא יודע מי כתב את המסמך של הממשק :(
מודה שגם אני לא איש תוכנה - ובהתאם כך נראה הקוד שלי (פעם אחרונה שכתבתי ב C לפני 20 שנים)
בנוסף מודה שלא לגמרי אני עדיין מכיר את כל השטויות של esphome ושל HA
אבל עדיין כרגע זה עובד בצורה לא רעה אבל רק לטלמטריה
יש לי סנסור על מצב האזעקה
וכן סנסור על כל האזורים הפתוחים

אני צריך עוד קצת לבשל את זה וללמוד לעבוד עם GIT
ואעלה את זה למקום מסודר כדי שאם יש אנשים שרוצים לשפר את זה יוכלו לקחת את זה קדימה

<div dir="ltr">