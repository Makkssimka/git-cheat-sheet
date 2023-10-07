# Шпаргалка по Git

#### Инициализировать git

`git init`

#### Удалить папку с git

`rm -rf .git`

#### Показать состояние репозитория

`git status`

#### Добавить файлы для отслеживания

```
git add --all
git add .
git add text.txt
```

#### Добавить коммит

`git commit -m "Описание коммита"`

#### Посмотреть историю коммитов

`git log`

#### Добавить удаленный репозиторий

`git remote add origin адрес коммита`

#### Отправить изменения на удаленный репозиторий

```
// Первый раз
git push -u origin master

//Последующие разы
git push
```

```mermaid
flowchart TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
```

