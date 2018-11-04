# Требования к выполнению тасков в RSSchool stage#2

## Репозиторий
 Начиная с stage#2, по умолчанию все таски необходимо сохранять в приватный репозиторий на GitHub.  
 Приватный репозиторий будет выдан вам в начале stage#2.  
 Дата выдачи будет оглашена дополнительно в чате https://gitter.im/rolling-scopes-school/announcements  
 Выдача репозиториев происходит следующим образом:
  - мы создаем вам приватный репозиторий
  - добавляем вас в контрибьютеры
  - GitHub автоматически присылает вам инвайт для доступа в репозиторий. Инвайт приходит на почту указаную вами при регистрации на GitHub (а не на почту указаную вами в Padawans).
 
## Как работать с приватным репозиторием? 
* создаем новую папку
* переходим в нее
* открываем git bash
* `git init`
* `git remote add origin <your repo url>`
* `git config user.name "Name Surname"`
* `git config user.email "your@email"` (емэйл должен совпадать с емэйлом указаным в github-e)
* создаем в папке текстовый файл README.md
* `git add README.md`
* `git commit -m "initial commit"`
* смотрим как нужно называть папку с таском и также называем бранч в котором будем работать
* `git co -b <task folder name>`
* добавляем папку с соответствующим именем
* копируем все нужные файлы в эту папку
* добавляем файлы при помощи `git add`
* коммитаем
* `git push origin master`
* `git push origin <task folder name>`
* Создаем Pull Request из бранча <task folder name> в ветку master.
 
## Требования к коммитам
- Названия коммитов должны быть согласно гайдлайна - https://www.conventionalcommits.org/en/v1.0.0-beta.2/ 
Основные требования:
```
  * Allowed Types:
    * docs: - *documentation only changes*
    * feat: - *a new feature*
    * fix: - *a bug fix*
    * perf: - *a code change that improves performance*
    * refactor: - *a code change that neither fixes a bug nor adds a feature*
    * style: - *сhanges that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)*
    * ...
  * Use the present tense ("add feature" not "added feature")
  * Use the imperative mood ("move cursor to..." not "moves cursor to...")
  * Limit the first line to 72 characters or less
  * Reference issues and pull requests liberally after the first line
```
 
## Требования к Pull Request (PR)
### Описание Pull Request должно содержать следующую информацию
1. ссылка на задание
2. скриншот вашего задания (достаточного одного), ссылка либо прямо вставленая в пул реквест
3. дата сдачи / дата дедлайна 
4. ваша самопроверка с предварительной оценкой

Пример оформления
```
1. задание - https://github.com/rolling-scopes-school/tasks/blob/2018-Q3/tasks/markup-2018q3.md
2. скриншот - https://imgur.com/a/vB30e5R
3. 2018-11-03 / 04.11.2018
4. Total
Task ( 8.5 / 12 )
Header. (2 / 3)
+ Interactive nav
+ Think of where h1 should be used
- Interactive login/register
Main. ( 4.5 / 7)
- Interactive domain input with dropdown of first domains (.com, .net, .org).
+ Table should strictly be the same as design, and the cells number should be as much, as visible cells are.
+ The circle elements should be made using CSS, transformations.
+ The itmes should be intractive on hover.
+ links in "about us" should be interactive.
+ / - The feddback items should be interactive. (слайдер делать функциональным не обязательно, но желательно)
- Services items should be links.
Footer (2 / 2)
+ Menus should be intractive
+ Phone and mail interactions should correspond correctly. (например, при нажатии на телефон должно предложить звонок)

mark calculation:
100 - 10.5 - 30 = 59.5
(0) За сдачу не в срок ментор может вычесть до 40 баллов из общего результата!
(-10.5) За невыполнение какого-либо из пунктов ТЗ ментор может вычесть от 3 до 10 баллов.
(-0 - проверял на валидаторе) За неправильное оформление кода или некорректный синтаксис ментор может вычесть до 20 баллов.
(-0 - сверял 2 раза) За несоблюдение дизайна, кроме нюансов со шрифтами, ментор может вычесть до 40 баллов.
(-30 - не успел выполнить)  Если при масштабировании верстка сильно плывет (не responsive), выпадают элементы, скрывается часть контента, то ментор может вычесть до 30 баллов.
```

### Pull Request не должен содержать:
- Закоментированного кода
- Лишних файлов, автогенеренный кода, node_modules и т.д.

## Дедлайны
Дедлайны всех тасков указаны в расписании. 
Если вы не успели к дедлайну:
  - Если таск относится к категории "CodeJam" вы получаете 0. 
  - Для остальных типов тасков:
    - -10 баллов к оценке при опоздании до 3 дней включительно
    - -30% процентов к оценке при опоздании до 7 дней включительно
    - -70% процентов к оценке при опоздании более чем на неделю
    - по усмотрению ментора, при наличии уважительной причины (больница, армейский сборы и т.д.)
    
## Как происходит проверка тасков?
Все задания менторы проверяют в соответствующих PR студентов.  
В результате каждый PR студента, содержит ваши комментарии по коду, рекомендации и итоговую оценку.  
Оценка выставляется ментором на основании критериев оценки указанных для каждого задания.
После проверки ментор заносит оценку в форму - Score. 

## Спасибо контрибьютерам этого FAQ
- https://github.com/lesnitsky
- https://github.com/davojta

## Recommended links
- [How to write the perfect Pull Request](https://github.com/blog/1943-how-to-write-the-perfect-pull-request)
