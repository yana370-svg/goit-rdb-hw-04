#  HW4: Olist Brazilian E-commerce — DML, DDL та складні SQL-запити

##  Опис проєкту

Цей проєкт демонструє роботу з повноцінною реляційною схемою даних на прикладі **Olist Brazilian E-commerce Dataset**. Мета — підготувати багатотабличний dataset до подальшої аналітики та ML-моделювання: забезпечити цілісність даних, побудувати коректні зв'язки між таблицями, сформувати ознаки на рівні клієнтів і продавців, а також підготувати бізнес-метрики для прийняття рішень.

###  Основні завдання
- Створення **typed-схеми** з constraints (PK, FK, CHECK, NOT NULL).
- Використання **PostgreSQL-фіч**: `RETURNING`, `ON CONFLICT DO UPDATE`, `UPDATE ... FROM`, `DELETE ... USING`.
- Побудова **RFM-сегментації** клієнтів на рівні `customer_unique_id`.
- Виконання складних **JOIN-запитів** (INNER, LEFT, FULL OUTER, SELF, Anti-join).
- Робота з **віконними функціями** (`ROW_NUMBER()`) та set-операціями (`UNION`, `INTERSECT`).

---

##  Джерело датасету

**Назва:** Olist Brazilian E-commerce Dataset  
**Джерело:** [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)  
**Ліцензія:** Public Domain (CC0)  
**Опис:** Реальні дані про замовлення бразильського інтернет-магазину Olist (2016–2018). Містить інформацію про клієнтів, замовлення, товари, продавців, відгуки та статуси доставки.

---

## Спосіб отримання файлів

### Автоматичне завантаження через `kagglehub` (рекомендовано)

```python
import kagglehub
dataset_dir = kagglehub.dataset_download('olistbr/brazilian-ecommerce')
print(dataset_dir)


Вимоги до середовища
Python 3.8+
PostgreSQL 14+ (у проєкті використовується pgserver для локального запуску)
Бібліотеки:
  pgserver
  psycopg2-binary
  sqlalchemy
  pandas
  kagglehub
