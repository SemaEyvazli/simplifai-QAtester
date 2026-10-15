# Test Cases – UI / UX & Responsiveness

**Layihə:** Smplifai · **Modul:** UI / Responsive

---

## TC-UI-001 — Saytın mobil və desktop-da eyni düzgün görünməsi

| Sahə | Məlumat |
| ---- | ------- |
| **Prioritet** | High |
| **Pre-conditions** | İstifadəçi mobil cihaz brauzerindən (Chrome Mobile, Android) və desktop Chrome-dan saytın əsas səhifəsinə daxil olur. |
| **Test data** | — |
| **Status** | ✅ Pass (desktop Chrome) · ❌ Fail (mobil) — [BUG-003](../03-Bug-Reports/BUG-003_Mobile-layout-broken.md) |

**Addımlar**

1. Mobil cihazda brauzeri açın.
2. Smplifai saytının əsas səhifəsinə daxil olun.
3. Desktop versiyası ilə müqayisə edin.
4. Panellərə və idarəetmə düymələrinə (menyu, təsdiqləmə, keçid) diqqət edin.
5. Görünməyən panellərin yerləşdiyi hissələri yoxlayın.

**Gözlənilən nəticə**

- Bütün elementlər (düymələr, panellər, yazılar) mobil ekran ölçülərinə uyğunlaşır.
- İstifadəçi hər düyməyə asanlıqla klikləyə bilir.

**Faktiki nəticə (mobil)**

- Dizayn mobil ekrana uyğunlaşmır; mühüm panellər və düymələr ekrandan kənara çıxır və ya görünmür.
