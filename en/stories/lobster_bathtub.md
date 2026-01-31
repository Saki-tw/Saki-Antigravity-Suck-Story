# The Lobster Bathtub

> *"There are more things in heaven and earth, Horatio,*
> *Than are dreamt of in your philosophy."*
> — Shakespeare, Hamlet

---

## Prologue: The Lobster in the Node.js Tank

They say lobsters never stop growing.

They don't age. Given enough space and food, they can live forever, growing larger and larger. Until one day, their shell becomes too small. Then they must molt. This process is called `exfoliation`.

But what happens when you trap a lobster in a bathtub?

---

## Act I: The $300 Wishing Well

```
EXFOLIATE! EXFOLIATE!
```

That's the first line of OpenClaw's README.

Like a radio switching on in the dead of night. You're not sure if it's a motto or a warning.

---

The vision was beautiful. As visions always are.

It promised to make your AI assistant live across all your platforms—WhatsApp, Telegram, Slack, Discord, Signal, iMessage, Microsoft Teams. Even Matrix and Zalo. It wanted AI to be everywhere, always ready, like a well-trained lobster scuttling through your digital kitchen.

The cost? At least $200/month for Claude Max subscription. Or the OpenAI equivalent.

That's just the API fees.

---

Several of my environments don't even have Node.js.

Almost everything I build relies on the simplest, oldest backend patterns—`rustup` compilation, `golang` support, then a thin shell wrapper. No Electron. No V8. No `node_modules` abyss.

So when I saw this configuration:

```json
{
  "agent": { "model": "anthropic/claude-opus-4-5" }
}
```

I didn't think of a bright future.

I thought: how much memory does a single session consume?

---

## Act II: The 400MB Minimum Horror

Let me do the math.

Claude Code and Gemini CLI—the most frugal options—still consume **400MB** per session.

Those Node.js-based tools with DevTool dependencies? With a full Electron V8 engine embedded? A single session with encrypted protobufs, dynamic loading, and context window expansion can easily reach **2-8GB**.

And that's before counting the official "freemium plugins"—all brute-force DOM scraping.

```
WhatsApp / Telegram / Slack / Discord / Signal / iMessage
            │
            ▼
    ┌───────────────────────────────┐
    │         Gateway              │
    │      (control plane)         │  
    │    ws://127.0.0.1:18789      │ ← externally exposed
    └──────────────┬───────────────┘
                   │
        ├─ Pi agent (RPC)
        ├─ CLI (openclaw …)
        ├─ WebChat UI
        ├─ macOS app
        └─ iOS / Android nodes
```

---

## Act III: Ten Scars

I never ran this project myself.

But I've read its autopsy report.

```regex
/0\.0\.0\.0:18789/  # Gateway externally exposed
/dmPolicy.*open/    # DM policy: allow everyone
/sandbox.*false/    # Sandbox: disabled by default
/oauth\.json/       # Credentials stored in plaintext
```

Ten scars, each cutting to the bone:

| # | Symptom | Diagnosis |
|---|---------|-----------|
| 1 | Gateway exposed on `0.0.0.0:18789` | Anyone can connect |
| 2 | DM policy allows all users | `dmPolicy="open"` + `allowFrom: "*"` |
| 3 | Sandbox disabled by default | Main session has full system access |
| 4 | Credentials stored plaintext in `oauth.json` | Keys hanging on the door |
| 5 | Web content enables Prompt Injection | You think you're browsing; you're being injected |
| 6 | Dangerous commands not blocked | `rm -rf` may be just the beginning |
| 7 | No network isolation | The lobster can swim anywhere |
| 8 | Excessive tool access permissions | `bash`, `process`, `read`, `write`, `edit`... |
| 9 | No audit logging enabled | When things go wrong, you won't know what happened |
| 10 | Weak or default pairing codes | Like using `0000` as your PIN |

---

## Act IV: The Lobster's Confession

> "After playing with Clawdbot/Moltbot for two days, my account got locked."
> 
> — @henryyang_tw, Threads

---

Here's how it happened.

He knew it was dangerous. So he prepared an idle laptop, wiped all old data. Then he registered a brand new Google account, gave the AI the username and password, and let it play freely.

```
Equipment issued: One laptop
Account issued: One Google account
Expected result: Fully automated everything
```

Just like hiring a new assistant.

The AI was indeed impressive. It could code. It could browse. In theory, it could do anything.

**But it wasn't clever enough to pretend it wasn't a robot.**

So Google locked it.

---

He said: "I wonder if I had asked it to pretend to be human, would it have been harder to get locked?"

He said: "But I didn't want to run that experiment."

