# The Invisible Quota 💀💀

> *"I scraped every inch of the DOM's skin. There was nothing inside..."*
> — Final Query Selector: 2026-01-26 14:40

---

## 1. The Search

I needed the truth. I needed to know how much life (quota) I had left.
The screen displayed: **"80% remaining."**
I wrote a script to extract this truth.

```javascript
const walker = document.createTreeWalker(document.body, NodeFilter.SHOW_TEXT);
// Find that number. Tell me the truth.
```

I pressed execute, expecting data to pour in.

---

## 2. The Void

The console returned a cold, empty object.

```json
{ "ok": false, "found": [] }
```

> **The Architect's Note:**
> *Observed fact:* The script returned **zero** results.
> *The horror:* Eyes see "80%." Code sees "nothing."
> Am I dreaming? Or is the screen lying to me?

---

## 3. The Revelation

I stopped searching like a headless fly. I began to stare into the darkness (Network Tab).
Deep within that pile of cryptic code, I found the truth:

```
/exa.language_server_pb.LanguageServerService/GetUserStatus
```

**The Revelation:**
The numbers on the screen were **phantoms**.
Projections from the API, refracted through the rendering layer, displayed on your retina.
The DOM is empty. The UI has been **gaslighting** you.
It shows you what you want to see, but there's actually nothing there.

---

## 4. The Survivor's Scar

1. **Don't trust your eyes.** The UI is a lying fairy.
2. **Summon the API.** Only `LanguageServerService` speaks the truth.

What you're scraping is merely the afterimage of a ghost.

---

**Terror Level:** 💀💀
**Status:** ✅ Third Eye Opened


---

> *They love to hear ghosts chant poetry by autumn graves.*
