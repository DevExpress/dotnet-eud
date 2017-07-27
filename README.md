# DevExpress End-User Documentation

In addition to [developer documentation](https://www.devexpress.com/Support/Documentation/), DevExpress also provides **end-user documentation** for its Desktop (Windows Forms & WPF) and ASP.NET products. This documentation contains information on individual user interface elements (such as grids, navigation panes, data editors, charts, etc.), and provides instructions for end-users about how to solve the most-common tasks with these interface elements.

The main goal of this repository is to provide developers who create applications with DevExpress .NET controls with drafts for their own help documents. You can distribute the included help documents to your end-users "as is" or create documentation for your own products based on them. Help documents are provided as markdown files, which are easy to edit and reuse. The [docfx.json](docfx.json) file allows you to build a documentation website using the [DocFX](https://dotnet.github.io/docfx/) documentation generation tool.

## Browse End-User Documentation
You can browse the end-user documentation content starting from the [index.md](index.md) document.

## Build Your Own Documentation Website
Follow the steps below to create the documentation website for your application. 
- Download and install the [latest version of DocFX](https://github.com/dotnet/docfx/releases). 
- Choose the repository branch corresponding to the DevExpress controls version your application is based on. The **master** branch corresponds to the version which is currently in development and generally there is no need to use it.
- Clone this repository to your computer, or download and extract the ZIP file.
- If you want to reuse the end-user documentation as is, skip this step. Otherwise, make the required changes that may include:
  - removing files that are not needed in your documentation;
  - adding new documents specific to your application;
  - changing screenshots to match your app UI;
  - creating a [custom DocFX template](https://dotnet.github.io/docfx/tutorial/howto_create_custom_template.html);
  - etc...
  > Do not forget to update *toc.yml* ([table-of-content](https://dotnet.github.io/docfx/tutorial/intro_toc.html)) files if you have created or removed certain topics.
- Build the website. Open the console window and call the DocFX executable with the *docfx.yml* file as a parameter. Optionally, you can pass the *--serve* command line switch - it allows you to immediately view the generated website at http://localhost:8080 when the build process is completed. The documentation content is placed into the *\_site* folder.
    ```
    docfx.exe docfx.json --serve
    ```
- Finally, you can deploy the created documentation to any web server or even browse the documentation directly from the local file system, as DocFX creates static HTML files only.

## Obtain End-User Documentation for Versions Prior to 17.1
This repository provides help files for DevExpress product versions starting from 17.1. End-user documentation for previous versions is published in CHM and PDF formats at https://www.devexpress.com/Support/Documentation/download.xml?platform=user-dev-docs.

## Licensing Questions
According to the [End-User Documentation License Agreement](LICENSE.md), you have a permit to modify, re-use and distribute this end-user documentation.
