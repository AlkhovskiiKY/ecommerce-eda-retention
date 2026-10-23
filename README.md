# E-commerce EDA & Retention Analysis

## Цель

Исследовательский анализ поведения пользователей e-commerce
за октябрь 2019 и расчёт метрик удержания (Retention D1/D7/D30, cohort triangle).

## Данные

- Источник: Kaggle "eCommerce behavior data"
- Строк: 42 448 764
- Период: 1–31 октября 2019
- Уникальных пользователей: 3 022 290
- Уникальных сессий: 9 244 421

## Стек

Python, DuckDB (для больших данных), pandas, matplotlib.

## Первые результаты

- Распределение событий: view 96.07%, cart 2.18%, purchase 1.75%.
- Среднее сессий на пользователя: 3.06.
- Воронка по сессиям: 9.24M viewed → 570K carted → 289K purchased.
- Воронка по пользователям: 3.02М viewed → 337K carted → 196K purchased.
- Конверсии по сессиям: View → Cart: 6.18%, Cart → Purchase: 50.7%.
- Конверсии по пользователям: View → Cart: 11.14%, Cart → Purchase: 58.34%.

## Прогресс

- [x] Загрузка в DuckDB
- [x] Первичный осмотр (shape, nulls, типы)
- [x] Диапазон дат, уникальные пользователи
- [x] Распределение event_type
- [x] Session funnel
- [х] Retention D1/D7/D30 (в работе)
- [х] Когортная таблица
- [ ] Визуализации (DAU, retention heatmap)
- [ ] Выводы и рекомендации

## Структура

```text
eda.ipynb          # основной ноутбук (EDA + воронка)
README.md
.gitignore
```

## Автор

Альховский Константин (@Alkhovskii)
