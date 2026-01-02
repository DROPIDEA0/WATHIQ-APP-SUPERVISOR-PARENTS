# 📋 قائمة المهام الموحدة - مشروع WATHIQ

**آخر تحديث:** 2 يناير 2026  
**حالة المشروع:** قيد التطوير النشط

---

## 📊 ملخص الإنجاز العام

| المشروع | نسبة الإنجاز | الحالة |
|---------|--------------|--------|
| **Backend API** | 75% | 🟢 نشط ومنشور |
| **Frontend Dashboard** | 60% | 🟡 قيد الربط بالـ API |
| **Mobile Apps** | 10% | 🔴 مرحلة التخطيط |
| **الإجمالي** | 48% | 🟡 قيد التطوير |

---

## 🎯 المهام حسب الأولوية

---

## 🔴 أولوية قصوى (Critical Priority)

### 1️⃣ ربط Frontend Dashboard بالـ Backend API

**الهدف:** تفعيل لوحة التحكم بشكل كامل للاستخدام الفعلي

#### 1.1 إعداد API Client
- [ ] إنشاء خدمة Axios موحدة في `/src/services/api.ts`
- [ ] إعداد Base URL (https://api.wathiq.pro/api/v1)
- [ ] إعداد Interceptors لإضافة JWT Token تلقائياً
- [ ] معالجة الأخطاء المركزية (Error Handling)
- [ ] معالجة انتهاء صلاحية Token (Token Refresh)

#### 1.2 نظام المصادقة (Authentication)
- [ ] ربط صفحة Login بـ API endpoint `/auth/login`
- [ ] تخزين JWT Token في localStorage أو sessionStorage
- [ ] إنشاء Context للمصادقة (AuthContext)
- [ ] إنشاء Protected Routes باستخدام React Router
- [ ] تفعيل وظيفة Logout (مسح Token والتوجيه للـ Login)
- [ ] عرض معلومات المستخدم الحالي في Header

#### 1.3 صفحة Dashboard الرئيسية
- [ ] جلب الإحصائيات من `/pickup-requests/statistics`
- [ ] عرض عدد المدارس، الطلاب، أولياء الأمور، المشرفات
- [ ] عرض إحصائيات طلبات الاستلام (معلقة، قيد التنفيذ، مكتملة)
- [ ] إضافة Loading State أثناء جلب البيانات
- [ ] معالجة الأخطاء وعرض رسائل مناسبة

#### 1.4 إدارة المدارس (Schools Management)
- [ ] **عرض القائمة:** GET `/schools`
- [ ] **إضافة مدرسة:** POST `/schools` + Form مع Validation
- [ ] **تعديل مدرسة:** PUT `/schools/:id` + Modal للتعديل
- [ ] **حذف مدرسة:** DELETE `/schools/:id` + Confirmation Dialog
- [ ] **تفعيل/تعطيل:** PATCH `/schools/:id` (تغيير is_active)
- [ ] **البحث والفلترة:** حسب الاسم، المدينة، الحالة
- [ ] **Pagination:** إذا كان عدد المدارس كبيراً

#### 1.5 إدارة الطلاب (Students Management)
- [ ] **عرض القائمة:** GET `/students`
- [ ] **إضافة طالب:** POST `/students` + Form مع Validation
- [ ] **تعديل طالب:** PUT `/students/:id`
- [ ] **حذف طالب:** DELETE `/students/:id` + Confirmation
- [ ] **رفع صورة الطالب:** File Upload (بعد إعداد File Upload API)
- [ ] **البحث والفلترة:** حسب الاسم، المدرسة، الصف، ولي الأمر
- [ ] **Pagination**

#### 1.6 إدارة أولياء الأمور (Parents Management)
- [ ] **عرض القائمة:** GET `/parents`
- [ ] **إضافة ولي أمر:** POST `/parents` (يتطلب إنشاء User أولاً)
- [ ] **تعديل ولي أمر:** PUT `/parents/:id`
- [ ] **حذف ولي أمر:** DELETE `/parents/:id` + Confirmation
- [ ] **عرض أبناء ولي الأمر:** GET `/students?parent_id=X`
- [ ] **البحث والفلترة:** حسب الاسم، البريد الإلكتروني، الهاتف
- [ ] **Pagination**

#### 1.7 إدارة المشرفات (Supervisors Management)
- [ ] **عرض القائمة:** GET `/supervisors`
- [ ] **إضافة مشرفة:** POST `/supervisors`
- [ ] **تعديل مشرفة:** PUT `/supervisors/:id`
- [ ] **حذف مشرفة:** DELETE `/supervisors/:id` + Confirmation
- [ ] **تحديث الموقع:** PATCH `/supervisors/:id/location` (عرض على خريطة)
- [ ] **تغيير حالة التوفر:** PATCH `/supervisors/:id/availability`
- [ ] **البحث والفلترة:** حسب المدرسة، الحالة
- [ ] **Pagination**

#### 1.8 إدارة طلبات الاستلام (Pickup Requests Management)
- [ ] **عرض القائمة:** GET `/pickup-requests`
- [ ] **إنشاء طلب:** POST `/pickup-requests`
- [ ] **عرض تفاصيل الطلب:** GET `/pickup-requests/:id`
- [ ] **تحديث حالة الطلب:** PATCH `/pickup-requests/:id/status`
- [ ] **إضافة تقييم:** PATCH `/pickup-requests/:id/feedback`
- [ ] **عرض الموقع على الخريطة:** استخدام Google Maps API
- [ ] **البحث والفلترة:** حسب الحالة، الطالب، ولي الأمر، المشرفة، التاريخ
- [ ] **Pagination**

#### 1.9 تحسينات UI/UX
- [ ] **Loading States:** Spinner أو Skeleton أثناء جلب البيانات
- [ ] **Error States:** رسائل خطأ واضحة مع إمكانية إعادة المحاولة
- [ ] **Empty States:** رسائل عند عدم وجود بيانات
- [ ] **Toast Notifications:** لعرض رسائل النجاح والخطأ (استخدام مكتبة مثل react-hot-toast)
- [ ] **Confirmation Dialogs:** قبل الحذف أو العمليات الحساسة
- [ ] **Form Validation:** التحقق من المدخلات قبل الإرسال
- [ ] **Responsive Design:** التأكد من عمل التطبيق على الموبايل

---

### 2️⃣ إكمال APIs المتبقية في Backend

**الهدف:** إكمال جميع الوظائف المطلوبة في Backend

#### 2.1 File Upload API
- [ ] تثبيت مكتبة Multer أو مشابهة
- [ ] إنشاء Endpoint: `POST /upload/student-photo`
- [ ] إنشاء Endpoint: `POST /upload/document`
- [ ] حفظ الملفات في مجلد `/uploads` أو ربط مع Amazon S3
- [ ] إرجاع URL للملف المرفوع
- [ ] التحقق من نوع وحجم الملف
- [ ] حماية الـ Endpoint (Authentication Required)

#### 2.2 Authorized Persons API
- [ ] إنشاء Controller: `authorizedPersonsController.ts`
- [ ] إنشاء Routes: `/authorized-persons`
- [ ] **GET** `/authorized-persons` - جلب جميع الأشخاص المفوضين
- [ ] **GET** `/authorized-persons/:id` - جلب شخص مفوض محدد
- [ ] **GET** `/authorized-persons/student/:studentId` - جلب المفوضين لطالب معين
- [ ] **POST** `/authorized-persons` - إضافة شخص مفوض جديد
- [ ] **PUT** `/authorized-persons/:id` - تعديل بيانات شخص مفوض
- [ ] **DELETE** `/authorized-persons/:id` - حذف شخص مفوض
- [ ] Validation للمدخلات
- [ ] Role-based Access Control

#### 2.3 Notifications API
- [ ] إنشاء Controller: `notificationsController.ts`
- [ ] إنشاء Routes: `/notifications`
- [ ] **GET** `/notifications` - جلب جميع الإشعارات للمستخدم الحالي
- [ ] **GET** `/notifications/unread` - جلب الإشعارات غير المقروءة
- [ ] **GET** `/notifications/:id` - جلب إشعار محدد
- [ ] **POST** `/notifications` - إنشاء إشعار جديد
- [ ] **PATCH** `/notifications/:id/read` - تحديد إشعار كمقروء
- [ ] **DELETE** `/notifications/:id` - حذف إشعار
- [ ] إعداد Push Notifications (Firebase Cloud Messaging) - مرحلة لاحقة

#### 2.4 Activity Logs API
- [ ] إنشاء Controller: `activityLogsController.ts`
- [ ] إنشاء Routes: `/activity-logs`
- [ ] **GET** `/activity-logs` - جلب سجلات الأنشطة
- [ ] **GET** `/activity-logs/user/:userId` - سجلات مستخدم محدد
- [ ] فلاتر: حسب المستخدم، نوع العملية، التاريخ
- [ ] Pagination للسجلات
- [ ] حماية الـ Endpoint (Admin Only)

#### 2.5 تحسينات Backend
- [ ] إضافة Swagger Documentation لجميع APIs
- [ ] إعداد Error Logging (Winston أو مشابه)
- [ ] إعداد Rate Limiting لحماية APIs
- [ ] تحسين استعلامات قاعدة البيانات (Indexing)
- [ ] إعداد Caching (Redis) للبيانات المتكررة

---

### 3️⃣ إعداد Auto-Deployment للـ Backend

**الهدف:** أتمتة عملية النشر عند الرفع على GitHub

#### 3.1 إنشاء GitHub Webhook
- [ ] الدخول إلى Settings → Webhooks في مستودع `API-WATHIQ-APP`
- [ ] إضافة Webhook جديد
- [ ] Payload URL: `https://api.wathiq.pro/webhook.php`
- [ ] Content type: `application/json`
- [ ] Secret: (اختياري لكن موصى به)
- [ ] Events: اختيار `push` فقط
- [ ] حفظ الـ Webhook

#### 3.2 إنشاء Webhook Handler
- [ ] إنشاء ملف `webhook.php` في `/home/api-wathiq/htdocs/api.wathiq.pro/`
- [ ] التحقق من صحة الطلب (GitHub Signature)
- [ ] استدعاء سكريبت `deploy-api.sh`

#### 3.3 إنشاء Deploy Script
- [ ] إنشاء ملف `deploy-api.sh` في مجلد المشروع
- [ ] إضافة الأوامر التالية:
  ```bash
  #!/bin/bash
  cd /home/api-wathiq/htdocs/api.wathiq.pro
  git pull origin main
  npm install
  npm run build
  pm2 restart wathiq-api
  ```
- [ ] إعطاء صلاحيات التنفيذ: `chmod +x deploy-api.sh`

#### 3.4 الاختبار
- [ ] رفع تحديث بسيط على GitHub
- [ ] التحقق من تشغيل Webhook
- [ ] التحقق من تحديث الملفات على الخادم
- [ ] التحقق من إعادة تشغيل PM2
- [ ] اختبار API للتأكد من عمله بشكل صحيح

---

## 🟡 أولوية متوسطة (Medium Priority)

### 4️⃣ تطوير تطبيقات الموبايل

**الهدف:** بناء تطبيقات موبايل لولي الأمر والمشرفة

#### 4.1 إعداد البنية الأساسية

**تطبيق ولي الأمر (Parent App)**
- [ ] إنشاء مشروع React Native + Expo
- [ ] إعداد TypeScript
- [ ] إعداد Navigation (Expo Router)
- [ ] إعداد State Management (TanStack Query)
- [ ] إعداد API Client (Axios)
- [ ] إعداد Environment Variables

**تطبيق المشرفة (Supervisor App)**
- [ ] نفس الخطوات السابقة

#### 4.2 تطوير تطبيق ولي الأمر

**شاشات المصادقة**
- [ ] Splash Screen
- [ ] Login Screen
- [ ] Register Screen
- [ ] Forgot Password Screen
- [ ] ربط مع Backend API

**الشاشات الرئيسية**
- [ ] Home Screen (عرض قائمة الأبناء)
- [ ] Student Details Screen
- [ ] Create Pickup Request Screen
- [ ] Pickup Tracking Screen (مع خريطة)
- [ ] Authorized Persons Management (CRUD)
- [ ] Notifications Screen
- [ ] Profile & Settings Screen

**الميزات**
- [ ] Real-time Location Tracking
- [ ] Push Notifications
- [ ] Offline Support
- [ ] Biometric Authentication

#### 4.3 تطوير تطبيق المشرفة

**شاشات المصادقة**
- [ ] Splash Screen
- [ ] Login Screen

**الشاشات الرئيسية**
- [ ] Home Screen (عرض الطلبات المعلقة)
- [ ] Request Details Screen
- [ ] Map View (عرض موقع ولي الأمر)
- [ ] Students List Screen
- [ ] Profile & Statistics Screen

**الميزات**
- [ ] Real-time Location Sharing
- [ ] Push Notifications
- [ ] Offline Support

#### 4.4 نشر التطبيقات
- [ ] Build للإنتاج (iOS + Android)
- [ ] رفع على App Store
- [ ] رفع على Google Play
- [ ] TestFlight للاختبار

---

## 🟢 أولوية منخفضة (Low Priority)

### 5️⃣ الميزات المتقدمة والتحسينات

#### 5.1 Real-time Features
- [ ] إعداد WebSocket Server على Backend
- [ ] ربط Frontend لتحديثات فورية
- [ ] ربط Mobile Apps لتحديثات فورية
- [ ] تتبع موقع المشرفة Real-time
- [ ] تحديث حالة الطلب Real-time

#### 5.2 Notifications
- [ ] ربط مع خدمة SMS (Twilio أو مشابه)
- [ ] ربط مع خدمة Email (Mailgun أو مشابه)
- [ ] إعداد Firebase Cloud Messaging للموبايل
- [ ] إشعارات تلقائية عند تغيير حالة الطلب

#### 5.3 Documentation
- [ ] إضافة Swagger/OpenAPI Documentation للـ Backend
- [ ] كتابة دليل المستخدم للـ Dashboard
- [ ] كتابة دليل المستخدم للتطبيقات
- [ ] إنشاء فيديوهات تعليمية

#### 5.4 Testing
- [ ] **Backend:** Unit Tests (Jest)
- [ ] **Backend:** Integration Tests
- [ ] **Frontend:** Unit Tests (Vitest)
- [ ] **Frontend:** E2E Tests (Playwright)
- [ ] **Mobile:** Unit & E2E Tests

#### 5.5 Performance & Security
- [ ] **Performance:**
  - [ ] Database Indexing & Query Optimization
  - [ ] Caching (Redis)
  - [ ] CDN للملفات الثابتة
  - [ ] Code Splitting في Frontend
  - [ ] Lazy Loading للصور
- [ ] **Security:**
  - [ ] Two-Factor Authentication (2FA)
  - [ ] Password Reset via Email
  - [ ] Account Lockout بعد محاولات فاشلة
  - [ ] Rate Limiting على APIs
  - [ ] Security Audit

#### 5.6 Analytics & Monitoring
- [ ] إعداد Google Analytics أو مشابه
- [ ] إعداد Error Tracking (Sentry)
- [ ] إعداد Performance Monitoring
- [ ] Dashboard للإحصائيات المتقدمة

---

## 📝 ملاحظات مهمة

### للمطورين والوكلاء

1. **هذا الملف هو المرجع الوحيد لقائمة المهام**
   - لا تقم بإنشاء ملفات TODO جديدة
   - قم بتحديث هذا الملف فقط عند إكمال مهام أو إضافة مهام جديدة

2. **عند إكمال مهمة:**
   - ضع علامة ✅ بجانب المهمة: `- [x] المهمة المكتملة`
   - قم برفع التحديث على GitHub مع رسالة commit واضحة
   - حدّث ملف `WATHIQ_UNIFIED_DOCUMENTATION.md` إذا لزم الأمر

3. **الأولويات:**
   - ركز على المهام ذات الأولوية القصوى 🔴 أولاً
   - لا تبدأ مهام الأولوية المنخفضة قبل إكمال الأولويات الأعلى

4. **الاختبار:**
   - اختبر كل ميزة قبل الرفع على GitHub
   - تأكد من عدم كسر الميزات الموجودة

5. **التوثيق:**
   - وثّق أي تغييرات مهمة في ملف التوثيق الموحد
   - اكتب تعليقات واضحة في الكود

---

**آخر تحديث:** 2 يناير 2026  
**المطور الحالي:** AI Agent (Manus)  
**الحالة:** نشط ✅
