# Test Cases – Authentication & User Management

**Layihə:** Smplifai · **Modul:** Authentication

> Test datada parol saxlanılmır. `<TEST_PASSWORD>` yerinə test hesabının parolunu daxil edin.

---

## TC-AUTH-001 — Düzgün məlumatlarla giriş (Log In)

| Sahə | Məlumat |
| ---- | ------- |
| **Prioritet** | High |
| **Pre-conditions** | Təsdiqlənmiş istifadəçi hesabı mövcuddur. |
| **Test data** | Email: `smaeyvazli@mail.ru` · Password: `<TEST_PASSWORD>` |
| **Status** | ✅ Pass |

**Addımlar**

1. [Smplifai giriş səhifəsini](https://appstudentsecret.smplifai.com/auth/login) açın.
2. Email sahəsinə test datadakı e-poçtu daxil edin.
3. Password sahəsinə test datadakı şifrəni daxil edin.
4. "Log In" ("Sign In") düyməsinə klikləyin.

**Gözlənilən nəticə**

- İstifadəçi uğurla daxil olur və Dashboard səhifəsinə yönləndirilir.
- Əsas paneldə istifadəçinin profil adı görünür.

**Negative variant:** yanlış e-poçt və ya səhv şifrə daxil edildikdə sistem xəta mesajı göstərməlidir və giriş baş verməməlidir.

---

## TC-AUTH-002 — Tələbə qeydiyyatı (Student Registration)

| Sahə | Məlumat |
| ---- | ------- |
| **Prioritet** | High |
| **Pre-conditions** | Test datadakı e-poçt sistemdə mövcud deyil. |
| **Test data** | First name: `Sema` · Last name: `Eyvazli` · Email: `smaeyvazli@mail.ru` · Phone: `+994552794665` · Password / Repeat password: `<TEST_PASSWORD>` |
| **Status** | ✅ Pass |

**Addımlar**

1. [Qeydiyyat səhifəsini](https://appstudentsecret.smplifai.com/auth/register) açın.
2. First name və Last name sahələrini doldurun.
3. Email və Phone sahələrini doldurun.
4. Password və Repeat password sahələrini doldurun.
5. "Terms of use" xanasını işarələyin.
6. "Create account" düyməsinə klikləyin.

**Gözlənilən nəticə**

- Hesab uğurla yaradılır.

---

## TC-AUTH-003 — Hesabdan çıxış (Logout)

| Sahə | Məlumat |
| ---- | ------- |
| **Prioritet** | Medium |
| **Pre-conditions** | İstifadəçi öz hesabına daxil olub. |
| **Test data** | — |
| **Status** | ✅ Pass |

**Addımlar**

1. Sol menyunun yuxarı hissəsindəki profil panelinə baxın.
2. "Logout" düyməsinə klikləyin.
3. "Sign out" düyməsinə klikləyin.

**Gözlənilən nəticə**

- Sol menyuda istifadəçinin adı və e-poçt ünvanı düzgün göstərilir.
- "Cancel" və "Sign out" düymələri görünür.
- İstifadəçi uğurla giriş səhifəsinə yönləndirilir.

---

## TC-AUTH-004 — Şifrə sıfırlama e-poçtunun göndərilməsi

| Sahə | Məlumat |
| ---- | ------- |
| **Prioritet** | High |
| **Pre-conditions** | İstifadəçinin aktiv hesabı var; istifadəçi şifrə sıfırlama səhifəsindədir. |
| **Test data** | Email: `smaeyvazli@mail.ru` |
| **Status** | ❌ Fail — [BUG-001](../03-Bug-Reports/BUG-001_Password-reset-email-not-sent.md) |

**Addımlar**

1. Smplifai saytını açın.
2. "Forgot password" düyməsinə klikləyin.
3. Qeydiyyatdan keçmiş valid e-poçt ünvanını daxil edin.
4. "Terms of Use" xanasını işarələyin.
5. "Reset password" düyməsinə klikləyin.
6. E-poçt qutusunu yoxlayın.

**Gözlənilən nəticə**

- Sistem şifrə sıfırlama e-poçtunu göndərir.
- "Şifrə sıfırlama linki e-poçtunuza göndərildi" mesajı göstərilir.

**Faktiki nəticə**

- Heç bir məktub və ya keçid linki gəlmir.
