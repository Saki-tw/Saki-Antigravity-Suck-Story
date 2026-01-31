---
layout: default
title: "The Invisible Quota 💀💀"
---
# The Invisible Quota 💀💀

> *"Have you ever wondered where those quota numbers come from?"*
> *"...I don't dare to ask."*
> — Last Query: 2026-01-26 14:40

---

## Prologue: The Lie That Started It All

This story begins with a lie.

Some developer who built a quota monitoring extension wrote this in their README:

> *"There's an invisible UI element in Antigravity that displays quota information.*
> *Our extension captures this hidden UI to show you the quota."*

Shadow DOM? Hidden elements? The romance of technical hacking. Sounds like Institute-level tech.

**I believed it.**

I thought: if they could do it, so could I.
So I started building my own implementation.

---

## Act I: Hunting the Phantom

I wrote a DOM search script.

```javascript
const walker = document.createTreeWalker(document.body, NodeFilter.SHOW_TEXT);
// Search for all elements containing quota, usage, remaining...
// Find that hidden UI. Prove it exists.
```

Shadow DOM penetration, MutationObserver listeners, every corner where secrets might hide in that Electron wasteland...

I pressed execute, expecting the hidden truth to emerge.

---

## Act II: The Void

The result came back.

```json
{ "ok": false, "found": [] }
```

Nothing.

I didn't believe it. I expanded the search. All percentage signs.

```json
{ "count": 0, "samples": [] }
```

**Zero results.**

> **The Architect's Note:**
> There's nothing in the DOM.
> No hidden UI. No Shadow DOM. No concealed elements.
> **The "hidden UI" that developer talked about never existed.**

I began to doubt myself.
Those quota extensions clearly display numbers.
If they're not scraping from the DOM, where are those numbers coming from?

---

## Act III: Staring into the Abyss

I stopped searching blindly. I opened the Network Tab.

Deep in that pile of gRPC requests, I saw the truth:

```
/exa.language_server_pb.LanguageServerService/GetUserStatus
```

**This is where those quota numbers come from.**

Not some hidden UI.
Not some magical DOM capture.

---

## Act IV: Two Paths

Now I know quota comes from the Language Server's `GetUserStatus`.
But the question is: **how do you get it?**

### Method A: Active Querying (What Those Extensions Do)

Directly send requests to the Language Server, asking for quota data.

**Problems**:
- The Language Server's quota API is for **internal IDE/Agent use**
- Every request you actively send is one the official UI would never send
- Is this "normal usage"? Or "unauthorized API access"?
- **Risk level: Gray area**

### Method B: Passive Listening (The Correct Approach)

Only listen to quota requests that the Language Server **has already sent**, parse them, display the result.

**Problems**:
- The official quota queries are for internal interface use only
- **You cannot predict when it will send one**
- Ten minutes? An hour? Several hours? All possible
- You get what you can parse, nothing more

> **The Architect's Verdict:**
> Method B is the morally correct approach—you're just listening, not asking.
> But the cost is: **you never know when the next update will come.**
> This is the price of uncertainty paid for safety.

---

## Epilogue: The Legacy of a Lie

That developer's "hidden UI capture" was a lie.
Maybe ignorance. Maybe marketing. Maybe self-deception.

But the lie has been spread.

And the truth is:

1. **There's no quota info in the DOM**—not even hidden
2. **Quota comes from the Language Server API**—the `GetUserStatus` endpoint
3. **Active querying**—gray area risk
4. **Passive listening**—correct approach, but timing is unpredictable

---

## Appendix: If You Still Want to See Your Quota

| Method | Risk | Cost |
|--------|------|------|
| **Official** | Zero | Wait until you run out |
| **Active Query** | Gray area | May be flagged as anomalous |
| **Passive Listen** | Low | Updates every 10 min to hours |
| **Don't look** | Zero | Peace of mind |

Sometimes, what's invisible should stay invisible.

---

**Terror Level:** 💀💀
**Ghost Story Type:** Technical Lies / Gray Area / Information Hiding
**Keywords:** `DOM`, `GetUserStatus`, `Language Server`, `Gray Area`
**Occurrence:** 2026-01-26 14:00-14:40
**Survival Status:** ⚠️ Truth known, but risk cannot be eliminated

---

> *"READMEs tell you the author's beautiful delusions.*
> *Commits and Issues tell you the truth.*
> *The Network Tab? That's where the secrets even the author doesn't want you to know."*

---

> *They love to hear ghosts chant poetry by autumn graves.*
> *— Those quota numbers are whispers from the Language Server in the darkness.*
> *You heard them. But you weren't supposed to.*
