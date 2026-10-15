# Test Execution & Summary Report

**Layihə:** Smplifai  
**Modullar:** User Management, Application Submission, API Integration, UI/Responsive  
**Test edən:** Səmayə Heybətova  
**Test dövrü:** Oktyabr 2026  
**Mühit:** Windows 11 / Chrome / Chrome Mobile (Android) / Postman / Swagger

---

## 1. Ümumi nəticə

| Göstərici | Say |
| --------- | --- |
| **Cəmi test case** | 13 |
| **Passed** | 10 |
| **Failed** | 3 |
| **Blocked** | 0 |
| **Pass rate** | 77 % (10 / 13) |
| **Tapılan bug** | 3 |

## 2. Bug-ların severity üzrə bölgüsü

| Severity | Say | Bug ID |
| -------- | --- | ------ |
| **Critical** | 0 | — |
| **High** | 2 | BUG-001, BUG-003 |
| **Medium** | 1 | BUG-002 |
| **Low** | 0 | — |

## 3. Test case nəticələri

| Test Case | Başlıq | Modul | Status | Bug |
| --------- | ------ | ----- | ------ | --- |
| TC-AUTH-001 | Düzgün məlumatlarla giriş | Authentication | ✅ Pass | — |
| TC-AUTH-002 | Tələbə qeydiyyatı | Authentication | ✅ Pass | — |
| TC-AUTH-003 | Hesabdan çıxış | Authentication | ✅ Pass | — |
| TC-AUTH-004 | Şifrə sıfırlama e-poçtu | Authentication | ❌ Fail | BUG-001 |
| TC-APP-001 | Yeni müraciət və sənəd yüklənməsi | Application | ✅ Pass | — |
| TC-APP-002 | Müraciət statusunun əks olunması | Application | ✅ Pass | — |
| TC-PROF-001 | Profil şəklinin qorunması | Profile | ❌ Fail | BUG-002 |
| TC-API-001 | POST /api/applications | API | ✅ Pass | — |
| TC-API-002 | GET /api/applications | API | ✅ Pass | — |
| TC-API-003 | DELETE – düzgün | API | ✅ Pass | — |
| TC-API-004 | DELETE – token olmadan (401) | API | ✅ Pass | — |
| TC-API-005 | DELETE – yanlış ID (404) | API | ✅ Pass | — |
| TC-UI-001 | Mobil/desktop responsive | UI | ❌ Fail (mobil) | BUG-003 |

> `TC-UI-001` desktop Chrome-da keçir, mobildə uğursuz olur; ümumi nəticə **Fail** sayılıb.

## 4. Əsas problemlər

1. **BUG-001 (High):** Şifrə sıfırlama e-poçtu istifadəçiyə çatmır.
2. **BUG-003 (High):** Mobil cihazlarda düymələr və panellər düzgün görünmür.
3. **BUG-002 (Medium):** Profil şəkli yenidən daxil olduqda silinir.

## 5. Yekun QA statusu

- **Status:** Conditional Approval (yenidən test tələb olunur)
- **Tövsiyə:** High severity xətalar düzəldildikdən sonra təkrar regression test icra edilməlidir.
