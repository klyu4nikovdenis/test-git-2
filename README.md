1. git status
2. git add (добавляет файлы в stage) - команда для подготовки имеющихся файлов к записи, синтаксис
git add index.html index.js и тд, но чтобы записат все файлы проекта разом пишется git add .
3. git commit (команда для записи файлов) пишется git commit -m(это флаг) и "комментарий" по типу
git commit -m "init project" (инициализация проекта)
4. git log // чтобы посмотреть запись git log --oneline //краткая инфа о записи
5. git push [rep_link] [branch_name] // ссылка на репозиторий и имя ветки, о ветках позже
для просмтра ссылки на текущий проект команда git remote -v
для просмотра ветки git branch
6. git remote add origin [link] // связать файлы в vsc с репозиторием gits
7. git reset [название файла]// позволяет удалить файлы из промежуточной области stage
8. git diff позволяет посмотреть все строки которые мы изменяли либо добавляли
9. git reset --hard // возвращает все изменения файлов до предыдущего вывода в стейдж в файлах типа html js

Тема: Основы ветвления и слияния
1. git branch [branch-name] // чтобы создать новую ветку вводим команду и имя ветки
после добавления появляется ветка develop, но она  серая, а зеленым горит та, на которой мы сейчас, то есть master // для удаления ветки git branch -d [branch-name]
2. git checkout [branch-name] //переключаемся на другую ветку и теперь она горит зеленым, а масте серым
для слияния и проверки ошибок в ветках кодов других разработчиков есть встроенный инструмент github - pull request на самом сайте добавляем комменты и мёрджим ветки после проверки ошибок
3. git pull [rep_link] [branch_name] // команда для загрузки изменения замёрдженных веток из гита в редактор кода

Слияние меток можем делать и через терминал
1. git merge [branch-name] // вводим имя ветки которую переносим в ту ветку в которой находимя сейчас
в этом примере это мы находясь в master переносим feature/main-page в мастер

Конфликты при мердже веток
возникают тогда, когда 2 разных разработика написали на разных ветках разный код на одной и той же строке кода

при мердже таких веток в vsc  появляется конфликт и он показывает: зеленым выделяет код - изменения в главной ветке, а синим входище изменения и vsc предлагает нам варианты: принять изменения в основном файле, входящие, принять оба, не принять ничего