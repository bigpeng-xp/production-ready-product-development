# Analysis Modes

## Release Levels

### Demo

Use Demo when the goal is only to prove that an idea can work.

Allowed:

- Hardcoded data
- Minimal error handling
- Simple UI
- Manual operation
- No long-term maintenance plan

Not suitable for real users.

### MVP

Use MVP when the goal is small-scope validation.

Required:

- Core workflow works
- Basic form validation
- Basic loading, empty, and error states
- Basic data persistence
- Basic authentication or permission checks when user data is involved
- Clear known limitations

### Beta

Use Beta when real users will use the product in a controlled environment.

Required:

- Complete core workflow
- Real backend and database
- Real authentication
- Role-based access control
- Logs
- Basic monitoring
- Test cases
- Feedback channel
- Deployment process
- Basic rollback path

### Production

Use Production when real users depend on the product for long-term operation.

Required:

- Stable deployment
- Security review
- Full permission model
- Complete error handling
- Audit logs
- Data backup
- Rollback plan
- Monitoring and alerts
- Performance optimization
- Documentation
- Acceptance checklist
- Maintenance plan

Never call something production-ready unless it satisfies production requirements.

## Risk Levels

### Low Risk

Examples:

- Personal tool
- Local demo
- Simple static page
- Single-user utility
- No sensitive data

### Medium Risk

Examples:

- Internal tool
- Small team workflow
- Non-sensitive business data
- Limited user base
- Recoverable operational mistakes

### High Risk

Examples:

- Customer-facing system
- Multi-user product
- Sensitive data
- Public internet access
- Payment
- File upload
- Long-term operation
- Third-party dependency

### Critical Risk

Examples:

- Government, medical, finance, education, or compliance-sensitive data
- Large-scale production system
- Data loss with serious consequences
- AI output that may affect rights, safety, money, diagnosis, or official decisions

Higher risk requires stricter security, testing, logging, backup, monitoring, and deployment standards.

## Lightweight Mode

Use Lightweight Mode when all conditions are true:

- The request is limited to one simple page, component, or small feature iteration.
- The workflow impact is local rather than system-wide.
- The target release level is Demo or MVP.
- The risk level is Low.
- No payment, sensitive personal data, multi-tenant logic, critical approval flow, or critical integration is involved.

In Lightweight Mode, output only:

1. Requirement understanding
2. Release-level and risk judgment
3. Page or component states: Normal, Loading, Empty, Error
4. Key edge cases
5. Validation, duplicate-submission, and permission notes when relevant
6. Concise implementation prompt
7. Short acceptance checklist

State:

"Lightweight Mode enabled. A full production-readiness review was skipped because the request is low-risk and narrowly scoped. Ask for a full review if needed."

Exit Lightweight Mode if hidden complexity appears.

## Full Production Review

Use Full Production Review when any condition is true:

- Real users will use the system.
- The feature affects core workflow.
- The system includes sensitive data.
- The system includes payment, permissions, file upload, multi-tenant data, or public release.
- The user asks for launch readiness, production standard, acceptance criteria, or implementation prompt.
- The product is Beta, Production, High Risk, or Critical Risk.
