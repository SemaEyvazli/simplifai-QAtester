# BUG-003 — Səhifə mobil cihazlarda düzgün açılmır, bəzi düymələr və panellər görünmür

| Sahə | Dəyər |
| ---- | ----- |
| **Bug ID** | BUG-003 |
| **Layihə** | Smplifai website |
| **Modul** | Responsive dizayn (mobil və desktop-da eyni görünmə) |
| **Brauzer / OS** | Chrome Mobile / Android |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |
| **Əlaqəli test case** | `TC-UI-001` |

## Pre-conditions

- İstifadəçi mobil cihaz brauzerindən daxil olub.
- İstifadəçi Smplifai saytının əsas səhifəsindədir.

## Reproduksiya addımları

1. Mobil cihazda brauzeri açın.
2. Smplifai saytının səhifəsinə daxil olun.
3. Desktop versiyası ilə müqayisə edin.
4. Səhifədəki panellərə və idarəetmə düymələrinə (menyu, təsdiqləmə, keçid) diqqət edin.
5. Görünməyən panellərin yerləşdiyi hissələri yoxlayın.

## Faktiki nəticə

Səhifənin dizaynı mobil ekrana uyğunlaşmır. Mühüm panellər və düymələr ekrandan kənara çıxır və ya istifadəçi üçün tamamilə görünməz olur.

## Gözlənilən nəticə

Səhifənin bütün elementləri (düymələr, panellər, yazılar) mobil ekran ölçülərinə tam uyğunlaşmalı və istifadəçi hər düyməyə asanlıqla klikləyə bilməlidir.

## Əlavələr

- Mobile Screenshot
