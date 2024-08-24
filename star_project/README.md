# Oписание проекта - Прогнозирование температуры звезды.

Исследовать данные о температурах на поверхности звезды. В нашем распоряжении характеристики 240 изученных звёзд.

## Данные

Согласно документации к данным, данные находятся в файле 6_class.csv и содержит следующие признаки:

- Относительная светимость L/Lo — светимость звезды относительно Солнца.
- Относительный радиус R/Ro — радиус звезды относительно радиуса Солнца.
- Абсолютная звёздная величина Mv — физическая величина, характеризующая блеск звезды.
- Звёздный цвет (white, red, blue, yellow, yellow-orange и др.) — цвет звезды, который определяют на основе спектрального анализа.
- Тип звезды.
- Абсолютная температура T(K) — температура на поверхности звезды в Кельвинах.

## Задача

Разработать нейронную сеть, которая поможет предсказывать абсолютную температуру на поверхности звезды. Необходимо учесть условия, которые важны для заказчика:

- качество предсказания (метрика RMSE < 4500);

## Используемые библиотеки
*os*, *time*, *pandas*, *matplotlib*, *seaborn*, *numpy*, *scipy*, *sklearn*, *PyTorch*, *statsmodels*, *tqdm*

## Вывод

По результатам исследования были обучены две нейронных сети, которые могут предсказывать температуры звезды. Их сравнительный анализ сведен в таблицу.

Достоинство работы заключается в том, что было достигнуто необходимое условие по метрике RMSE

Недостатки работы в том, что метрика близка к минимально возможной. Так же видно, что модель плохо предсказывает температуру редких звезд.

Как можно улучшить работу? Добиться уменьшения метрики, стоит добавить еще больше нелинейности в данные, либо увеличить количество скрытых слоев, либо же попытаться синтезировать значения, чтобы было больше данных для обучения.