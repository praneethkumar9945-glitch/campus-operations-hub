# Merge the school-management apps

## Build
Use **Admit And Academy** as the main school suite. Replace its placeholder Academic, Admin, and Finance screens with the corresponding supplied trainer portal, administration app, and finance app. Keep the main admissions, workspace, HR, marketing, and director areas intact.

## Integration
- Keep one app and one navigation shell; map Academic, Admin, and Finance to their actual screens.
- Convert the trainer portal's hash-based navigation to the project's existing TanStack routing, with its dashboard at `/academic` and its remaining views below `/academic/`.
- Place the admin and finance views under `/admin/` and `/finance/`, updating their internal links, route metadata, and navigation so the sections do not collide with each other or the main suite.
- Bring over required page logic, supporting data and assets, and styles without copying repository metadata, generated files, dependency folders, environment files, or secrets. Keep the current project's framework and pinned framework versions.

## Data and access
- No data exports were included. Preserve only source-code demo/default data in the preview; do not claim existing browser-saved records or accounts have moved.
- The repositories use browser storage for most records, and the base repository's only detected table is user profiles. No app role checks were found, so the Admin section will not be presented as access-restricted unless role requirements are supplied.
- Do not invent imported user accounts or transfer browser data without safe exports.

## Verification
Check the home screen and each section, verify that navigation stays within the correct section, run the existing relevant tests, and review build/runtime logs. Record data, account, and access-control items that remain unavailable from the supplied repositories or exports.

## Technical details
Use the current TanStack Start routes and design-system tokens. Preserve the source modules' meaningful interactions while replacing React Router-specific navigation with TanStack Router. Keep the source apps' existing browser-storage behavior where no shared database-backed behavior exists; do not create a new school-data schema or invent permission roles without a source definition.
