---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Типографские соглашения

## Программный код

Пример кода внутри строки, обозначается так: `echo "Hello, World!"`.

Команда вводимая в терминал Unix подобных систем:
```console
$ echo "Hello, World!"
```
Символ **$** является приглашением командной строки. Его вводить не нужно.

<!--
Команда вводимая в командной строке Windows:
```console
c:\> echo "Hello, World!"
```
Символы **c:\\>** являются приглашением командной строки. Их вводить не нужно.
-->

Команда вводимая в терминал Unix подобных систем вместе с выводом:
```{code-cell} python
%%bash
echo "Hello, World!"
```

Python код выглядит
```python
message = "Hello, World!"
print(message)
```

А так — python код и результат его исполнения
```{code-cell} python
message = "Hello, World!"
print(message)
```

+++

## Сочетания клавиш

```{list-table}
:header-rows: 1
:name: tbl_img_notation

* - Нотация
  - Значение
* - {bdg-dark}`a`
  - Нажать одну клавишу {bdg-dark}`a`
* - {bdg-dark}`Esc`
  - Нажать клавишу Escape
* - {bdg-dark}`Enter`
  - Нажать клавишу Enter
* - {bdg-dark}`Ctrl`
  - Нажать клавишу Ctrl
* - {bdg-dark}`Shift`
  - Нажать клавишу Shift
* - {bdg-dark}`Tab`
  - Нажать клавишу Tab
* - {bdg-dark}`Space`
  - Нажать клавишу пробел
* - {bdg-dark}`Up`
  - Нажать клавишу со стрелкой вверх
* - {bdg-dark}`Down`
  - Нажать клавишу со стрелкой вниз
* - {bdg-dark}`Right`
  - Нажать клавишу со стрелкой вправо
* - {bdg-dark}`Left`
  - Нажать клавишу со стрелкой влево
* - {bdg-dark}`a` {bdg-dark}`b`
  - Нажать клавишу {bdg-dark}`a`, отпустить и нажать клавишу {bdg-dark}`b`
* - {bdg-dark}`a` {bdg-dark}`b` {bdg-dark}`с`
  - Нажать клавишу {bdg-dark}`a`, отпустить, затем нажать {bdg-dark}`b`, отпустить и нажать {bdg-dark}`c`
* - {bdg-dark}`Ctrl`-{bdg-dark}`b`
  - Одновременно нажать клавиши {bdg-dark}`Ctrl` и {bdg-dark}`b`
* - {bdg-dark}`Ctrl`-{bdg-dark}`Tab`
  - Одновременно нажать клавиши {bdg-dark}`Ctrl` и {bdg-dark}`Tab`
* - {bdg-dark}`Ctrl`-{bdg-dark}`b` {bdg-dark}`t`
  - Одновременно нажать клавиши {bdg-dark}`Ctrl` и {bdg-dark}`b`, отпустить и нажать {bdg-dark}`t`
* - {bdg-dark}`g` {bdg-dark}`Ctrl`-{bdg-dark}`]`
  - Нажать клавишу {bdg-dark}`g`, отпустить и одновременно нажать клавиши {bdg-dark}`Ctrl` и {bdg-dark}`]`
* - {bdg-dark}`Ctrl`-{bdg-dark}`a` {bdg-dark}`Ctrl`-{bdg-dark}`c`
  - Одновременно нажать клавиши {bdg-dark}`Ctrl` и {bdg-dark}`a`, отпустить и одновременно нажать клавиши {bdg-dark}`Ctrl` и {bdg-dark}`c`
* - {bdg-dark}`f` {bdg-dark}`[char]`
  - Нажать клавишу {bdg-dark}`f`, затем ввести любой символ
* - {bdg-dark}`m` {bdg-dark}`[a-z]`
  - Нажать клавишу {bdg-dark}`m`, затем ввести любой символ нижнего регистра
* - {bdg-dark}`m` {bdg-dark}`[A-Z]`
  - Нажать клавишу {bdg-dark}`m`, затем ввести любой символ верхнего регистра
* - {bdg-dark}`m` {bdg-dark}`[a-zA-Z]`
  - Нажать клавишу {bdg-dark}`m`, затем ввести любой символ нижнего регистра или верхнего регистра
* - {bdg-dark}`d` {bdg-dark}`[motion]`
  - Нажать клавишу {bdg-dark}`d`, затем ввести любой символ нижнего регистра или верхнего регистра
```


+++

## Графические выделения

<!--
:::{admonition} This is a title
:class: note
:class: warning
:class: tip
:class: caution
:class: attention
:class: danger
:class: error
:class: hint
:class: important
:class: seealso
An example of an admonition with a title.
:::
-->

:::{note}
Так обозначаются замечания общего характера.
:::

:::{tip}
Так обозначаются советы и рекомендации.
:::

:::{hint}
Так обозначаются подсказки.
:::

:::{seealso}
Так обозначаются ссылки на материал по теме.
:::

:::{attention}
Материал, требующий особого внимания обозначается так.
:::

:::{warning}
Так обозначаются предупреждения и предостережения.
:::

:::{error}
Так обозначаются действия, которые могут привести к ошибке.
:::

:::{danger}
Потенциально опасные действия, обозначаются так.
:::

+++
