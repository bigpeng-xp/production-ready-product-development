# AI Product Evaluation Loop

For AI products, production readiness must include an evaluation and regression loop.

Do not treat an AI system as production-ready only because it gives plausible answers. It must answer consistently, safely, measurably, and with a repeatable quality-evaluation process.

Any AI product without a repeatable evaluation loop should be considered at risk of silent quality regression.

## Required Checks

Check:

- Golden dataset for recurring evaluation
- Task-based benchmark coverage for core user intents
- Regression testing before every prompt, model, retrieval, or policy update
- Hallucination rate tracking
- Refusal rate tracking
- Citation accuracy or evidence-grounding checks when applicable
- Retrieval hit quality
- Source traceability
- Context window failure cases
- Prompt injection resistance
- Sensitive content filtering
- User feedback collection such as thumbs-up, thumbs-down, issue tagging, or correction notes
- Failure case review and labeling workflow
- Prompt version rollback mechanism
- Model version rollback mechanism
- Knowledge base version rollback mechanism
- Safety policy regression checks
- Human-review escalation path for high-risk outputs
- Abuse prevention and rate limiting
- Cost monitoring by model, route, user, or tenant
- Latency monitoring
- Conversation log policy and retention policy

## Golden Dataset

Define:

- User intent category
- Input question or task
- Expected answer characteristics
- Required evidence or citation
- Unacceptable answer patterns
- Risk level
- Pass/fail scoring rule

The golden dataset should cover common tasks, high-value tasks, edge cases, adversarial inputs, and previous production failures.

## Metrics

Track when relevant:

- Answer acceptance rate
- Hallucination rate
- Citation correctness rate
- Retrieval precision
- Retrieval recall
- Refusal rate
- Unsafe answer rate
- Escalation rate
- User correction rate
- Average latency
- Cost per successful task

## Release Gate

Before release, require:

- No critical regression on golden dataset
- No unresolved high-risk safety issue
- Prompt/model/knowledge-base version recorded
- Rollback path confirmed
- Monitoring and feedback collection enabled
