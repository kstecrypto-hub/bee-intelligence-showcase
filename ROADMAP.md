# Roadmap

The roadmap keeps robotics ambitious but sequenced. The current project is strongest in the intelligence layer; physical action should only follow validated sensing, evidence-grounded reasoning, and human-supervised decision support.

## 1. Evidence-Grounded Agricultural Intelligence

Continue hardening document ingestion, retrieval, knowledge graph support, citations, answer verification, trace persistence, and operational abstention.

Goal: make the system reliably distinguish general education from local operational claims.

## 2. Real-World Telemetry Integration

Extend physical telemetry ingestion while preserving raw payloads, normalized readings, device identity, assignment history, timestamps, and alert evidence.

Goal: make the intelligence layer depend on durable, inspectable sensor data rather than dashboard-only readings.

## 3. Live Beehive Deployment

Install sensors in live hives under controlled conditions and collect data over meaningful periods.

Goal: validate that the hardware and backend can handle real apiary conditions, not only bench or synthetic samples.

## 4. Computer Vision and Richer Sensing

Add visual inspection support and richer signal types where they clearly improve operator decisions.

Possible inputs include frame images, entrance activity, weight, external weather, and richer acoustic features. Each new sensor type should have a clear provenance and validation path.

## 5. Decision-Support Validation With Experts

Work with beekeepers, agronomists, and agricultural researchers to review outputs against real observations.

Goal: measure whether the system improves decision quality, catches overlooked factors, and communicates uncertainty appropriately.

## 6. Robotic Components for Narrow Hive Tasks

Introduce robotics only for tightly scoped, supervised tasks after the intelligence layer has been validated.

Examples of future narrow tasks could include sensor positioning, non-invasive inspection assistance, controlled sampling support, or simple repetitive apiary operations. These are future concepts, not current validated product claims.

## 7. Closed-Loop Sensing to Reasoning to Safe Action

Build a controlled loop where sensor evidence, operational history, expert rules, and human approval constrain any physical action.

Goal: ensure robotic behavior is bounded, explainable, reversible where possible, and never driven by unsupported model speculation.

## 8. Expansion Into Other Agricultural Verticals

Generalize the intelligence layer to other agricultural domains with similar needs:

- fragmented expert knowledge
- field telemetry
- operational history
- evidence-grounded decision support
- eventual physical automation

Beekeeping is the first proving ground, not the final market boundary.

## Stage Discipline

Robotics remains future work until the earlier stages prove:

- reliable sensing in real agricultural conditions
- trustworthy evidence grounding
- expert-reviewed decision support
- safe operator workflows
- clear failure handling and auditability
