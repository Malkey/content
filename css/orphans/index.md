---
title: "`orphans`"
description: "Сколько строчек должно остаться на предыдущей странице при печати?"
authors:
  - furtivite
contributors:
  - skorobaeus
related:
  - js/match-media
  - css/media
  - js/window-print
tags:
  - doka
---

## Кратко

Свойство `orphans` указывает минимальное количество строк, которое должно остаться на странице при печати, если на весь абзац не хватило места.

Работает только внутри директивы [`@media`](/css/media/) со значением `print`. Отправьте страницу на печать, чтобы посмотреть, что получится.

## Пример

```css
@media print {
  p {
    orphans: 2;
  }
}
```

## Как пишется

В качестве значения можно передать целое положительное число, которое обозначает минимальное количество строк абзаца, которое должно остаться на предыдущей странице при печати. Не работает при отрицательном значении.

## Как понять

Свойство `orphans` тесно связано со свойством [`widows`](/css/widows/) и обозначает строки, которые остаются на предыдущей странице для печати.

![Пример напечатанного на двух страницах текста](images/orphans.png)
Поэма А. С. Пушкина «Руслан и Людмила». Синим выделены оставшиеся одни «верхние висячие строки».

Свойство `orphans` [наследуемое](/css/inheritance/) и вместо положительного числа можно передать значение `inherit`, при этом в свойство нельзя передавать отрицательные значения. Они работать не будут.

## На что обратить внимание

Обратите внимание, свойство `widows` имеет преимущество перед `orphans`. Браузер выполнит это свойство, а затем постарается выполнить то, что указано в `orphans`.

Так же, если на странице может поместиться пять строк, а в свойстве `orphans` вы укажете две строки, на печати будут размещены все пять строк.
