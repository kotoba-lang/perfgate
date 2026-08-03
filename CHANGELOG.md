# Changelog

## 0.1.0 — 2026-08-03

Initial implementation.

- `observation` — one measured arm, refusing an empty source or a machine
  descriptor that does not validate.
- `qualify` — seven named refusals, including `:not-separated-from-noise`
  (a 6% improvement whose arms overlap within their own spread) and
  `:provenance-too-weak` (a claim resting on `machine.core/portable-64`).
- `claim` / `verify-claim` — an unqualified result gets no artifact at all;
  a sealed one detects edits to either a sample or the headline number.
- `stale-on?` / `applicable` — a claim records the fingerprint of the machine
  it was proved on, so a system can carry its own list of retired
  optimizations instead of accumulating fossils.
- Statistics are mean / sample stdev / median / p95, and the separation test
  is documented as a heuristic rather than a significance test.

18 tests, 54 assertions.
