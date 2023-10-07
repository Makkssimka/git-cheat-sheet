# Шпаргалка по Git

Небольшой справочник по Git для личного использования

### Основные команды

Блок основных команд для git

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

### Основные сведения

> **HEAD** - это ссылка на хеш последнего коммита

Статусы файлов в git

**untraked** - _неотслеживаемый_, назначается новым файлам, у этих файлов нет предыдущих версий.

**staged** - _подготовленный_, файл после команды `git add`, т.е. подготовленный к отправке.

**tracked** - _отслеживаемый_, все файлы, которые были зафиксированны через `git commit` и добавлены через `git add`.

**modified** - _измененный_, файл, который был изменен по отношению к последней сохраненной версии.

```mermaid
flowchart TD
    A(untraked) -->|git add| B(staged + tracked)
    B -->|git commit| C(tracked)
    B -->|изменения| D(modified)
    D -->|git add| B
    C -->|изменения| D
```