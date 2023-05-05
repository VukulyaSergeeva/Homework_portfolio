# GIT Homework 1


##JSON
 1. Создать внешний репозиторий c названием JSON.
 2. Клонировать репозиторий JSON на локальный компьютер.

>mkdir github_lesson_json
>cd github_lesson_json
>git clone https://github.com/VukulyaSergeeva/Json.git

 3. Внутри локального JSON создать файл “new.json”.
>touch new.json

 4. Добавить файл под гит.git add
>git add .

 5. Закоммитить файл.
>git commit -m "create new.json file"

 6. Отправить файл на внешний GitHub репозиторий.
>git push

 7. Отредактировать содержание файла “new.json” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате JSON.

> cat > new.json
>{
>   "personal_data":[
>      {
>         "name":"Victoria",
>         "surname":"Sergeeva",
>         "number_of_animals":"one",
>         "desired_salary":2500
>      }
>   ]
>}

 8. Отправить изменения на внешний репозиторий.
>git add
>git commit -m "change new.json"
>git push

 9. Создать файл preferences.json

> touch preferences.json
 

 10. В файл preferences.json добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате JSON.

> cat > preferences.json
>{
>   "hobbies":[
>      {
>         "film":"Destruction",
>         "TV_series":"The Office",
>         "Food":"Meat",
>         "time of the year":"spring",
>         "Travel":"Sweden"
>      }
>   ]
>}

 11. Создать файл sklls.json добавить информацию о скиллах которые будут изучены на курсе в формате JSON

>touch sklls.json
>cat >skills.json
>{"skills":"SQL, Postman, Git, Terminal, XCode, Dev Tools"}

12. Отправить сразу 2 файла на внешний репозиторий.
>git add .
>git commit -m "create two news json file"
>git push

13. На веб интерфейсе создать файл bug_report.json.
14. Сделать Commit changes (сохранить) изменения на веб интерфейсе.
15. На веб интерфейсе модифицировать файл bug_report.json, добавить баг репорт в формате JSON.
16. 19. Сделать Commit changes (сохранить) изменения на веб интерфейсе.
17. Синхронизировать внешний и локальный репозиторий JSON
>git pull





##XML
1. Создать внешний репозиторий c названием XML.
2. Клонировать репозиторий XML на локальный компьютер.
>mkdir github_lesson_XML
>cd github_lesson_XML
>git clone https://github.com/VukulyaSergeeva/XML.git

3. Внутри локального XML создать файл “new.xml”.
>cd XML
> touch new.xml

4. Добавить файл под гит.
>git add .

5. Закоммитить файл.
6. >git commit -m "add new file new.xml"

6. Отправить файл на внешний GitHub репозиторий.
>git push .

7. Отредактировать содержание файла “new.xml” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате XML.

>vim new.xml(открывается редактор vi)
В редакторе нажимаем на клавишу I и вносим данные в файл

	
><?xml version="1.0" encoding="UTF-8"?>
><info>
>        <name>Victoria</name>
>        <surname>Sergeeva</surname>
>        <pats>1</pats>
>        <salary>2500$</salary>
></info>

Нажимаем Esc,после нажимаем сочитание клавиш Shift+: ,а пеосле сохраняем файл сочетанием клавиш wq и жмем Enter

8. Отправить изменения на внешний репозиторий.
>git add .
>git commit -m "add new info about myself to new.xml"
>git push

9. Создать файл preferences.xml
>touch preferences.xml

10. В файл preferences.xml добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате XML.

>vim preferences.xml(открывается редактор vi)
В редакторе нажимаем на клавишу I и вносим данные в файл

> <?xml version="1.0" encoding="UTF-8"?>
> <favorite_things>
>        <film>Destraction</film>
>        <TV_series>The Office</Tv_series>
>        <food>Meat</food>
>        <time_of_year>Spring</time_of_year>
>        <country>Sweden</country>
></favorite_things>

Нажимаем Esc,после нажимаем сочитание клавиш Shift+: ,а пеосле сохраняем файл сочетанием клавиш wq и жмем Enter

11. Создать файл sklls.xml добавить информацию о скиллах которые будут изучены на курсе в формате XML

>touch sklls.xml
>cat > sklls.xml
><info>
>	<skills>SQL, Postman, Git, Terminal, XCode, Dev Tools</skills>
></info>

12. Сделать коммит в одну строку.
>git add .
>git commit -m "create two news xml file"


13. Отправить сразу 2 файла на внешний репозиторий.
>git push

14. На веб интерфейсе создать файл bug_report.xml.
15. Сделать Commit changes (сохранить) изменения на веб интерфейсе.
16. На веб интерфейсе модифицировать файл bug_report.xml, добавить баг репорт в формате XML.
17. Сделать Commit changes (сохранить) изменения на веб интерфейсе.
18. Синхронизировать внешний и локальный репозиторий XML
>git pull





##TXT
 1. Создать внешний репозиторий c названием TXT.
 2. Клонировать репозиторий TXT на локальный компьютер.

>mkdir git_less_txt
> cd git_less_txt
>git clone git@github.com:VukulyaSergeeva/TXT.git

 3. Внутри локального TXT создать файл “new.txt”.
>cd TXT
>touch new.txt

 4. Добавить файл под гит.
>git add .

 5. Закоммитить файл.
>git commit -m "create new yxy file"

 6. Отправить файл на внешний GitHub репозиторий.
>git push

 7. Отредактировать содержание файла “new.txt” - написать информацию о себе (ФИО, возраст, количество домашних животных, будущая желаемая зарплата). Всё написать в формате TXT.

>cat> new.txt
>Sergeeva
>Victoria
>I have one cat
>I would like to have 2500$ salary.


 8. Отправить изменения на внешний репозиторий.
>git add .
>git commit -m "add new info about myself to new.txt"
>git push

 9. Создать файл preferences.txt
>touch preferences.txt
 10. В файл preferences.txt” добавить информацию о своих предпочтениях (Любимый фильм, любимый сериал, любимая еда, любимое время года, сторона которую хотели бы посетить) в формате TXT.

> cat > preferences.txt
>My favorite film is Destruction
>My favorite TV series is The Office
>My favorite food is Meat
>My favorite time of the year is spring
>I would like to travel to Sweden

 11. Создать файл sklls.txt добавить информацию о скиллах которые будут изучены на курсе в формате TXT
>touch sklls.txt
>cat > sklls.txt 
> Что такое клиент-серверная архитектура.
> HTTP Методы запросов на сервер.
> Коды ответов HTTP сервера.
>Что такое JSON, XML. Их структура.

 12. Сделать коммит в одну строку.
>git add .
>git commit -m "create two news txt file"

 13. Отправить сразу 2 файла на внешний репозиторий.
>git push 

 14. На веб интерфейсе создать файл bug_report.txt.
 15. Сделать Commit changes (сохранить) изменения на веб интерфейсе.
 16. На веб интерфейсе модифицировать файл bug_report.txt, добавить баг репорт в формате TXT.
 17. Сделать Commit changes (сохранить) изменения на веб интерфейсе.
 18. Синхронизировать внешний и локальный репозиторий TXT
>git pull

