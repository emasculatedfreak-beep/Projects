# Publishing Checklist

This plugin is close to being publishable on the official QGIS Python plugin repository, but a few maintainer-owned steps still need to be completed.

## Before you upload

1. Create a public source repository, for example on GitHub or GitLab.
2. Replace the placeholder metadata URLs in [gee_data_fetcher/metadata.txt](/C:/Users/Jay/Documents/New%20project/gee_data_fetcher/metadata.txt).
3. Replace the placeholder author email with the maintainer email you want shown in QGIS.
4. Decide whether `experimental=True` should remain enabled for the first public release.
5. Test the packaged zip in a clean QGIS profile.
6. Create an OSGEO ID for the QGIS plugin repository.

## Required QGIS repository rules

- The zip must contain a top-level plugin folder.
- The plugin folder name must be ASCII-only and cannot start with a digit.
- `metadata.txt`, `__init__.py`, and `LICENSE` must be included.
- The `repository` metadata value must be a valid URL.
- The uploaded version number must be unique.

## Packaging

Use the PowerShell script in [scripts/package_plugin.ps1](/C:/Users/Jay/Documents/New%20project/scripts/package_plugin.ps1) to create a zip that contains only the plugin folder.

## Recommended next improvements

- Add screenshots for the plugin repository page.
- Add automated tests for the non-QGIS service logic.
- Consider adding a Processing provider so the plugin can be used in batch workflows.
