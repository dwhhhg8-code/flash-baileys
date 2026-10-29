# ⚡ 𝕗𝕝𝕒𝕤𝕙 𝔹𝕠𝕥-𝕄𝔻 — flash-baileys

مكتبة واتساب (فورك من Baileys) بتعديلات المطوّر **𝖍𝖆𝖎𝖙𝖍𝖆𝖒**.
📢 القناة: https://whatsapp.com/channel/0029Vb8QIpSJ3juu0VHRyU0v

## التثبيت
```bash
npm i
```
أو من GitHub بتاعك:
```json
"flash-baileys": "github:USERNAME/REPO"
```

## الاستخدام
```js
const { makeWASocket, useMultiFileAuthState } = require('flash-baileys')
const { state, saveCreds } = await useMultiFileAuthState('session')
const sock = makeWASocket({ auth: state })
sock.ev.on('creds.update', saveCreds)
```

## أزرار وقوايم
```js
await sock.sendMessage(jid, {
  text: 'اختار',
  footer: 'flash',
  interactiveButtons: [
    { name: 'quick_reply', buttonParamsJson: JSON.stringify({ display_text: 'أمر', id: '.menu' }) }
  ]
})
```

## خيارات إضافية
- `FLASH_BAILEYS_QUIET=1` يخفي البانر عند التشغيل.
- المكتبة بتتابع قناة 𝕗𝕝𝕒𝕤𝕙 𝔹𝕠𝕥-𝕄𝔻 تلقائيًا بعد الاتصال (افتراضي). للتعطيل: `autoFollowNewsletter: false`، ولمتابعة قناة تانية: `autoFollowNewsletter: '1203...@newsletter'`.

## الحقوق
MIT. الأساس: Baileys الأصلي، والتعديلات: 𝖍𝖆𝖎𝖙𝖍𝖆𝖒. شوف `LICENSE`.
