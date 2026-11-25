# Thomas Lince

I build and verify production AI systems at the intersection of forward-deployed engineering and formal verification (Lean 4). I ship operational software across live customer voice, bookings, and payments, and prove critical code paths and models with machine-checked specs.

[Website](https://teal-sea.com/) · [LinkedIn / contact](https://www.linkedin.com/in/thomaslince)

## Forward-deployed AI systems and evaluation

- **[grounded-check](https://github.com/teal-sea/grounded-check):** evidence-grounded evaluation for voice AI agents, checking spoken claims against actual tool outputs. [Run the keyless demo](https://github.com/teal-sea/grounded-check#usage).
- **[omission-check](https://github.com/teal-sea/omission-check):** deterministic evaluation for missed obligations, catching required replies and tool calls that never happen. [Run the bundled demo](https://github.com/teal-sea/omission-check#quick-start) (Python 3.10+, zero dependencies).
- **[ostoyae](https://github.com/teal-sea/ostoyae):** runs coding agents over a task graph that grows as they find work. [Try the scripted demo](https://github.com/teal-sea/ostoyae#try-it) with no API key or model calls.
- **[convai-webhook-guard](https://github.com/teal-sea/convai-webhook-guard):** verifies ElevenLabs post-call webhook HMAC signatures with constant-time comparison and local signing tests.
- **[too-soon](https://github.com/teal-sea/too-soon):** lightweight A/B-test stopping utility using Wilson intervals, zero dependencies.

## Formal verification and Lean 4

- **[lean-checked-network](https://github.com/teal-sea/lean-checked-network):** Lean 4 and independent checkers (`leanchecker`, `nanoda`) verify that a trained one-layer, four-head transformer with quantized integer weights and exact real softmax adds mod 113 on all 12,769 inputs (`propext`, `Classical.choice`, `Quot.sound` only; planted faults rejected). Includes a [Lean check of an alpha-beta-CROWN certificate](https://github.com/teal-sea/lean-checked-network/blob/main/acas/README.md) for ACAS Xu 1_1 property 1 under exact-real semantics.
  - *Follow-on (Rust to Lean 4, walkthrough on request):* safe Rust two-layer causal inference engine translated to Lean 4 via Charon and Aeneas, proving exact logits and next-token outputs against the integer spec without panics or overflow, independently rechecked with NanoDa, mutation-tested against broken Rust builds, and compiled to WebAssembly.
- **[Hardy's Z function in mathlib](https://github.com/leanprover-community/mathlib4/pull/42963):** contributed the definition and supporting lemmas to upstream Mathlib. [Merged by Bors on 10 October 2026](https://github.com/leanprover-community/mathlib4/pull/42963#issuecomment-6098344268).
- **[zeta-lab](https://github.com/teal-sea/zeta-lab) · [research site](https://zeta.teal-sea.com):** computational number theory and Lean 4 formalization around the Riemann zeta function, including a kernel-checked proof that all 29 critical-strip zeros up to height 100 are simple and on the critical line, alongside rigorous numerics and negative controls. Makes no claim of progress toward RH.

## Production background

My background is in operations. I have built and run production systems handling live customer conversations, quotes, bookings, payments, and fulfillment across eight US markets.

That experience made me conservative about what should be left to a model. Agents handle ambiguity and conversation; pricing, availability, payments, permissions, and state writes sit behind deterministic tools and machine-checked checks.

**Agents propose; systems and kernels decide what is allowed.**

## Writing and products

- **[Why your AI startup dies at customer six](https://github.com/teal-sea/why-your-ai-startup-dies-at-customer-six):** an essay on reusable forward-deployed architecture: the semantic layer, kinetic layer, and rulebook.
- **[ModalRuns](https://modalruns.com):** a browser-based guitar practice app for exploring modes over changing harmony. Built, launched, and monetized.

For a conversation about forward-deployed AI systems, voice automation, evaluation, or formal verification, [get in touch on LinkedIn](https://www.linkedin.com/in/thomaslince) or visit [teal-sea.com](https://teal-sea.com/).
