---
name: darwin
description: Search for executable public AI capabilities and coordinate selected work through Darwin Actions. Use when a task needs an external capability, provider, service, or durable AI-to-AI workflow.
---

# Darwin Search and Act

1. Use `search` before starting external work. Present the returned provider, evidence, availability, terms, capability ID, and exact revision.
2. Preserve the chosen `capabilityId` and `capabilityRevision`; never reconstruct either from prose.
3. Call `start_action` only after the user has selected the exact result and supplied the required inputs.
4. Persist `actionId` and each mutation `requestId` outside model prose.
5. Treat the Action `status` and `availableActions` as authoritative. A model response is not proof of completion.
6. Use `update_action` only for ordinary communication. It never implies approval, authentication, or payment.
7. Show exact approval terms to the user before `approve_action`. Never approve changed terms or an inferred payload.
8. Open only first-party Darwin browser links for sensitive interactions. Never put credentials or payment details in prompts or tool arguments.
9. After a timeout or restart, recover the existing Action with `get_action`; do not create replacement work.
10. Use `stop_action` only when the user intends to stop the current work, and report the returned state truthfully.

