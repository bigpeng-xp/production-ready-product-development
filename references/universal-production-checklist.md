# Universal Production Checklist

## Product Value

Clarify:

- What problem does this product solve?
- Who uses it?
- Why do they need it?
- What is the core user task?
- What is the success metric?
- What is the minimum complete workflow?

Avoid building a collection of functions without a product loop.

## User Roles And Permissions

Identify possible roles:

- Guest
- Normal user
- Operator
- Reviewer
- Admin
- Organization admin
- Super admin
- Developer or maintainer

For each role, define:

- Accessible pages
- Viewable data
- Allowed actions
- Hidden or masked sensitive fields
- Approval authority
- Export authority
- Delete authority

Frontend permission control is only for user experience. Real permission control must be enforced by the backend.

## Business Workflow

For each core workflow, define:

- Entry point
- User input
- System processing
- Result output
- Save, edit, delete, export, and share behavior
- Failure recovery path
- Whether the workflow can be paused, retried, cancelled, or rolled back

Do not only describe the happy path. Every workflow must include abnormal paths.

## Page And Component States

Every major page or component should include:

- Normal state
- Loading state
- Empty state
- Error state
- Success state
- Disabled state
- No-permission state
- Offline or weak-network state when relevant

For each state, define:

- What the user sees
- What action is available
- What feedback is shown
- Whether retry, cancel, refresh, or return is supported

A page without empty and error states is usually still demo-level.

## Edge Cases

Check:

- Repeated button clicks
- Duplicate submission
- Network timeout
- API failure
- Login expiration
- Permission denied
- Empty data
- Extremely long text
- Special characters
- Emoji
- File too large
- Wrong file type
- Upload interruption
- Page refresh
- Back navigation
- Concurrent editing
- Third-party service failure
- Mobile screen adaptation
- Weak network
- Frontend and backend data inconsistency

## Data Model

For each entity, define:

- Entity name
- Field name
- Field type
- Required or optional
- Default value
- Validation rule
- Business meaning
- Index or uniqueness requirement
- Relationship with other entities

Production data models usually include:

- id
- created_at
- updated_at
- created_by
- updated_by
- status
- deleted_at or deleted_flag
- version when history matters

For important operations, include operation logs.

## API Contract

For each API, define:

- Endpoint
- HTTP method
- Request parameters
- Request body
- Response structure
- Error codes
- Pagination format
- Authentication requirement
- Permission requirement
- Timeout behavior
- Retry behavior
- Idempotency requirement

Recommended success response:

```json
{
  "code": 0,
  "message": "success",
  "data": {}
}
```

Recommended list response:

```json
{
  "code": 0,
  "message": "success",
  "data": {
    "list": [],
    "total": 0,
    "page": 1,
    "pageSize": 10
  }
}
```

Recommended failed response:

```json
{
  "code": 40001,
  "message": "No permission",
  "data": null
}
```

## Security

Check:

- Authentication
- Token expiration
- Token refresh
- Backend authorization
- Data permission
- Field-level permission
- Sensitive information masking
- Password encryption
- Input validation
- File validation
- XSS prevention
- SQL injection prevention
- CSRF consideration when relevant
- Rate limiting
- Duplicate submission protection
- Critical operation confirmation
- Audit logs

Never claim a system is secure if only frontend restrictions exist.

## Performance

Check:

- First screen loading time
- Lazy loading
- Image compression
- Pagination
- Virtual scrolling for long lists
- Request caching
- Debounce and throttle
- Bundle size
- CDN strategy
- API response time
- Database indexes
- Large file upload performance
- Weak network behavior

## Testing

Generate test cases for:

- Happy path
- Empty state
- Loading state
- Error state
- Permission denied
- Invalid input
- Duplicate submission
- Network failure
- Weak network
- Mobile adaptation
- Boundary values
- Concurrent operation
- Data export
- Login expiration
- Regression testing

Use this format:

| Test Case | Operation | Expected Result | Priority |
| --------- | --------- | --------------- | -------- |

## Deployment And Operations

Analyze:

- Local development environment
- Testing environment
- Staging environment
- Production environment
- Environment variables
- Build process
- Deployment process
- Rollback plan
- Database migration
- Backup strategy
- Error monitoring
- Operation logs
- User feedback channel
- Third-party service dependency
- Cost risk

A production feature is not complete without deployment and recovery considerations.

## Maintenance

Check:

- Clear directory structure
- Component reuse
- API abstraction
- Error handling abstraction
- Permission abstraction
- Type safety
- Constants management
- Configuration management
- Documentation
- Version history
- Onboarding notes for future developers

Avoid one huge file with mixed UI, business logic, request code, and data transformation logic.
