# repise-app

Retseptlarni Boshqarish API

Bu loyiha FastAPI yordamida yaratilgan bo‘lib, foydalanuvchilarga retseptlar, toifalar (categories) va teglar (tags) bilan ishlash imkonini beradi.

O‘rnatish

Python virtual muhitini yaratish (ixtiyoriy, ammo tavsiya etiladi):

Windows: python -m venv venv
venv\Scripts\activate

Linux/macOS: python -m venv venv
source venv/bin/activate

Kerakli kutubxonalarni o‘rnatish:

pip install fastapi
pip install uvicorn
pip install sqlalchemy
pip install pydantic

Agar SQLite ishlatilsa, qo‘shimcha kutubxona kerak emas. Agar PostgreSQL ishlatilsa, quyidagini o‘rnating:

pip install psycopg2-binary

Loyihani ishga tushirish

Quyidagi buyruq orqali serverni ishga tushiring:

uvicorn main:app --reload

reload parametri yordamida koddagi o‘zgarishlar avtomatik yangilanadi.

API Yo‘llari

Kategoriyalar:

POST /categories/ – Yangi kategoriya yaratish

GET /categories/ – Barcha kategoriyalarni olish

Teglar:

POST /tags/ – Yangi teg yaratish

GET /tags/ – Barcha teglarni olish

Retseptlar:

POST /recipes/ – Yangi retsept yaratish

GET /recipes/ – Barcha retseptlarni olish

GET /recipes/{recipe_id} – Berilgan ID bo‘yicha retseptni olish

DELETE /recipes/{recipe_id} – Retseptni o‘chirish

Loyihaning Tuzilishi

main.py – FastAPI ilovasi
crud.py – CRUD funksiyalar
models.py – SQLAlchemy modellar
schemas.py – Pydantic sxemalar
database.py – Ma’lumotlar bazasi bilan ulanish
README.md – Loyihani tushuntiruvchi fayl
