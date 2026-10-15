# Test Cases – API (Swagger & Postman)

**Layihə:** Smplifai · **Modul:** Applications API  
**Base URL:** `https://smplifai-backend.vercel.app`

**Ümumi pre-condition:** İstifadəçi autentifikasiyadan keçib və aktiv Bearer Token-ə sahibdir (`TC-API-004` istisnadır).

---

## TC-API-001 — Yeni müraciətin yaradılması (POST)

| Sahə | Məlumat |
| ---- | ------- |
| **Endpoint** | `POST /api/applications` |
| **Prioritet** | Medium |
| **Status** | ✅ Pass |

**Addımlar**

1. Swagger UI və ya Postman-da `POST /api/applications` endpoint-ini seçin.
2. Headers bölməsinə Bearer Token əlavə edin.
3. "Execute" (və ya "Send") düyməsinə klikləyin.
4. Cavabın status kodunu və body-ni yoxlayın.

**Gözlənilən nəticə**

- Status: `201 Created`
- Body: yaradılmış obyekt, `status` = `DRAFT`:

```json
{
  "id": "f6c4373c-e6b9-4727-ab2e-73fac97f10e7",
  "user_id": "54efe78c-f0d3-4ee2-a318-2d1ad24941b9",
  "type": "My Passport",
  "email": null,
  "phone": null,
  "passport_data": null,
  "file_url": null,
  "status": "DRAFT",
  "created_at": "2026-09-09T16:04:44.747629+00:00",
  "updated_at": "2026-09-09T16:04:44.747629+00:00",
  "documents_uploaded": false,
  "reject_reason": null
}
```

---

## TC-API-002 — Müraciətlərin siyahısının çəkilməsi (GET)

| Sahə | Məlumat |
| ---- | ------- |
| **Endpoint** | `GET /api/applications` |
| **Prioritet** | Medium |
| **Status** | ✅ Pass |

**Addımlar**

1. Postman və ya Swagger UI-ı açın.
2. `GET /api/applications` endpoint-ini seçin.
3. Headers hissəsinə aktiv Bearer Token əlavə edin.
4. "Send" düyməsinə klikləyin.

**Gözlənilən nəticə**

- Status: `200 OK`
- Body: mövcud müraciətlərin siyahısı JSON formatında.

---

## TC-API-003 — Müraciətin silinməsi (DELETE)

| Sahə | Məlumat |
| ---- | ------- |
| **Endpoint** | `DELETE /api/applications/{id}` |
| **Prioritet** | High |
| **Pre-conditions** | Silinəcək müraciət sistemdə mövcuddur (məsələn, `TC-APP-001` ilə yaradılıb). |
| **Test data** | `id`: `72a38e24-5f54-43d5-82bc-d20bad97dd81` |
| **Status** | ✅ Pass |

**Addımlar**

1. Saytda "New Application" ilə müraciət yaradın (`TC-APP-001`).
2. Swagger API sənədinə (`Smplifai API Docs`) daxil olun.
3. "Authorize" düyməsinə klikləyin, Bearer token-i daxil edib təsdiqləyin.
4. `DELETE /api/applications/{id}` sorğusunu seçin.
5. `id` xanasına silinəcək müraciətin ID-sini daxil edin və "Execute" düyməsinə klikləyin.

**Gözlənilən nəticə**

- Status: `200 OK`
- Body: `"success": true`
- Yoxlama: `GET /api/applications/{id}` sorğusu `404 Not Found` qaytarır.

---

## TC-API-004 — Token olmadan silmə cəhdi (Security / Negative)

| Sahə | Məlumat |
| ---- | ------- |
| **Endpoint** | `DELETE /api/applications/{id}` |
| **Prioritet** | High |
| **Pre-conditions** | Bearer Token **daxil edilmir** (Authorize olunmayıb). |
| **Test data** | `DELETE https://smplifai-backend.vercel.app/api/applications/72a38e24-5f54-43d5-82bc-d20bad97dd81` |
| **Status** | ✅ Pass |

**Addımlar**

1. Authorize olmadan `DELETE /api/applications/{id}` sorğusunu icra edin.

**Gözlənilən nəticə**

- Status: `401 Unauthorized`
- Body:

```json
{
  "success": false,
  "message": "Unauthorized"
}
```

- Silinməyə cəhd edilən müraciət sistemdə toxunulmaz qalır.

---

## TC-API-005 — Yanlış ID ilə silmə (Negative)

| Sahə | Məlumat |
| ---- | ------- |
| **Endpoint** | `DELETE /api/applications/{id}` |
| **Prioritet** | High |
| **Pre-conditions** | İstifadəçi aktiv token-dən istifadə edir. |
| **Test data** | `id`: `99999` (mövcud olmayan ID) |
| **Status** | ✅ Pass |

**Addımlar**

1. Swagger UI-da `DELETE /api/applications/{id}` seçin.
2. `id` xanasına mövcud olmayan ID (`99999`) yazın.
3. "Execute" düyməsinə klikləyin.

**Gözlənilən nəticə**

- Status: `404 Not Found` və müvafiq xəta mesajı.
