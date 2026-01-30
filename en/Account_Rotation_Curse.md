# The Curse of Account Rotation 💀💀💀💀💀

> *"First, one account died. Then they all began to scream."*
> — GitHub Issues #643, #655, #1114

---

## 1. The Seduction

It all started with a temptation.
A repository whispered: *"Why pay? Why wait? Why be limited?"*

It handed you a poison apple called **"Account Rotation."**
*"Give me all ten of your accounts,"* it said. *"When one dries up, I'll switch to the next. Unlimited compute."*

The developer was blinded by greed.
He thought he was a god. He thought he had outsmarted God (Google).

---

## 2. The Glitch

The first few days, everything was beautiful. The **Reverse Proxy** hid his tracks perfectly.
Then the first notification arrived.

**#643: Account banned**
> *"I suddenly can't log in..."*

**#655: Does this mean I'm banned?**
> *"403 Forbidden no matter where I connect..."*

The developer waved it off. "Just a bug," he thought. "The proxy protects me anyway."
But he didn't know: Proxies can hide IPs, but they can't hide **Behavior Patterns**.

---

## 3. The Mass Grave

Then Issue #1114 appeared. It was the death knell.
**[CRITICAL] Chain-Ban Due to Reverse Proxy Failure**

Let's reconstruct the crime scene logs to see how this massacre unfolded:

```http
POST /v1/generate_content HTTP/1.1
Host: antigravity.api
Account-ID: [REDACTED_UID_A]
< 429 Too Many Requests (Quota Exceeded)

-- [Rotation Logic Triggered] 0ms delay --

POST /v1/generate_content HTTP/1.1
Host: antigravity.api
Account-ID: [REDACTED_UID_B]
< 429 Too Many Requests (Risk Detected)

-- [Rotation Logic Triggered] 0ms delay --

POST /v1/generate_content HTTP/1.1
Host: antigravity.api
Account-ID: [REDACTED_UID_C]
< 403 Forbidden (Account Suspended)
```

> **The Architect's Note:**
> *What the code did:* When Account A failed, it **instantly** switched to B. Then C.
> *What the server saw:* A single crazed entity changing masks and banging on the door.
> *The horror:* Humans hesitate. Humans wait.
> Only machines switch accounts in **0 milliseconds**.
> In pursuit of "unlimited," you proved yourself to be a Bot.

**The hammer of judgment fell.**
Not one. **All of them.**
What was supposed to be an "unlimited pool" became a mass grave in an instant.
Years of history, emails, documents... all turned to ash.
Sacrificed to the dark god named "Free."

---

## 4. The Survivor's Scar

In the Terms of Service—that necronomicon—there are two incantations you must never recite together:

| The Incantation | The Consequence |
|-----------------|-----------------|
| **Account Rotation** | ⚠️ Mark of the Beast |
| **Reverse Proxy** | ⚠️ Veil of Deception |
| **Rotation + Proxy** | ❌ **Total Existence Erasure** |

Don't eat the free lunch.
That meat... it's human.

---

**Terror Level:** 💀💀💀💀💀
**Status:** ⚠️ Evaded (Heard the warning and ran)


---

> *They love to hear ghosts chant poetry by autumn graves.*
