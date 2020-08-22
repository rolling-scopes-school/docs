## Цели второго этапа обучения
- Получение студентами знаний по Core Js
- Подготовка студентов к прохождению технических интервью
- Подготовка студентов к выступлению на английском языке
- Выполнение студентами курсового проекта

# Требования к выполнению тасков в RSSchool stage#2
## Репозиторий
 Начиная с stage#2, по умолчанию все таски необходимо сохранять в приватный репозиторий на GitHub.
 Приватный репозиторий будет выдан вам в начале stage#2 после [завершения набора студентов менторами](technical-screening.md)
 Дата выдачи будет оглашена дополнительно в чате discord канал [announcements](https://discord.gg/WkYCfV2)
 Выдача репозиториев происходит следующим образом:
  - мы создаем вам приватный репозиторий
  - добавляем вас в контрибьютеры
  - GitHub автоматически присылает вам инвайт для доступа в репозиторий. Инвайт приходит на почту указанную вами при регистрации на GitHub (а не на почту указанную вами в RS APP)

До момента выдачи приватного репозитория школы вы можете выполнять задания из Stage #2 в личном приватном репозитории.

## Как работать с приватным репозиторием?
* Склонировать его себе:  
  `git clone git@github.com:rolling-scopes-school/<your-school-repository>.git`
* Укажите в конфиге ваши данные (email впишите привязанный [к аккаунту GitHub](https://github.com/settings/emails)):  
   `git config user.name "Name Surname"`  
   `git config user.email "your@email"`
* Из ветки `master` создать ветку по имени задания:  
  `git checkout -b <task-name>`
* Создать папку по имени задания:  
  `mkdir <task-name>`  
  Все относящиеся к заданию файлы должны быть в ней.
* Выполнить задание, в процессе коммитая решения (см. [требования к коммитам](https://docs.rs.school/#/stage2?id=%d0%a2%d1%80%d0%b5%d0%b1%d0%be%d0%b2%d0%b0%d0%bd%d0%b8%d1%8f-%d0%ba-%d0%ba%d0%be%d0%bc%d0%bc%d0%b8%d1%82%d0%b0%d0%bc)).
* Залить ветку в remote branch на GitHub:  
  `git push origin <task-name>`
* Создать Pull Request из бранча `<task-name>` в ветку `master`.

## Как сделать деплой задания из приватного репозитория школы?
* Переходим в ветку `gh-pages` и мержим в нее ветку задания:  
  `git checkout gh-pages`  
  `git merge <task-name>`
* Используя сборщик проекта (webpack, gulp), учитывайте, что сборка будет в подпапке `dist`. Или в той, какую настроите в конфиге сборщика. Убедитесь, что названия этой папки нет в файле `.gitignore` в корне репозитория. Перед отправкой ссылки в сабмит для кроссчека и добавлением в PR для ментора удостоверьтесь, что по этой ссылке открывается именно рабочая версия (деплой) проекта.
* В ветке `gh-pages` в файл `README.md` добавляем ссылку на папку задеплоенного таска:  
  `[Task name](./<task-name>)`
  используя сборщик проекта, добавьте папку со сборкой, например:  
  `[Task name](./<task-name>/dist)`
* Деплой задания будет доступен по ссылке:  
  `http://rolling-scopes-school.github.io/<your-school-repository>/<task-name>`  
  используя сборщик проекта, добавьте папку со сборкой, например:  
  `http://rolling-scopes-school.github.io/<your-school-repository>/<task-name>/dist`
* Здесь можно увидеть ссылки на все сделанные вами задания:  
  `http://rolling-scopes-school.github.io/<your-school-repository>`
* Публикация на GitHub Pages может занять какое-то время.

Если часть заданий Stage #2 вы делали в личном репозитории, перенесите их в выданный вам приватный репозиторий школы.

### Перенос кода задания из личного репозитория в выданный школой репозиторий

Личный репозиторий существует на вашем аккаунте:  
`https://github.com/your-username/...`

Школьный репозиторий размещен на аккаунте школы:  
`https://github.com/rolling-scopes-school/...`

Если вы начали делать задания 2 этапа в личном репозитории, когда выдадут школьный, надо будет перенести их туда.

Если сделано немного, проще всего в школьном репозитории от ветки `master` создать ветку задания, скопировать туда актуальные файлы и папки задания и коммитать с нуля. 

Если важно сохранить историю коммитов, можно сделать зеркало вашего личного репозитория в школьном. Для этого:

1. В личном репозитории закоммитайте и запушьте все необходимые для задания изменения, чтобы не потерять их.
2. У вас должна быть ветка `master`, в ней те же файлы, что и в ветке `master` вашего школьного репозитория. Учитывайте, что если будете менять `master` после того, как создали ветку с заданием и что-то там изменили, при потенциальном слиянии могут быть конфликты. Поэтому никаких лишних файлов и папок в `master` быть не должно.
3. В ветке, где делали задание, создайте отдельную папку, туда перенесите все относящиеся к заданию файлы и папки. Обычно в описании задания указано, как должна называться папка. Например, для задания „Fancy Weather“ папка называется `fancy-weather`. Ветка, в которой вы выполняли задание, должна быть одна и должна называться, как указано в задании. Переименовать ветку, находясь в ней, можно следующим образом:  
`git branch -m task-branch-name`  
из другой ветки репозитория:  
`git branch -m old-branch-name task-branch-name`
4. В ветке задания в корне репозитория (вне папки с заданием) должны остаться те же файлы, что и в ветке `master`.
5. Больше никаких веток (промежуточная разработка фич, hotfixes и т. д.) в репозитории быть не должно, только `master` и ветка с заданием. Если у вас несколько веток для заданий, оставьте их и оформите согласно п. 3-4.
6. Заходим в приватный репозиторий школы и копируем ссылку, которую используют для клонирования. В зависимости от предпочтительного метода работы с Git, она будет такой:  
`git@github.com:rolling-scopes-school/your-username-RSYEARQn.git`  
или такой:  
`https://github.com/rolling-scopes-school/your-username-RSYEARQn.git`
7. Делаем школьный репозиторий полной копией вашего текущего репозитория (внимание: все ветки школьного репозитория будут перезаписаны ветками нового!):  
`git push --mirror link`  
*вместо `link` вставьте ссылку, которую скопировали в п. 6*
8. Далее через терминал переходим в папку, в которой предполагается склонировать ваш школьный репозиторий и пишем:  
`git clone link`  
*вместо `link` вставьте ссылку, которую скопировали в п. 6*
9. Переходим в папку школьного репозитория и продолжаем разработку уже там.

## Требования к коммитам
[Conventional Commits](git-convention.md)

## Требования к стилю написания кода
[Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)

## Как происходит проверка тасков?
## Автопроверяемые задания
Оценки за задания, которые проверяются автоматически (*Codewars*, *Codecademy*, и. т. д.), ставятся и в последствии исправляются в том случае, если студент вовремя отправил свои корректные данные. Такими данными, как правило, являются логины (*username*) соответствующих сервисов. Форма для отправки корректных данных открывается после дедлайна, ссылка на форму, а также информация о дате и времени ее закрытия публикуется в канале `announcements`. После закрытия формы претензии и оправдания за невыставленную, либо выставленную некорректно оценку, не принимаются.

## Проверка задания ментором
1. Студент выполняет задание в приватном репозитории.
2. Студент создает и оформляет Pull Request до дедлайна.
    - Правила оформления PR указаны [ниже](https://docs.rs.school/#/stage2?id=%d0%9e%d0%bf%d0%b8%d1%81%d0%b0%d0%bd%d0%b8%d0%b5-pull-request-%d0%b4%d0%be%d0%bb%d0%b6%d0%bd%d0%be-%d1%81%d0%be%d0%b4%d0%b5%d1%80%d0%b6%d0%b0%d1%82%d1%8c-%d1%81%d0%bb%d0%b5%d0%b4%d1%83%d1%8e%d1%89%d1%83%d1%8e-%d0%b8%d0%bd%d1%84%d0%be%d1%80%d0%bc%d0%b0%d1%86%d0%b8%d1%8e)
    - Штрафы за нарушения дедлайна указаны [ниже](https://docs.rs.school/#/stage2?id=%d0%94%d0%b5%d0%b4%d0%bb%d0%b0%d0%b9%d0%bd%d1%8b)
    - При применении штрафных коэффициентов, округление происходит в пользу студента
3. До выставления финальной оценки ментором, студент может продолжать реализовывать фичи после дедлайна со штрафом 50% к их стоимости в баллах.
    - Названия коммитов должны явно говорить о реализованной фиче
    - Студент должен оставить отдельный комментарий в открытом Pull Request о функционале, который был реализован и его стоимости в баллах с учетом 50% штрафа
    - При применении штрафных коэффициентов, округление происходит в пользу студента
4. Ментор проверяет PR, оставляет свои замечания и рекомендации по качеству кода (copy-paste, magic numbers, project structure, etc.) и реализованной функциональности. Указывает предварительную оценку в комментарии.
    - Оценка выставляется ментором на основании критериев оценки указанных для каждого задания
    - При выставлении оценки учитывается весь реализованный функционал. Например, студент выполнил минимальные требования не на 100 процентов, но выполнил часть дополнительных - все требования должны учитываться
    - Ментор может выставить предварительную оценку авансом, с учетом того, что студент исправит все замечания ментора
5. Студент в течении 5 дней исправляет замечания ментора.
    - Если комментарии ментора к PR предполагают ответ студента - студент пишет ответ
    - Если студент вкомитал правки, он должен оставить комментарий о том, что именно было вкомитанно/исправлено
6. По результатам исправления ментор выставляет окончательную оценку в Score RS APP. 
    - Ментор сам решает снимать баллы или нет за правки после дедлайна.
    - Если студент не исправил замечания ментора по качеству кода, ментор может дополнительно снизить оценку. Размер штрафа на усмотрение ментора, максимум -50 баллов.

## Требования к Pull Request (PR)
### Описание Pull Request должно содержать:
1. Ссылка на задание.
2. Скриншот вашего задания (достаточного одного), ссылка либо прямо вставленая в пул реквест.
3. Ссылка на деплой задания (см. [инструкцию по деплою](https://docs.rs.school/#/stage2?id=%d0%9a%d0%b0%d0%ba-%d1%80%d0%b0%d0%b1%d0%be%d1%82%d0%b0%d1%82%d1%8c-%d1%81-%d0%bf%d1%80%d0%b8%d0%b2%d0%b0%d1%82%d0%bd%d1%8b%d0%bc-%d1%80%d0%b5%d0%bf%d0%be%d0%b7%d0%b8%d1%82%d0%be%d1%80%d0%b8%d0%b5%d0%bc)):  
  `http://rolling-scopes-school.github.io/<your-school-repository>/<task-name>`
4. Дата сдачи / дата дедлайна.
5. Ваша самопроверка с предварительной оценкой.

### Пример оформления
```
1. Task:
   https://github.com/rolling-scopes-school/tasks/blob/master/tasks/rslang/english-for-kids.md
2. App screenshot:
   https://i.imgur.com/9N60IHl.png
3. Deploy:  
   https://rolling-scopes-school.github.io/hallovarvara-RS2020Q1/english-for-kids/dist/
4. Done 19.04.20 (deadline 19.04.20)
5. Score: 200 / 200
- [x] UI, markup, design of main page (+10) and category page (+10)
	- [x] both mobile and desktop versions have all described elements
	- [x] fulfilled all task requirements to app design
- [x] UI, markup, design of menu (+10)
	- [x] both mobile and desktop versions have all described elements
	- [x] fulfilled all task requirements to app design
	- [x] menu links work
	- [x] current page link differ from others
	- [x] all pages have sliding menu
	- [x] menu closes with smooth animation by clicking on crest or any other app element including menu link
- [x] Training mode (+20)
	- [x] english words sound while clicking on card
	- [x] all cards has button for flipping. there's word translation at the back side. card flip back after mouse cursor goes out from card area.
- [x] Code quality (+30)
	- [x] code dublicating minimized (+10)
	- [x] modular JS (+10)
	- [x] webpack, eslint, eslint-config-airbnb-base, babel connected and are used (+10)
- [x] Game mode (+80)
	- [x] click on mode switcher Train/Play turns on game mode. Here're no flipping button and text on card. Card image takes up all card area (if it's ok with app design). „Start game” button appears. (+10)
	- [x] clicking on „Start game” button activate english word pronouncing. Word should be one of presented on page and it should be chosen randomly. For each page and every new game words should generating randomly from scratch (+10)
	- [x] a click on „Start game” button change text on it with „Repeat” icon and view of button. Clicking on „Repeat” button repeats current word pronouncing (+10)
	- [x] if user've clicked on wrong card, „error” sound sounds (+10)
	- [x] if user've clicked on correct card, „correct” sound sounds and new random english word from this page is pronouncing. One word can't participate twice in one game. (+10)
	- [x] card with guessed word become inactive and changes view. Clicking on inactive card doesn't call sound effects and doesn't affect on game score. (+10)
	- [x] when game's started, every click on active card is right or wrong answer. They're shown up like stars or other symbols of different colors on rating panel. Rating panel shows up in game mode. If rating panel fulls of stars, first stars hide, new continues to show. (+10)
	- [x] when all words've guessed: (+10)
		- if all of them are rightly guessed, „success” sound sounds, cards hide, happy smile shows (or another appropriate image),
		- else „failure” sound sounds, cards hide, sad smile shows (or another appropriate image) and mistakes quantity,
		- app automatically redirects to main page with categories' list.
- [x] Statistics page (+40)
	- [x] here're all categories, all words of each category, every word's translation. Page must be shown correctly minimum on 320 px. (+10)
	- [x] close to each word are shown and saved in statistics after page reload: (+10)
		- number of clicks on it's card in training mode,
		- times word was guessed,
		- number of mistaken word in game mode,
		- mistakes density of word.
	- [x] feature to sort data. Strings sort alphabetically, number by number. Sort can be ascending and descending and must cover all data. (+10)
	- [x] here're buttons „Repeat difficult words” и „Reset”: (+10)
		- „Reset” resets statistics,
		- „Repeat difficult words” open category-like page with words with the highest mistakes density. There can be 0–8 words according in how many words user guessed wrong in game mode. After clicking on „Reset” button, on „Repeat difficult words” page should be no words.
- [x] Penalties (0)
	- [x] In app less than 8 categories and less than 8 words in each category (-10)
	- [x] Errors while app's working. (-10 for each, but no more than the total number of points for requirement implementation)
	- [x] Not comply with the requirements for Pull Request, repository, commits names (-10) scores by mentor
```

### Pull Request не должен содержать:
- Закоментированного кода
- Лишних файлов, автосгенерированного кода, node_modules и т.д.

### Этикет
Pull Request - это место для обсуждения кода. Он не должен выглядеть как монолог студента или ментора. Будьте культурными, уважайте время и работу друг друга.

## Дедлайны
Дедлайны всех тасков указаны в расписании.
Если вы не успели к дедлайну:
  - Если таск относится к категории "CodeJam" и не подразумевает проверку кода ментором - вы получаете 0. Пример таких заданий - Lodash Quick Draw, Websocket Challenge, etc.
  - Если таск подразумевает автоматическую проверку смотри п. [Автопроверяемые задания](#автопроверяемые-задания)
  - Для остальных типов тасков:
    - -10 баллов к оценке при опоздании до 3 дней включительно
    - -30% процентов к оценке при опоздании до 7 дней включительно
    - -70% процентов к оценке при опоздании более чем на неделю
    - по усмотрению ментора, при наличии уважительной причины (больница, армейские сборы и т.д.)

## Recommended links
- [How to write the perfect Pull Request](https://github.com/blog/1943-how-to-write-the-perfect-pull-request)
