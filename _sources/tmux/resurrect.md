---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

(tmux_resurrect)
# Восстановление окружения `tmux` после перезагрузки системы

## Tmux Resurrect

`tmux-resurrect` решает проблему потери рабочих сессий при перезапуске компьютера,
включая запущенные процессы, текущие директории и структуру панелей.
Для работы не требуется предварительная настройка или регулярное обновление конфигурации.

### Основные возможности:
- Полное восстановление сессий, окон, панелей и их иерархии
- Сохранение рабочей директории для каждой панели
- Точное воссоздание расположения панелей (включая масштабированные)
- Восстановление активных сессий, окон и панелей
- Поддержка групповых сессий (для многомониторных конфигураций)
- Опциональное восстановление:
  - [Сессий Vim/Neovim](https://github.com/tmux-plugins/tmux-resurrect/tree/master/docs/restoring_vim_and_neovim_sessions.md)
  - [Содержимого панелей](https://github.com/tmux-plugins/tmux-resurrect/tree/master/docs/restoring_pane_contents.md)
  - [Истории окружений](https://github.com/tmux-plugins/tmux-resurrect/tree/master/docs/restoring_previously_saved_environment.md)

Интеграция с [tmux-continuum](https://github.com/tmux-plugins/tmux-continuum)
позволяет настроить автоматическое сохранение и восстановление.

### Управление
- Сохранение состояния: `PREFIX + Ctrl-s`
- Восстановление: `PREFIX + Ctrl-r`

### Технические требования
- Минимальная версия tmux: 1.9+
- Зависимости: bash
- Поддерживаемые ОС: Linux, macOS, Cygwin

###  Принцип работы:
Плагин избегает конфликтов с существующими элементами tmux.
Единственное исключение --- перезапись единственной панели при начальном
восстановлении окружения.

### Установка

#### Установка через Tmux Plugin Manager
1. Добавить в `.tmux.conf`:
   ```bash
   set -g @plugin 'tmux-plugins/tmux-resurrect'
   ```
2. Активировать плагин комбинацией `PREFIX + I`.

#### Ручная установка
1. Клонировать репозиторий:
   ```bash
   git clone https://github.com/tmux-plugins/tmux-resurrect /путь/до/плагина
   ```
2. Добавить в `.tmux.conf`:
   ```bash
   run-shell /путь/до/плагина/resurrect.tmux
   ```
3. Применить изменения:
   ```bash
   tmux source-file ~/.tmux.conf
   ```

Для автоматизации процессов сохранения рекомендуется использовать
[tmux-continuum](https://github.com/tmux-plugins/tmux-continuum).

## Tmux Continuum

tmux-continuum --- плагин для автоматизации управления сессиями tmux.

### Основные функции

1. **Фоновое сохранение окружения**
   Состояние tmux сохраняется каждые 15 минут без прерывания работы пользователя.
   *Требование:* статусная строка должна быть активна (используется хук `status-right`).

2. **Автозапуск tmux**
   Tmux автоматически стартует при включении компьютера/сервера.
   [Инструкции по настройке](docs/automatic_start.md) для разных ОС.

3. **Восстановление сессий**
   Последнее сохранённое состояние автоматически восстанавливается при запуске tmux.
   Активация: добавить в `.tmux.conf`:
   ```bash
   set -g @continuum-restore 'on'
   ```
   *Примечание:* восстановление происходит только при старте сервера tmux.

### Поддерживаемые системы
- Linux
- macOS
- Cygwin

### Технические требования
- Tmux версии 1.9+
- Bash
- Плагин [tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect)

#### Установка через Tmux Plugin Manager

1. Добавить в `.tmux.conf`:
   ```bash
   set -g @plugin 'tmux-plugins/tmux-resurrect'
   set -g @plugin 'tmux-plugins/tmux-continuum'
   ```
2. Активировать комбинацией `PREFIX + I`.

Плагин начнёт работать в фоновом режиме без дополнительных действий.

#### Ручная установка

1. Клонировать репозиторий:
   ```bash
   git clone https://github.com/tmux-plugins/tmux-continuum /путь/для/установки
   ```
2. Добавить в `.tmux.conf`:
   ```bash
   run-shell /путь/для/установки/continuum.tmux
   ```
3. Применить изменения:
   ```bash
   tmux source-file ~/.tmux.conf
   ```

Функционал активируется автоматически после перезагрузки конфигурации.
