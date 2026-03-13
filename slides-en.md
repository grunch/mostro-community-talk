---
theme: default
title: "Mostro Community Talk #1"
info: |
  ## First call with Spanish-speaking communities
  mostro.community
class: text-center
drawings:
  persist: false
transition: fade-out
mdc: true
fonts:
  mono: 'Fira Code'
---

# Mostro Community Talk #1 {.font-mono .text-green-400}

## First call with English-speaking communities {.text-gray-400 .font-mono}

<div class="mt-10 flex justify-center items-center gap-4">
  <img src="/mostro-node.png" class="h-20 rounded-lg" />
</div>

<div class="abs-br m-6 text-sm text-gray-500 font-mono">
mostro.community · 2026
</div>

<!--
Short welcome. Goal: align vision + real operation.
Suggested total duration: 20-25 min + Q&A.
-->

---
layout: center
class: text-center
transition: fade
---

<div class="text-3xl font-mono text-green-400 leading-relaxed">

We're not here to sell hype.<br/>
We're here to build community P2P markets.

</div>

<!--
Tone slide.
-->

---
transition: slide-left
---

# Agenda (25 min) {.font-mono}

<!--
Note: Keep pace. If Q&A extends, shorten community intros to 2 key questions.
-->
<div class="mt-8 text-left max-w-3xl mx-auto text-lg">

1. Welcome and introduction
2. What is Mostro and how it works
3. What running a node implies
4. Technical requirements + installation
5. Community introductions
6. Questions and answers
7. Next steps and closing

</div>

---
transition: slide-left
---

# What is Mostro? {.font-mono}

<!--
Key message: Mostro doesn't replace community, it empowers it with infrastructure.
Avoid long technical jargon here.
-->
<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

- P2P infrastructure on **Lightning + Nostr**  
- No central custody of funds  
- With reputation and dispute resolution  
- Designed for communities, not closed platforms

</div>

<div class="mt-8 p-4 border border-green-700/50 rounded-lg bg-green-950/20 text-sm text-gray-300">
Mostro is not "an app". It's an operational ecosystem.
</div>

---
transition: slide-left
---

# Key ecosystem projects {.font-mono}

<!--
Suggested script (60-90s):
- mostro = engine
- mobile = user entry point
- mostrix = operational/dispute panel (essential today)
- watchdog = instant alerts (without this you miss disputes)
-->
<div class="grid grid-cols-2 gap-5 mt-6 text-left">

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="flex items-center gap-3 mb-2">
    <img src="/mostro-node.png" class="h-10 w-10 rounded" />
    <div class="font-bold">mostro</div>
  </div>
  <div class="text-sm text-gray-400">P2P market core daemon.</div>
  <div class="text-xs font-mono text-green-400 mt-2">github.com/MostroP2P/mostro</div>
</div>

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="flex items-center gap-3 mb-2">
    <img src="/mostro-mobile.png" class="h-10 w-10 rounded" />
    <div class="font-bold">mobile</div>
  </div>
  <div class="text-sm text-gray-400">Client for end users.</div>
  <div class="text-xs font-mono text-green-400 mt-2">github.com/MostroP2P/mobile</div>
</div>

<div class="p-4 border border-yellow-700 rounded-lg bg-yellow-950/20">
  <div class="flex items-center gap-3 mb-2">
    <img src="/mostrix-logo.png" class="h-10 w-10 rounded" />
    <div class="font-bold text-yellow-300">mostrix</div>
  </div>
  <div class="text-sm text-gray-300">Most complete panel today for admin and disputes.</div>
  <div class="text-xs font-mono text-yellow-300 mt-2">github.com/MostroP2P/mostrix</div>
</div>

<div class="p-4 border border-yellow-700 rounded-lg bg-yellow-950/20">
  <div class="flex items-center gap-3 mb-2">
    <img src="/mostro-watchdog.png" class="h-10 w-10 rounded" />
    <div class="font-bold text-yellow-300">watchdog</div>
  </div>
  <div class="text-sm text-gray-300">Telegram bot: real-time dispute alerts.</div>
  <div class="text-xs font-mono text-yellow-300 mt-2">github.com/MostroP2P/mostro-watchdog</div>
</div>

</div>

<!--
Key point: today mostrix + watchdog are essential for serious operation.
-->

---
transition: slide-left
---

# How it works (simple view) {.font-mono}

<!--
Don't dive into protocol internals details.
Goal: anyone understands an order flow in <90s.
-->
<div class="mt-8 text-sm font-mono">

```text
Maker publishes order  →  Taker accepts  →  Hold invoice active
        ↓                                      ↓
    Nostr messaging                     Fiat confirmation
        ↓                                      ↓
     Release ------------------> BTC to buyer
```

</div>

<div class="mt-6 text-gray-400 text-sm">
Lightning settles. Nostr coordinates. Mostro enforces rules.
</div>

---
transition: slide-left
---

# What running a node implies {.font-mono}

