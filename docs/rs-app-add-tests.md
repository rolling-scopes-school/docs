## Добавление тестов в RS APP (только для тренеров и администраторов курса)

1. Для добавления тестов нужно перейти на страницу "Manage Tasks":
![](https://docs.rs.school/images/rs-app-add-tests-1.png)

2. Далее нажимаем на кнопку "Add Task":
![](https://docs.rs.school/images/rs-app-add-tests-2.png)

3. Следующим шагом заполняем форму и сохраняем ее:
    - "Name" - название задания;
    - "Task Type" - выбираем "RSAPP Test";
    - "Discipline" - выбираем дисциплину которая относится к курсу;
    - "Tags" - теги, по желанию, чтобы было понятнее к какой области курса это задание относится. Например "javascript", "html/css", "react", и т. п.;
    - "Description URL" - ссылка на описание задания;
    - "JSON Attributes" - сюда необходимо вставить заранее подготовленный JSON с настройкой теста, а также вопросами и вариантами ответов [(см. ниже)](https://docs.rs.school/#/rs-app-add-tests?id=json-attributes).
![](https://docs.rs.school/images/rs-app-add-tests-3.png)

4. Затем в меню выбранного курса переходим на "Course Tasks":
![](https://docs.rs.school/images/rs-app-add-tests-4.png)

5. И тут также нажимаем на кнопку "Add Task":
![](https://docs.rs.school/images/rs-app-add-tests-5.png)

6. Снова заполняем форму и сохраняем:
    - "Task" - выбираем из списка только что созданное задание;
    - "Task Type" - выбираем "RSAPP Test";
    - "Checker" - выбираем "Auto-Test";
    - "Task Owner" - выбираем человека, ответственного за это задание;
    - "Start Date - End Date" - дата выдачи задания и дедлайн;
    - "Score" - тут пишем какое максимальное количество баллов студент может получить за это задание;
    - "Score Weight" - вес задания (по умолчанию 1), нужен для того чтобы в дальшем менеджер курса мог скорректировать влияние некоторых не очень важных заданий на общий результат. Не трогаем это поле.
![](https://docs.rs.school/images/rs-app-add-tests-6.png)

7. Задание добавлено! Теперь можно вернуться в меню курса и перейти на "Auto-Test" чтобы удостоверится что задание добавилось корректно:
![](https://docs.rs.school/images/rs-app-add-tests-7.png)

8. Далее выбираем наш тест из списка и проверяем что все корректно:
![](https://docs.rs.school/images/rs-app-add-tests-8.png)

----
### JSON Attributes

#### Параметры:
- "strictAttemptsMode" - по умолчанию включен строгий режим, чтобы отключить нужно установить этот флаг в значение "false".
- "maxAttemptsNumber" - если строгий режим включен то после истечения указанного количества попыток студент получит 0, в противном случае сдавать можно будет до бесконечности (дедлайна), но оценка будет поделена на 2.
- "numberOfQuestions" - количество вопросов (должно быть равно длине массивов "answers" и "public"."questions").
- "tresholdPercentage" - количество процентов которое студент должен набрать чтобы задание засчиталось принятым (иначе он получает 0 и теряет одну попытку).
- "public"."questions" - тут описываются вопросы и варианты ответов. Если нужно добавить вариант с мультивыбором - то ставим флаг "multiple" в "true".
- "answers" - массив с номерами правильных ответов (порядок должен быть таким же как и в "public"."questions"!).

**Обратите внимание!**, что сдавая это задание несколько раз - студент получит последнюю оценку (не лучшую!). То есть можно пересдать и на 0.

#### Пример:
```json
    {
        "public": {
            "tresholdPercentage": 70,
            "numberOfQuestions": 10,
            "maxAttemptsNumber": 2,
            "strictAttemptsMode": false,
            "questions": [
                {
                    "question": "Do you like html?",
                    "answers": ["Yes", "No", "Maybe"],
                    "multiple": false
                },
                {
                    "question": "What is css?",
                    "answers": ["Cascade style sheets", "cosmic super solutions", "cool super stuff"],
                    "multiple": true
                },
                {
                    "question": "What is not a css selector?",
                    "answers": ["<div>", "div", "a.a", "p<div>"],
                    "multiple": true
                }
            ]
        },
        "answers": [
            [0],
            [0, 2],
            [0, 3]
        ]
    }
```

#### PR-ы с описанием добавленной функциональности для тестов и примерами:
- [Базовый пример (см. выше)](https://github.com/rolling-scopes/rsschool-app/pull/530)
- [Если нужны картинки в тестах](https://github.com/rolling-scopes/rsschool-app/pull/798)

