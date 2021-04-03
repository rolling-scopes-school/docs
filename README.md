https://docs.rs.school

Как добавить изменения в чужой репозиторий.
Отправляя Pull Request, вы предлагаете автору репозитория и всем заинтересованным лицам рассмотреть внесённые вами изменения и влить их в проект. Если изменения разумны и целесообразны, ваш Pull Request будет принят.

Покажу как это сделать на примере репозитория https://github.com/rolling-scopes-school/docs

1. Делаем собственную копию репозитория.
Для этого нажимаем кнопку "Fork" на странице репозитория.

image

В результате копия репозитория появляется в вашем аккаунте. image

Адрес вашей копии репозитория содержит имя вашего аккаунта на гитхабе.

Оригинальный репозиторий https://github.com/rolling-scopes-school/docs
Созданная копия https://github.com/irinainina/docs
2. Клонируем собственную копию репозитория себе на компьютер
git clone https://github.com/irinainina/docs

3. Привязываем локальную копию к оригинальному репозиторию
Для этого заходим в папку склонированного репозитория и выполняем две команды

git remote add upstream https://github.com/rolling-scopes-school/docs git fetch upstream image

4. Создаём собственную ветку разработки
Имя ветки, как правило, указывает на содержание правок. Предположим, что наша ветка будет называться "fix-typo". Создаёт новую ветку "fix-typo" и делает её активной команда.

git checkout -b fix-typo

В этой точке мы уже можем править код и добавлять в него необходимые изменения.

5. Добавляем изменения в собственную копию репозитория
Как только вы сделали работу (или её часть), отправьте её в собственную копию репозитория на GitHub. Для этого выполните команды:

git add . git commit -m "feat: add fix-typo" git push origin fix-typo

6. Возвращаем изменения: Pull request
Итак, всё сделано. Вы написали код, он у вас в ветке fix-typo как у вас на компьютере, так и на GitHub. Осталось только отправить его в оригинальный репозиторий.

Заходите на страницу вашей копии репозитория на GitHub, выбираете ветку fix-typo и нажимаете кнопку Pull Request. image

Добавляете название и описание ваших изменений и нажимаете на кнопку "Create pull request". 
