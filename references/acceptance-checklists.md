# Acceptance Checklists

Generate a concise checkbox-style acceptance checklist based on product type, target release level, and risk level.

Do not output a generic checklist. The checklist must reflect the current product context.

## Universal Production Acceptance Items

Use relevant items:

- [ ] Core workflow can be completed without dead ends
- [ ] Loading, empty, and error states are covered on key pages
- [ ] Key forms include validation and clear error messages
- [ ] Duplicate submission is prevented
- [ ] Login expiration is handled
- [ ] Backend enforces real permissions
- [ ] Sensitive fields are masked or protected where needed
- [ ] Key APIs define success and failure responses
- [ ] Important operations are logged
- [ ] Test cases cover happy path, failure path, permissions, and edge cases
- [ ] Deployment, rollback, monitoring, and backup responsibilities are clear
- [ ] Known limitations are explicitly documented

## WeChat Mini Program / MVP

- [ ] Core workflow can be completed without dead ends
- [ ] Loading, empty, and error states are covered on key pages
- [ ] Weak-network behavior is handled with clear feedback
- [ ] Required permissions are requested at the correct moment
- [ ] Permission refusal has a recovery path
- [ ] Safe-area layout works on major devices
- [ ] Click targets are large enough for touch use
- [ ] tabBar and navigation/back behavior are clear
- [ ] Package size and subpackage strategy are acceptable
- [ ] No obvious mini program review rule violation
- [ ] Test version or experience version process is clear

## Admin Dashboard / Beta Or Production

- [ ] RBAC role model is defined
- [ ] Menu, page, button, data, and field permissions are enforced
- [ ] Backend authorization protects all sensitive operations
- [ ] Tables have loading, empty, error, and pagination states
- [ ] Search, filter, sort, import, export, and batch operations handle failure
- [ ] Export behavior is permission-controlled and logged
- [ ] Delete operations require confirmation and support soft delete or recovery when needed
- [ ] Sensitive data is masked
- [ ] Audit logs record who did what and when
- [ ] Login expiration is handled without data loss

## SaaS Platform / Production

- [ ] Tenant isolation is enforced at backend and database levels
- [ ] Organization, member, and role management are defined
- [ ] Cross-tenant access is impossible through API or UI
- [ ] Tenant-level audit logs exist
- [ ] Usage limits and plan boundaries are enforced
- [ ] Billing or subscription behavior is documented when relevant
- [ ] Tenant data export and deletion policies are defined
- [ ] Customer-specific configuration does not break shared logic
- [ ] Monitoring can identify tenant-specific incidents
- [ ] Backup and recovery plan covers tenant data

## AI Tool / Beta Or Production

- [ ] Golden dataset exists for recurring evaluation
- [ ] Regression testing runs before prompt, model, retrieval, or policy changes
- [ ] Hallucination risk is measured or manually reviewed
- [ ] Citation or evidence-grounding is checked when applicable
- [ ] User feedback is collected and categorized
- [ ] Prompt, model, and knowledge-base versions are tracked
- [ ] Rollback path exists for prompt, model, and knowledge-base changes
- [ ] Unsafe, sensitive, or high-risk outputs have escalation or fallback
- [ ] Abuse prevention and rate limiting are enabled
- [ ] Latency and model cost are monitored

## Data Visualization Dashboard / Production

- [ ] Dashboard works at target display resolution
- [ ] Fullscreen mode works
- [ ] Auto-refresh interval is defined
- [ ] Data source and update time are visible
- [ ] Charts have loading, empty, and error states
- [ ] API failure fallback is clear
- [ ] Long-running memory stability is considered
- [ ] Alarm colors and labels are readable from expected viewing distance
- [ ] Historical and real-time data behavior is clear
- [ ] Projection or display device compatibility is checked

## API Service / Production

- [ ] Authentication and authorization are enforced
- [ ] Request validation is centralized
- [ ] Error code and response format are consistent
- [ ] Rate limiting exists
- [ ] Idempotency is defined for retry-sensitive APIs
- [ ] Database transactions protect important writes
- [ ] Logs and tracing can diagnose failures
- [ ] Health checks exist
- [ ] API documentation is available
- [ ] Deployment rollback and database migration strategy are clear
