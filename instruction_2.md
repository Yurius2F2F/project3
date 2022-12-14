# Инструкция для GIT
---
## Перед работой скачиваем и устанавливаем VS и Git
1. Создаём папку
2. В редакторе VS открываем созданную папку через Файл - Открыть папку. Нажимаем "Открыть папку"
3. В левом верхнем углу нажимаем кнопку "Создать файл"
4. Называем файл любым именем, ставим расширение .md
5. Запускаем терминал через меню Вид - Терминал
6. Для запуска Git вводим команду git init
7. Добавляем созданный документ командой git add .\project1.md (в конце можно нажать TAB после ввода первых букв файла)
8. Пишем первую строку-заголовок, начиная с символа # This is my first project.
9. Сохраняем проект через меню Файл - Сохранить
10. Добавляем коммит командой git commit -m "Добавили заголовок". Успешно:
	[master (root-commit) e9d6c95] Добавили заголовок
	1 file changed, 0 insertions(+), 0 deletions(-)
	create mode 100644 project1.md
11. Редактируем документ: добавляем подзаголовок ## Today is the 23d of September
12. Без команды добавления просматриваем статус командой git status. Получаем ответ:
	On branch master
	Changes not staged for commit:
	(use "git add <file>..." to update what will be committed)
	(use "git restore <file>..." to discard changes in working directory)
			modified:   project1.md
	
	no changes added to commit (use "git add" and/or "git commit -a")
13. Сохраняем документ
14. Добавляем сохранённые изменения командой git add .\project1.md
15. Прописываем коммит командой git commit -m "Добавили подзаголовок". Успешно:
	[master d751e5a] Добавили подзаголовок
	1 file changed, 2 insertions(+)
	16. Смотрим статус командой git status. Получаем ответ:
	[master d751e5a] Добавили подзаголовок
	1 file changed, 2 insertions(+)
	PS C:\Users\BiG-BoSS\Desktop\education\project1> git status
	On branch master
	nothing to commit, working tree clean
16. Добавляем ненумерованный список в документ
	* carrot
	* cabbage
	* raspberry
17. Сохраняем документ
18. Добавляем сохранённые изменения командой git add .\project1.md
19. Прописываем коммит командой git commit -m "Добавили ненумерованный список". Успешно:
	[master 6dcded0] Добавили ненумерованный список
	1 file changed, 4 insertions(+), 1 deletion(-)
20. Добавляем нумерованный список в документ
	1. potatoes
	2. cucumber
	3. pineapple
21. Сохраняем документ
22. Добавляем сохранённые изменения командой git add .\project1.md
23. Прописываем коммит командой git commit -m "Добавили нумерованный список". Успешно:
	[master 5f9a7d5] Добавили нумерованный список
	1 file changed, 5 insertions(+), 1 deletion(-)
24. Меняем текст нумерованного списка, чтобы 1 строка была курсивом **, 2 строка была жирная ____, 3 строка была зачёркнутая ~~~~
25. Сохраняем документ
22. Добавляем сохранённые изменения командой git add .\project1.md
23. Прописываем коммит командой git commit -m "Добавили форматирование в нумерованный список". Успешно:
	[master a0504e7] Добавили форматирование в нумерованный список
	1 file changed, 5 insertions(+), 3 deletions(-)
24. Смотрим лог изменений командой git log. Видим все изменения с нашими коммитами, автора и дату внесения изменений. Для выхода из лога нужно нажать кнопку q. Текущее состояние - master
25. Для перехода к конкретному изменению нужно воспользоваться командой git checkout d751e5a. Успешно
	Note: switching to 'd751e5a'.
	
	You are in 'detached HEAD' state. You can look around, make experimental
	changes and commit them, and you can discard any commits you make in this
	state without impacting any branches by switching back to a branch.
	
	If you want to create a new branch to retain commits you create, you may
	do so (now or later) by using -c with the switch command. Example:
	
	git switch -c <new-branch-name>
	
	Or undo this operation with:
	
	git switch -
	
	Turn off this advice by setting config variable advice.detachedHead to false
	
	HEAD is now at d751e5a Добавили подзаголовок
26. Возвращаемся к актуальной версии с помощью команды git checkout master

---
# Продолжение инструкции для GIT.
Для создания новой ветки из главной (master) нужно воспользоваться командой git branch <наименование_новой_ветки>.

После этого для переключения на новую ветку и работу в ней нужно вопспользоваться командой git checkout <наименование_новой_ветки>.

Для того, чтобы убедиться, что ветка выбрана правильно, нужно воспользоваться командой git branch.
В ответе:

master
*work_with_pictures

то есть, активная ветка будет со звёздочкой (*)

## Списки
Чтобы добавить ненумерованные списки, необходимо пункты выделить звёздочкой (*).
Нпример:
* Элемент 1
* Элемент 2
* Элемент 3

Чтобы добавить нумерованные списки, нужно пункты просто пронумеровать.
Например:
1. Первый элемент
2. Второй элемент
3. Третий элемент

+++++йййй++++йййй
а я хочу тут добавить коммент, которого нет в ветке master
в итоге, создал конфликт, оставил оба варианта
## Работа с изображениями
Создадим и перейдём в новую ветку **work_with_pictures**

Чтобы вставить изображение в текст, достаточно написать следующее:
![Привет, я люблю пироженки))](Cake.jpeg)

После создания ветки work_with_pictures сделал слияние с веткой master с помощью команды git merge <наименование_переносимой_ветки>.
В ответе получил:

PS C:\Users\BiG-BoSS\Desktop\education\project2> git merge work_with_pictures
Auto-merging instruction_2.md
Merge made by the 'ort' strategy.
 .gitignore       | 1 +
 instruction_2.md | 3 +++
 2 files changed, 4 insertions(+)
 create mode 100644 .gitignore

## Ссылки
![Ссылка на GeekBrains](https://gb.ru/)
![Ссылка на YouTube](https://www.youtube.com/)
![Ссылка на HH.ru](http://hh.ru/)
## Работа с таблицами
Вот так оформляются таблицы:

Номер ПП |   Имя   | Фамилия
:-------:|:-------:|:-------:|
1| Игорь | Иванов
2| Владимир | Синицын
3| Тони | Старк

## Заключение
_**Спасибо за уроки!**_