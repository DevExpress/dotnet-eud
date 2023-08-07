---
title: Reports with a Visual PDF Signature
author: Eugene Polevikov
---
# Reports with a Visual PDF Signature

This tutorial describes how to create a report with a visual PDF signature.

![](../../../../images/pdf-signature-report-result-after-sign-lower.png)

## Create a Report Layout

1. Drop the **RichText** control from the report controls Toolbox tab onto the **Detail** band.

    ![](../../../../images/pdf-signature-report-drop-rich-text.png)

2. Double-click the control and insert the [DevExpress Website Terms of Use](https://www.devexpress.com/aboutus/legal.xml) text.

    ![](../../../../images/pdf-signature-report-add-data-to-rich-text.png)

3. Right-click the design surface. Select **Insert Band / ReportFooter** from the context menu. Enable the footer band's **Print at Bottom** property.

    ![](../../../../images/pdf-signature-report-add-report-footer.png)

4. Drop the **PdfSignature** control from the report controls Toolbox tab onto the **Report Footer** band.

    ![](../../../../images/pdf-signature-report-add-pdf-signature.png)

5. Place the **Label** control to the left of the **PdfSignature** control and add the following text: _I have read and accept this Website Terms of Use statement_.

    ![](../../../../images/pdf-signature-report-add-xr-label-and-line.png)

Click the **Preview Tab** to show the result.

![](../../../../images/pdf-signature-report-result-before-sign.png)

## Export and Sign the Report

1. In **Preview**, click **Export Document** and select **PDF File**.

    ![](../../../../images/pdf-signature-report-sign-1.png)

2. In the invoked **PDF Export Options** dialog, click the **Digital Signature** option's ellipsis button.

    ![](../../../../images/pdf-signature-report-sign-2.png)

3. In the invoked **Signature Options** dialog, choose a certificate and specify signature details.

    ![](../../../../images/pdf-signature-report-sign-3.png)

Save and open the document to show the final result.

![](../../../../images/pdf-signature-report-result-after-sign.png)
