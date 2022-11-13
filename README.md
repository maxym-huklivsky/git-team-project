# git-team-project

\* - додаткові підказки

Як процювати з проектом?

1. Спочатку скопіювати собі локально проетк з гітхаба (git clone (адреса репозиторію));
2. У головній гілці ми НЕ працюємо! Тому створюємо нові гілки для наших задач (git branch (назва гілки))
   // Перглянути всі наші локальні гілки можна за допомогою команди - (git branch) \* та гілка на якій ми знаходимося підсвічується зірочкою
3. Переходимо на потрібну нам гілку (git checkout (назва гілки))
4. Вже тепер можемо працювати зі своєю задачею))
   // Щоб переглянути зміни файлів, за якими гіт ще не слідкує, треба викликати команду (git status)
5. Зберігаємо змінені і створені файли (git add .)
   // git status покаже що ми зберегли(зеленим кольором)
   // в робочій області НЕзбережені створені файли познач. - U, а збережені - А; .
   // в робочій області НЕзбережені змінені файли познач. - М(більш ТЕМНО-жовтим кольором), а збережені - М(більш СВІТЛО-жовтим кольором);
   // збереження можна відмінити (git reset)
6. Підписуємо збережені файли (git commit -m "(описуємо свої зміни)")
7. Тепер потрібно відправити зміни на гітхаб (git push), але ми працюємо в гілці, яку створили собі локально, і на гітхабі її нема, тому це не спрацює((;
8. Після того як ми ввели git push, термінал нам підкаже, яку використати команду. Копіюємо її і викликаємо. Ця команда створить гілку на гітхаб реппозиторії, і лише після цього запушить туди наш коміт.
