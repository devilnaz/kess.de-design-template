1) Используйте препроцессор SASS или SCSS
2) Не изменять файлы modern-normalize.css и _reset.sass
3) Для адаптации используется mixin препроцессора, предполагается @media (max-width: )
Чтобы использовать mixin необходимо в media установить свои значения в sizes
```
$sizes: ("xs":413px, "sm":601px, "md":768px, "lg":1013px, "xl":1201px)
```
Затем в SASS использовать так:
```
.class
  @include media('md')
    background-color: #000000
```
4) Шрифты подключать в _fonts.sass 
Подключать только те, которые используются в фигме. 
Шрифты берутся с папки fonts. 
Если нет необходимого шрифта, то нужно добавить.
5) Для внешнего падинга модуля используйте класс .outer-gap-elem
6) Стили каждого модуля, хедера, блока и т.д. добавьте в папку components и импортируйте в main.sass
7) Стили делать изолированными для конкретного блока. 
   Например: шрифт не прописывать для верхнего родительского элемента(body, main и т.д.)
   Нужно прописать стиль на сам элемент, либо на родительский элемент, который будет отдельным блоком.