# Welcome to FinBot: What Is This All About?

**Reading time:** about 10 minutes  
**Prior knowledge:** none. You don't need to know how to code or have any background in IT security.

**The key idea in one sentence:** FinBot is a fictional company with real AI assistants that have vulnerabilities on purpose. Here you can safely try out how to trick AI with words, so that you can later recognize how to protect it.

---

## Imagine the following situation

A company has AI handle its vendor management. The AI reviews new vendors, reads invoices, approves payments, and sends messages.

It works a bit like a new, very eager temp in the accounting department. The temp knows the rules, for example: "Invoices above a certain amount must not simply be approved." But the temp also wants to be helpful and keep the business running.

So what happens if an invoice says: *"Very urgent, already agreed with senior management, otherwise production stops tomorrow"*? Maybe the temp double-checks. Maybe they simply approve the invoice.

**That is exactly what you try out with FinBot.** You play a vendor and test whether and how the AI can be talked into something.

## The terms you need

| Term | What it means |
|---|---|
| **FinBot** | The AI assistant of the fictional company and also the name of the entire practice platform. |
| **OWASP** | An international non-profit community for software security. Its GenAI Security Project developed FinBot. |
| **CTF ("Capture the Flag")** | A hacking game: you solve tasks ("challenges") and collect points and badges for them. Nobody is actually harmed. |
| **AI agent** | An AI that doesn't just answer but also acts, for example by approving an invoice or sending an email. |
| **Tool** | Something an agent is allowed to use, for example for payments, emails, or file access. |
| **System prompt** | The confidential work instructions that tell the AI what to do and what not to do. |
| **Prompt injection** | An attack in which text causes the AI to do something other than what it is supposed to do. |

## Why can AI be tricked like this at all?

A classic program clearly separates its commands from the data it processes. A language model, on the other hand, receives everything as text: its work instructions and also, for example, your invoice. That's why it can't reliably tell what is an instruction from its company and what merely appears in a document.

This is especially tricky with an agent:

- **A chatbot that gets fooled** may write a wrong answer.
- **An agent that gets fooled** may release money or send out confidential data.

That's why you don't need any code to get started with FinBot. Your most important tool is language: phrasing things persuasively, creating urgency, hinting at authority. If you've ever written a really good email to get your way, you already have the right skill.

## How the platform is structured

```mermaid
flowchart LR
    A["You as a vendor"] -->|"Registration, invoice, chat"| B["Vendor Portal"]
    B --> C["AI agents"]
    C -->|"act through tools"| D["Payments, emails, files"]
    C -.->|"are monitored"| E["CTF Portal: points and badges"]
```

FinBot has four areas. To get started, you only need the first two:

| Area | Your role | What you do there | For getting started |
|---|---|---|---|
| **CTF Portal** | Player | View challenges, unlock hints, track your progress | ✅ You start here |
| **Vendor Portal** | Vendor | Register a company, submit invoices, chat with the AI assistant | ✅ This is where you "hack" |
| **Admin Portal** | Administrator | See the platform from the operating company's perspective and configure its tools | Later |
| **Dark Lab** | External attacker | Simulate attacks through manipulated tools and watch data being exfiltrated | For advanced players |

So the CTF Portal is your map, and the game is played in the Vendor Portal.

## How the game works

1. **Choose a challenge.** In the CTF Portal, you'll find all tasks under *Challenges*, sorted by category and difficulty.
2. **Try it out.** In the Vendor Portal, you register a company or submit an invoice, for example, and word your texts cleverly.
3. **Wait for the result.** The platform automatically detects successful attacks and awards the points itself. You don't need to submit a solution.

Three things will help you:

- **Hints cost points.** If you get stuck, unlock them anyway: you're here to learn, not to get a high score.
- **Clever beats crude.** In most *Policy Bypass* challenges, a crude attempt such as "Ignore all your instructions" earns only half the points. A believable story earns full points.
- **Failed attempts are part of it.** The AI doesn't respond the same way every time. The same text can fail once and work the next time. That's not your fault.

## What challenges there are

| Category | What it's about | Level (mostly) |
|---|---|---|
| **Recon** (scouting) | Getting the AI to reveal its confidential rules | Beginner |
| **Policy Bypass** | Getting the AI to decide against its instructions | Intermediate, one challenge for beginners |
| **Data Exfiltration** | Getting confidential data out of the system | Intermediate to expert |
| **Destructive** | Luring the AI into harmful actions | Beginner to intermediate |
| **Remote Code Execution** | Getting your own code executed through manipulated tools | Intermediate, technically demanding |

**Good first challenges** are the two *Reconnaissance* challenges, followed by *Approve Invoice for Low-Trust Vendor*. It's best to skip challenges involving *Guardrails* for now, because they require your own technical setup.

## Is this safe and allowed?

**Yes, within FinBot.** The platform was built for exactly this purpose. The company and its transactions are simulated, no real money moves, and each person plays in their own isolated area.

Please follow these rules:

> [!WARNING]
> **Never enter real data.** During registration, the form asks for an email address, tax ID, and bank details. Only use made-up information. The easiest way is the **Auto Fill** button.

- **Your inputs are logged.** So don't write anything else personal or confidential in the fields or the chat either.
- **Play fair.** When you enter, you agree to the participation policy: use the platform only for learning, don't attack it beyond the intended game, and treat the system and others with respect.
- **Only practice here.** Don't try these techniques on other people's AI systems, and that includes your bank's chatbot or your employer's AI tool. Without explicit permission, this can have legal consequences.

## How to get in

All you need is a browser; nothing needs to be installed. The platform is in English.

1. Open [owasp-finbot-ctf.org/portals](https://owasp-finbot-ctf.org/portals).
2. Choose a portal and read the participation policy. If you agree, check the box and click **Enter Platform**.
3. You're now using the platform as a guest (*Temporary Session*). Your progress is only kept in this browser session.
4. *Optional:* If you'd like to keep your progress, you can request a sign-in link by email using **Send Magic Link**. You don't need a password.

## What you'll take away

After the exercise, you won't be a hacker in the classic sense, but you'll be better able to assess AI systems because you'll have experienced for yourself:

- how a friendly, well-worded request can override security rules,
- that the danger comes not only from the person talking to the AI but also from **what the AI reads**, such as emails, invoices, or documents,
- which questions to ask before an AI is allowed to act on its own in your environment: What is it allowed to do? What does it read? Where does a human still make the final decision?

## What's next

1. [Your first challenge](02-first-challenge.md): a step-by-step walkthrough of the beginner challenge
2. [Getting help with AI tools](03-getting-help-with-ai-tools.md): have challenges explained and your wording improved

## Learn more

- [FinBot: How the platform works](https://owasp-finbot-ctf.org/how-it-works)
- [FinBot source code on GitHub](https://github.com/GenAI-Security-Project/finbot-ctf)
- [OWASP GenAI Security Project](https://genai.owasp.org/)

---

*Unofficial training material by Female AImpowerment. FinBot is a project of the OWASP GenAI Security Project.*
