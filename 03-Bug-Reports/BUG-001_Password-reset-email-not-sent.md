# BUG-001 — Şifrə sıfırlama e-poçtu istifadəçiyə çatmır

| Sahə | Dəyər |
| ---- | ----- |
| **Bug ID** | BUG-001 |
| **Layihə** | Smplifai website |
| **Modul** | Password Reset |
| **Brauzer / OS** | Chrome / Windows 11 |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |
| **Əlaqəli test case** | `TC-AUTH-004` |

## Pre-conditions

1. İstifadəçinin aktiv hesabı var.
2. İstifadəçi şifrə sıfırlama səhifəsindədir.

## Reproduksiya addımları

1. Smplifai saytını açın.
2. "Forgot password" düyməsinə klikləyin.
3. Qeydiyyatdan keçdiyiniz valid e-poçt ünvanını (`smaeyvazli@mail.ru`) daxil edin.
4. "Terms of Use" xanasını işarələyin.
5. "Reset password" düyməsinə klikləyin.
6. Həmin e-poçt qutusunu yoxlayın.

## Faktiki nəticə

Sistem e-poçt ünvanına şifrə sıfırlama ilə bağlı heç bir məktub və ya keçid linki göndərmir.

## Gözlənilən nəticə

Sistem şifrə sıfırlama e-poçtunu göndərməli və "Şifrə sıfırlama linki e-poçtunuza göndərildi" mesajı göstərməlidir.

## Əlavələr

- Screenshot
- Video recording
