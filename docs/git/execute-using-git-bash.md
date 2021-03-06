# Command for Git
![Git basic operation](/img/git-basic-operations.webp)

## Description

- Все команды кроме `git clone` выполняются в `terminal`/`cmd` в directory с проектом
- Команда `git clone` выполняется в directory `dev`, которая должна быть создана в пользовательской directory
- Команды для работы в `cmd`
    - `cd ..` - изменить directory на directory выше
    - `cd dir_name` - изменить directory на directory с именем `dir_name` - directory в которую необходимо перейти и которая находится в текущей directory
    - `c:` - перейти на диск `c`

## Workflow
![Git basic operation](/img/execute-using-git-bash.svg)

### Как копировать remote repository когда его нет на компьютере?

*Необходимо делать единожды*

`git clone https://github.com/GITHUB_USERNAME/GITHUB_REPOSITORY.git`

где `https://github.com/GITHUB_USERNAME/GITHUB_REPOSITORY.git` - ссылка на НУЖНЫЙ репозиторий


### Как сконфигурировать git

*Необходимо делать единожды*

`git config --global user.name 'YOUR FULLNAME'`

где `YOUR FULLNAME` - ваше имя и фамилия

`git config --global user.email 'YOUR_EMAIL'`

где `YOUR_EMAIL` - ваш email

### Как посмотреть состояние `working directory`

`git status`


### Как посмотреть `commits` для `local repository`

`git log`

### Как переключать `branch`

`git checkout BRANCH_NAME`

где `BRANCH_NAME` - имя `branch` в который необходимо переключиться

### Как добавить файлы из `working directory` в `staging area` для предстоящего `commit` 

`git add .`

где `.` - все файлы, можно также использовать имя файла, для добавления только файла

### Как добавить файлы из `staging area` в `local repository` с определенным заголовком 

`git commit -m "YOUR_COMMIT_MEASSAGE"`

где `YOUR_COMMIT_MEASSAGE` - залоговок который НУЖНО использовать

### Как отправить изменения из `local repository` в `remote repository`

`git push GITHUB_REPOSITORY`

### Как обновить текущий `local repository`, если произошли изменения в `remote repository`

`git fetch GITHUB_REPOSITORY`

`git pull GITHUB_REPOSITORY`

где `GITHUB_REPOSITORY` - краткое имя `remote repository` с которого необходимо вытянуть изменения

### Как добавит `remote repository` ментора

`git remote add GITHUB_USERNAME https://github.com/GITHUB_USERNAME/GITHUB_REPOSITORY.git`

где `https://github.com/GITHUB_USERNAME/GITHUB_REPOSITORY.git` - ссылка на НУЖНЫЙ репозиторий