# Анализ резюме HeadHunter

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-EDA-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-вычисления-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-интерактивные_графики-3D4F9F?style=for-the-badge&logo=plotly&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-визуализация-11557c?style=for-the-badge&logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-статистика-44AF77?style=for-the-badge)

**EDA · очистка данных · feature engineering · визуализация · Z-score (асимметричные границы)**

Исследовательский анализ резюме с [HeadHunter](https://hh.ru): загрузка и преобразование признаков, интерактивные графики, поиск выбросов и выводы по рынку труда.

**Автор:** [theKerimKerimov](https://github.com/theKerimKerimov) · **2026**  
**Репозиторий:** [headhunter-resume-data-analysis](https://github.com/theKerimKerimov/headhunter-resume-data-analysis)

---

## О проекте

| Этап | Что сделано |
|------|-------------|
| Загрузка | Чтение CSV, первичный осмотр структуры |
| Преобразование | Образование, пол/возраст, опыт, город, one-hot, зарплата в рублях по курсу валют |
| EDA | Распределения и медианы по образованию, городу, мобильности, возрасту |
| Очистка | Дубликаты, выбросы по возрасту (log + Z-score, 3σ слева / 4σ справа) |
| Визуализация | Plotly → HTML в папке [`visualization/`](visualization/) |

## Стек

- **Python** 3.10+
- **pandas**, **NumPy** — таблицы и признаки
- **Plotly** — основные диаграммы (можно открыть без Jupyter)
- **Matplotlib**, **Seaborn** — гистограммы и Z-score при очистке
- **Jupyter Notebook** — [`notebooks/headhunter_resume_eda.ipynb`](notebooks/headhunter_resume_eda.ipynb)

## Данные

Основной датасет **>400 МБ**, в репозиторий не входит.

1. Скачать: [Google Диск — данные проекта](https://drive.google.com/drive/folders/13KZHpvXoXhlcVe-zpxpHIGBcyoVTBgXG)
2. Положить в `data/` и переименовать:

| Файл на диске (как в архиве) | Имя в проекте |
|------------------------------|---------------|
| `dst-3.0_16_1_hh_database.csv` | `data/hh_resumes.csv` |
| `ExchangeRates.csv` | `data/exchange_rates.csv` |

Данные — учебный дамп в формате HeadHunter; только для портфолио и обучения, не для коммерческого парсинга.

## Быстрый старт

```bash
git clone https://github.com/theKerimKerimov/headhunter-resume-data-analysis.git
cd headhunter-resume-data-analysis

python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS / Linux:
# source .venv/bin/activate

pip install -r requirements.txt
jupyter notebook notebooks/headhunter_resume_eda.ipynb
```

В ноутбуке: **Kernel → Restart & Run All**.  
Пути к `data/` и `visualization/` работают, если Jupyter запущен из корня репозитория или из `notebooks/`.

## Структура репозитория

```
headhunter-resume-data-analysis/
├── notebooks/
│   └── headhunter_resume_eda.ipynb   # основной анализ
├── data/                              # датасеты (в .gitignore)
├── visualization/                     # экспорт графиков Plotly (HTML)
├── requirements.txt
├── LICENSE
└── README.md
```

## Лицензия

MIT — см. [LICENSE](LICENSE). Условия использования исходных данных определяет поставщик датасета.