<!--
Emphasize that running node = technical + social responsibility.
Don't sell it as "just spin up a docker".
-->
<div class="grid grid-cols-2 gap-8 mt-8 text-left">

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="font-bold mb-2">Technical</div>
  <ul class="text-sm text-gray-300">
    <li>Uptime and monitoring</li>
    <li>Backups and updates</li>
    <li>Observability and alerts</li>
  </ul>
</div>

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="font-bold mb-2">Operational</div>
  <ul class="text-sm text-gray-300">
    <li>Community support</li>
    <li>Clear policies</li>
    <li>Dispute management</li>
  </ul>
</div>

</div>

---
transition: slide-left
---

# Recommended minimum stack {.font-mono}

<!--
Strong phrase: without mostrix/watchdog there's no serious dispute operation.
-->
<div class="grid grid-cols-4 gap-4 mt-8 text-center">

<div class="p-3 border border-gray-700 rounded-lg">
  <img src="/mostro-node.png" class="h-14 mx-auto mb-2 rounded" />
  <div class="text-sm font-bold">mostro</div>
</div>

<div class="p-3 border border-gray-700 rounded-lg">
  <img src="/mostrix-logo.png" class="h-14 mx-auto mb-2 rounded" />
  <div class="text-sm font-bold">mostrix</div>
</div>

<div class="p-3 border border-gray-700 rounded-lg">
  <img src="/mostro-watchdog.png" class="h-14 mx-auto mb-2 rounded" />
  <div class="text-sm font-bold">watchdog</div>
</div>

<div class="p-3 border border-gray-700 rounded-lg">
  <img src="/mostro-mobile.png" class="h-14 mx-auto mb-2 rounded" />
  <div class="text-sm font-bold">mobile</div>
</div>

</div>

<div class="mt-8 text-sm text-yellow-300 font-mono">
Node without mostrix + watchdog = operating blind on disputes.
</div>

---
transition: slide-left
---

# Technical requirements {.font-mono}

<!--
Keep it realistic: start small, but with operational discipline.
-->
<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

- Stable Linux server (VPS or bare metal)  
- Operational Lightning node  
- Connectivity to Nostr relays  
- Secure secrets and backups management

</div>

---
transition: slide-left
---

# Installation (high level) {.font-mono}

<div class="mt-8 text-sm font-mono">

```bash
1) Prepare server
2) Configure Lightning
3) Deploy mostro
4) Configure mostrix
5) Activate watchdog (Telegram alerts)
6) Validate end-to-end flow with test orders
```

</div>

<div class="mt-6 text-gray-400 text-sm">
Command details go in the technical guide later.
</div>

---
transition: slide-left
---

# Community round (2-3 min each) {.font-mono}

<!--
If many people: ask for short answers (30-45s per point).
Prioritize: 30-day goal + main blocker.
-->
<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

1. Community name and region  
2. Team's technical level  
3. Goal for the next 30 days  
4. Current main blocker

</div>

---
transition: slide-left
---

# Questions and answers {.font-mono}

<div class="mt-8 grid grid-cols-2 gap-8 text-left">

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="font-bold">Technical</div>
  <div class="text-sm text-gray-400 mt-2">Infrastructure, security, operation, monitoring.</div>
</div>

<div class="p-4 border border-gray-700 rounded-lg">
  <div class="font-bold">Community</div>
  <div class="text-sm text-gray-400 mt-2">Support, reputation, disputes, local governance.</div>
</div>

</div>

---
transition: slide-left
---

# Next steps {.font-mono}

<!--
Close with operational clarity: who does what, by when, and through which channel.
-->
<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

- Create Spanish-speaking pilot group  
- Publish deployment guide + operational checklist  
- Define health metrics per node  
- Schedule second call with learnings

</div>

---
layout: center
class: text-center
transition: fade
---

# Thank you {.font-mono .text-green-400}

<div class="mt-6 text-gray-300">
Let's build resilient, open and community-driven P2P infrastructure.
</div>

<div class="mt-10 text-sm text-gray-500 font-mono">
mostro.community · @MostroP2P · @lnp2pBot
</div>

<!--
Closing (20s):
- Thanks for joining early.
- This stage defines operation standards for the entire network.
- See you in the next call with concrete progress.
-->

---
transition: slide-left
---

# Backup Q&A: Disputes {.font-mono}

<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

- Recommended flow today: **mostrix + watchdog**  
- Watchdog alerts on Telegram when dispute appears  
- Operator enters mostrix and manages resolution  
- Record lessons to improve local policy

</div>

<div class="mt-6 p-4 border border-yellow-700 rounded-lg bg-yellow-950/20 text-sm text-gray-300">
Without alerts, disputes may go unattended. That risk is real today.
</div>

---
transition: slide-left
---

# Backup Q&A: Operational security {.font-mono}

<div class="mt-8 text-left max-w-4xl mx-auto text-lg">

Minimum checklist per node:

- Hardened SSH access + updates  
- Frequent and verified backups  
- Critical services monitoring  
- Documented incident procedure

</div>

<div class="mt-6 text-sm text-gray-400">
Goal: operate predictably, not heroically.
</div>
