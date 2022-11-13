# git-team-project

\* - додаткові підказки

Як процювати з проектом?

1. Спочатку скопіювати собі локально проетк з гітхаба (git clone (адреса репозиторію));
2. У головній гілці ми НЕ працюємо! Тому створюємо нові гілки для наших задач (git branch (назва гілки));
   // Перглянути всі наші локальні гілки можна за допомогою команди - (git branch) \* та гілка на якій ми знаходимося підсвічується зірочкою;
3. Переходимо на потрібну нам гілку (git checkout (назва гілки));
4. Вже тепер можемо працювати зі своєю задачею));
   // Щоб переглянути зміни файлів, за якими гіт ще не слідкує, треба викликати команду (git status);
5. Зберігаємо змінені і створені файли (git add .);
   // git status покаже що ми зберегли(зеленим кольором);
   // в робочій області НЕзбережені створені файли познач. - U, а збережені - А; .
   // в робочій області НЕзбережені змінені файли познач. - М(більш ТЕМНО-жовтим кольором), а збережені - М(більш СВІТЛО-жовтим кольором);
   // збереження можна відмінити (git reset);
6. Підписуємо збережені файли (git commit -m "(описуємо свої зміни)");
7. Тепер потрібно відправити зміни на гітхаб (git push), але ми працюємо в гілці, яку створили собі локально, і на гітхабі її нема, тому це не спрацює((;
8. Після того як ми ввели git push, термінал нам підкаже, яку використати команду. Копіюємо її і викликаємо. Ця команда створить гілку на гітхаб реппозиторії, і лише після цього запушить туди наш коміт. \* Або використовуємо скорочену версію цієї команди - (git push -u origin (назва гілки));
9. Уже наступні пуші в цю гілку нам потрібно робити через команду (git push), бо ця гілка вже створена;
10. Щоб підтянути всі зміни, які зробили наші тімейти, з гітхабу на наш локальний проект треба викон. ком. (git pull)
    // При тому треба памятати, що зміни підтягуються тільки на ту гілку на якій ми знаходимося!!!;
11. Для того щоб злити тимчасову гілку із головною для початку треба перейти на ту гілку, яка приймає злиття(тобто головна), і вик. ком. (git merge (назва гілки, яку ми зливаємо));
    // Перед мержом важливо перевіряти, чи всі зміни у нас збережені!
12. Якщо нам гілка вже не потрібна, то видаляємо її(git branch -d (назва гілки)). При видал. ми можемо знаходитися на будь-якій гілці, крім тої, яку видаляємо!;
13. Також видаляємо цю гілку на гітхабі (git push origin --delete (назва гілки));
14. При злитті гілок можуть виникати конфлікти. Якщо ми зараз не хочемо їх вирішувати, то можемо скасувати злиття (git merge --abort)
15. При переході між гілками незбережені дані будуть видалені. Але ми не хочемо робити коміт. Тоді використ. (git stash) - ця крманда додає незбережені дані в буфер обміну. А коли ми повернулися на цю гілку то викон. ком. (git stash apply) і всі дані з буферу обміну стануть на своє місце.

Команди для упрощення роботи:

- (git checkout -b (назва гілки)) - замінює відразу дві команди (git branch (назва гілки)) і (git checkout (назва гілки))
- (git commit -am "(описуємо свої зміни)") - замінює відразу дві команди (git add .) і (git commit -m "(описуємо свої зміни)")
