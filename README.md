# Thomas Lince

I build production AI agents, voice automation and tools for checking whether their outputs are correct.

[Website](https://teal-sea.com/) · [LinkedIn / contact](https://www.linkedin.com/in/thomaslince)

## Selected work

- **Production agent evaluation — [grounded-check](https://github.com/teal-sea/grounded-check):** checks a voice agent's claims against the data its tools returned. [Run the keyless demo](https://github.com/teal-sea/grounded-check#usage).
- **Agent orchestration — [ostoyae](https://github.com/teal-sea/ostoyae):** runs coding agents over a graph that grows as they find work. [Try the scripted demo](https://github.com/teal-sea/ostoyae#try-it), with no API key or model calls.
- **Formal verification — [lean-checked-network](https://github.com/teal-sea/lean-checked-network):** Lean 4 proves a trained, frozen integer-weight network adds modulo 113 correctly on all 12,769 inputs, including 6,385 held out from training. The circle-only mechanism is also checked; a planted fault is rejected. These proofs concern the specified network and finite task.
- **Open source — [Hardy's Z function in mathlib](https://github.com/leanprover-community/mathlib4/pull/42963):** contributed the function and supporting results. [Merged by Bors on 10 October 2026](https://github.com/leanprover-community/mathlib4/pull/42963#issuecomment-6098344268).

## More tools and research

- **[omission-check](https://github.com/teal-sea/omission-check):** detects required replies and tool calls that never happen. Complements grounded-check's checks on spoken claims. [Run the bundled demo](https://github.com/teal-sea/omission-check#quick-start): Python 3.10+, no network, model or dependencies.
- **[convai-webhook-guard](https://github.com/teal-sea/convai-webhook-guard):** verifies ElevenLabs post-call webhook signatures before downstream systems trust the envelope; includes local signing tests.
- **[zeta-lab](https://github.com/teal-sea/zeta-lab) · [research site](https://zeta.teal-sea.com):** computational number theory and Lean 4 formalization, combining checked proofs, rigorous numerics and negative controls around the Riemann zeta function. Makes no claim of progress toward RH.
- **[too-soon](https://github.com/teal-sea/too-soon):** a small A/B-test utility using Wilson intervals, with no dependencies.

## Production background

My background is in operations. I've built and run systems that handle customer conversations, quotes, bookings, payments and fulfillment across several US markets.

That experience has made me conservative about what should be left to a model. Agents handle ambiguity and conversation; pricing, availability, payments, permissions and writes to operational systems sit behind controlled tools.

**Agents propose; systems decide what they're allowed to do.**

## Writing and products

- **[Why your AI startup dies at customer six](https://github.com/teal-sea/why-your-ai-startup-dies-at-customer-six):** an essay on reusable deployment architecture — the semantic layer, kinetic layer and rulebook.
- **[ModalRuns](https://modalruns.com):** a browser-based guitar practice app for exploring modes over changing harmony. Built, launched and monetized.

For a conversation about AI systems, voice automation, evaluation or verification, [get in touch on LinkedIn](https://www.linkedin.com/in/thomaslince) or visit [teal-sea.com](https://teal-sea.com/).
