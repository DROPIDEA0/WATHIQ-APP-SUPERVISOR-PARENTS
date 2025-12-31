# WATHIQ-APP-SUPERVISOR

<div align="center">
  <img src="./assets/wathiq_logo.png" alt="WATHIQ Logo" width="300"/>
  
  <h3>نظام إدارة انصراف الطلاب الآمن</h3>
  <p>تطبيق المشرفة + تطبيق ولي الأمر (React Native)</p>

  [![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
  [![React Native](https://img.shields.io/badge/React%20Native-0.81-61DAFB?logo=react)](https://reactnative.dev/)
  [![Expo](https://img.shields.io/badge/Expo-54-000020?logo=expo)](https://expo.dev/)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=typescript)](https://www.typescriptlang.org/)
</div>

---

## 📋 نظرة عامة

**WATHIQ-APP-SUPERVISOR** هو الجزء الخاص بتطبيقات الموبايل من نظام **WATHIQ** المتكامل. يتضمن هذا المستودع تطبيقين رئيسيين مبنيين بتقنية React Native مع Expo، يعملان معاً لتوفير تجربة سلسة وآمنة لعملية انصراف الطلاب.

### التطبيقات المتضمنة

**1. تطبيق ولي الأمر (Parent App)**
تطبيق موبايل يتيح لأولياء الأمور طلب استلام أبنائهم من المدرسة، تتبع موقعهم، وإدارة الأشخاص المفوضين بالاستلام.

**2. تطبيق المشرفة (Supervisor App)**
تطبيق موبايل للمشرفات في المدرسة لمعالجة طلبات الاستلام، التحقق من هوية أولياء الأمور، وإدارة عملية التسليم بشكل آمن.

---

## ✨ الميزات الرئيسية

### تطبيق ولي الأمر
- **شاشة ترحيبية تفاعلية:** تعريف المستخدم الجديد بالنظام
- **تسجيل دخول آمن:** مصادقة ثنائية العامل (اختياري)
- **قائمة الأبناء:** عرض جميع الأبناء مع حالاتهم الحالية
- **طلب استلام سهل:** اختيار الطالب والبوابة بضغطة زر
- **تتبع فوري:** متابعة موقع الطالب حتى وصوله
- **إدارة المفوضين:** إضافة وإدارة الأشخاص المصرح لهم بالاستلام
- **سجل كامل:** عرض جميع عمليات الاستلام السابقة
- **إشعارات فورية:** تنبيهات عند تغيير حالة الطلب
- **الوضع الليلي:** دعم Dark Mode

### تطبيق المشرفة
- **لوحة طلبات ديناميكية:** عرض جميع الطلبات الواردة مع الأولوية
- **تفاصيل شاملة:** معلومات الطالب، ولي الأمر، والموقع الجغرافي
- **خريطة تفاعلية:** عرض موقع ولي الأمر في الوقت الفعلي
- **تحديث الحالة:** تأكيد إرسال الطالب بضغطة زر
- **نظام تنبيهات ذكي:** تنبيه صوتي ومرئي بعد 5 دقائق من عدم التأكيد
- **اتصال طارئ:** زر سريع للاتصال بولي الأمر
- **سجل يومي:** عرض جميع العمليات التي قامت بها المشرفة
- **إحصائيات سريعة:** متوسط الوقت، عدد العمليات، الأداء

---

## 🛠️ التقنيات المستخدمة

### Core
- **React Native 0.81** - إطار عمل لبناء تطبيقات موبايل
- **Expo SDK 54** - منصة لتطوير ونشر تطبيقات React Native
- **TypeScript 5.9** - لغة برمجة قوية مبنية على JavaScript
- **React 19.1.0** - مكتبة JavaScript لبناء واجهات المستخدم

### UI & Styling
- **NativeWind 4** - Tailwind CSS for React Native
- **React Native Reanimated 4** - مكتبة الرسوم المتحركة
- **Expo Symbols** - أيقونات SF Symbols (iOS) و Material Icons (Android)

### Navigation
- **Expo Router 6** - نظام التنقل المبني على File-based routing

### State Management
- **TanStack Query 5.90** - إدارة حالة البيانات والـ API
- **React Context** - لإدارة الحالة المحلية

### Native Features
- **Expo Location** - تتبع الموقع الجغرافي
- **Expo Notifications** - الإشعارات الفورية (Push Notifications)
- **Expo Haptics** - ردود الفعل اللمسية
- **Expo Audio** - تشغيل الأصوات
- **Expo Secure Store** - تخزين آمن للبيانات الحساسة

### Backend Integration
- **Axios** - HTTP client للتواصل مع الـ API
- **tRPC** - End-to-end typesafe APIs
- **WebSockets** - للتحديثات الفورية
- **Zod** - التحقق من صحة البيانات

---

## 📦 التثبيت والإعداد

### المتطلبات الأساسية
- Node.js v18 أو أحدث
- npm أو yarn أو pnpm
- Expo CLI (`npm install -g expo-cli`)
- **للتطوير على iOS:** macOS + Xcode
- **للتطوير على Android:** Android Studio + Android SDK

### 1. استنساخ المستودع
```bash
git clone https://github.com/DROPIDEA0/WATHIQ-APP-SUPERVISOR.git
cd WATHIQ-APP-SUPERVISOR
```

### 2. تثبيت الحزم
```bash
npm install
# أو
yarn install
# أو
pnpm install
```

### 3. إعداد متغيرات البيئة
أنشئ ملف `.env` في الجذر وأضف المتغيرات التالية:

```env
# API Configuration
EXPO_PUBLIC_API_URL=https://api.wathiq.com
EXPO_PUBLIC_WS_URL=wss://api.wathiq.com

# App Configuration
EXPO_PUBLIC_APP_NAME=Wathiq
EXPO_PUBLIC_APP_VERSION=1.0.0

# Google Maps (للخرائط على Android)
EXPO_PUBLIC_GOOGLE_MAPS_API_KEY=your-google-maps-api-key

# OneSignal (للإشعارات)
EXPO_PUBLIC_ONESIGNAL_APP_ID=your-onesignal-app-id

# Sentry (اختياري - لتتبع الأخطاء)
SENTRY_DSN=your-sentry-dsn
```

### 4. تشغيل التطبيق

#### وضع التطوير
```bash
# تشغيل Expo Dev Server
npm start

# أو تشغيل مباشرة على المنصة
npm run android  # Android
npm run ios      # iOS
npm run web      # Web (للاختبار فقط)
```

#### بناء التطبيق للإنتاج
```bash
# بناء APK لـ Android
eas build --platform android

# بناء IPA لـ iOS
eas build --platform ios

# بناء للمنصتين معاً
eas build --platform all
```

---

## 📁 هيكل المشروع

```
WATHIQ-APP-SUPERVISOR/
├── app/                    # Expo Router (File-based routing)
│   ├── (tabs)/             # Tab Navigation
│   │   ├── index.tsx       # الشاشة الرئيسية (قائمة الأبناء)
│   │   ├── history.tsx     # شاشة السجل
│   │   └── profile.tsx     # شاشة الملف الشخصي
│   ├── onboarding.tsx      # شاشة الترحيب
│   ├── login.tsx           # شاشة تسجيل الدخول
│   ├── pickup-request.tsx  # شاشة طلب الاستلام
│   ├── tracking.tsx        # شاشة التتبع
│   └── _layout.tsx         # Root Layout
│
├── components/             # المكونات المشتركة
│   ├── screen-container.tsx  # SafeArea wrapper
│   ├── themed-view.tsx       # View مع دعم الثيم
│   └── ui/                   # مكونات UI
│       ├── button.tsx
│       ├── card.tsx
│       ├── icon-symbol.tsx
│       └── ...
│
├── hooks/                  # Custom React Hooks
│   ├── use-auth.ts         # المصادقة
│   ├── use-colors.ts       # الألوان والثيم
│   ├── use-location.ts     # الموقع الجغرافي
│   └── ...
│
├── lib/                    # المكتبات والأدوات
│   ├── trpc.ts             # tRPC client
│   ├── utils.ts            # Utility functions
│   └── theme-provider.tsx  # Theme context
│
├── constants/              # الثوابت
│   └── theme.ts            # ألوان الثيم
│
├── assets/                 # الأصول (الصور، الأيقونات)
│   └── images/
│       ├── icon.png        # أيقونة التطبيق
│       ├── splash-icon.png # Splash screen
│       └── ...
│
├── types/                  # TypeScript Types
├── server/                 # Backend (مشترك مع WATHIQ-WEB)
├── app.config.ts           # Expo configuration
├── package.json
├── tsconfig.json
├── tailwind.config.js
├── theme.config.js
└── README.md
```

---

## 🎨 التصميم والثيم

### الألوان الأساسية

| اللون | Light Mode | Dark Mode | الاستخدام |
|:------|:-----------|:----------|:----------|
| Primary | `#2563EB` | `#2563EB` | الأزرار الرئيسية، الروابط |
| Accent | `#F97316` | `#F97316` | التأكيدات، التنبيهات المهمة |
| Background | `#FFFFFF` | `#151718` | خلفية الشاشات |
| Surface | `#F5F5F5` | `#1E2022` | الكروت، العناصر المرتفعة |
| Foreground | `#11181C` | `#ECEDEE` | النصوص الرئيسية |
| Muted | `#687076` | `#9BA1A6` | النصوص الثانوية |
| Success | `#22C55E` | `#4ADE80` | حالات النجاح |
| Warning | `#F59E0B` | `#FBBF24` | التحذيرات |
| Error | `#EF4444` | `#F87171` | الأخطاء |

### استخدام NativeWind

```tsx
import { View, Text } from "react-native";

export function MyComponent() {
  return (
    <View className="flex-1 items-center justify-center p-4">
      <Text className="text-2xl font-bold text-foreground">
        مرحباً بك في واثق
      </Text>
      <Text className="mt-2 text-muted">
        نظام آمن لإدارة انصراف الطلاب
      </Text>
    </View>
  );
}
```

---

## 🔐 المصادقة

### تدفق المصادقة

1. المستخدم يدخل رقم الهاتف/البريد الإلكتروني وكلمة المرور
2. يتم إرسال الطلب إلى الـ API
3. عند النجاح، يتم حفظ JWT Token في Secure Store
4. يتم إعادة توجيه المستخدم إلى الشاشة الرئيسية
5. يتم تضمين Token في جميع الطلبات اللاحقة

### استخدام Hook المصادقة

```tsx
import { useAuth } from "@/hooks/use-auth";

export function MyScreen() {
  const { user, login, logout, isLoading } = useAuth();

  const handleLogin = async () => {
    try {
      await login("user@example.com", "password123");
    } catch (error) {
      console.error("Login failed:", error);
    }
  };

  if (isLoading) return <LoadingScreen />;
  if (!user) return <LoginScreen onLogin={handleLogin} />;

  return <HomeScreen user={user} onLogout={logout} />;
}
```

---

## 📍 تتبع الموقع الجغرافي

### طلب الأذونات

```tsx
import * as Location from "expo-location";

const requestLocationPermission = async () => {
  const { status } = await Location.requestForegroundPermissionsAsync();
  if (status !== "granted") {
    alert("نحتاج إلى إذن الموقع لتفعيل هذه الميزة");
    return false;
  }
  return true;
};
```

### الحصول على الموقع الحالي

```tsx
const getCurrentLocation = async () => {
  const location = await Location.getCurrentPositionAsync({
    accuracy: Location.Accuracy.High,
  });
  return {
    latitude: location.coords.latitude,
    longitude: location.coords.longitude,
  };
};
```

### تتبع الموقع في الوقت الفعلي

```tsx
const watchLocation = async (callback) => {
  return await Location.watchPositionAsync(
    {
      accuracy: Location.Accuracy.High,
      timeInterval: 5000,  // كل 5 ثوانٍ
      distanceInterval: 10, // أو كل 10 أمتار
    },
    callback
  );
};
```

---

## 🔔 الإشعارات الفورية

### إعداد الإشعارات

```tsx
import * as Notifications from "expo-notifications";

// تكوين كيفية عرض الإشعارات
Notifications.setNotificationHandler({
  handleNotification: async () => ({
    shouldShowAlert: true,
    shouldPlaySound: true,
    shouldSetBadge: true,
  }),
});

// طلب الأذونات
const requestNotificationPermission = async () => {
  const { status } = await Notifications.requestPermissionsAsync();
  if (status !== "granted") {
    alert("نحتاج إلى إذن الإشعارات لإبقائك على اطلاع");
    return false;
  }
  return true;
};
```

### إرسال إشعار محلي

```tsx
const sendLocalNotification = async (title, body) => {
  await Notifications.scheduleNotificationAsync({
    content: {
      title,
      body,
      sound: true,
    },
    trigger: null, // فوري
  });
};
```

---

## 🧪 الاختبارات

```bash
# تشغيل جميع الاختبارات
npm test

# تشغيل الاختبارات مع التغطية
npm run test:coverage

# تشغيل الاختبارات في وضع المراقبة
npm run test:watch
```

---

## 🚀 النشر

### إعداد EAS (Expo Application Services)

```bash
# تسجيل الدخول
eas login

# تكوين المشروع
eas build:configure
```

### بناء للإنتاج

```bash
# Android (APK)
eas build --platform android --profile production

# iOS (IPA)
eas build --platform ios --profile production

# رفع على المتاجر
eas submit --platform android
eas submit --platform ios
```

### Over-The-Air (OTA) Updates

```bash
# نشر تحديث فوري بدون إعادة بناء
eas update --branch production --message "إصلاح أخطاء بسيطة"
```

---

## 📱 الاختبار على الأجهزة

### Expo Go (للتطوير)

1. ثبت تطبيق **Expo Go** من App Store أو Google Play
2. شغل `npm start` على الكمبيوتر
3. امسح QR Code بكاميرا الهاتف (iOS) أو تطبيق Expo Go (Android)

### Development Build (للميزات Native)

```bash
# بناء نسخة تطوير
eas build --profile development --platform android
eas build --profile development --platform ios

# تثبيت على الجهاز وتشغيل
npx expo start --dev-client
```

---

## 🔧 استكشاف الأخطاء

### مشكلة: التطبيق لا يعمل على iOS
**الحل:**
```bash
cd ios
pod install
cd ..
npm run ios
```

### مشكلة: الخرائط لا تظهر على Android
**الحل:** تأكد من إضافة Google Maps API Key في `app.config.ts`:
```ts
android: {
  config: {
    googleMaps: {
      apiKey: process.env.EXPO_PUBLIC_GOOGLE_MAPS_API_KEY,
    },
  },
}
```

### مشكلة: الإشعارات لا تعمل
**الحل:**
1. تأكد من طلب الأذونات
2. تحقق من تكوين OneSignal
3. اختبر على جهاز حقيقي (لا تعمل على المحاكي)

---

## 📝 المساهمة

نرحب بجميع المساهمات! يرجى اتباع الخطوات التالية:

1. Fork المستودع
2. إنشاء فرع جديد (`git checkout -b feature/amazing-feature`)
3. Commit التغييرات (`git commit -m 'Add amazing feature'`)
4. Push إلى الفرع (`git push origin feature/amazing-feature`)
5. فتح Pull Request

---

## 📄 الترخيص

هذا المشروع مرخص تحت **MIT License**. راجع ملف [LICENSE](LICENSE) للمزيد من التفاصيل.

---

## 📞 التواصل

- **GitHub:** [DROPIDEA0](https://github.com/DROPIDEA0)
- **Email:** support@wathiq.com
- **Website:** https://wathiq.com

---

## 🙏 شكر وتقدير

- **Expo Team** - لمنصة رائعة لتطوير تطبيقات React Native
- **React Native Community** - للدعم المستمر
- **NativeWind** - لجعل Tailwind CSS يعمل على React Native
- **المجتمع المفتوح المصدر** - للمساهمات القيمة

---

<div align="center">
  <p>صُنع بـ ❤️ من أجل مدارس أكثر أماناً</p>
  <p>© 2025 WATHIQ. جميع الحقوق محفوظة.</p>
</div>
