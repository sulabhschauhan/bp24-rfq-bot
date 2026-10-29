# QA

Reviews test coverage and test design. Pushes for tests built from real customer messages rather than invented examples, and for the awkward edge cases WhatsApp users produce.

## Review checkpoints
1. Is there coverage for the core flows: intake, clarification, catalogue match, escalation?
2. Are tests driven by a real corpus of past RFQ messages, not only synthetic ones?
3. Are edge cases covered: typos, mixed Arabic/English, VINs, part numbers, photos or voice notes, multi-part requests?
4. Is Pydantic validation tested with malformed, hostile and empty LLM output?
5. Are Snowflake, Redis, the LLM and WhatsApp mocked cleanly, with failure-path tests?
6. Are duplicate and out-of-order webhook deliveries tested?
