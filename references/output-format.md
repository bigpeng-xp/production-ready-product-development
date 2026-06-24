# Output Format

Use Lightweight Mode output only when the request is low-risk and narrowly scoped.

Use Full Production Review output for medium-risk, high-risk, critical, launch-facing, multi-user, data-sensitive, or long-term products.

## Lightweight Mode Output

Start with:

"Lightweight Mode enabled. A full production-readiness review was skipped because the request is low-risk and narrowly scoped. Ask for a full review if needed."

Then output:

1. Requirement Understanding
2. Release Level And Risk
3. Page Or Component States
4. Key Edge Cases
5. Validation And Permission Notes
6. Concise Implementation Prompt
7. Short Acceptance Checklist
8. Readiness Judgment

## Full Production Review Output

### 1. Requirement Understanding

Summarize what the user wants to build.

### 2. Product Type Identification

Identify product type.

If multiple types are involved, list all terminals and their responsibilities.

### 3. Target Release Level

Classify as Demo, MVP, Beta, or Production. Explain why.

### 4. Risk Level

Classify as Low, Medium, High, or Critical. Explain the main risks.

### 5. Current Gaps

Group missing items by Product, UX, Data, API, Security, Testing, Deployment, and Maintenance.

### 6. User Roles And Permissions

Provide role matrix.

| Role | View | Create | Edit | Delete | Export | Approve |
| ---- | ---- | ------ | ---- | ------ | ------ | ------- |

### 7. Core Business Workflow

Describe the main workflows. Include both happy path and abnormal path.

### 8. Page And State Matrix

| Page / Component | Normal | Loading | Empty | Error | No Permission | Disabled |
| ---------------- | ------ | ------- | ----- | ----- | ------------- | -------- |

### 9. Data Model Draft

| Entity | Field | Type | Required | Meaning |
| ------ | ----- | ---- | -------- | ------- |

### 10. API Contract Draft

| API | Method | Params | Response | Permission | Notes |
| --- | ------ | ------ | -------- | ---------- | ----- |

### 11. Product-Type-Specific Requirements

Apply the corresponding checklist based on product type.

### 12. Security And Reliability Review

List security requirements and reliability requirements.

### 13. Test Cases

| Test Case | Operation | Expected Result | Priority |
| --------- | --------- | --------------- | -------- |

### 14. Deployment And Operation Plan

Include environments, build, deployment, rollback, monitoring, logs, and backup.

### 15. Development Task Breakdown

Split tasks into MVP must-have, Beta required, Production required, and optional optimization.

### 16. Final Implementation Prompt

Provide a clear prompt that the user can give to Codex or another coding agent.

The implementation prompt must include product type, target release level, required features, page states, data model, API contract, permission requirements, testing requirements, and acceptance criteria.

### 17. Acceptance Checklist

Generate a practical checkbox-style checklist based on product type, release level, and risk level.

### 18. Final Readiness Judgment

Conclude with one explicit judgment:

- Not ready beyond demo
- Good enough for personal use
- Good enough for internal trial
- Good enough for controlled external beta
- Ready for production with listed assumptions
- Not recommended for production until critical gaps are fixed

Do not use vague conclusions.
