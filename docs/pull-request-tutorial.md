# Как добавить изменения в чужой репозиторий

Если вы заметили неточность или опечатку в документации о курсе https://docs.rs.school/#/, или условии задания, их желательно исправить.  
При необходимости обсудить изменения, это можно сделать в issue: 
https://github.com/rolling-scopes-school/docs/issues/33  
Но, если содержание исправлений для вас очевидно, лучше создать **Pull Request**.  

Отправляя Pull Request, вы говорите автору репозитория (и всем заинтересованным лицам): "Смотрите, что я сделал, не хотите ли принять мои изменения и влить их в проект?". Если изменения разумны и целесообразны, ваш Pull Request будет принят.  

Покажу как это сделать на примере репозитория https://github.com/rolling-scopes-school/docs 

## 1. Делаем собственную копию репозитория.
Для этого нажимаем кнопку "Fork" на странице репозитория.  

<details><summary>Скриншот</summary>

![image](https://s8.hostingkartinok.com/uploads/images/2019/09/d597969969fcb575af350ce928b8da14.png)
</details>

В результате копия репозиторий появляется в вашем аккаунте

<details><summary>Скриншот</summary>

![image](https://s8.hostingkartinok.com/uploads/images/2019/09/fe171ed94181058cfb26479c147bb177.png)
</details>

Адрес вашей копии репозитория содержит имя вашего аккаунта на гитхабе.   
Оригинальный репозиторий https://github.com/rolling-scopes-school/docs   
Созданная копия https://github.com/irinainina/docs    

## 2. Клонируем собственную копию репозитория себе на компьютер

```git clone https://github.com/irinainina/docs```  

## 3. Привязываем локальную копию  к оригинальному репозиторию
Для этого заходим в папку склонированного репозитория и выполняем две команды  

```git remote add upstream https://github.com/rolling-scopes-school/docs```  
```git fetch upstream```

<details><summary>Скриншот</summary>

![image](https://s8.hostingkartinok.com/uploads/images/2019/09/04e8c861e038cda1dc5803870b875c3b.png)
</details>

## 4. Создаём собственную ветку разработки

Имя ветки, как правило, указывает на содержание правок.  
Предположим, что наша ветка будет называться "pr-tutopial".     
Создаёт новую ветку  "pr-tutopial" и делает её активной команда  

```git checkout -b pr-tutopial```  

В этой точке мы уже можем править код и делать коммиты.

## 5. Добавляем изменения в собственную копию репозитория

Как только вы сделали работу (или её часть), отправьте её в собственную  копию репозитория на GitHub.  
Для этого выполните команды:

```git add .```    
```git commit -m "feat: add  pr-tutopial"```    
```git push origin pr-tutopial```    

## 6. Возвращаем изменения: Pull request

Итак, всё сделано. Вы написали код, он у вас в ветви pr-tutopial как у вас на компьютере, так и на GitHub'е. Осталось только отправить его в оригинальный репозиторий.

Заходите на страницу вашей копии репозитория на GitHub, выбираете ветвь pr-tutopial и нажимаете кнопку Pull Request.

<details><summary>Скриншот</summary>

![image](https://s8.hostingkartinok.com/uploads/images/2019/09/eb90a6c70262ed07ce3b22f0fc2fabae.png)
</details>

Добавляете название и описание ваших изменений и нажимаете на кнопку "Create pull request"

<details><summary>Скриншот</summary>

![image](https://s8.hostingkartinok.com/uploads/images/2019/09/d90f3537d2d85f0c429b98c0d7d6239b.png)
</details>

Что дальше?

Следите за вашим пулл-реквестом. Что прокомментируют люди, что скажет мэйнтэйнер, примет или нет ваш пулл реквест.

Творите добро (и пусть оно будет выражаться в коммитах).  

[Источник](https://habr.com/ru/post/125999/)