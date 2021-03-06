# Media

- [Теория цвета](#Теория-цвета)
- [Композиция](#Композиция)
- [Типографика](#Числа)
- [Иконографика](#Массивы)
- [Калиграфия](#Объекты)
- [Фотография](#Фотография)
- [Блоки](#Блоки)
- [Контролы](#Контролы)
- [Сетки](#Сетки)
- [Динамика](#Динамика)
- [Прототипирование](#Прототипирование)

## Теория цвета
[ Уровень темы ]
И первое с чего мы начали, это с формирования уровня темы. Уровень темы включает в себя цвета, отступы и размеры.

Я покажу как это работает на примере.

Для начала мы собрали все цвета, которые использовались в интерфейсе на тот момент, их было около 60-70. И стало понятно, что осмысленно работать с таким набором невозможно.

[ 6 цветов ]
Затем на один артборд мы выделили основную палитру. Она получилась из 6 основных цветов.

[ Цвета блоков ]
Дальше определились с возможными состояниями текста и блоков. И создали под них переменные. А их значения наследовали от базовых цветов изменяя Hue/Saturation/Lightness. 

[ Цвета текста ]
Оттенки серого задали путем изменения прозрачности от черного. Это позволяет использовать текст на различных цветных подложках. Получая приятный эффект тонирования.

[ Изменение палитры ]
В итоге у нас появилась возможность быстро управлять темой проекта изменяя значения базовой палитры, и получать новые значения сразу для нескольких состояний блоков.
 
[ Изменение математики ]
Но при этом все-таки осталось место для более тонкой настройки, за счет изменения математики.
 
На практике в стилях любого блока ни один цвет не пишется руками, используются только переменные. Это делает блок по умолчанию кастомным и готовым к дальнейшим изменениям.
 
После того как у нас появилось понимание о фундаменте мы перешли к следующему слою. Содержимому или Контенту.


## Композиция
### Обвязки
### Сетки

## Типографика
[ Цитата Zeldman-а ]
И если проанализировать содержимое практически любого интерфейса, то можно увидеть, что большую часть занимает текст. 

Есть даже такое выражение, что 90% современно интерфейса составляет типографика.

[ Страница с Яндекс.Денег 2 вида ]
Делать я не проверял но если взглянуть на пример, то можно сказать что эта цифра близка к правде

[ Текст с модификациями ]
Для более легкого жонглирования с внешним видом блоков, мы вынесли блок text с модификаторами на цвет, размер, жирность, регистр и еще несколько дополнительных. Используя их в различных комбинациях, мы получаем все необходимые состояния.

В интерфейсе text встречается двух типов:
 
[ Оффер ]
Первое внутри интерфейсных блоков. Как пример оффер, который реально есть на портале Яндекс.Денег в разделе скидки и бонусы. Тут есть два текстовых элемента с размером скидки и описанием. К которым мы примиксовываем блок текст в нужных модификациях. Таким образом мы получаем консистентный типографический визуал не написав ни одной строчки CSS.

[ Страница ]
И второй вариант внутри информационных страниц
Здесь текст является вполне самостоятельным блоком. У которого добавляется еще один модификатор —type... (с учетом семантики), для него прописаны относительные отступы, они высчитываются с учетом заложенных типографических рекомендаций. Это позволяет более легко считывать информацию

## Иконографика
[ Иконки ]
Если говорить про графически блоки, то иконки самая уязвимая часть интерфейса и небрежное отношение к ним может убить даже самую прекрасную эстетику.

[ Размер иконок ]
У нас как и многих была проблема, что иконки рисовались под конкретный блок и в какой-то момент мы получили неконтролируемое наследие.

Даже ходила шутка, что по иконки можно узнать дизайнера. Но проблема тут в том, что мы не можем изменить всю библиотеку иконок разом. Для этого пришлось бы вручную проходиться по каждому блоку.

К их проработке мы подошли также системно как и другим интерфейсными сущностям. Мы сделали блок icon.

Иконки существуют двух размеров и отрисовываются по сетке.

[ Модификаторы на цвет ]
Что касается их использования. То иконку можно встретить в совершенно различных частях интерфейса, она может быть как самостоятельной сущность или находиться внутри контрола, но чаще всего иконка используется рядом с текстовым блоком, поэтому для нее мы сделала точно такие же цветовые модификации. Это позволяет легко собирать новые комбинации.

## Калиграфия
### Арабская
### Готика
### Рваная

## Фотография
### Пленка ч/б
### Пленка цветная

## Блоки
… 

## Контролы
### Особенности 
### БЭМ компонентс


## Динамика
### 3 типа анимации

## Прототипирование
### БЭМ
### Whitepaper
