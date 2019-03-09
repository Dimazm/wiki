# Command for Git
![Git basic operation](images/git-basic-operations.webp)

#### Как копировать свой репозиторий на компьютер когда его нет на компьютере?

`git clone https://github.com/rakovets/wiki.git`

где `https://github.com/rakovets/wiki.git` - ссылка на НУЖНЫЙ репозиторий

#### Как сконфигурировать git

`git config --global user.name 'Dmitry Rakovets'`

где `Dmitry Rakovets` - ваше имя

`git config --global user.email 'dmitryrakovets@gmail.com'`

где `dmitryrakovets@gmail.com` - ваш email

#### Как посмотреть состояние текущей рабочей директории

`git status`


#### Как посмотреть commit для local repository

`git log`

#### Как добавить файлы из рабочей директории для предстоящего commit 

`git add .`

где `.` - все файлы, можно также использовать имя файла, для добавления только файла

#### Как сделать commit c с определенным заголовком

`git commit -m "Message"`

где `Message` - залоговок который НУЖНО использовать

#### Как отправить изменения из local repository в remote repository

`git push`

#### Как обновить текущий local repository, если произошли изменения в remote repository

`git fetch`

`git pull`