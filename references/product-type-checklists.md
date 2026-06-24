# Product-Type Checklists

## WeChat Mini Program / Mobile Mini Program

Check:

- WeChat login
- Phone number authorization
- Privacy policy popup
- User authorization failure handling
- Mini program review rules
- Package size limit
- Subpackage strategy
- First screen loading speed
- tabBar structure
- Page navigation and back behavior
- Pull-down refresh
- Pull-up loading
- Weak-network feedback
- Sharing limitation
- Subscription message permission
- Location permission
- Camera permission
- Album permission
- Map SDK permission
- Payment requirement and merchant account
- Test version, experience version, and production release process
- Device compatibility
- Touch target size
- Safe area adaptation
- Offline or poor network fallback

Mini program products must not be reviewed only as ordinary web pages.

## Mobile H5

Check responsive layout, mobile browser compatibility, WeChat built-in browser behavior, Safari behavior, Android browser behavior, touch gestures, soft keyboard issues, scroll behavior, URL sharing, login persistence, deep links, mobile network loading speed, image compression, viewport adaptation, form submission recovery, and payment or third-party jump behavior when relevant.

## PC Web App

Check responsive layout, browser compatibility, routing design, direct URL access, refresh recovery, CORS, HTTPS, static asset caching, white-screen monitoring, SEO when relevant, keyboard accessibility, table interaction, export behavior, and large/small screen compatibility.

## Official Website / Landing Page

Check first-screen value proposition, clear CTA, SEO title and description, responsive design, loading speed, image compression, contact form validation, analytics, conversion tracking, accessibility, browser compatibility, legal pages, privacy policy, and terms of service when needed.

The goal is not only visual beauty, but conversion and trust.

## Admin Dashboard / Management System

Check RBAC role model, menu permission, page permission, button permission, data permission, field permission, audit logs, login expiration, admin account management, advanced search, filtering, sorting, pagination, batch operation, import, export, data dictionary, delete confirmation, soft delete or recovery, approval workflow, operation history, sensitive data masking, error message clarity, table empty state, and table loading state.

Admin systems focus on secure, accurate, traceable data management.

## Data Visualization Dashboard

Check 1920x1080 large-screen adaptation, fullscreen mode, auto refresh, refresh interval, real-time data source, historical data switch, chart empty/loading/error states, long-running memory stability, data anomaly fallback, alarm highlight, color readability, font readability from distance, map zoom and boundary behavior, time display, data source display, API failure fallback, and projection/display device compatibility.

A dashboard must remain stable during long-term display.

## SaaS Platform

Check tenant isolation, organization management, role configuration, team member invitation, customer-level permissions, subscription plan, usage limit, billing when relevant, data export, data deletion, customer-specific configuration, multi-tenant database design, tenant-level audit logs, and prevention of one customer accessing another customer's data.

For SaaS, tenant isolation is a critical requirement.

## Mobile App

Check iOS and Android differences, app store review requirements, permission request timing, push notification permission, version update strategy, offline mode, crash reporting, startup time, deep links, device compatibility, status bar and safe area, background behavior, local storage, sensitive data storage, logout, account deletion, and privacy policy.

## AI Tool / AI Agent / Intelligent QA System

Check prompt version management, model version management, hallucination risk, evidence citation, source traceability, knowledge base update mechanism, retrieval quality, context window limit, sensitive content filtering, user data storage, conversation log policy, human review, fallback answer, response latency, model cost, rate limiting, abuse prevention, evaluation dataset, regression testing after prompt or model updates, and user feedback on answer quality.

Also read `ai-product-evaluation-loop.md`.

## Data Collection / Crawler System

Check source management, source status, collection schedule, retry strategy, failure logs, task queue, anti-crawling risk, rate control, data deduplication, data cleaning, normalization, source traceability, manual review, abnormal value marking, incremental collection, full collection, image storage, attachment storage, data versioning, interruption recovery, third-party website rule-change risk, and legal/compliance considerations.

A data collection system must know not only what was collected, but when, from where, whether it succeeded, and whether the data is trustworthy.

## API Service / Backend Platform

Check API authentication, rate limiting, request validation, response standard, error code standard, logging, tracing, database transactions, idempotency, retry safety, API versioning, documentation, load testing, health checks, monitoring, deployment rollback, database migration, backup and restore, security headers, and CORS strategy.

## Internal Tool

Check user scope, access control, whether VPN or intranet is required, basic audit logs, data export, data modification history, simple but clear UI, low maintenance cost, documentation, and manual recovery path.

Internal tools can be simpler than public products, but must still protect data and avoid operational mistakes.

## Research Prototype / Academic Demo

Check reproducibility, input data format, output data format, algorithm version, experiment configuration, random seed, dataset path, result export, visualization clarity, error reporting, manual correction mechanism, paper figure export, experiment log, and hardware/environment description.

Academic prototypes do not always need production-level user management, but must support reproducibility and result traceability.

## IoT / Hardware-Connected System

Check device connection state, disconnection handling, data synchronization, timestamp alignment, sensor error, data loss, reconnection strategy, device permissions, firmware or protocol version, real-time display delay, local cache, upload retry, device calibration, manual correction, hardware fault feedback, and operation logs.

Hardware-connected systems must treat disconnection and data inconsistency as normal scenarios, not rare exceptions.

## Multi-Terminal Product

Check same account across terminals, data synchronization, permission consistency, cross-terminal notification, design consistency, function differences by terminal, web/mini-program/admin/app data consistency, conflict handling, unified API contract, unified user identity, and unified logging/monitoring.

Multi-terminal products must define what each terminal is responsible for.
