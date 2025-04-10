
# 🌍 Travel Agency Web Project (PHP)

Bu loyiha — sayyohlik agentligi uchun mo‘ljallangan PHP (Laravel yoki Core PHP) asosida yaratilgan web tizimdir. Foydalanuvchilar sayt orqali mavjud sayohat turlarini ko‘rib chiqishlari, buyurtma berishlari va aloqa qilishlari mumkin.

## ✨ Asosiy imkoniyatlar

- 🏝 Turlar ro‘yxatini ko‘rish
- 🔍 Mamlakat va narx bo‘yicha filtrlash
- 📅 Har bir tur uchun batafsil ma'lumot
- 📝 Onlayn buyurtma shakli
- 🔐 Admin panel orqali turlarni boshqarish
- 📥 Buyurtmalar ro‘yxatini ko‘rish

## ⚙️ Texnologiyalar

- **Til:** PHP 8.x
- **Framework:** Laravel / Core PHP (belgilab qo‘ying)
- **Ma’lumotlar bazasi:** MySQL
- **Frontend:** HTML5, Tailwind CSS / Bootstrap
- **Admin panel:** Laravel Nova / Custom CRUD

## 🗃 Ma’lumotlar bazasi tuzilmasi

### `travel` jadvali:
| Field          | Type     | Description            |
|----------------|----------|------------------------|
| id             | int      | Avtoinkrement ID       |
| title          | varchar  | Tur nomi               |
| country        | varchar  | Mamlakat               |
| price          | decimal  | Narxi                  |
| duration       | int      | Necha kun              |
| description    | text     | Tavsifi                |
| image          | string   | Rasm fayli yo‘li       |

### `bookings` jadvali:
| Field           | Type     | Description              |
|-----------------|----------|--------------------------|
| id              | int      | ID                       |
| tour_id         | int      | Tashqi kalit (tours)     |
| name            | varchar  | Mijoz ismi               |
| phone           | varchar  | Telefon raqami           |
| passport_number | varchar  | Pasport raqami           |
| date            | date     | Safar sanasi             |

## 🔧 O‘rnatish (Installation)

```bash
git clone https://github.com/shahzodkenjayev/travel.git
cd travel-project

# Agar Laravel bo‘lsa
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
