---
title: Data Binding Modes
author: Anna Vekhina
---
# Data Binding Modes

The Report Designer uses one of the following modes to provide dynamic content to your reports: expression bindings or standard data bindings.

## <a name="expressions"></a>Expression Bindings

Expression bindings enable you to use complex [expressions](../use-expressions.md) that include two or more fields and various functions. Expressions also allow you to calculate complex summaries without scripts and conditionally shape your data without formatting rules.

This mode is enabled in the Report Designer if it provides the [Expressions](../report-designer-tools/ui-panels/expressions-panel.md) ![](../../../images/eurd-web-expressions-panel-icon.png) panel.

![](../../../images/eurd-web-property-grid-expression-bindings-mode.png)


## <a name="databindings"></a> Data Bindings

Standard data bindings enable you to assign a single data field to a report control or use [report scripts](../report-designer-tools/script-editor.md) to provide custom logic.

This mode is enabled in the Report Designer if it does not provide the [Expressions](../report-designer-tools/ui-panels/expressions-panel.md) ![](../../../images/eurd-web-expressions-panel-icon.png) panel.


![](../../../images/eurd-web-property-grid-data-bindings-mode.png)

## <a name="dialog"></a>Conversion Dialog

The following dialog appears only when [expression bindings](#expressions) are enabled in the Report Designer, and you [open an existing report](../open-reports.md) that uses standard [data bindings](#databindings):

![](../../../images/eurd-web-bindings-to-expressions-conversion-dialog.png)

This dialog prompts you to convert your report to use expressions (the new binding mechanism). Click **Yes** to run the report conversion, click **No** to open the report without changes.

See the section below for information on how to use expressions instead of data bindings.


## <a name="comparison"></a>Binding Mode Comparison

### **Bind to a Single Data Field**

* The [Field List](../report-designer-tools/ui-panels/field-list.md) panel allows you to drop fields onto the design surface or existing report controls. All binding ways are identical in the **data bindings** and **expression bindings** modes. 

    ![](../../../images/eurd-web-field-list-drop-fields.png)

* You can select a report control and bind it to data in the [Properties](../report-designer-tools/ui-panels/properties-panel.md) panel.

    <table><tr><th><p>Expression Bindings</p>
    </th><th><p>Data Bindings</p>
    </th></tr><tr><td>
    <p>Switch to the <a class="xref" href="..\report-designer-tools\ui-panels\expressions-panel.md"> Expressions</a> panel, click the <strong>Text</strong> property's ellipsis button and specify the expression.</p>

    <p><img src="../../../images/eurd-web-property-grid-expression-binding.png"></p>
    </td><td><p>Expand the <strong>Data Bindings</strong> drop-down list and select a data field.</p>
    <p><img src="../../../images/eurd-web-property-grid-text-data-binding.png"></p>
    </td>
    </tr></table>



See the following topics for more information:

* [Bind Report Controls to Data (Expression Bindings)](bind-controls-to-data-expression-bindings.md)
* [Bind Report Controls to Data (Data Bindings)](bind-controls-to-data-data-bindings.md)


### **Bind to Multiple Data Fields**

<table><tr><th><p>Expression Bindings</p>
</th><th><p>Data Bindings</p>
</th></tr><tr><td><p>Use the <a class="xref" href="use-embedded-fields-mail-merge.md">mail merge</a> functionality.</p>
<p><img src="../../../images/eurd-web-binding-modes-mail-merge.png"></p>
<p>Switch to the <a class="xref"
href="../report-designer-tools/ui-panels/expressions-panel.md"> Expressions</a> panel, click the <strong>Text</strong> property's ellipsis button and specify the expression.</p>
<p><img src="../../../images/eurd-web-expression-binding-multiple-fields.png"></p>
</td><td><p>Use the <a class="xref" href="use-embedded-fields-mail-merge.md">mail merge</a> functionality.</p>
<p><img src="../../../images/eurd-web-binding-modes-mail-merge.png"></p>
</td>
</tr></table>

### **Calculate Summary**

<table><tr><th><p>Expression Bindings</p>
</th><th><p>Data Bindings</p>
</th></tr><tr><td><p> Select the summary function in the <strong>Expression Editor</strong>'s <strong>Summary</strong> section. </p>
<p>All functions have the 'sum' prefix.</p>
<p><img src="../../../images/eurd-web-expression-binding-summary-function.png"></p>
<p>See <a class="xref" href="..\shape-report-data\shape-data-expression-bindings\calculate-a-summary.md">Calculate a Summary</a> for more information.</p>
</td><td><p>Expand the <strong>Summary</strong> node in the <strong>Actions</strong> category and select the summary function in the <strong>Function</strong> drop-down list.</p>
<p><img src="../../../images/eurd-web-data-binding-summary-function.png"></p>
<p>See <a class="xref" href="..\shape-report-data\shape-data-data-bindings\calculate-a-summary.md">Calculate a Summary</a> for more information.</p>
</td>
</tr></table>

### **Complex Bindings, Custom Summary**

<table><tr><th><p>Expression Bindings</p>
</th><th><p>Data Bindings</p>
</th></tr><tr><td><p>Use the <strong>Expression Editor</strong> to construct an <a class="xref" href="..\use-expressions.md">expression</a> of any complexity.</p>
<p><img src="../../../images/eurd-web-label-advanced-summary-expression.png"></p>
<p>Refer to <a class="xref" href="..\shape-report-data\shape-data-expression-bindings\calculate-an-advanced-summary.md">Calculate an Advanced Summary</a> for an example.</p>
</td><td><p>Use <a class="xref" href="..\report-designer-tools/script-editor.md">report scripts</a>.</p>
<p>Refer to <a class="xref" href="..\shape-report-data\shape-data-data-bindings\calculate-a-custom-summary.md">Calculate a Custom Summary</a> for an example.</p>
</td>
</tr></table>

### **Conditionally Customize Appearance**

<table><tr><th><p>Expression Bindings</p>
</th><th><p>Data Bindings</p>
</th></tr><tr><td><p>Switch to the <a class="xref"
href="../report-designer-tools/ui-panels/expressions-panel.md"> Expressions</a> panel, click the <strong>Style Name</strong> property's ellipsis button and specify the expression.</p>
<p><img src="../../../images/eurd-web-shaping-style-name-expression.png"></p>
<p>Refer to <a class="xref" href="..\shape-report-data\shape-data-expression-bindings\conditionally-change-a-control-appearance.md">Conditionally Change a Control Appearance</a> for an example.</p>
</td><td><p>Create formatting rules and assign them to report controls.</p>
<p><img src="../../../images/eurd-web-shaping-formattin-rule-appearance-settings.png"></p>
<p>Refer to <a class="xref" href="..\shape-report-data\shape-data-data-bindings\conditionally-change-a-control-appearance.md">Conditionally Change a Control Appearance</a> for an example.</p>
</td>
</tr></table>
