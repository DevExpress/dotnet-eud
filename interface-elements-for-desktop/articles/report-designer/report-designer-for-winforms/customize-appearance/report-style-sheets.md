---
title: Report Style Sheets
owner: Mary Sammal
---
# Report Style Sheets

You can combine [report styles](customize-appearance\report-visual-styles.md) into a style sheet to reuse them between reports. This topic explains how to create and use style sheets in reports.

## Save Styles as Style Sheets

Press the caption button on the toolbar's Styles group to invoke the Styles Editor.

![eurd-win-save-styles](../../../../images/eurd-win-save-styles.png)

Press the ![Save](../../../../images/eurd-win-save-button-styles-editor.png) button to save the styles as a style sheet. This saves the newly created style sheet to an external file with the REPSS extension.

## Add a Style Sheet to a Report

Do the following to embed the styles that a style sheet provides to a report:

- invoke the Styles Editor;

![eurd-win-invoke-styles-editor](../../../../images/eurd-win-invoke-styles-editor.png)

- press ![]() and choose the required style sheet file in the Open dialog.

![eurd-win-open-style-sheet](../../../../images/eurd-win-open-style-sheet.png)

All the styles become available in the report's toolbar and the Report Explorer.

![eurd-win-added-styles](../../../../images/eurd-win-added-styles.png)


## Reuse Style Sheets in Reports

You can utilize styles from a style sheet in a report. To do this, specify the path to the style sheet file for the report's **StyleSheetPath** property.

![eurd-win-stylesheetpath](../../../../images/eurd-win-stylesheetpath.png)

The styles that the attached style sheet contains become available in the report's toolbar and the Report Explorer. Note that you can apply these styles, but **can not edit them**.

![eurd-win-read-only-styles](../../../../images/eurd-win-read-only-styles.png)


