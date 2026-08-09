# Thomas Lince

I build AI systems that operate in the real world — and the tools that keep them from quietly doing the wrong thing.

Most of my projects start the same way: something breaks in production, I figure out why, and the fix turns into something reusable.

## Production AI

I run operations for a business where an AI agent answers the phone and can carry a sale from discovery through quoting, payment, and booking.

The model handles the conversation. Pricing, availability, payments, business rules, and writes stay behind deterministic tools and endpoints.

That separation — **reasoning in the model, authority in the system** — is the architectural theme behind most of what I build.

## Tools from production failure modes

### [grounded-check](https://github.com/teal-sea/grounded-check)

Audit what an AI agent said against what its tools actually returned.

Built after a production quality monitor flagged dozens of correct quotes as hallucinations because it could see the transcript but not the ground truth the agent had received.

### [convai-webhook-guard](https://github.com/teal-sea/convai-webhook-guard)

Verify ElevenLabs post-call webhooks before downstream systems trust them.

Small, boring infrastructure. Exactly the kind you want to be boring.

### [too-soon](https://github.com/teal-sea/too-soon)

A tiny guardrail for A/B tests that refuses to call a winner before the sample can support one.

Because a number looking decisive and a number being decisive are different things.

## Architecture

### [Why your AI startup dies at customer six](https://github.com/teal-sea/why-your-ai-startup-dies-at-customer-six)

An essay about the point where bespoke AI deployments stop scaling.

The model I use separates a system into:

* **semantic layer** — what things are
* **kinetic layer** — what can be done
* **rulebook** — where each customer is allowed to differ

The goal is to make customer-specific behavior configuration rather than customer-specific software.

## Research

### [zeta-lab](https://github.com/teal-sea/zeta-lab)

A computational and formal laboratory around the Riemann Hypothesis.

It includes arbitrary-precision numerics, classical analytic-number-theory machinery, Lean proofs, and a falsification harness built around a broader idea I care about:

> When generating plausible claims becomes cheap, reliable rejection becomes infrastructure.

No RH proof claims. Quite the opposite: the lab is designed to kill bad ideas quickly and preserve the evidence.

## Elsewhere

### [modalruns.com](https://modalruns.com)

A browser-based guitar practice app for exploring modes over evolving drones and harmony.

Built, launched, and monetized.

---

### What I keep coming back to

**Autonomous systems. Deterministic boundaries. Adversarial testing. Reliable rejection.**

Build things that can act.

Then build the machinery that tells you when they're wrong.
