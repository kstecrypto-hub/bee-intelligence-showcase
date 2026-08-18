# Example Question

This is a synthetic public example. It demonstrates the type of evidence-grounded interaction the system is designed for without exposing private prompts, source material, production schemas, or real sensor data.

## User

Using the sample telemetry and hive notes below, should I be worried about Hive H-17 today?

## Available Evidence

- Synthetic telemetry sample for Hive H-17:
  - brood-area temperature: 34.1 c
  - relative humidity: 67 percent
  - acoustic fundamental frequency: 142 hz
  - acoustic RMS: 0.19 normalized_adc
  - observed window: 2026-07-14T16:30:00Z to 2026-07-14T16:40:00Z
- Synthetic inspection note:
  - last inspection: 2026-07-12
  - summary: queen seen, capped brood present, moderate stores, no visible disease signs
- Synthetic alert state:
  - no active backend alerts
- Public-style source note placeholder:
  - brood temperature stability and inspection context matter more than a single reading when assessing colony state

## Desired Answer Behavior

The answer should:

- avoid diagnosing the hive from one short telemetry window
- cite the evidence used
- distinguish sensor observations from operational conclusions
- suggest concrete next checks for a beekeeper
- say what is not known
