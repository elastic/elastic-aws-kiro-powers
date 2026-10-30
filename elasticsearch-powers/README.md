# Elasticsearch (Elastic Search)

A Kiro Power that packages Elastic's **Search** skills for Elasticsearch. It helps an agent translate natural language to ES|QL, design indexes and mappings, ingest and reindex data, tune search relevance, optimize slow queries, run ML anomaly detection, and triage cluster health.

Built to the [Agent Plugins v1.0.0](https://agent-plugins.org/) specification, so it is portable across any conformant client.

## Skills

| Skill | What it does |
|-------|--------------|
| `elasticsearch-onboarding` | Gets developers new to Elasticsearch from zero to a working search experience — understand intent, map data, build search with best practices. |
| `elasticsearch-esql` | Executes ES\|QL queries to analyze logs, aggregate metrics, explore data, and build charts/dashboards from results. |
| `elasticsearch-index-design` | Designs and reviews index mappings for stated access patterns: field types, text+keyword multi-fields, `doc_values`, mapping-explosion avoidance, shard settings. |
| `elasticsearch-ingest` | Loads CSV/JSON files into indices via the bulk API with explicit mappings; verifies counts and mappings after ingest. |
| `elasticsearch-reindex` | Guides reindex for performance — local and remote, slicing, throttling, the task API; mapping changes and transforms during reindex. |
| `elasticsearch-search-relevance` | Improves relevance with query rules (pin/promote) and organic ranking tuning (`multi_match`, field boosts) grounded in the index mapping. |
| `elasticsearch-query-optimization` | Diagnoses slow Query DSL searches using the profiling API and proposes measured fixes (filter context, wildcard elimination, re-profile). |
| `elasticsearch-cluster-health` | Diagnoses a non-green cluster and surfaces the single most likely cause with remediation; replica-vs-primary impact and data-loss awareness. |
| `elasticsearch-anomaly-detection` | Creates and manages ML anomaly detection jobs and datafeeds via the API. |
| `elasticsearch-anomaly-detection-explainer` | Explains ML anomaly scores, model behavior, and result interpretation. |

## Prerequisites

- Elasticsearch 8.x / 9.x, Elastic Cloud Hosted, or Serverless (feature support varies per skill — see each `SKILL.md` `compatibility` note).
- The `elastic` CLI ≥ 0.2 with `stack es` support for skills that run queries against a cluster.

## Install in Kiro

1. Open the Kiro Powers UI → **Add Custom Power** → **Local Directory**.
2. Point it at the absolute path of this directory.
3. Click **Add**, then use **Try Power** on its detail page.

## Example prompts

- "Write an ES|QL query against my `logs-*` indices to count errors per service over the last 15 minutes."
- "Design a mapping for an e-commerce product catalog with full-text search and faceted filtering."
- "My search results aren't relevant — help me pin a specific product to the top for the query 'running shoes'."
- "This search is slow; here's the profile output — what should I fix?"

## Source and license

Skills are sourced from Elastic's [agent-skills](https://github.com/elastic/agent-skills) repository (`skills/elasticsearch`) and are licensed **Apache-2.0** by Elastic. This power repackages them as a Kiro Power without modifying the skill content.
