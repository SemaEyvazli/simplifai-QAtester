# QA Checklist – Smplifai Platform

**Layihə:** Smplifai (Tələbə qeydiyyatı və sənəd avtomatlaşdırılması)  
**Müəllif:** Səmayə Heybətova  
**Əlamətlər:** ✅ Keçdi · ❌ Uğursuz (bug tapıldı)

---

## 1. Authentication & User Management

- ✅ Sign In səhifəsinin açılması və giriş elementlərinin (Email, Password, Login düyməsi) işləkliyi — `TC-AUTH-001`
- ✅ Düzgün məlumatlarla uğurlu giriş (Valid Login) — `TC-AUTH-001`
- ✅ Yanlış məlumat və ya səhv şifrə daxil edildikdə xəta mesajı (Negative Test) — `TC-AUTH-001`
- ✅ Yeni istifadəçi qeydiyyatı — `TC-AUTH-002`
- ✅ Hesabdan çıxış (Logout) — `TC-AUTH-003`
- ❌ Şifrə sıfırlama e-poçtunun göndərilməsi — `TC-AUTH-004` → [BUG-001](../03-Bug-Reports/BUG-001_Password-reset-email-not-sent.md)

## 2. Application Submission & File Upload ("My Application")

- ✅ "New Application" düyməsinin kliklənməsi və formanın açılması — `TC-APP-001`
- ✅ Məcburi sahələrin (Email, Phone) doldurulması və validasiya — `TC-APP-001`
- ✅ "Browse files" ilə sənədin seçilməsi və yüklənməsi — `TC-APP-001`
- ✅ "Next" düyməsi ilə müraciətin yaradılması və siyahıda görünməsi — `TC-APP-001`
- ✅ Müraciət statusunun düzgün əks olunması — `TC-APP-002`
- ❌ Profil şəklinin yenidən daxil olduqdan sonra qorunması — `TC-PROF-001` → [BUG-002](../03-Bug-Reports/BUG-002_Profile-photo-lost-after-relogin.md)

## 3. API Testing (Swagger & Postman)

- ✅ Bearer Token ilə Swagger UI / Postman-da avtorizasiya — `TC-API-001` … `TC-API-005`
- ✅ `POST /api/applications` ilə yeni müraciətin yaradılması (201 Created) — `TC-API-001`
- ✅ `GET /api/applications` ilə siyahının çəkilməsi (200 OK) — `TC-API-002`
- ✅ `DELETE /api/applications/{id}` ilə müraciətin silinməsi (200 OK) — `TC-API-003`
- ✅ Token olmadan DELETE → `401 Unauthorized` — `TC-API-004`
- ✅ Yanlış/saxta ID ilə DELETE → `404 Not Found` — `TC-API-005`

## 4. UI / UX & Responsiveness

- ✅ Google Chrome (desktop) brauzerində elementlərin düzgün hizalanması — `TC-UI-001`
- ❌ Mobil brauzerdə düymə, forma və panellərin görünməsi — `TC-UI-001` → [BUG-003](../03-Bug-Reports/BUG-003_Mobile-layout-broken.md)
