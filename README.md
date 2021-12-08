# AI-Week8

Link: https://eliavamar.itch.io/ai-week8


Changes we made to the original code:

In this game you can navigate between the states in the enemy's state machine, in order to define the enemy behavior:

Press E:  The enemy will choose the furthest target from the player in his arsenal of target destinations and move towards it.

Press G: The enemy will choose the closest target from the player in his arsenal of target destinations and move towards it.

Press C: The enemy will chase the player.

Press H: The enemy will go after the engine inside the building.

במשימה זו בחרנו לעשות state machine, להלן המצבים:

![image](https://user-images.githubusercontent.com/73071299/145189395-87768412-8edf-48dc-8726-a4a20240500c.png)


מצב התחלתי-Idle:
הגדרנו את המשחק כך שכשאנו מתחילים האויב לא יזוז עד שנלחץ על אחד מהמקשים שהגדרנו.
וכעת אנו בודקים אם לחצנו עליהם אם כן נשנה את המשתנה הבולאני שמעביר אותנו לשלב שמתאים לכפתור ל-true

![image](https://user-images.githubusercontent.com/73071299/145189653-82b7c9a7-e1ce-4a77-98a2-7528a5606390.png)


EscapingPlayer:

תחילה נחפש את הנק' הרחוקה ביותר מהשחקן שקיימית לנו בעולם ונלך לכיוונה:

![image](https://user-images.githubusercontent.com/73071299/145190679-8d42c9fd-3a06-4dca-b63e-a93b646041e1.png)

נבנה פונקציה שאומרת לנו האם יש נק רחוקה יותר, דבר זה יכול לקרות מכייון שהשחקן יכול לזוז והתרחק מנק אחת ולהתקרב לאחרת:

![image](https://user-images.githubusercontent.com/73071299/145191069-cb261cc4-ce49-4bde-95a3-e0febd7a4431.png)

נבנה פונקציה אשר בודקת האם לחצנו על אחד ממקשי האומרים לאויב לשנות את אופיו, אם אכן לחצנו נשנה את המצב:

![image](https://user-images.githubusercontent.com/73071299/145191289-dbd18936-0660-4c90-be82-a29b1ec7145e.png)


ולבסוף נראה את הפונקציה אשר מנהלת את כל התהליך:

![image](https://user-images.githubusercontent.com/73071299/145191501-9f4e5894-a6de-4ba7-818c-44b2ae56678a.png)


GuardingPlayer:

כעת נרצה לבחור את המטרה הקרובה ביותר לשחקן ולהתקדם עם האויב לכיוונה:

![image](https://user-images.githubusercontent.com/73071299/145191810-c285265f-0d70-4ca4-940f-6107f2270953.png)


ולאחר מכן נרצה לבדוק כי אין מטרה קרובה יותר:

![image](https://user-images.githubusercontent.com/73071299/145191891-5ed6efc9-97b4-4c2a-8b3f-cb43bb3b3cd5.png)

בנוסף נרצה לבדוק האם לחצנו על כפתור שינוי מצב:

![image](https://user-images.githubusercontent.com/73071299/145191972-1ab9b914-30c5-4c0e-86c8-81992c8d9418.png)

ולבסוף נבנה פונקציה אשר מנהלת את הכל:

![image](https://user-images.githubusercontent.com/73071299/145192058-86423254-2532-498b-bab8-2713c3dd836e.png)


ChaseEngine:

במצב זה נתן לאויב את מיקום המנוע כדי שינוע לכיוונו:

![image](https://user-images.githubusercontent.com/73071299/145192530-7391050d-e77f-4d5b-b559-39b6ca4a7e36.png)

בנוסף אנו בודקים שלא עברנו מצב:

![image](https://user-images.githubusercontent.com/73071299/145192611-5f5bda5f-22d2-4063-bf98-07ae0cdef4ae.png)

ChasePlayer:

במצב זה אנו נתן לאויב את מיקום השחקן על מנת שיזוז לכיוונו:


![image](https://user-images.githubusercontent.com/73071299/145193063-d1f54e2c-25c6-4b68-a62b-f76038a44e07.png)



כשאנחנו יוצאים מכל מצב אנו מכבים אותו, דוגמא:

![image](https://user-images.githubusercontent.com/73071299/145193170-a486f46e-394a-4271-b138-31c71d48e301.png)




