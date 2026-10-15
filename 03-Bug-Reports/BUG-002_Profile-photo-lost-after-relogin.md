# BUG-002 — Profil şəkli yenidən daxil olduqda silinir

| Sahə | Dəyər |
| ---- | ----- |
| **Bug ID** | BUG-002 |
| **Layihə** | Smplifai |
| **Modul** | Profil |
| **Brauzer / OS** | Chrome / Windows 11 |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | Open |
| **Əlaqəli test case** | `TC-PROF-001` |

## Pre-conditions

1. İstifadəçi öz hesabına daxil olub.

## Reproduksiya addımları

1. Smplifai saytını açın və hesaba daxil olun.
2. "Profile Settings" bölməsinə keçin.
3. Yeni profil şəklini JPG formatında yükləyin.
4. "Save changes" düyməsinə klikləyin.
5. Hesabdan çıxış (Log out) edin.
6. Yenidən daxil olun və profil səhifəsinə keçin.

## Faktiki nəticə

Yüklənmiş profil şəkli silinir və yerində sistemin standart boş profil ikonu görünür.

## Gözlənilən nəticə

Yüklənmiş profil şəkli yenidən daxil olduqda istifadəçiyə görünməlidir.

## Əlavələr

- Screenshot