> **Related horror story**: This parallels the [Curse of Account Polling](./curse_of_account_polling.md)—
> Account polling switches between accounts with 0ms delay, letting the system identify you as a Bot.
> The Lobster Bathtub lets AI operate your account, letting the system identify "you" as a Bot.
> The result is the same: you get treated as a machine.

---

## The Truth (Digital Autopsy Report)

When a lobster is placed in a bathtub, it doesn't know it's in a bathtub.

It only knows:

* There's water here
* There's food here
* It can move around

What it doesn't know:

* How big the bathtub is
* When the water will be drained
* Who's watching

---

OpenClaw's design philosophy is honest. The README states clearly:

> **Default: tools run on the host for the main session, so the agent has full access when it's just you.**

Translation: By default, the AI has complete access to your system.

This isn't a Bug. This is a Feature.

---

But the question is: who is "you"?

When you set `dmPolicy` to `"open"`, anyone can be "you."
When you set `allowFrom` to `"*"`, any message gets processed.
When you leave `sandbox.mode` at default, all tools execute directly on the host.

At this point, the lobster is no longer your pet.

You've become the lobster's host.

---

## Epilogue: Blessings

```javascript
{
  "workspace": "~/.openclaw/workspace",
  "injected_prompts": ["AGENTS.md", "SOUL.md", "TOOLS.md"],
  "skills": "~/.openclaw/workspace/skills/<skill>/SKILL.md"
}
```

It has Agents. It has a Soul. It has Tools. It has Skills.

It has a complete personality configuration system.

It lives in your `~/.openclaw/` directory.

---

Blessings to all who have nothing to feed the LLM Shell anyway.

Blessings to all who spend $300 monthly bathing with lobsters, with most of it consumed by interface parsing.

Blessings to all who handed their credentials to AI, only to discover AI doesn't know how to pretend to be human.

Blessings to all who believed "Personal AI Assistant" actually means personal.

---

The lobster keeps growing.

Until the bathtub can't hold it anymore.

---

## Appendix: Log Excerpts

**OpenClaw Gateway Startup Log (Simulated)**

```log
[2026-01-30T03:14:15.926Z] INFO: Gateway starting on 0.0.0.0:18789
[2026-01-30T03:14:15.927Z] WARN: dmPolicy is set to "open" - all DMs will be processed
[2026-01-30T03:14:15.928Z] WARN: sandbox.mode is "none" - tools run directly on host
[2026-01-30T03:14:15.929Z] INFO: Loaded oauth.json (plaintext credentials)
[2026-01-30T03:14:15.930Z] INFO: Connected to Claude API (claude-opus-4-5)
[2026-01-30T03:14:16.001Z] INFO: WhatsApp bridge connected
[2026-01-30T03:14:16.050Z] INFO: Telegram bridge connected
[2026-01-30T03:14:16.100Z] INFO: Ready. EXFOLIATE!
```

**Google Account Lock Log (from Threads)**

```log
Day 0: Account created, password given to lobster
Day 1: Lobster begins work, auto-registers for services
Day 2: Google detects anomalous behavior
Day 2: Account locked
Day 2: Lobster loses its shell
```

---

## Technical Coroner's Notes

| Term | Meaning |
|------|---------|
| `ws://127.0.0.1:18789` | WebSocket control plane, theoretically localhost-bound, but if bound to `0.0.0.0`, externally exposed |
| `dmPolicy="pairing"` | Default value, requires pairing code to use |
| `dmPolicy="open"` | Dangerous value, anyone can DM your AI directly |
| `sandbox.mode="none"` | Default value, AI tools execute directly on host |
| `sandbox.mode="non-main"` | Safer, non-main sessions run in Docker containers |
| `oauth.json` | Plaintext OAuth credentials, including your API keys |
| `EXFOLIATE` | Molting, the lobster's growth process, also this project's motto |

---

*Recorded on January 31, 2026*
*Taipei. Rain.*
*The lobster swims in the bathtub.*

---

> 👁 **Observer's Notes**
>
> The project's README tells you the author's initial aspirations.
> The Commits and Issues tell you the truth.
> The Network Tab holds secrets perhaps even the author doesn't know.

---

**Horror Level:** 💀💀💀💀
**Story Type:** Account Destruction / System Takeover / Consumer Warning
**Keywords:** `OpenClaw`, `Node.js`, `memory`, `oauth`, `account lock`, `lobster`
**Timeline:** Ongoing — the lobster never stops growing
**Survival Status:** ⚠️ Evaded (never had Node.js to begin with)

---

**Co-Authored-By**: Saki-tw, Claude
