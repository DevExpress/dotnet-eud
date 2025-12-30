---
title: Reports with Embedded PDF Content
author: Eugene Polevikov
---

# Reports with Embedded PDF Content

This tutorial explains how to use the [PDF Content](../use-report-elements/use-basic-report-controls/pdf-content.md) control to do the following:

* Append PDF file pages to a report and make their paper kind the same as in the inital report.
* Add sequential page numbers to the report and PDF file pages.
* Include additional information in the embedded PDF file pages.

The image below shows an invoice report that contains information about order items.

![Final Report Page 1](../../../images/create-report-with-pdf-content-final-report-page1.png)

The following image illustrates the first PDF file page embedded to the invoice report. This page has the same paper kind as the initial report. [Report controls](../use-report-elements/use-basic-report-controls.md) are used to add item title, item price, line, logo image, and sequential page numbers to this page.

![Final Report Page 2](../../../images/create-report-with-pdf-content-final-report-page2.png)

To create the above report with PDF content, follow the steps described in these sections:

* [Create the Main Report](#create-the-main-report)
* [Create a Report with PDF Content](#create-a-report-with-pdf-content)
* [Add the Report with PDF content to the Main Report](#add-the-report-with-pdf-content-to-the-main-report)

## Create the Main Report

1. Open the [Report Designer](../../report-designer-for-winforms.md) and [add a new blank report](../../report-designer-for-winforms/add-new-reports.md).
2. Design the report layout. In this tutorial, we create an invoice report that contains information about order items.

    ![Main Report Layout](../../../images/pdfcontent-embedded-mode-main-report-layout.png)

    To supply the report with data, use the following JSON string:

    ```
    {
        "InvoiceNumber": 241756,
        "OrderDate": "2018-04-23T18:25:43.511Z",
        "Customer": {
            "Name": "Walters",
            "HomeOffice_Line": "200 Wilmot Rd",
            "HomeOffice_City": "Deerfield",
            "HomeOffice_StateName": "IL",
            "HomeOffice_ZipCode": "60015"
        },
        "Store": {
            "Address_City": "Anaheim",
            "Address_Line": "1720 W La Palma Ave",
            "Address_StateName": "CA",
            "Address_ZipCode": "83709"
        },
        "Employee": {
            "FullName": "Harv Mudd"
        },
        "PONumber": "122023",
        "ShipMethod": 0,
        "OrderTerms": "15 Days",
        "OrderItems": [
            {
                "ProductName": "SuperLED 42",
                "ProductPrice": 1050,
                "ProductUnits": 2,
                "Discount": 50,
                "Total": 2050
            },
            {
                "ProductName": "SuperLED 50",
                "ProductPrice": 1100,
                "ProductUnits": 5,
                "Discount": 500,
                "Total": 5000
            },
            {
                "ProductName": "Projector PlusHD",
                "ProductPrice": 600,
                "ProductUnits": 5,
                "Discount": 250,
                "Total": 2750
            },
            {
                "ProductName": "HD Video Player",
                "ProductPrice": 220,
                "ProductUnits": 10,
                "Discount": 200,
                "Total": 2000
            }
        ],
        "ShippingAmount": 375,
        "TotalAmount": 12175
    }
    ```

The following image illustrates the main report's **Preview**:

![Main Report Preview](../../../images/pdfcontent-embedded-mode-main-report-preview.png)

## Create a Report with PDF Content

1. Create a new blank report. Remove the report's margins.

    ![Add a New Blank Report and Remove Margins](../../../images/create-report-with-pdf-content-add-new-blank-report-and-remove-margins.png)

2. Drop the [PDF Content](../use-report-elements/use-basic-report-controls/pdf-content.md) control from the **Toolbox** onto the *Detail* band.

    ![Drop the PDF Content Control Onto the Detail Band](../../../images/create-report-with-pdf-content-drop-xrpdfcontent-control-onto-detail-band.png)

3. Expand the control's smart tag, click the **Source** or **Source URL** property's ellipsis button, and select PDF file. In this demo, we use the following PDF specification: [Specification.pdf](https://github.com/DevExpress-Examples/DataSources/blob/master/Specification.pdf).

    ![Specify PDF File Source](../../../images/create-report-with-pdf-content-specify-pdf-file-source.png)

4. Disable the control's **Generate Own Pages** property. Adjust the control size to make PDF content fit the entire *Detail* band. For this, set the *Detail* band's **Height** to *1095* and the control's **Width** and **Height** to *850* and *1095*.

    ![Make PDF Content Fit the Entire Detail Band](../../../images/create-report-with-pdf-content-make-pdf-content-fit-entire-detail-band.png)

5. Disable the report's **Designer Options -> Show Export Warnings** property. Bind the report to the following JSON data:
    
    ```
    {
        "InvoiceNumber": 241756,
        "OrderDate": "2018-04-23T18:25:43.511Z",
        "Customer": {
            "Name": "Walters",
            "HomeOffice_Line": "200 Wilmot Rd",
            "HomeOffice_City": "Deerfield",
            "HomeOffice_StateName": "IL",
            "HomeOffice_ZipCode": "60015"
        },
        "Store": {
            "Address_City": "Anaheim",
            "Address_Line": "1720 W La Palma Ave",
            "Address_StateName": "CA",
            "Address_ZipCode": "83709"
        },
        "Employee": {
            "FullName": "Harv Mudd"
        },
        "PONumber": "122023",
        "ShipMethod": 0,
        "OrderTerms": "15 Days",
        "OrderItems": [
            {
                "ProductName": "SuperLED 42",
                "ProductPrice": 1050,
                "ProductUnits": 2,
                "Discount": 50,
                "Total": 2050
            },
            {
                "ProductName": "SuperLED 50",
                "ProductPrice": 1100,
                "ProductUnits": 5,
                "Discount": 500,
                "Total": 5000
            },
            {
                "ProductName": "Projector PlusHD",
                "ProductPrice": 600,
                "ProductUnits": 5,
                "Discount": 250,
                "Total": 2750
            },
            {
                "ProductName": "HD Video Player",
                "ProductPrice": 220,
                "ProductUnits": 10,
                "Discount": 200,
                "Total": 2000
            }
        ],
        "ShippingAmount": 375,
        "TotalAmount": 12175
    }
    ```
    
6. Place two [labels](../use-report-elements/use-basic-report-controls/label.md), a [line](../use-report-elements/draw-lines-and-shapes/draw-lines.md), and a [picture box](../use-report-elements/use-basic-report-controls/picture-box.md) on the PDF page header as shown below:

    ![Add Controls to Page Header](../../../images/create-report-with-pdf-content-make-pdf-content-add-controls-to-page-header.png)

    Use the following locations and sizes:

    | Control Name | Location | Size |
    | --- | --- | --- |
    | label1 | 105, 94 | 280, 44 |
    | label2 | 105, 138 | 118, 30 |
    | line1 | 105, 69 | 687, 20 |
    | pictureBox1 | 647, 24 | 145, 45 |

7. Set the line's **Width** and **Fore Color** to *2* and *Orange* respectively. Assign the following image to the picture box's **Image Source** property:

    ![DevAV Icon](../../../images/devav.png)

    Make the label1's font bold. Set up label appearance as shown in the table below:

    | Control Name | Font | Font Size | Text Property's Expression | Text Format String |
    | --- | --- | --- | --- | --- |
    | label1 | Segoe UI | 21 | *ProductName* | - |
    | label2 | Segoe UI | 12 | *ProductPrice* | {0:$0} |

    ![Bind Labels to Data](../../../images/create-report-with-pdf-content-make-pdf-content-bind-labels-to-data.png)

    To display a product name and price of each order item on a corresponding PDF file page, set the PDF Content **Page Range** property's [expression](../use-expressions.md) to *[DataSource.CurrentRowIndex] + 1*.

    ![Assign Expression to the Page Range Property](../../../images/create-report-with-pdf-content-assign-expression-to-page-range.png)

8. Add the [Page Info](../use-report-elements/use-basic-report-controls/page-info.md) control to the PDF page footer. Use the following settings for this control:

    | Location | Size | Font | Font Size | Text Alignment | Text Format String |
    | --- | --- | --- | --- | --- | --- |
    | 0, 1045 | 850, 50 | Segoe UI | 12 | Middle Center | Page {0} of {1} |

    ![Add Page Numbers](../../../images/create-report-with-pdf-content-add-page-numbers.png)

Open **Preview** to show the result. The image below shows the report's first page:

![Final Report Preview](../../../images/create-report-with-pdf-content-preview.png)

## Add the Report with PDF Content to the Main Report

1. Add a footer to the main report. Right-click the design surface, choose **Insert Band**, and select **ReportFooter**.

    ![Add Report Footer](../../../images/create-report-with-pdf-content-add-report-footer.png)

2. Add the [Subreport](../use-report-elements/use-basic-report-controls/subreport.md) control to the footer. Assign the path the report with PDF content to the control's **Report Source URL** property. Enable the control's **Generate Own Pages** property.

    ![Add the Subreport](../../../images/create-report-with-pdf-content-add-subreport.png)

3. Add the [Page Info](../use-report-elements/use-basic-report-controls/page-info.md) control to the report's **Bottom Margin** band. Set the control's **Text Alignment** propery to *Middle Center* and the **Text Format String** property to *Page {0} of {1}*.

    ![Add Page Numbers to Main Report](../../../images/create-report-with-pdf-content-add-page-number-to-main-report.png)

Open **Preview** to show the result.

![Final Report Page 1](../../../images/create-report-with-pdf-content-final-report-page1.png)

![Final Report Page 2](../../../images/create-report-with-pdf-content-final-report-page2.png)