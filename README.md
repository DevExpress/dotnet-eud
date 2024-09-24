# DevExpress End-User Documentation

> By accessing this repository, you agree to the terms of the [DevExpress End-User Documentation License Agreement](LICENSE.md).

Learn how to clone DevExpress End-User documentation and use sources as a white-labeled documentation. Create your own documentation websites and PDF files for projects based on DevExpress technologies. You can also review a sample pre-built website.

End-User Documentation contains information about [WinForms](https://www.devexpress.com/products/net/controls/winforms/) and ASP.NET [WebForms](https://www.devexpress.com/products/net/controls/asp/)/[MVC](https://www.devexpress.com/products/net/controls/asp/mvc/) products, as well as [Reporting](https://www.devexpress.com/subscriptions/reporting/) and [Business Intelligence Dashboard](https://www.devexpress.com/products/net/dashboard/).

If you search for **Developer Documentation with API Reference**, refer to [docs.devexpress.com](https://docs.devexpress.com).


## Document Format and Supported Output Types
Documents in this repository are written in markdown. You can manually copy the information to your own help file according to our [license](LICENSE.md).

The repository uses [DocFX](https://dotnet.github.io/docfx/) to convert these files from a set of markdown topics to an HTML website or a PDF file.

You can make the following changes to the documentation, or skip this step if you want to reuse the end-user documentation as is:
   
- Remove unnecessary files.
- Add new documents to your application. You should update the *toc.yml* ([table-of-content](https://dotnet.github.io/docfx/docs/table-of-contents.html)) files if you added or removed topics.
- Change screenshots to match your app's UI.
- Specify logo and site titles: [Template Metadata](https://dotnet.github.io/docfx/docs/template.html#template-metadata).
- Create a [custom DocFX template](https://dotnet.github.io/docfx/tutorial/howto_create_custom_template.html).

## View Content
Do one of the following to view the End-User Documentation content:

1. Browse this repository's content directly: [index.md](index.md)
1. View the sample pre-built website: [devexpress.github.io/dotnet-eud](https://devexpress.github.io/dotnet-eud/)
1. [Build an HTML Website](#build-an-html-website)
1. [Build PDF files](#build-pdf-files)

### Build an HTML Website

> Prerequisites
> - Familiarity with the command line
> - Install [.NET SDK](https://dotnet.microsoft.com/en-us/download) 6.0 or higher
> - [Git](https://git-scm.com/)

Make sure you have [.NET SDK](https://dotnet.microsoft.com/en-us/download) installed, then open a terminal and enter the following command to install the latest DocFX:

```bash
dotnet tool update -g docfx
```

> You can also download the latest version of DocFX directly: [releases](https://github.com/dotnet/docfx/releases).

Copy the repository to your computer and checkout the branch corresponding to the version of DevExpress controls your application uses. 

Do not use the `master` branch because it is the version currently under development:

```
git clone https://github.com/DevExpress/dotnet-eud
git switch 20.1
```

Once you switched to a version-based branch, you can make changes to the documentation.

To preview changes, open a console window and call the `docfx build` command with the path to *docfx.json* in the downloaded _dotnet-eud_ repository. DocFX will place the generated documentation content into the *\_site* folder. Add `--serve` to preview the generated website at http://localhost:8080 once the build process is complete. 

```bash
docfx build D:/dotnet-eud/docfx.json --serve
```
Docfx produces static HTML files under the _site folder ready for publishing to any static site hosting servers. Deploy the created documentation to a web server or browse the documentation directly from local file system. To begin, you can refer to the DocFX documentation: [Publish to GitHub Pages](https://dotnet.github.io/docfx/index.html#publish-to-github-pages).

### Build PDF Files
If your end users require a printed version, you can build a PDF file.

You can configure PDF file generation in several ways.

The resulted PDF file will be located near *toc.yml* in the *_site* folder.

#### Build locally

Open the console and call  `docfx pdf D:\test-eud\docfx.json`. You need a succeeded build before you proceed.

#### docfx.json

Include the `pdf` command to _docfx.json_. 

```json
{
  "build": {
    "fileMetadata":{
      "pdf": true
    }
  }
}
```

You can generate PDF only for a specific _toc.yml_:
  
```json
{
  "build": {
    "fileMetadata":{
      "pdf": {
        "dashboard-for-web/**/toc.yml": true
      }
    }
  }
}
```

#### toc.yml

Include the `pdf` command to _toc.yml_ to generate PDF according to this table of content: 

```yaml
pdf: true
items:
- name: Reporting for Web
  href: reporting-for-web/
  topicHref: reporting-for-web/articles/index.md
```

Refer to the following article for detailed instructions: [Create PDF Files](https://dotnet.github.io/docfx/docs/pdf.html).


## Troubleshooting

Below are the common issues you can face when building this repository's documentation. 

* #### The build failed with errors/warnings

  Refer to build output to find the cause of the problem.

* #### The build process fails with the *System.IO.PathTooLongException* exception
  Reduce your working directory's full path (move the repository closer to a drive root).

  *See also:* https://github.com/dotnet/docfx/issues/156
  
* #### The table of contents is not displayed when browsing the generated documentation from the file system
  Your browser security configuration may restrict executing the JavaScript code that accesses your local files (the table of contents is in a separate *toc.html* file when using the [default](https://github.com/dotnet/docfx/tree/dev/src/docfx.website.themes/default) DocFX template). In this case, you can use the [statictoc](https://github.com/dotnet/docfx/tree/dev/src/docfx.website.themes/statictoc) template instead. To switch to this template, add `--template statictoc` to the docfx.exe parameters:
    ```
    docfx.exe build ../dotnet-eud/docfx.json --template statictoc
    ```
  The table of contents is embedded into each topic with this template which increases the build time and HTML file sizes. Alternatively, you can override the browser's restrictions (which may be unsecure). For example, Google Chrome and Microsoft Edge accept the `--allow-file-access-from-files` command line switch which allows loading local files.
  
  > We recommend you to use the `--serve` DocFX switch to preview documentation, and then share it with end users via a web server instead of browsing the file system.

If your issue is not listed, you can [submit a new issue to this repository](https://github.com/DevExpress/dotnet-eud/issues/new) or contact us via the [DevExpress Support Center](https://supportcenter.devexpress.com/ticket/create). You can search the [DocFX issues list](https://github.com/dotnet/docfx/issues), or try building the [docfx-seed](https://github.com/docascode/docfx-seed) sample documentation project to check if your issue is specific to this repository.

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
