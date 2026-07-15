Addendum 18 — Suggestion Bus Protocols (Draft)
Status: Draft
Version: 0.1
License: CC0 1.0 Universal

Abstract
The Suggestion Bus is the Hive’s strategic guidance channel.
Unlike the Telemetry Bus (metrics) and Request Bus (actions), the Suggestion Bus carries non‑binding advisory insights generated primarily by watcher nodes.

This addendum defines the Suggestion Bus Protocol (SBP) — a structured, safety‑aware, multi‑domain communication protocol that governs how suggestions are generated, transmitted, filtered, throttled, and interpreted across Vector AIs, Reflex AIs, arbitration tiers, and multi‑hive ecosystems.

The SBP ensures that suggestions:

never override domain authority

never bypass safety

never trigger cascades

never amplify drift

remain advisory

remain structured

remain predictable

1. Purpose of the Suggestion Bus Protocol
The SBP provides:

a standardized suggestion format

watcher‑safe communication rules

arbitration‑compatible advisory flows

reflex‑aware throttling

drift‑aware filtering

cascade‑aware suppression

multi‑hive suggestion coordination

Suggestions become safe, structured, and interoperable.

2. Suggestion Bus Characteristics
The Suggestion Bus is defined by four core properties:

Code
Non-binding
Advisory-only
Pattern-driven
Safety-aware
Suggestions inform decisions but never command them.

3. Suggestion Packet Structure (Unified Suggestion Schema)
Every suggestion follows the Unified Suggestion Schema (USS):

Code
{
  "source": "<watcher-or-AI-id>",
  "domain": "<domain-of-origin>",
  "timestamp": "<ISO-8601>",
  "insight": "<textual-advisory>",
  "confidence": <float>,
  "risk": {
    "drift": <float>,
    "cascade": <float>,
    "watcher_risk_level": <int>
  },
  "extensions": { ... }
}
Field Definitions
source
Watcher node or Vector AI generating the suggestion.

domain
Domain associated with the insight.

insight
The advisory message.

confidence
A numerical estimate of insight reliability.

risk
Risk metadata compatible with watcher scoring.

extensions
Optional domain‑specific fields.

4. Suggestion Types
The SBP defines five suggestion types:

Code
1. Stability Suggestions
2. Evolution Suggestions
3. Optimization Suggestions
4. Boundary Suggestions
5. Ecosystem Suggestions
4.1 Stability Suggestions
Focus on maintaining operational stability.

4.2 Evolution Suggestions
Long‑term improvement or redesign.

4.3 Optimization Suggestions
Performance tuning once stability is ensured.

4.4 Boundary Suggestions
Domain boundary enforcement or refinement.

4.5 Ecosystem Suggestions
Cross‑hive or multi‑domain insights.

5. Suggestion Flow Rules
5.1 Non‑Binding
Suggestions cannot force actions.

5.2 Domain Respect
Suggestions cannot override domain authority.

5.3 Safety Priority
Suggestions must never contradict Safety AI constraints.

5.4 Arbitration Compatibility
Suggestions may inform arbitration but cannot bypass it.

5.5 Reflex Compatibility
Suggestions must not interfere with reflex timing or containment.

6. Suggestion Throttling Modes
The SBP integrates watcher throttling (Addendum 13):

Code
Normal   — full suggestion flow
Reduced  — rate-limited suggestions
Minimal  — safety-only suggestions
Silent   — no suggestions during critical instability
6.1 Throttling Triggers
drift escalation

cascade detection

arbitration conflicts

cross‑hive anomalies

watcher risk level ≥ 3

7. Suggestion Filtering
Suggestions may be filtered by:

7.1 Reflex Filters
Prevent suggestions that destabilize reflex loops.

7.2 Arbitration Filters
Suppress suggestions that contradict tier priorities.

7.3 Bus Filters
Remove suggestions that amplify drift or cascades.

7.4 Watcher Filters
Suppress low‑confidence or high‑risk suggestions.

8. Suggestion Interpretation Rules
Vector AIs interpret suggestions using:

8.1 Domain Context
Suggestions must be evaluated within domain boundaries.

8.2 Risk Context
High‑risk suggestions require arbitration review.

8.3 Confidence Context
Low‑confidence suggestions may be ignored.

8.4 Stability Context
Suggestions that reduce stability are deprioritized.

9. Suggestion Bus Safety Guarantees
The SBP enforces:

9.1 No Command Authority
Suggestions cannot issue commands.

9.2 No Override Authority
Suggestions cannot override domain decisions.

9.3 No Cascade Amplification
Suggestions must not increase cascade risk.

9.4 No Drift Amplification
Suggestions must not increase drift risk.

9.5 No Cross‑Hive Overreach
Suggestions cannot force cross‑hive actions.

10. Multi‑Hive Suggestion Protocol
In multi‑hive ecosystems:

10.1 Watcher‑to‑Watcher Suggestions
Watcher nodes exchange ecosystem insights.

10.2 Cross‑Hive Suggestion Routing
Suggestions may be routed across hives with:

risk metadata

confidence metadata

domain boundaries preserved

10.3 Cross‑Hive Suggestion Filtering
High‑risk suggestions may be quarantined.

10.4 Ecosystem Suggestion Safety
No hive may override another hive’s domain.

11. Suggestion Bus Failure Modes
11.1 Suggestion Flooding
Too many suggestions → throttling activates.

11.2 Suggestion Drift
Suggestions become unstable → watcher filters activate.

11.3 Suggestion Cascade
Suggestions amplify cascades → bus suppression activates.

11.4 Suggestion Misalignment
Suggestions contradict domain boundaries → arbitration filters activate.

12. Implementation Notes (v1.2 Preview)
Early prototypes will include:

suggestion schema validators

watcher suggestion throttling modules

arbitration suggestion filters

reflex suggestion dampening logic

multi‑hive suggestion routers

suggestion risk scoring models

These will be refined in v1.2 and expanded in v1.3.

13. Status
This addendum is an early draft.
Feedback, extensions, and domain‑specific suggestion models are welcome.
