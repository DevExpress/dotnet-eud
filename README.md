# DevExpress End-User Documentation

This article explains how to clone DevExpress End-User documentation sources and how to create your own documentation websites and help files for projects based on DevExpress technologies. It also provides links to a sample pre-built website and PDF files.


> If you require End-User documentation for **v17.1 and earlier**, you can download previous versions in CHM and PDF formats from https://www.devexpress.com/Support/Documentation/download.xml?platform=user-dev-docs.
>
> For **Developer Documentation with API Reference** see [https://documentation.devexpress.com](https://www.devexpress.com/Support/Documentation/).

## The Scope
DevExpress products for WinForms, WPF and ASP.NET WebForms/MVC. 

## Licensing
By accessing this repository, you agree to the terms of the [DevExpress End-User Documentation License Agreement](LICENSE.md).

## How to View Content
Do one of the following to view the End-User Documentation content:

1. Browse this repository's content directly. Start with [index.md](index.md).
2. View the sample pre-built website at [devexpress.github.io/dotnet-eud](https://devexpress.github.io/dotnet-eud/).
3. Download these PDF files:
   * [dotnet-eud_interface-elements-for-web.pdf](https://devexpress.github.io/dotnet-eud/pdf/dotnet-eud_interface-elements-for-web.pdf)
   * [dotnet-eud_interface-elements-for-desktop.pdf](https://devexpress.github.io/dotnet-eud/pdf/dotnet-eud_interface-elements-for-desktop.pdf)
   * [dotnet-eud_dashboard-for-web.pdf](https://devexpress.github.io/dotnet-eud/pdf/dotnet-eud_dashboard-for-web.pdf)
   * [dotnet-eud_dashboard-for-desktop.pdf](https://devexpress.github.io/dotnet-eud/pdf/dotnet-eud_dashboard-for-desktop.pdf)

## Document Format and Supported Output Types
Documents in this repository are written in markdown. You can manually copy the information to your own help file.

The repository also includes a [docfx.json](docfx.json) file. You can use [DocFX](https://dotnet.github.io/docfx/) and [wkhtmltopdf](https://github.com/wkhtmltopdf/wkhtmltopdf) to convert this file from a set of topics to an HTML website or a PDF file.   

## Build an HTML Website
Follow the steps below to create a documentation website for your application.

- Download and install the [latest version of DocFX](https://github.com/dotnet/docfx/releases). 
- Copy the repository to your computer and checkout the branch corresponding to the version of DevExpress controls your application uses. Do not use the **master** branch because it represents the version currently under development.
    ```
    git clone https://github.com/DevExpress/dotnet-eud.git --branch 18.1
    ```
  If you do not have [Git](https://git-scm.com/) installed, use the GitHub web interface to select the branch and then download and extract the ZIP archive.
  
  ![Download ZIP](https://user-images.githubusercontent.com/20167812/29712204-4ffaee9e-89a1-11e7-8a0e-3ff0464adda4.png)
- You can make the following changes to the documentation, or skip this step if you want to reuse the end-user documentation as is:
  - remove unnecessary files;
  - add new documents to your application;
  - change screenshots to match your app's UI;
  - create a [custom DocFX template](https://dotnet.github.io/docfx/tutorial/howto_create_custom_template.html).
  > You should update the *toc.yml* ([table-of-content](https://dotnet.github.io/docfx/tutorial/intro_toc.html)) files if you added or removed topics.
- Open a console window, change the current directory to the repository root folder and call the DocFX executable with the *build* and *docfx.json* parameters. DocFX will place the generated documentation content into the *\_site* folder. Add the `--serve` switch to preview the generated website at http://localhost:8080 once the build process is complete. 
    ```
    docfx.exe build docfx.json --serve
    ```
- Finally, deploy the created documentation to a web server or browse the documentation directly from local file system. Since DocFX creates static HTML files only, no additional deployment or configuration steps are required.

## Build Printer-Friendly PDF Files
If your end users require a printed version, you can create a PDF file:
- Ensure that you can successfully build a website with DocFX (see the [previous section](#build-your-own-documentation-website)).
- Download and install [wkhtmltopdf](https://wkhtmltopdf.org/downloads.html).
- Open a console window and add the **wkhtmltopdf** executable path to the %PATH% environment variable:
    ```
    set PATH=%PATH%;C:\Program Files\wkhtmltopdf\bin
    ```
- Change the current directory to the repository root folder and call the DocFX executable with the *pdf* and *docfx.json* parameters. This generates a *_pdf* subfоlder with a PDF file for each included table-of-contents file.
    ```
    docfx.exe pdf docfx.json
    ```

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
    docfx.exe build docfx.json --template statictoc
    ```
  The table of contents is embedded into each topic with this template which increases the build time and HTML file sizes. Alternatively, you can override the browser's restrictions (which may be unsecure). For example, Google Chrome and Microsoft Edge accept the `--allow-file-access-from-files` command line switch which allows loading local files.
  
  > We recommend using the `--serve` DocFX switch to preview documentation, and then share it with end users via a web server instead of browsing the file system.

If your issue is not listed, you can [submit a new issue to this repository](https://github.com/DevExpress/dotnet-eud/issues/new) or contact us via the [DevExpress Support Center](https://www.devexpress.com/Support/Center/). You can search the [DocFX issues list](https://github.com/dotnet/docfx/issues), or try building the [docfx\-seed](https://github.com/docascode/docfx-seed) sample documentation project to check if your issue is specific to this repository. 
