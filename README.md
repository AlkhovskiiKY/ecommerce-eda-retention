# E-commerce EDA & Retention Analysis

## Цель

Исследовательский анализ поведения пользователей e-commerce
за октябрь 2019 и расчёт метрик удержания.

## Данные

- Источник: Kaggle "eCommerce behavior data"
- Строк: 42 448 764
- Период: 1–31 октября 2019
- Уникальных пользователей: 3 022 290
- Уникальных сессий: 9 244 421

## Стек

Python, DuckDB, pandas, matplotlib, seaborn, NumPy.

## Первые результаты

- Распределение событий: view 96.07%, cart 2.18%, purchase 1.75%.
- Среднее сессий на пользователя: 3.06.
- Воронка по сессиям: 9.24M viewed → 570K carted → 289K purchased.
- Воронка по пользователям: 3.02М viewed → 337K carted → 196K purchased.
- Конверсии по сессиям: View → Cart: 6.18%, Cart → Purchase: 50.7%.
- Конверсии по пользователям: View → Cart: 11.14%, Cart → Purchase: 58.34%.
- Замечен баг: нулевые ценники в количестве 68523 в заказах со статусом 'view', но далее мы имеем 150 нулевых заказов со статусом 'cart' и 0 со статусом 'purchase'.

## Прогресс

- [x] Session funnel
- [x] User funnel + сравнение с session
- [x] Retention D1/D7/D30 (strict / windowed)
- [x] Когортная таблица (cohort triangle)
- [x] Retention heatmap
- [x] Retention curves по когортам
- [x] Boxplot + median/IQR цены по неделям
- [x] Проверка аномалий (price = 0, дубликаты)
- [ ] DAU по дням
- [ ] GMV и средний чек
- [ ] Выводы и рекомендации
- [ ] README: визуализация(дашборд и отдельно ключевые таблицы) + рекомендации

## Структура

```text
eda.ipynb          # основной ноутбук (EDA + воронка)
README.md
.gitignore
```

## Автор

Альховский Константин (@Alkhovskii)
