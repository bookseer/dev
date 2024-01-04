---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.16.0
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# Типографские соглашения

## Программный код

Пример кода внутри строки, обозначается так: `echo "Hello, World!"`.

Команда вводимая в терминал Unix подобных систем:
```bash
echo "Hello, World!"
```
Символ **$** является приглашением командной строки. Его вводить не нужно. 

Команда вводимая в командной строке Windows подобных систем:
```shell
echo "Hello, World!"
```
Символы **C:\\>** являются приглашением командной строки. Их вводить не нужно. 

Команда вводимая в терминал Unix подобных систем вместе с выводом:
```bash
echo "Hello, World!"
```
```{code-cell} ipython3
:tags: ["remove-input"]
%%bash
echo "Hello, World!"
```

Python код выглядит 
```python
message = "Hello, World!"
print(message)
```
А так — python код и результат его исполнения

```{code-cell} ipython3
message = "Hello, World!"
print(message)
```

+++

## Графические выделения

<!--
```{admonition} This is a title
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
```
-->

```{admonition} Замечание
:class: note
Так обозначаются замечания общего характера.
```

```{admonition} Совет
Так обозначаются советы и рекомендации,
```

```{admonition} Подсказка
:class: hint
Так обозначаются подсказки.
```

```{admonition} Смотрите также
:class: seealso
Так обозначаются ссылки на материал по теме.
```

```{admonition} Внимание
:class: important
Материал, требующий особого внимания обозначается так.
```

```{admonition} Предупреждение 
:class: warning
Так обозначаются предупреждения и предостережения.
```

```{admonition} Опасность
:class: danger
Потенциально опасные действия, обозначаются так.
```

```{admonition} Ошибка
:class: error
Так обозначаются действия, которые могут привести к ошибке.
```

---

```{code-cell} ipython3
note = "Python syntax highlighting"
print(note)
```

```{code-cell} python
note = "Python syntax highlighting"
print(note)
```


+++

## Математика

````{prf:proof}
We'll omit the full proof.

But we will prove sufficiency of the asserted conditions.

To this end, let $y \in \mathbb R^n$ and let $S$ be a linear subspace of $\mathbb R^n$.

Let $\hat y$ be a vector in $\mathbb R^n$ such that $\hat y \in S$ and $y - \hat y \perp S$.

Let $z$ be any other point in $S$ and use the fact that $S$ is a linear subspace to deduce

```{math}
\| y - z \|^2
= \| (y - \hat y) + (\hat y - z) \|^2
= \| y - \hat y \|^2  + \| \hat y - z  \|^2
```

Hence $\| y - z \| \geq \| y - \hat y \|$, which completes the proof.
````

````{prf:theorem} Теорема Пифагора
:label: thm-pythagor

В прямоугольном треугольнике, длины катетов которого равны $a$ и $b$, а длина гипотенузы — $c$, выполнено соотношение
$a^2 + b^2 = c^2$. 
````








