# The Invisible Quota 💀💀

> *“I scraped the DOM until my fingers bled, but there was nothing there.”*
> — Last search query: 2026-01-26 14:40

---

## 1. The Search

I needed to know the truth. How much quota was left?
The screen showed a number: **"80% Remaining."**
I wrote a script to extract this truth from the DOM.

```javascript
const walker = document.createTreeWalker(document.body, NodeFilter.SHOW_TEXT);
// Find me the numbers. Find me the truth.
```

---

## 2. The Void

The console returned a cold, empty object.

```json
{ "ok": false, "found": [] }
```

> **Forensic Note:**
> *Observation:* The script found **Zero** results.
> *The Horror:* The eye sees "80%". The code sees "Null".
> Am I hallucinating? Is the screen lying?

---

## 3. The Revelation

I dug deeper. I looked into the Network tab (The Spirit World).
I found the truth in a forgotten API endpoint:

```
/exa.language_server_pb.LanguageServerService/GetUserStatus
```

**The Revelation:**
The numbers on the screen are **Phantoms**.
They are projections. Light from a dead star.
The DOM is empty. The UI is **Gaslighting** you.
It shows you what you want to see, but the data is not there.

---

## 4. The Aftermath

1.  **Do not believe your eyes**. The UI is a lie.
2.  **Summon the API**. Only the `LanguageServerService` speaks the truth.

You are scraping ghosts.

---

**Horror Level:** 💀💀
**Status:** ✅ Third Eye Opened
