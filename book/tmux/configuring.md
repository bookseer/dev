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

(tmux_configuring)=
# Настройка tmux

Сейчас, уже имея некоторый опыт работы с tmux, давайте создадим собственную конфигурацию, которую сможем использовать
для наших остальных рабочих задач.

tmux по умолчанию имеет не самые удобные настройки. 
Многие из наиболее важных и полезных функции назначаются труднодоступным сочетаниям клавиш или состоят из длинных многословных команд. 
А цветовая схема tmux по умолчанию не особенно приятна для глаз. 
В этом разделе мы создадим базовый конфигурационный файл, который затем будем использовать в оставшейся части руководства. 
После изучения данного материала, у вас будет лучшее представление о том, насколько гибок tmux, и вы сможете конфигурировать его самостоятельно.
Давайте начнем с разговора о том, что нужно настроить в tmux в первую очередь.


## Файл .tmux.conf

По умолчанию tmux ищет параметры конфигурации в двух местах. 
Сначала в **/etc/tmux.conf** он ищет общесистемную конфигурацию. 
Затем --- файл с именем **.tmux.conf** в домашнем каталоге текущего пользователя. 
Если эти файлы не существуют, tmux просто использует настройки по умолчанию. 
Нам не нужно создавать общесистемный файл конфигурации, поэтому давайте создадим пустой файл конфигурации в нашем домашнем каталоге. 
Для этого можно использовать следующую команду:
```console
$ touch ~/.tmux.conf 
```

В этом файле мы можем делать все, от определения новых сочетаний клавиш до настройки окружения по умолчанию с нескольими окнами, панелями и запущенными программами. 
Давайте начнем с установки нескольких основных параметров, которые сделают работу с tmux намного проще.

:::{note}
Файл .tmux.conf является скрытым и не отображается в файловых менеджерах или списках каталогов по умолчанию. 
:::
