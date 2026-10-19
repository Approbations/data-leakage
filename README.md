# Примеры утечки данных

Ноутбук иллюстрирует три типа утечек из презентации: Target Leakage, Train-Test Contamination, Feature Leakage. Остальные разделы презентации (причины, последствия, выявление) — теоретические.

## Содержание

1. **Утечка обучающего/тестового множества** — отбор признаков
   на всём датасете до разделения на train/test.
2. **Утечка целевой переменной** — признак, производный от таргета, 
    попадает в модель.
3. **Утечка на уровне признаков** — монотонный `row_id` и target encoding,
   посчитанный на всём датасете.

Для каждого примера приведены: «неправильный» код, объяснение механизма
утечки, «правильный» код и рекомендация.

## Требования

- Python 3.10+
- Зависимости из `requirements.txt`

## Установка и запуск

```bash
# 1. Клонировать репозиторий
git clone https://github.com/Approbations/data-leakage.git
cd data-leakage

# 2. Создать виртуальное окружение
python -m venv .venv
source .venv/bin/activate        # Linux/macOS
# .venv\Scripts\activate         # Windows

# 3. Установить зависимости
pip install -r requirements.txt

# 4. Запустить Jupyter
jupyter notebook examples.ipynb
```