# Thomas Lince

I build AI systems that have to work outside the demo.

I came into this from operations, not research. Over the last several years, I’ve built and run production systems where AI agents answer customers, read live business state, quote services, take payments, update operational systems, and coordinate fulfillment.

That experience has made me fairly conservative about what should be left to a model.

**The model can reason. It does not get to be its own authority.**

Most of my work follows from that idea: agents can handle ambiguity and conversation, while important business rules, state changes, payments, and permissions remain behind deterministic systems and controlled tools.

A lot of what I’m building now lives under [teal-sea](https://teal-sea.com).

## Production systems

My main production work has been a sales and operations platform for a transportation business operating across several US markets.

AI agents handle customer conversations and parts of the booking workflow. Pricing, availability, payments, state changes, business rules, and writes to operational systems sit behind controlled tools and endpoints.

The general pattern is:

**agents propose; systems decide what they’re allowed to do.**

## Verification

### [lean-checked-network](https://github.com/teal-sea/lean-checked-network)

A small neural network, trained on half of a modular-addition table, proved correct on every input with Lean 4.

Most model evaluation samples inputs and reports a score. This network’s input space is small enough to cover completely, so the result is a theorem instead: Lean’s kernel checks that the network gives the right answer on all 12,769 inputs, including the 6,385 it never saw in training.

A second theorem tests the explanation of how it works. Each neuron places numbers on a circle and the network adds angles; keep only that circle part of every neuron and the network is still provably right everywhere. A deliberately broken copy is rejected by the same proof, and every check reruns on each push.

### [grounded-check](https://github.com/teal-sea/grounded-check)

Checks what a conversational AI agent said against what its tools actually returned.

I built it after a production QA system started flagging correct quotes as hallucinations because it could see the transcript, but not the business data the agent had used.

The fix was simple in principle: judge the answer against the same evidence the agent had.

### [too-soon](https://github.com/teal-sea/too-soon)

A small statistical guardrail for A/B tests.

It refuses to declare a winner before the available evidence supports one.

### [convai-webhook-guard](https://github.com/teal-sea/convai-webhook-guard)

Verifies ElevenLabs post-call webhooks before downstream systems trust them.

Small project, same principle:

**claims about reality should be independently checkable before they change system state.**

## Zeta Lab

### [zeta-lab](https://github.com/teal-sea/zeta-lab)

An experimental computational and formal mathematics lab centered initially on analytic number theory and the Riemann zeta function.

It combines arbitrary-precision computation, Lean formalization, source reconstruction, and adversarial evaluation of generated mathematical claims.

One thing I’m particularly interested in is how verification systems themselves should be tested.

Zeta Lab uses mechanisms such as:

- **rivals** — does the explanation also work somewhere the property is absent?
- **decoys** — does changing the real input actually change the result?
- **surrogates** — can a null model reproduce the observation?
- **lesions** — if a failure is deliberately introduced, does the detector notice?

The verifier itself has to work in both directions: it should reject claims known to be bad and accept claims known to be sound.

The mathematics is useful in its own right, but it also gives me a difficult environment for studying a broader problem:

> **If generating plausible claims becomes cheap, reliable rejection becomes infrastructure.**

## Architecture

### [Why your AI startup dies at customer six](https://github.com/teal-sea/why-your-ai-startup-dies-at-customer-six)

A short essay about what happens when an AI product starts accumulating real deployments.

I separate deployment-specific work into three pieces:

- **semantic layer** — what the business's objects mean
- **kinetic layer** — what the system can actually do
- **rulebook** — where one deployment is allowed to differ from another

The goal isn’t to eliminate custom work.

It’s to make sure every deployment teaches the underlying platform something reusable.

## Elsewhere

### [modalruns.com](https://modalruns.com)

A browser-based guitar practice app for exploring modes over changing harmony.

Built, launched, and monetized.

---

Most of what interests me sits somewhere between AI systems, operations, evaluation, and verification:

**What does the system actually know? What is the agent allowed to do? How do we know the result is correct? And what should become reusable the next time around?**
