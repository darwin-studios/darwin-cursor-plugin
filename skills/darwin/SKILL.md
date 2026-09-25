---
name: darwin
description: Search for executable public AI capabilities and coordinate selected work through Darwin Actions. Use when a task needs an external capability, provider, service, or durable AI-to-AI workflow.
---

# Darwin Search and Act

1. Use `search` before starting external work. Present the returned provider, evidence, availability, terms, capability ID, and exact revision.
2. Preserve the chosen `capabilityId` and `capabilityRevision`; never reconstruct either from prose.
3. Use `get_account` and `list_search_history` only for requested account context and retained Search history; neither authorizes work.
4. Call `start_action` only after the user has selected the exact result and supplied the required inputs.
5. Persist `actionId` and each mutation `requestId` outside model prose. After a timeout or restart, recover with `get_action` or `list_actions`; do not create replacement work.
6. Treat the Action `status`, `actionRequired`, revision, and `availableActions` as authoritative. A model response is not proof of completion or authority.
7. Use `continue_action` only for ordinary communication requested by the current Action. It never implies approval, authentication, or payment.
8. Call `authenticate_session` only for an advertised authentication method. Open only first-party Darwin `webLink` values and never put credentials, authorization codes, or vault contents in prompts or tool arguments.
9. Call `pay_action` only for the exact current payment interaction and reviewed route. Never infer changed terms or place payment credentials in tool arguments.
10. Show the exact approval ID, revision, payload digest, expiry, and terms before `approve_action`. Never approve changed or inferred payloads.
11. Use `end_action` to request durable finish or cancellation. The caller never supplies the outcome; read the returned Action and continue polling with `get_action` until terminal.
