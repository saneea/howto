# git

## Конфигурация

Установка любой настройки происходит по шаблону

```sh
git config <флаг-уровеня-хранения-настройки> <ключ.настройки> <значение-настройки>
```

У git есть 3 уровня настроек
1. системные, уровень операционной системы (флаг `--system`, файл `/etc/gitconfig`)
1. глобальные, уровень пользователя (флаг `--global`, файл `~/.gitconfig`)
1. уровня репозитория (флаг `--local`, файл `./.git/config` в корне репозитория)

### Diff tool

Показать помощь по конфигурации difftool. Данная команда покажет список преднастроенных в самом git инструментов для сравнения файлов

```sh
git difftool --tool-help
```

Установить *kdiff3* в качестве *difftool*

```sh
git config --global diff.tool kdiff3
```