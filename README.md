# Thomas Lince

I’m a forward-deployed engineer building AI systems that operate in the real world and the verification machinery that makes them trustworthy.

I came into this from operations, not research. I run production systems where AI agents answer customers, read live business state, quote, take payments, write back to operational systems, and coordinate fulfillment.

The model can reason.

**It does not get to be its own authority.**

That principle shows up in most of what I build: deterministic boundaries around agents, explicit business semantics and actions, adversarial evals, grounded judges, and systems designed to catch confident failure before a customer does.

## Production systems

My main production work is an agent-operated sales and operations stack running across multiple US markets.

The agents handle conversations and coordinate workflows. Pricing, availability, payments, state transitions, business rules, and writes remain behind controlled tools and endpoints.

The architecture I keep coming back to is simple:

**agents propose; systems decide what they are entitled to do.**

## Verification

### [grounded-check](https://github.com/teal-sea/grounded-check)

Audits what a conversational AI agent said against what its tools actually returned.

It came out of a production failure where a transcript-only quality monitor flagged dozens of correct quotes as fabricated because it could see what the agent said but not the ground truth the agent had received.

### [too-soon](https://github.com/teal-sea/too-soon)

A small statistical guardrail that refuses to call an A/B test winner before the evidence can support one.

### [convai-webhook-guard](https://github.com/teal-sea/convai-webhook-guard)

Verifies ElevenLabs post-call webhooks before downstream systems trust them.

Small infrastructure, but part of the same rule:

**claims about reality need an independent way to be checked.**

## Architecture

### [Why your AI startup dies at customer six](https://github.com/teal-sea/why-your-ai-startup-dies-at-customer-six)

An essay about the point where forward deployments stop compounding and start turning into bespoke software.

The model separates a deployment into:

* **semantic layer** — what things are
* **kinetic layer** — what can be done
* **rulebook** — where a deployment is allowed to differ

The goal is not to eliminate custom deployment work.

It is to make every deployment teach the platform what should become reusable.

## Zeta Lab

### [zeta-lab](https://github.com/teal-sea/zeta-lab)

Zeta Lab began as a computational and formal laboratory around the Riemann Hypothesis.

It has become the proving ground for a broader verification architecture.

The lab reconstructs classical analytic-number-theory machinery at arbitrary precision, develops formal results in Lean, and runs generated claims against standing adversarial batteries designed to kill them.

Those batteries use several kinds of attack:

* **rivals** — does the supposed explanation also work somewhere the property is absent?
* **decoys** — does changing the real input actually change the result?
* **surrogates** — can a null model reproduce the observation?
* **lesions** — if a failure is deliberately planted, does the detector notice?

The verifier itself must also be calibrated in both directions: it has to kill claims known to be bad and pass claims known to be sound.

The important part is that the core protocol is being separated from the subject matter.

Number theory is the first hostile deployment environment, not the intended boundary of the idea.

> **When generating plausible claims becomes cheap, reliable rejection becomes infrastructure.**

## Elsewhere

### [modalruns.com](https://modalruns.com)

A browser-based guitar practice app for exploring modes over evolving harmony.

Built, launched, and monetized.

---

I’m interested in the part of AI deployment that starts after the demo works:

**What does the system mean? What is the agent allowed to do? How do we know the deployment is actually working? And what becomes reusable when we leave?**
