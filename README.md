
# `pdf-tool/pdftool` documentation

---
# Table of Contents
1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Supported Actions](#supported-actions)
4. [Supported Options](#supported-options)
5. [Example Usage](#example-usage)
6. [Value Constraints](#value-constraints)
7. [Usage Synopsis](#usage-synopsis)
8. [Options and Examples](#options-and-examples)
9. [Execution Assurance](#execution-assurance)
10. [Notes](#notes)
11. [Authors and Contributors](#authors-and-contributors)

---

## Overview

`pdf-tool` (version 1.0.1) is a versatile Linux command-line utility designed to manipulate PDF files. With `pdf-tool`, you can <br /> 
perform a wide range of actions such as **compressing**, **rotating**, **numbering**, **concatenating**, **extracting**, **including**, <br />
**excluding**, **encrypting**, **decrypting**, **bursting**, **stamping** ... PDF files.

Once the package is installed, you can use the alias `pdftool` instead of `pdf-tool`.

---

## Get started

To install the PDF file, follow these steps:

1. **Clone the repository**  <br />
   Run the following command to clone the repository with the specified branch:
   ```bash
   git clone --depth 1 --branch v1.0.1-electron https://github.com/baldeuniversel/pdf-tool.git

2. **Install the package** <br />
   Once the repository is cloned, install the package using the following command:
   ```bash
   sudo dpkg --install pdf-tool/package/deb/pdf-tool-1.0.1.deb

3. **Install the dependencies if necessary** (optional/requirement) <br />
   If you use `apt` as package manager
   ```bash
   sudo apt install -f 

---

## Requirements

### Supported Actions

The following actions are supported by `pdf-tool`:

- `--extract`
- `--number`
- `--concat`
- `--compress`
- `--rotate`
- `--include`
- `--exclude`
- `--stamp`
- `--burst`
- `--encrypt`
- `--decrypt`
- `--doc`
- `--help`
- `--version`

### Supported Options

These are the options that can be used with the actions:

- `--input` or `-i`
- `--from` or `-f`
- `--to` or `-t`
- `--source` or `-s`
- `--destination` or `-d`
- `--after-page` or `-a`
- `--level` or `-l`
- `--cardinal` or `-c`
- `--scope` or `-s`
- `--output` or `-o`

**Note:** When executing an action, at least one option must be provided (except for `--help`, `--doc`, and `--version`).

#### Example Usage

```sh
pdf-tool --extract --input <pdf-file.pdf> --from 1 --to 2 --output <new-pdf.pdf>
```

### Value Constraints

- **Positive Integers:** Options like `--from`, `--to`, `--level`, and `--after-page` require a positive integer as a value.
- **String Values:** Options like `--cardinal` and `--scope` require string values.
- **PDF Files:** Options like `--input`, `--source`, and `--destination` require valid PDF file paths.

**Note:** For the `--concat` action, multiple PDF files can be provided as inputs.

---

## Usage Synopsis

```sh
pdf-tool [action] || [action] [option] [argument(s)] [option] [argument(s)]
```

---

## Options and Examples

### `--extract`
Extract pages from a PDF file.

```sh
pdf-tool --extract --input <pdf-file.pdf> --from 1 --to 2 --output <new-pdf.pdf>
```

### `--number`
Add page numbers to a PDF.

```sh
pdf-tool --number --input <pdf-file.pdf> --output <new-pdf.pdf>
```

### `--concat`
Concatenate multiple PDF files.

```sh
pdf-tool --concat --input <pdf-file1.pdf> <pdf-file2.pdf> --output <new-pdf.pdf>
```

### `--compress`
Compress a PDF file.

```sh
pdf-tool --compress --input <pdf-file1.pdf> --level 4 --output <new-pdf.pdf>
```

### `--rotate`
Rotate pages in a PDF file.

```sh
pdf-tool --rotate --input <pdf-file1.pdf> --cardinal east --output <new-pdf.pdf>
```

### `--include`
Include a PDF file into another.

```sh
pdf-tool --include --source <pdf-file1.pdf> --destination <pdf-file2.pdf> --after-page 2 --output <new-pdf.pdf>
```

### `--exclude`
Exclude specific pages from a PDF.

```sh
pdf-tool --exclude --input <pdf-file1.pdf> --from 3 --to 5 --output <new-pdf.pdf>
```

### `--stamp`
Stamp a PDF with a specific scope.

```sh
pdf-tool --stamp --input <pdf-file1.pdf> --scope confidential --output <new-pdf.pdf>
```

### `--burst`
Burst a PDF file into individual pages.

```sh
pdf-tool --burst --input <pdf-file1.pdf> --output <new-template-name.pdf>
```

### `--encrypt`
Encrypt a PDF file.

```sh
pdf-tool --encrypt --input <pdf-file.pdf> --output <new-pdf-encrypted.pdf>
```

### `--decrypt`
Decrypt a PDF file.

```sh
pdf-tool --decrypt --input <pdf-file.pdf> --output <new-pdf-decrypted.pdf>
```

### `--doc`
View the documentation.

```sh
pdf-tool --doc
```

### `--help`
Get help on using `pdf-tool`.

```sh
pdf-tool --help
```

### `--version`
Check the current version of `pdf-tool`.

```sh
pdf-tool --version
```

---

## Execution Assurance

To ensure successful execution, the command must follow the specified preconditions. Each action must be accompanied by the appropriate options and arguments in the correct sequence, as outlined above.

---

## Notes

`pdf-tool` depends on several external programs. These dependencies are included in the global package of `pdf-tool`. Once an action like `--encrypt` is called, the order of subsequent options is flexible.

---

## Authors and Contributors

**Author:**  
Baldé Amadou (<baldeuniversel@protonmail.com>)

**Contributor:**  
Diallo Ismaila (<diallois@protonmail.com>)

---

## Wiki 
### [Get started](#get-started)
Learn how to install `pdf-tool`.

<!-- ## Wiki

### [Get started](#getting-started)
Learn how to install `pdf-tool`.

### [Advanced Usage](#advanced-usage)
Explore advanced use cases and examples.

### [Troubleshooting](#troubleshooting)
Find solutions to common issues encountered when using `pdf-tool`.

### [FAQ](#faq)
Frequently asked questions about `pdf-tool`.

-->

---

This documentation aims to provide comprehensive guidance on using `pdf-tool` effectively. <br />
For any request, write to me via this email address : (<baldeuniversel@protonmail.com>)
