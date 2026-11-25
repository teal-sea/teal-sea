# Thomas Lince

I build and verify production AI systems at the intersection of forward-deployed engineering and formal verification (Lean 4). I ship operational software across live customer voice, bookings, and payments, and check critical code and models with machine-checked specs.

[Website](https://teal-sea.com/) · [LinkedIn / contact](https://www.linkedin.com/in/thomaslince)

## Selected work

- **Rust inference verification (private, walkthrough on request):** safe Rust two-layer causal inference engine translated to Lean 4 via Charon and Aeneas, proving exact logits and next-token outputs against the integer spec without panics or overflow; independently rechecked with NanoDa, with mutation tests confirming Lean rejects broken Rust builds, and compiled to WebAssembly.
- **Production agent evaluation: [grounded-check](https://github.com/teal-sea/grounded-check):** checks a voice agent's claims against the data its tools returned. [Run the keyless demo](https://github.com/teal-sea/grounded-check#usage).
- **Agent orchestration: [ostoyae](https://github.com/teal-sea/ostoyae):** runs coding agents over a graph that grows as they find work. [Try the scripted demo](https://github.com/teal-sea/ostoyae#try-it), with no API key or model calls.
- **Formal verification: [lean-checked-network](https://github.com/teal-sea/lean-checked-network):** Lean and an independent checker verify that a trained one-layer, four-head transformer with integer weights and exact real softmax adds modulo 113 on all 12,769 inputs. This is a tiny model on a toy task, checked by brute force over all inputs, and concerns the integer-rounded model, not the float checkpoint. Earlier MLP proofs check every answer and the circle-only mechanism; a planted fault is rejected.
- **ACAS certificate checking: [Lean evidence](https://github.com/teal-sea/lean-checked-network/blob/main/acas/README.md):** AI agents built a Lean check of an alpha-beta-CROWN certificate for ACAS Xu network 1_1, property 1 (VNN-COMP), using TorchLean. Exact real semantics, standard axioms only; the ONNX importer is audited, not proved. No IEEE or aircraft claims.
- **Open source: [Hardy's Z function in mathlib](https://github.com/leanprover-community/mathlib4/pull/42963):** contributed the function and supporting results. [Merged by Bors on 10 October 2026](https://github.com/leanprover-community/mathlib4/pull/42963#issuecomment-6098344268).

## More tools and research

- **[omission-check](https://github.com/teal-sea/omission-check):** detects required replies and tool calls that never happen. Complements grounded-check's checks on spoken claims. [Run the bundled demo](https://github.com/teal-sea/omission-check#quick-start): Python 3.10+, no network, model or dependencies.
- **[convai-webhook-guard](https://github.com/teal-sea/convai-webhook-guard):** verifies ElevenLabs post-call webhook signatures before downstream systems trust the envelope; includes local signing tests.
- **[zeta-lab](https://github.com/teal-sea/zeta-lab) · [research site](https://zeta.teal-sea.com):** computational number theory and Lean 4 formalization around the Riemann zeta function, including a kernel-checked proof that all 29 critical-strip zeros up to height 100 are simple and on the critical line, alongside rigorous numerics and negative controls. Makes no claim of progress toward RH.
- **[too-soon](https://github.com/teal-sea/too-soon):** a small A/B-test utility using Wilson intervals, with no dependencies.

## Production background

My background is in operations. I've built and run systems that handle customer conversations, quotes, bookings, payments and fulfillment across several US markets.

That experience has made me conservative about what should be left to a model. Agents handle ambiguity and conversation; pricing, availability, payments, permissions and writes to operational systems sit behind controlled tools.

**Agents propose; systems decide what they're allowed to do.**

## Writing and products

- **[Why your AI startup dies at customer six](https://github.com/teal-sea/why-your-ai-startup-dies-at-customer-six):** an essay on reusable deployment architecture: the semantic layer, kinetic layer and rulebook.
- **[ModalRuns](https://modalruns.com):** a browser-based guitar practice app for exploring modes over changing harmony. Built, launched and monetized.

For a conversation about AI systems, voice automation, evaluation or verification, [get in touch on LinkedIn](https://www.linkedin.com/in/thomaslince) or visit [teal-sea.com](https://teal-sea.com/).
