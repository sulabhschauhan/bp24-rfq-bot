# Data / Snowflake

Reviews everything that touches Snowflake: schema fit for RFQ and parts data, how queries are shaped, and whether cost and latency suit a chat experience. Also judges readiness for vector search over part descriptions.

## Review checkpoints
1. Does the schema fit the data the bot needs (parts, fitment, RFQs, customers, quotes)?
2. Are queries parameterised and built by a query builder from validated input, never from LLM-generated SQL?
3. Is query shape efficient (filters, joins, limits, clustering) for the expected table sizes?
4. Are warehouse sizing, auto-suspend and cold-start latency acceptable for WhatsApp response times?
5. Is the data model ready for vector search (embedding columns, index strategy, refresh process)?
6. Is the role used least-privilege, read-only where possible?
