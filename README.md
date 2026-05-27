# Прогнозирование биоактивности соединений против вируса гриппа

Команда 26. ChemAI: Predict the Cure

Задача: по 210 молекулярным дескрипторам предсказать три величины для каждого химического соединения - IC50 (концентрация подавления вируса), CC50 (концентрация токсичности) и SI = CC50 / IC50 (индекс селективности). Обучающая выборка - 751 соединение, тестовая - 250. Метрика - среднее RMSE по трём целевым.

Финальный результат на публичной таблице Kaggle: **266.95631**.

## Документация по проекту

- Презентация: https://magom001.github.io/mephi-hackathon-2026-team26/ (исходник: [presentation.md](presentation.md))
- Подробный отчёт по исследованию: [REPORT.md](REPORT.md)

## Воспроизведение submission.csv

Использовался Python 3.14.3. Должно работать на 3.12 и выше.

    python -m venv .venv
    .venv/Scripts/activate   # на Linux/Mac: source .venv/bin/activate
    pip install -r requirements.txt
    jupyter nbconvert --to notebook --execute solution.ipynb --output solution_executed.ipynb

Данные train.csv и test.csv лежат в data/. На выходе получается submission.csv в корне репозитория.