# Build 1.2.14

## UX/UI Improvements
- Added previous / next record navigation to backend forms.
- Added new `fieldset` FormWidget that visually groups form fields together in the `Form` widget.

## API Changes
- Public controller methods used as a page action must now be named in lowercase — `coming_soon()` rather than `comingSoon()` — and dashed URLs are normalised to snake_case, so `/coming-soon` now resolves to `coming_soon()` instead of `comingSoon()`. Plugins with a camelCase page action should rename the method and its view file to match; the published URL does not need to change

## Bug Fixes
- Improved handling of the password reset flow for users that don't exist.
- Fixes issue where if an exception is thrown during a Halcyon force deletion it would leave the datastore stuck in force deletion mode.

## Security Improvements
- Improved escaping of `BrandSetting` & `EditorSetting` custom CSS settings.
- Fixed reflected XSS in the backend `Table` widget.
- Hardened the `image` column type to prevent potential XSS from untrusted user input.
- Tightened import export controller behavior permissions checking.
- Hardened the `MyAccount` controller added in v1.2.13.
- Hardened backend request routing to close off CSRF attacks targeting AJAX handlers.

## Translation Improvements
- Improved Ukrainian translations.

## Performance Improvements
- Reduced front-end database queries from CMS templates, theme data, and request logs.
- Resolve Halcyon DB template mtimes without a query per check.

## Community Improvements
- Added GitHub action to automatically update the official Winter docker image when new Winter versions are released.

## Dependencies
- Bump minimum version of `assetic/framework` to `v3.2.2`.
