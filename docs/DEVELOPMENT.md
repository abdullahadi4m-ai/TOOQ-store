# TOOQ Store - دليل التطوير

## 📋 محتويات الدليل

1. [البدء السريع](#البدء-السريع)
2. [هيكل المشروع](#هيكل-المشروع)
3. [إعدادات البيئة](#إعدادات-البيئة)
4. [تشغيل المشروع](#تشغيل-المشروع)
5. [API Endpoints](#api-endpoints)

---

## البدء السريع

### المتطلبات
- Node.js v16 أو أعلى
- MongoDB
- npm أو yarn

### التثبيت

```bash
# استنساخ المشروع
git clone https://github.com/abdullahadi4m-ai/tooq-store.git
cd tooq-store

# تثبيت Backend
cd backend
npm install

# تثبيت Frontend
cd ../frontend
npm install
```

---

## هيكل المشروع

```
tooq-store/
├── backend/
│   ├── routes/
│   │   ├── auth.js
│   │   ├── products.js
│   │   ├── categories.js
│   │   ├── users.js
│   │   ├── orders.js
│   │   ├── cart.js
│   │   ├── reviews.js
│   │   ├── wishlist.js
│   │   ├── coupons.js
│   │   └── admin.js
│   ├── models/
│   ├── middleware/
│   ├── server.js
│   ├── package.json
│   └── .env.example
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── redux/
│   │   ├── App.js
│   │   └── index.js
│   ├── package.json
│   └── .env.example
│
├── docs/
│   ├── DATABASE_SCHEMA.md
│   └── DEVELOPMENT.md
│
└── README.md
```

---

## إعدادات البيئة

### Backend (.env)

```bash
# Server
PORT=5000
NODE_ENV=development

# Database
MONGODB_URI=mongodb://localhost:27017/tooq-store

# JWT
JWT_SECRET=your_secret_key
JWT_EXPIRE=7d

# APIs
SHAM_CASH_API_KEY=key
WHATSAPP_API_KEY=key
```

### Frontend (.env)

```bash
REACT_APP_API_URL=http://localhost:5000/api
REACT_APP_ENV=development
```

---

## تشغيل المشروع

### تشغيل Backend

```bash
cd backend
npm install
npm run dev
```

السيرفر سيعمل على: `http://localhost:5000`

### تشغيل Frontend

```bash
cd frontend
npm install
npm start
```

الموقع سيفتح على: `http://localhost:3000`

---

## API Endpoints

### Authentication
- `POST /api/auth/register` - تسجيل مستخدم جديد
- `POST /api/auth/login` - تسجيل الدخول

### Products
- `GET /api/products` - الحصول على جميع المنتجات
- `GET /api/products/:id` - الحصول على تفاصيل منتج

### Orders
- `GET /api/orders` - طلبات المستخدم
- `POST /api/orders` - إنشاء طلب جديد

### More Routes
- `/api/categories` - التصنيفات
- `/api/users/profile` - ملف المستخدم
- `/api/cart` - سلة التسوق
- `/api/reviews` - التقييمات
- `/api/wishlist` - قائمة المفضلة
- `/api/coupons/verify` - التحقق من الكوبونات
- `/api/admin/dashboard` - لوحة التحكم

---

## نصائح التطوير

1. استخدم Postman لاختبار APIs
2. تأكد من تشغيل MongoDB قبل بدء الـ Backend
3. استخدم Redux DevTools للتطوير في Frontend
4. اتبع معايير الكود (Code Standards)

---

**آخر تحديث:** يونيو 2026
