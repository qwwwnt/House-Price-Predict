# House-Price-Predict

## Цель
Каждая строка в наборе данных описывает характеристики дома.

Наша цель - предсказать цену продажи дома, учитывая его характеристики.

Наши модели оцениваются по RMSE между логарифмом цены продажи, предсказанной нашей моделью, и логарифмом фактической цены продажи. Преобразование ошибок RMSE в логарифмическую шкалу гарантирует, что ошибки в прогнозировании дорогих и дешевых домов будут одинаково влиять на наш результат.

## Ключевые особенности
- Используем 12-fold cross-validation
- На каждой кросс-валидации используем 7 моделей: ridge, svr, gradient boosting, random forest, xgboost, lightgbm regressors
- Также используем StackingCVRegressor, оптимизированный с помощью xgboost
- Используем blending для получения более надежных прогнозов

## Итоги
- Итоговое значение RMSE модели 0.075476
- Значение на скрытых от модели данных 0.12253
