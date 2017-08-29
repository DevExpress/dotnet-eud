# DevExpress End-User Documentation

This **End-User Documentation** targets application end-users and explains how to use UI elements implemented by DevExpress. This information helps software developers create their own help files for projects that incorporate DevExpress technologies.

> For **Developer Documentation with API Reference** see [https://documentation.devexpress.com](https://www.devexpress.com/Support/Documentation/).

## The Scope
DevExpress products for WinForms, WPF and ASP.NET WebForms/MVC. 

## Licensing
By accessing this repository, you agree to be bound by the terms of the [DevExpress End-User Documentation License Agreement](LICENSE.md).

## Two Ways to Browse Content
To browse this repository's content, start with [index.md](index.md).  

We have also compiled this End-User Documentation into a sample website available at [devexpress.github.io/dotnet-eud](https://devexpress.github.io/dotnet-eud/).

## Document Format and Supported Output Types
Documents in this repository are written in markdown. One way to use them is to manually copy required information to your own help file.

The repository also includes a [docfx.json](docfx.json) file, which enables you to convert a set of topics to an HTML website or a PDF file using [DocFX](https://dotnet.github.io/docfx/) and [wkhtmltopdf](https://github.com/wkhtmltopdf/wkhtmltopdf).   

## Build an HTML Website
To create a documentation website for your application:

- Download and install the [latest version of DocFX](https://github.com/dotnet/docfx/releases). 
- Clone the repository to your computer and checkout the branch corresponding to the version of DevExpress controls your application uses. Make sure not to use the **master** branch, which represents the version currently under development.
    ```
    git clone https://github.com/DevExpress/dotnet-eud.git --branch 17.1
    ```
  If you do not have [Git](https://git-scm.com/) installed, select the required branch using the GitHub web interface and then download and extract the ZIP archive.
  
  ![Download ZIP](https://user-images.githubusercontent.com/20167812/29712204-4ffaee9e-89a1-11e7-8a0e-3ff0464adda4.png)
- If you want to reuse the end-user documentation as is, skip this step. Otherwise, make changes as required, which may include:
  - removing files that are not needed in your documentation;
  - adding new documents specific to your application;
  - changing screenshots to match your app UI;
  - creating a [custom DocFX template](https://dotnet.github.io/docfx/tutorial/howto_create_custom_template.html).
  > Make sure to update *toc.yml* ([table-of-content](https://dotnet.github.io/docfx/tutorial/intro_toc.html)) files if you have added or removed topics.
- Open a console window, change the current directory to the repository root folder and call the DocFX executable with the *build* and *docfx.json* parameters. DocFX will place the generated documentation content into the *\_site* folder. Add the *--serve* switch to preview the generated website at http://localhost:8080 once the build process is complete. 
    ```
    docfx.exe build docfx.json --serve
    ```
- Finally, deploy the created documentation to a web server or browse the documentation directly from local file system. Since DocFX creates static HTML files only, no additional deployment or configuration steps are required.

## Build Printer-Friendly PDF Files
If your end-users require a printed version, you can create a PDF file:
- Ensure that you can successfully build a website with DocFX (see the [previous section](#build-your-own-documentation-website)).
- Download and install [wkhtmltopdf](https://wkhtmltopdf.org/downloads.html).
- Open a console window and add the **wkhtmltopdf** executable path to the %PATH% environment variable:
    ```
    set PATH=%PATH%;C:\Program Files\wkhtmltopdf\bin
    ```
- Change the current directory to the repository root folder and call the DocFX executable with the *pdf* and *docfx.json* parameters. This will generate a *_pdf* subfоlder with a PDF file for each included table-of-contents file.
    ```
    docfx.exe pdf docfx.json
    ```

## Troubleshooting
Below are the common issues you may face when building this repository's documentation. 

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
  The table of contents is embedded into each topic with this template which increases the build time and HTML file sizes. Alternatively, you can override the browser's restrictions (which may be insecure). For example, Google Chrome and Microsoft Edge accept the `--allow-file-access-from-files` command line switch which allows loading local files.
  
  > We recommend using the `--serve` DocFX switch to preview documentation, and then share it with end users via a web server, instead of browsing the file system 

If your issue is not listed, do not hesitate to [submit a new issue to this repository](https://github.com/DevExpress/dotnet-eud/issues/new) or contact us using the [DevExpress Support Center](https://www.devexpress.com/Support/Center/). You can search the [DocFX issues list](https://github.com/dotnet/docfx/issues), or try building the [docfx\-seed](https://github.com/docascode/docfx-seed) sample documentation project to check if your issue is specific to this repository. 

## Obtain End-User Documentation for Versions Prior to 17.1
This repository provides help files for DevExpress versions 17.1 and above. End-user documentation for previous versions is published in CHM and PDF formats at https://www.devexpress.com/Support/Documentation/download.xml?platform=user-dev-docs.
