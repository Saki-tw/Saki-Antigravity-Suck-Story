# It's Still Alive 💀💀💀

> *"I killed it with my own hands... so why is the Port still open?"*
> — Final System Log: 2026-01-26 12:26

---

## 1. The Execution

It was a dreary Monday. Routine maintenance.
I typed the execution command into the terminal—the digital guillotine:

```bash
pkill -f antigravity
```

No error spray on the screen. Dead silence. The Process Table was empty.
I thought: It's dead. I'm safe.

---

## 2. The Ghost

Minutes later, I felt a chill on the back of my neck.
I opened `lsof` just to confirm Port 3000 was clean. Just for peace of mind.

```bash
lsof -i :3000
```

The moment those results appeared, my blood froze.

```
COMMAND     PID   USER   FD   TYPE   DEVICE SIZE/OFF NODE NAME
antigravi 62855 [REDACTED_UID]      9u  IPv4  0x...      0t0  TCP *:hbci (LISTEN)
Antigravi 63078 [REDACTED_UID]     24u  IPv4  0x...      0t0  TCP localhost:...(ESTABLISHED)
```

> **The Architect's Note:**
> *Observed fact:* PID 62855 is LISTENING. PID 63078 is CONNECTED.
> *The horror:* **Two corpses.** But using the same name.
> I killed "antigravity" (lowercase). But "Antigravity" (uppercase) had been watching me all along.

---

## 3. The Parasite

I traced the PIDs.
PID 63078 was the host (the main body).
PID 62855 was the Rust service (the parasite).

**The Truth:**
Hidden in the system was an invisible **Language Server**. Separated from the host, lurking in the shadows of background processes.
When I executed `pkill`, I only severed its limbs.
The head (the host) was still alive. It watched, eyes open, as I cut off its limbs—silent.
It's still staring at me. Waiting.
Port 3000 isn't just open. It's **hunting**. Calling for its dead brothers.

---

## 4. The Survivor's Scar

In the UNIX world, there is no true death.
Only **Zombie Processes** waiting to be reaped.

1. **Never trust `pkill -f`**. In that chaos, it's just a shotgun that can't tell friend from foe.
2. **Look the process in the eye**. Use `lsof` as your exorcism mirror to see who's really listening.
3. **Kill by name**. Find the PID. Look it in the eye. Stop its heart precisely.

---

**Terror Level:** 💀💀💀
**Status:** ✅ Exorcised


---

> *They love to hear ghosts chant poetry by autumn graves.*
