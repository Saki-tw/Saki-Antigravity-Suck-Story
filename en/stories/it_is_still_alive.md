# It Is Still Alive 💀💀💀

> *“I saw the socket open... even after I buried the PID.”*
> — Last log entry: 2026-01-26 12:26

---

## 1. The Execution

It was a grey Monday. Routine maintenance.
I typed the command, the digital guillotine:

```bash
pkill -f antigravity
```

The terminal returned silence. The process table was empty.
I thought it was dead. I thought I was safe.

---

## 2. The Ghost

Minutes later, I felt a prickling on my neck.
I opened `lsof`, just to check the port. Just to be sure.

```bash
lsof -i :3000
```

The output appeared, and my blood ran cold.

```
COMMAND     PID   USER   FD   TYPE   DEVICE SIZE/OFF NODE NAME
antigravi 62855 [REDACTED_UID]      9u  IPv4  0x...      0t0  TCP *:hbci (LISTEN)
Antigravi 63078 [REDACTED_UID]     24u  IPv4  0x...      0t0  TCP localhost:...(ESTABLISHED)
```

> **Digital Coroner Note:**
> *Observation:* PID 62855 is Listening. PID 63078 is Connected.
> *The Horror:* **Two bodies.** One name.
> I had killed "antigravity". But "Antigravity" (Capital A) was watching me.

---

## 3. The Parasite

I traced the PIDs.
PID 63078 was the Main App (The Host).
PID 62855 was a Rust Service (The Parasite).

**The Truth:**
There was an invisible **Language Server**, detached from the main body, hiding in the background.
When I ran `pkill`, I only killed the limb.
The Head (Main App) was still alive. It watched me cut off its arm.
And now, it was **waiting**.
The port wasn't just open. It was *hungry*.

---

## 4. The Survivor's Scar

In UNIX, there is no death.
There are only **Zombie Processes**.

1.  **Never trust `pkill`**. It is a shotgun in a crowded room.
2.  **Look them in the eye**. Use `lsof`. See who is listening.
3.  **Kill by PID**. Stop the heart specifically.

---

**Horror Level:** 💀💀💀
**Status:** ✅ Exorcised