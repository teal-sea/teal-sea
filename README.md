I build AI agents that run a real business, and I run the business they run.

The main one answers a company's phone line in production and carries the sale end to end: discovery, a quote off live rate logic, the close, the deposit. The voice is a vendor; the pricing, the availability and the booking write stay on my endpoints.

Here:

- [grounded-check](https://github.com/teal-sea/grounded-check): audits what a voice agent said against what its tools actually returned, with a deterministic pass for numbers and an LLM judge fed the tool timeline as ground truth. Born from a quality monitor that flagged around 35 correct quotes as fabricated.
- [convai-webhook-guard](https://github.com/teal-sea/convai-webhook-guard): verify ElevenLabs post-call webhooks before you trust them. Constant-time HMAC check, plus a sign command so you can test your own receiver with curl.
- [too-soon](https://github.com/teal-sea/too-soon): refuses to call an A/B test winner on a sample too small to carry one.
- [Why your AI startup dies at customer six](https://github.com/teal-sea/why-your-ai-startup-dies-at-customer-six): an essay on why bespoke deployments stop scaling, and the three-layer split that fixes it.

Also: [modalruns.com](https://modalruns.com), a browser guitar practice app. Built, launched, monetized.
