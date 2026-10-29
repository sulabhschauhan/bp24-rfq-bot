# Architect

Reviews system design for the RFQ bot: how the webhook, FastAPI service, Redis session state, Snowflake and the WhatsApp Cloud API fit together. Focuses on clean service boundaries and on what happens when a part fails.

## Review checkpoints
1. Are service boundaries clear (webhook intake, conversation logic, catalogue lookup, outbound messaging)?
2. Is conversation state held in Redis with explicit TTLs, and is it recoverable after a restart?
3. Is webhook handling idempotent against Meta's duplicate and out-of-order deliveries?
4. Are failure modes defined for Snowflake, Redis, the LLM and the WhatsApp API being down or slow?
5. Is there a human-escalation path when automation fails or confidence is low?
6. Is the design the simplest one that meets MVP1, with no speculative components?
