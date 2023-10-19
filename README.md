# Strapi config sync - excludedConfig ignored issue

Steps to run/reproduce the issue:
- Clone + cd into folder
- "yarn" to install deps
- "yarn config-sync e" to export config
- Notice it wants to create "admin-role.strapi-editor" and "admin-role.strapi-author" - All good
- Ctrl+C to cancel the export
- In plugins.ts, uncomment lines 12-13
- "yarn config-sync e" to export config
- Notice it still wants to create "admin-role.strapi-editor" and "admin-role.strapi-author" - Unexpected behavior
- Ctrl+C to cancel the export
- "rm -rf dist"
- "yarn config-sync e" to export config
- Notice it now correctly ignores "admin-role.strapi-editor" and "admin-role.strapi-author" - Expected behavior
