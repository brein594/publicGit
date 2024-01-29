Познания про Git

pwd // переход к домашнему каталогу
cd~ //  переход к домашнему каталогу
ls //  список директорий
touch // создать файл 
mkdir //создать директорию 
     -p // несколько вложенных директорий
cp  что_копируем куда_копируем/  // копирование файлов 
mv //перемещение файлов 
cat // чтение файла
rm //удалить файл 
   -r //удаление с файлами
rmdir  // удаление пустой директории
&&  // объединение команд 
tab // автозаполнение 
cat ~/.gitconfig  // настройки git



:wq // выход из vim
git init //создание рапозитория 

git add hello.html //добавление файлов
git commit -m "Initial Commit" //добавление коммита
git status //проверка состояния
git log //лог изменения 
git log main --all // лог + удаленные комиты
notepad //блокнот
git switch main // переключение к ветке 
git reset //сброc подготовки к комиту откат на шаг 
git revert HEAD // отмена изменений последнего комита, но сохраняется в логах. на локальных ветках

git reset --hard v1 //рабочая директория должна быть приведена к тому состоянию, которое соответствует HEAD-. v1 тэг
git tag -d oops // удаление тэга

git commit --amend -m "Added copyright statement with email" // изменение коммита
git switch -c style //создание ветки style 
git show v1 // показывает изменения в коммите v1

git clone --bare work work.git //клонирование репозитория
git push shared main //отправка данных в удаленный репозиторий 
git daemon --verbose --export-all --base-path=. //запуск сервера  git
git clone git://localhost/work.git network_work //копирование репозитория 
git clone work home  // клонирование откуда куда
git merge origin/main // слияние изменения в текущую ветку
git pull //  =git fetch+git merge origin/main
git branch new // создает ветку new
git merge new // объединене веток с изменениями (прилепляет)
git rebase new1 //объединене веток с изменениями (переносит базу). Дальше нужно объединить изменения веток 
git branch -f main HEAD~3 //Переместит (принудительно) ветку main на три родителя назад от HEAD.


/////////////////////////////////////////
ssh -T git@github.com  // проверка привязки ключа 
git remote add origin git@github.com:%ИМЯ_АККАУНТА%/first-project.git  // привязка локальной директории к удаленной 
git remote -v // проверка привязки репозитория 
git push -u origin main //отправка на удаленный сервер первый раз


/////////////////mermaid-схема////////////////
HEAD -- это голова.
Коммит -- это всему голова.
Статусы файлов:
<тут пустая строка!>



%% комментарий 
```mermaid
 graph LR;
  untracked -- "git add" --> staged;
  staged    -- "???"     --> tracked/comitted;

%% стрелка без текста для примера: 
  A --> B;
``` 

продолжение 
