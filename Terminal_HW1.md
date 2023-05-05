# Шаги воспроизведения ДЗ1 по Терминалу 
1. Посмотреть где я 
>pwd
2. Создать папку
>mkdir name_folder
3. Зайти в папку
> cd name
4. Создать 3 папки 
> mkdir name1 name2 name3
5. Зайти в любоую папку 
>cd name1
6. Создать 5 файлов (3 txt, 2 json)
>touch n1.txt n2.txt n3.txt 
> touch nam1.json nam2.json
7. Создать 3 папки
>mkdir  fol1 fol2 fol3
8. Вывести список содержимого папки
>ls -la
9. Открыть любой txt файл 
>vim n1.txt
10. написать туда что-нибудь, любой текст.
>tab on I , input some text 
11. сохранить и выйти.
>  tab on Esc,tab on shift+: , input wq
12. Выйти из папки на уровень выше
>cd ..
13. переместить любые 2 файла, которые вы создали, в любую другую папку.
>mv n2.txt n3.txt fol2
14. скопировать любые 2 файла, которые вы создали, в любую другую папку.
>cp n3.txt fol2 
>cp n4.txt fol3
15. Найти файл по имени 
>find / -iname n3.txt 
16. просмотреть содержимое в реальном времени (команда grep) изучите как она работает.
>tail -f name.txt
17. вывести несколько первых строк из текстового файла
>head -n 3 name.txt
18. вывести несколько последних строк из текстового файла 
>tail -n 3 name.txt
19. просмотреть содержимое длинного файла (команда less) изучите как она работает.
>less name.txt
20. вывести дату и время
>date


## Задание *

1. Отправить http запрос на сервер http://162.55.220.72:5005/terminal-hw-request 
>curl http://162.55.220.72:5005/terminal-hw-request

2. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
    
>    file contens:
>    mkdir shops
>    cd shops
>    mkdir milk butter  bread
>    cd bread
>    touch br1.txt br2.txt br3.txt
>    touch  br4.json br5.json
>    mkdir baguette croissant cookie
>    ls -la
>    mv br1.txt br2.txt br3.txt cookie
>    ls -la
>    cd cookie
>    ls -la

