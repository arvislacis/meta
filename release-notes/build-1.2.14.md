# Build 1.2.14

## UX/UI Improvements
- Added previous / next record navigation to backend forms.

## DX Improvements
-

## API Changes
- Public controller methods used as a page action must now be named in lowercase — `coming_soon()` rather than `comingSoon()` — and dashed URLs are normalised to snake_case, so `/coming-soon` now resolves to `coming_soon()` instead of `comingSoon()`. Plugins with a camelCase page action should rename the method and its view file to match; the published URL does not need to change

## Bug Fixes
-

## Security Improvements
- Improved escaping of `BrandSetting` & `EditorSetting` custom CSS settings.
- Fixed reflected XSS in the backend `Table` widget.
- Tightened import export controller behavior permissions checking.
- Hardened backend request routing to close off CSRF attacks targeting AJAX handlers.

## Translation Improvements
-

## Performance Improvements
- Reduced front-end database queries from CMS templates, theme data, and request logs.

## Community Improvements
-

## Dependencies
-
