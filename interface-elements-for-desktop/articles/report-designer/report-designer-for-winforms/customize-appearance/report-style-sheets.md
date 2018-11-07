---
title: Report Style Sheets
owner: Mary Sammal
---
# Report Style Sheets

You can combine [report styles](report-visual-styles.md) into a style sheet and reuse them in reports. This topic explains how to create and use style sheets in reports.

## Save Styles as Style Sheets

Press the caption button in the toolbar's Styles group to invoke the Style Editor.

![eurd-win-save-styles](../../../../images/eurd-win-save-styles.png)

Press the ![Save](../../../../images/eurd-win-save-button-styles-editor.png) button to save the styles as a style sheet (external REPSS file).

## Add a Style Sheet to a Report

Do the following to embed a style sheet's styles in a report:

- invoke the Styles Editor;

![eurd-win-invoke-styles-editor](../../../../images/eurd-win-invoke-styles-editor.png)

- press ![]() and choose a style sheet file in the Open dialog.

![eurd-win-open-style-sheet](../../../../images/eurd-win-open-style-sheet.png)

All the styles are now available in the report's toolbar and Report Explorer.

![eurd-win-added-styles](../../../../images/eurd-win-added-styles.png)


## Reuse Style Sheets in Reports

You can utilize styles from a style sheet in a report. To do this, specify the path to the style sheet file in the report's **StyleSheetPath** property.

![eurd-win-stylesheetpath](../../../../images/eurd-win-stylesheetpath.png)

The attached style sheet's styles are now available in the report's toolbar and the Report Explorer. You **cannot edit these styles**.

![eurd-win-read-only-styles](../../../../images/eurd-win-read-only-styles.png)


