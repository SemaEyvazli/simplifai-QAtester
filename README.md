# Smplifai – QA Test Package

**Layihə:** Smplifai (Tələbə qeydiyyatı və sənəd avtomatlaşdırılması)  
**Müəllif:** Səmayə Heybətova  
**Mənbə:** https://github.com/SemaEyvazli/QA-test-simplifai

## Struktur

```
Smplifai-QA/
├── README.md
├── 01-Checklist/
│   └── Smplifai_QA-Checklist.md
├── 02-Test-Cases/
│   ├── TC-01_Authentication.md          (TC-AUTH-001 … 004)
│   ├── TC-02_Application-and-Profile.md (TC-APP-001, 002 · TC-PROF-001)
│   ├── TC-03_API.md                     (TC-API-001 … 005)
│   └── TC-04_UI-Responsive.md           (TC-UI-001)
├── 03-Bug-Reports/
│   ├── BUG-001_Password-reset-email-not-sent.md
│   ├── BUG-002_Profile-photo-lost-after-relogin.md
│   └── BUG-003_Mobile-layout-broken.md
└── 04-Test-Summary-Report/
    └── Test-Summary-Report.md
```

## Nəticə qısaca

13 test case · 10 Pass · 3 Fail · 3 bug (2 High, 1 Medium) · Status: Conditional Approval

## ID qaydası

| Prefiks | Mənası |
| ------- | ------ |
| `TC-AUTH` | Authentication |
| `TC-APP` | Application lifecycle |
| `TC-PROF` | Profil |
| `TC-API` | API testləri |
| `TC-UI` | UI / Responsive |
| `BUG-xxx` | Bug report (əlaqəli test case hər faylın başında yazılıb) |

## Köhnə fayllar → yeni yer

| Köhnə fayl | Yeni yer |
| ---------- | -------- |
| `Checklist.md` | `01-Checklist/` |
| `test-cases.md` + `testcase.md` + `smplifai-application-testcase.md` + `application-delete-TC.md` | `02-Test-Cases/` (təkrarlar birləşdirilib, vahid ID ilə) |
| `bugreport.md` | `03-Bug-Reports/` (hər bug ayrıca fayl) |
| `Test-Summary-Report.md` | `04-Test-Summary-Report/` |
| `README.md` ("test") | Bu fayl |

> Təhlükəsizlik: parollar və giriş token-ləri paketə daxil edilməyib.
