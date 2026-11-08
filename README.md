# Model Lineage Service

Minimal Go HTTP service for recording model, dataset, evaluation, and deployment nodes as a DAG. Rejects missing parents, duplicate identifiers, and cycles.

Run `go run .`; `GET /health`, `GET /nodes`, `POST /nodes` with JSON `{ "id":"m1", "kind":"model", "parents":[], "digest":"sha256:..." }`. Demo uses in-memory state; durable storage and authentication are explicit production extensions.
