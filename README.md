# pgvision

PostgreSQL anomaly detection that explains root cause.

## The idea

Existing PostgreSQL monitoring tools tell you what changed — a metric spiked, a threshold was crossed, connections went high. They don't tell you why. An on-call engineer still has to open pg_stat_activity, pg_stat_statements, pg_locks, and pg_stat_bgwriter and manually correlate them to understand what actually happened.

pgvision closes that gap. When an anomaly is detected, it automatically collects a full PostgreSQL context snapshot — active sessions, top queries, locks, background writer stats, WAL pressure — and uses an LLM to produce a structured root cause report. The engineer reads one paragraph instead of investigating for 40 minutes.

Everything else the project will ship — time-series forecasting, persistence-based confirmation, semantic incident memory — is in service of that one outcome: turning "something broke" into "this is why it broke and what to do about it."

## License

Apache 2.0.
