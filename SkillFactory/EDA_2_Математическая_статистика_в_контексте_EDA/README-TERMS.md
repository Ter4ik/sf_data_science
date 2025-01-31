## Некоторые термины и определения модуля EDA-2 (Математическая статистика в контексте EDA) ##

**Математическая статистика**&nbsp;&mdash; раздел математики, который занимается
систематизацией и обработкой данных для их использования и получения выводов.

**Статистические данные**&nbsp;&mdash; упорядоченные, классифицированные данные
о каком-то явлении или процессе.

**Мера центральной тенденции**&nbsp;&mdash; число, которое описывает так
называемое &laquo;среднее&raquo; признака. Мера центральной тенденции может
рассчитываться по-разному в зависимости от типа признака или от его
распределения.

**Мода**&nbsp;&mdash; самый часто встречающийся элемент в числовом ряду. Чаще
всего мода используется в нечисловых рядах.

**Корреляция**&nbsp;&mdash; статистическая связь двух и более переменных. При
изменении значения одной из переменных происходит закономерное изменение другой
или других величин.

- $\pm$ (0&nbsp;&mdash; 0,3)&nbsp;&mdash; Отсутствие связи или очень слабая связь
- $\pm$ (0,3&nbsp;&mdash; 0,5)&nbsp;&mdash; Слабая связь
- $\pm$ (0,5&nbsp;&mdash; 0,7)&nbsp;&mdash; Средняя связь
- $\pm$ (0,7&nbsp;&mdash; 0,9)&nbsp;&mdash; Сильная связь
- $\pm$ (0,9&nbsp;&mdash; 1)&nbsp;&mdash; Очень сильная или абсолютная связь

**Мультиколлинеарность**&nbsp;&mdash; такая сильная зависимость переменных друг
от друга, что она затрудняет анализ и оценку будущей модели машинного обучения.

----

**Корреляция Пирсона (Pearson)**&nbsp;&mdash; используется для вычисления линейной
взаимосвязи между признаками (при этом у признаков должно быть нормальное
распределение).

**Линейная взаимосвязь**&nbsp;&mdash; вид связи между признаками, в котором
изменение одного признака всегда приводит к изменению другого признака на
величину, пропорциональную изменению (уравнение прямой).

[**`q-q plot`**](https://habr.com/ru/post/578754/)&nbsp;&mdash; построение
гистограммы распределения непрерывного признака. Можно быстро проверить признак
на нормальность распределения:

```python
import matplotlib.pyplot as plt
from scipy import stats
# Задание сетки рисунка, количества строк и столбцов
plt.subplot(1, 2, 1)
# qq plot
stats.probplot(df['feature'], plot=plt)
# Второй рисунок рядом
plt.subplot(1, 2, 2)
# Гистограмма распределения признака
plt.hist(df['feature'])
# Чтобы графики не наезжали другу на друга, используем tight_layout
plt.tight_layout()
# Просмотр графика
plt.show()
```

----

**Ранговая корреляция**&nbsp;&mdash; вид корреляции, отражающий отношения
переменных, упорядоченных по возрастанию их значения. Ранги&nbsp;&mdash;
порядковые номера единиц совокупности в упорядоченном (ранжированном) ряду. Если
проранжировать совокупность по двум признакам, связь между которыми изучается,
то полное совпадение рангов означает максимально тесную прямую связь, а полная
противоположность рангов&nbsp;&mdash; максимально тесную обратную связь.

**Корреляция Спирмена (Spearman)**&nbsp;&mdash; используется для вычисления
взаимосвязей между категориальными переменными.

**Корреляция Кендалла (Kendall)**&nbsp;&mdash; также предусмотрена для
нахождения взаимосвязей между категориальными переменными. В среднем выдаёт
меньшие значения коэффициента корреляции, чем корреляция Спирмена. Более
устойчива к ошибкам и выбросам в данных.

**Корреляция Мэтьюса (Matthews)**&nbsp;&mdash; мера силы связи между бинарными
переменными (Бинарные признаки являются подгруппой категориальных). Коэффициент
корреляции Мэтьюса может быть полезен в случае, когда в датасете представлены
только бинарные переменные. Кроме того, этот коэффициент используется для оценки
качества моделей, ответы которых также бинарны.

----
