# RecipeNLG

# RecipeNLG — Vegetarian vs Non‑Vegetarian Classification (NLP)

Учебный ноутбук по курсу **«Обработка текстов»**: классификация рецептов на **вегетарианские (1)** и **невегетарианские (0)** по тексту ингредиентов.

Решение построено в формате сравнения подходов:

- **Baseline (Classic ML):** TF‑IDF + Logistic Regression
- **Transformer:** DistilBERT (`distilbert-base-uncased`) + `Trainer`

В конце ноутбука формируется таблица метрик и график сравнения.

---


## Файлы

- `nlp_recipe_classification1.ipynb` — основной ноутбук
- `data/full_dataset.csv` — датасет 
- `checkpoints_bert/` — чекпоинты модели 

---

## Требования

- Python 3.9+
- Windows / Linux / macOS
- (опционально) GPU NVIDIA для ускорения BERT

---

## Установка

В корне проекта:


```bash

python -m venv venv
# Windows:
venv\Scripts\activate
# Linux/Mac:
# source venv/bin/activate

pip install -U pip
pip install pandas numpy matplotlib scikit-learn datasets transformers torch
```
## Данные

Ожидается файл:

```bash
data/full_dataset.csv
```

В CSV должна быть колонка с ингредиентами. По умолчанию ищется:

- ingredients
- или любая колонка, в названии которой есть ingredient

Опционально используется колонка названия рецепта:

- title / name / recipe_name

## Запуск

```bash
jupyter lab
# или
jupyter notebook
```
