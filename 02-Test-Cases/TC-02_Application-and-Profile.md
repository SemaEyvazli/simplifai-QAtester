# Test Cases – Application Lifecycle & Profile

**Layihə:** Smplifai · **Modul:** My Application, Profile

---

## TC-APP-001 — Yeni müraciətin yaradılması və sənəd yüklənməsi

| Sahə | Məlumat |
| ---- | ------- |
| **Prioritet** | High |
| **Pre-conditions** | İstifadəçi sistemə daxil olub. |
| **Test data** | Email və Phone üçün valid məlumatlar; yükləmək üçün sənəd faylı. |
| **Status** | ✅ Pass |

**Addımlar**

1. "New Application" düyməsinə klikləyin.
2. Email və Phone sahələrini doldurun.
3. "Choose" düyməsinə, ardından "Browse files" düyməsinə klikləyib faylı seçin.
4. "Next" düyməsinə klikləyin.

**Gözlənilən nəticə**

- "Document successfully uploaded" bildirişi görünür və müraciət yaradılır.
- Müraciət siyahıda yeni qeyd kimi görünür.

---

## TC-APP-002 — Müraciət statusunun əks olunması (Completeness Tracking)

| Sahə | Məlumat |
| ---- | ------- |
| **Prioritet** | Medium |
| **Pre-conditions** | İstifadəçi profilə daxil olub; göndərilmiş müraciətlər mövcuddur. |
| **Test data** | — |
| **Status** | ✅ Pass |

**Addımlar**

1. [Smplifai](https://appstudentsecret.smplifai.com/) saytına daxil olun.
2. Dashboard bölməsinə keçin.
3. Siyahıdakı müraciətlərin statusuna baxın.

**Gözlənilən nəticə**

- Müraciətin adı və tarixi düzgün görünür.
- Sistem tərəfindən qəbul edilmiş "Document Submitted" statusu gözləmədə olan işlər üçün "Pending Review" kimi əks olunur.

---

## TC-PROF-001 — Profil şəklinin yenidən daxil olduqdan sonra qorunması

| Sahə | Məlumat |
| ---- | ------- |
| **Prioritet** | Medium |
| **Pre-conditions** | İstifadəçi öz hesabına daxil olub. |
| **Test data** | JPG formatında profil şəkli. |
| **Status** | ❌ Fail — [BUG-002](../03-Bug-Reports/BUG-002_Profile-photo-lost-after-relogin.md) |

**Addımlar**

1. Smplifai saytını açın və hesaba daxil olun.
2. "Profile Settings" bölməsinə keçin.
3. Yeni profil şəklini JPG formatında yükləyin.
4. "Save changes" düyməsinə klikləyin.
5. Hesabdan çıxış (Log out) edin.
6. Yenidən daxil olun və profil səhifəsinə keçin.

**Gözlənilən nəticə**

- Yüklənmiş profil şəkli yenidən daxil olduqda görünür.

**Faktiki nəticə**

- Şəkil silinir, yerində standart boş profil ikonu görünür.
