# DevExpress End-User Documentation

This article explains how to clone DevExpress End-User documentation sources and how to create your own documentation websites and help files for projects based on DevExpress technologies. You can also find a link to a sample pre-built website.

> For **Developer Documentation with API Reference** see [https://docs.devexpress.com](https://docs.devexpress.com).

## The Scope
DevExpress products for WinForms and ASP.NET WebForms/MVC. 

## Licensing
By accessing this repository, you agree to the terms of the [DevExpress End-User Documentation License Agreement](LICENSE.md).

## How to View Content
Do one of the following to view the End-User Documentation content:

1. Browse this repository's content directly. Start with [index.md](index.md).
2. View the sample pre-built website at [devexpress.github.io/dotnet-eud](https://devexpress.github.io/dotnet-eud/).
3. [Build PDF files](#build-printer-friendly-pdf-files).

## Document Format and Supported Output Types
Documents in this repository are written in markdown. You can manually copy the information to your own help file.

The repository also includes a [docfx.json](docfx.json) file. You can use [DocFX](https://dotnet.github.io/docfx/) and [wkhtmltopdf](https://github.com/wkhtmltopdf/wkhtmltopdf) to convert this file from a set of topics to an HTML website or a PDF file.   

## Build an HTML Website
Follow the steps below to create a documentation website for your application.

1. Download and install the [latest version of DocFX](https://github.com/dotnet/docfx/releases). 
1. Copy the repository to your computer and checkout the branch corresponding to the version of DevExpress controls your application uses. Do not use the **master** branch because it represents the version currently under development.
    ```
    git clone https://github.com/DevExpress/dotnet-eud.git
    git switch 20.1
    ```
    If you do not have [Git](https://git-scm.com/) installed, use the GitHub web interface to select the branch and then download and extract the ZIP archive.
  
    ![Download ZIP](https://user-images.githubusercontent.com/20167812/29712204-4ffaee9e-89a1-11e7-8a0e-3ff0464adda4.png)
1. You can make the following changes to the documentation, or skip this step if you want to reuse the end-user documentation as is:
   
   - remove unnecessary files;
   - add new documents to your application;
   - change screenshots to match your app's UI;
   - create a [custom DocFX template](https://dotnet.github.io/docfx/tutorial/howto_create_custom_template.html).
   
   > You should update the *toc.yml* ([table-of-content](https://dotnet.github.io/docfx/tutorial/intro_toc.html)) files if you added or removed topics.
1. Open a console window, change the current directory to the repository root folder and call the DocFX executable with the following parameters: *build* and the path to *docfx.json* in the downloaded _dotnet-eud_ repository. DocFX will place the generated documentation content into the *\_site* folder. Add the `--serve` switch to preview the generated website at http://localhost:8080 once the build process is complete. 
    ```
    docfx.exe build ../dotnet-eud/docfx.json --serve
    ```
1. Deploy the created documentation to a web server or browse the documentation directly from local file system. Since DocFX creates static HTML files only, no additional deployment or configuration steps are required.

## Build Printer-Friendly PDF Files
If your end users require a printed version, you can build a PDF file like this:

1. Ensure that you can successfully [build a website with DocFX](#build-your-own-documentation-website).
1. Download and install [wkhtmltopdf](https://wkhtmltopdf.org/downloads.html).
1. In the folder with `docfx.exe`, open a console window and add the `wkhtmltopdf` executable path to the `%PATH%` environment variable:

    ```
    set PATH=%PATH%;C:\Program Files\wkhtmltopdf\bin
    ```

1. Build pdf:

    ```
    docfx.exe pdf ../dotnet-eud/docfx.json
    ```

This generates a *_pdf* subfоlder with a PDF file for each included table-of-contents file. Note that this is a time-consuming process.

## Troubleshooting

Below are the common issues you can face when building this repository's documentation. 

* #### The build process fails with the *System.IO.PathTooLongException* exception
  Reduce your working directory's full path (move the repository closer to a drive root).

  *See also:* https://github.com/dotnet/docfx/issues/156
  
* #### The *wkhtmltopdf is a prerequisite when generating a PDF* error occurs when creating a PDF
  Ensure that [wkhtmltopdf](https://wkhtmltopdf.org/downloads.html) is installed and its executable path is correctly added to the *%PATH%* environment variable.

  *See also:* [Generate PDF Documentation](http://dotnet.github.io/docfx/tutorial/walkthrough/walkthrough_generate_pdf.html)
 
* #### The table of contents is not displayed when browsing the generated documentation from the file system
  Your browser security configuration may restrict executing the JavaScript code that accesses your local files (the table of contents is in a separate *toc.html* file when using the [default](https://github.com/dotnet/docfx/tree/dev/src/docfx.website.themes/default) DocFX template). In this case, you can use the [statictoc](https://github.com/dotnet/docfx/tree/dev/src/docfx.website.themes/statictoc) template instead. To switch to this template, add `--template statictoc` to the docfx.exe parameters:
    ```
    docfx.exe build ../dotnet-eud/docfx.json --template statictoc
    ```
  The table of contents is embedded into each topic with this template which increases the build time and HTML file sizes. Alternatively, you can override the browser's restrictions (which may be unsecure). For example, Google Chrome and Microsoft Edge accept the `--allow-file-access-from-files` command line switch which allows loading local files.
  
  > We recommend you to use the `--serve` DocFX switch to preview documentation, and then share it with end users via a web server instead of browsing the file system.

If your issue is not listed, you can [submit a new issue to this repository](https://github.com/DevExpress/dotnet-eud/issues/new) or contact us via the [DevExpress Support Center](https://www.devexpress.com/Support/Center/). You can search the [DocFX issues list](https://github.com/dotnet/docfx/issues), or try building the [docfx\-seed](https://github.com/docascode/docfx-seed) sample documentation project to check if your issue is specific to this repository.

## Versions 17.1 and Earlier

If you require End-User documentation for v17.1 or earlier, download **End-User Documentation Installer** containing CHM and PDF files. Markdown is not available for these versions. 

| Version | Installer                                                                                      |
|:--------|:-----------------------------------------------------------------------------------------------|
| v17.1   | [DevExpressEndUserDocs171.exe](https://go.devexpress.com/Documentation_EUD_17_1.aspx "127 Mb") |
| v16.2   | [DevExpressEndUserDocs162.exe](https://go.devexpress.com/Documentation_EUD_16_2.aspx "128 Mb") |
| v16.1   | [DevExpressEndUserDocs161.exe](https://go.devexpress.com/Documentation_EUD_16_1.aspx "109 Mb") |
| v15.2   | [DevExpressEndUserDocs152.exe](https://go.devexpress.com/Documentation_EUD_15_2.aspx "96 Mb")  |
| v15.1   | [DevExpressEndUserDocs151.exe](https://go.devexpress.com/Documentation_EUD_15_1.aspx "84 Mb")  |
| v14.2   | [DevExpressEndUserDocs142.exe](https://go.devexpress.com/Documentation_EUD_14_2.aspx "75 Mb")  |
| v14.1   | [DevExpressEndUserDocs141.exe](https://go.devexpress.com/Documentation_EUD_14_1.aspx "73 Mb")  |
| v13.2   | [DevExpressEndUserDocs132.exe](https://go.devexpress.com/Documentation_EUD_13_2.aspx "61 Mb")  |
| v13.1   | [DevExpressEndUserDocs131.exe](https://go.devexpress.com/Documentation_EUD_13_1.aspx "35 Mb")  |
| v12.2   | [DevExpressEndUserDocs122.exe](https://go.devexpress.com/Documentation_EUD_12_2.aspx "35 Mb")  |
| v12.1   | [DevExpressEndUserDocs121.exe](https://go.devexpress.com/Documentation_EUD_12_1.aspx "35 Mb")  |

You are free to download these files and distribute them to your end users. However, Developer Express Inc. has the right to change or remove these files without notice.
