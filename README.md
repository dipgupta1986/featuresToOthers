## What is features2Others?

features2Others is a simple script that **creates HTML based documentation from Cucumber features**. The resulting layout
is also suitable for printing as PDF from your favorite web browser.

Note that the documentation is **generated from the source Cucumber feature files, and NOT from the test results** (there
are plenty of other tools that can do that).

Use features2Others when you want to **create a nice looking requirements specification**, that you can email to your customer.
You can focus on editing the actual feature files and let features2Others make the features presentable to your customers.

---

---

### Installation

CLone the repo and then run below commans to download libraries,

```
npm install
```

## Usage

### Demo usage

To get the feel of it, run the script without any options. This will create a sample HTML file in the subfolder `output`,
from the example feature sources in `examples/features`, using the templates and css styles in `default/templates`:

```
node features2Others.js create
```
 

### Real world usage

Have a look at the switches available:

```
-h, --help                        output usage information
-V, --version                     output the version number
-i, --input-dir [path]            read feature files from path (default: examples/features)
-t, --templates-dir [path]        read the files doc_template.html, feature_template.html and style.css from path (default: default/templates)
-o, --output-file [path]          send output to file path (default: output/feature_YYYYMMDD_HHmm.html)
-p, --product-name [string]       The name of your product used in headline and header (default: My Product Name)
-a, --author [string]             The author name used in header (default: John Doe)
-b, --break-before-word [string]  create a line break before every occurrence of this word in the background (default: null)
-l, --lang [en|sv]                language used in feature files (default: en)

```

What you normally want to do is:
* Copy the three files in `default/templates` (two template files and one css file) to another folder anywhere on your computer.
* Modify the templates and styles according to your demands. If you are happy with the demo design, all you have
to do is modify the Lorem Ipsum intro text in the template file doc_template.html.
* Use switches to point to your folders for templates and features.

Example:

```
node features2Others.js -i path-to-your-feature-file-folder -t path-to-your-modified-templates-folder -a "Your Name" -p "Your Product Name" create
```

---
