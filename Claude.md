
# Ravenwoods Business OS

## Project Mission

Build a reliable business management and financial operating system for two independent businesses:

- RAVENWOODS
- AYOS NA

The system has one CEO with access to both businesses and a separate AYOS NA operator who manages AYOS NA's day-to-day finances and operations.

The objective is to give management clear visibility over cash, projects, collections, expenses, payables, payroll, and profitability.

## Architecture

Preferred initial technology:
- Google Apps Script backend
- Google Sheets database
- HTML, CSS, and JavaScript frontend
- Responsive web application

Do not introduce paid infrastructure or a different database without presenting the technical justification and cost first.

## Non-negotiable Business Rules

1. Every business record must have a company_id.
2. Ravenwoods and AYOS NA financial records must remain separate.
3. The CEO can access both businesses.
4. The AYOS NA operator can access AYOS NA only.
5. All permissions must be enforced server-side.
6. Receivables are not cash until collected.
7. Payables are not cash payments until settled.
8. Bank-to-bank transfers are not income or expenses.
9. Intercompany funding must be recorded separately.
10. Payroll expense and payroll cash payment must be distinguished.
11. Historical opening balances must not be counted twice.
12. Posted financial records must be voided or reversed, never silently deleted.

## Development Rules

- Do not build the entire application in one step.
- Work in small, independently testable phases.
- Inspect existing project files before changing them.
- Do not overwrite the old CEO Dashboard or PAYROLL applications.
- Do not use real financial data in development testing.
- Keep frontend, backend, database and business logic modular.
- Validate all important data on the server.
- Protect shared database writes.
- Use unique IDs and maintain audit logs.
- Avoid storing the entire application database in one JSON cell.
- Do not assume authentication works until tested with both actual users.

## Working Method

Before implementing a major feature:

1. Explain the proposed approach.
2. Identify dependencies and risks.
3. Obtain approval for major architecture changes.
4. Implement the approved scope.
5. Test the implementation.
6. Document what changed and how to verify it.

Do not silently change agreed accounting rules, database structures, authentication assumptions or permission boundaries.

## Documentation

Maintain these documents as the project develops:

- docs/PRODUCT_BRIEF.md
- docs/SYSTEM_ARCHITECTURE.md
- docs/DATABASE_SCHEMA.md
- docs/ACCOUNTING_RULES.md
- docs/USER_PERMISSIONS.md
- docs/TEST_PLAN.md

Keep documentation consistent with the actual implementation.

## Priority

Security and financial accuracy come before convenience and visual design.

Build a dependable operating system for the businesses, not merely a dashboard that looks impressive.
