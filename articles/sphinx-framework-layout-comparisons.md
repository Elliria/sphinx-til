# Sphinx Framework Layout Comparisons

## About
There are two repository layouts that are often used for Sphinx in projects around the world. One puts Sphinx and your content into one repository and the other splits Sphinx and your content between two separate repositories. The directory maps below show the basic structural differences between them.

### Single Layout
This layout keeps the project's contents and their Sphinx framework in one repository and Sphinx references the project files internally.

The **sphinx-single** repository:
```text
sphinx-single/                   # Directory - Sphinx and your contents
├── .github/                     # Directory - GitHub assets
│   └── workflows/               # Directory - workflows
│       └── ci.yml               # File - CI pipeline
├── codebase/                    # Directory - your content
│   └── example.py               # File - Python module with reST docstrings
├── sphinx/                      # Directory - Sphinx framework
│   ├── conf.py                  # File - Sphinx configuration
│   ├── index.rst                # File - Sphinx root document
│   └── resources/               # Directory - documentation assets
│       ├── images/              # Directory - image assets
│       ├── rst/                 # Directory - documentation assets
│       │   ├── installation.rst # File - documentation
│       │   └── usage.rst        # File - documentation
│       ├── scripts/             # Directory - local automation scripts
│       ├── static/              # Directory - custom CSS style-sheets
│       └── templates/           # Directory - custom structural HTML overrides
├── .gitignore                   # File - defensive tracking shield
├── LICENSE                      # File - shared software license
└── README.md                    # File - main repository document
```
See a live example on GitHub: [https://github.com/sphinx-playground/sphinx-single](https://github.com/sphinx-playground/sphinx-single)

### Split Layout
This layout separates the project's contents from their Sphinx framework in two repositories and Sphinx references the project files externally.

And the **sphinx-split-host** repository:
```text
sphinx-split-host/               # Directory - Sphinx
├── .github/                     # Directory - GitHub assets
│   └── workflows/               # Directory - workflows
│       └── ci.yml               # File - CI pipeline
├── sphinx/                      # Directory - Sphinx framework
│   ├── conf.py                  # File - Sphinx configuration
│   ├── index.rst                # File - Sphinx root document
│   └── resources/               # Directory - documentation assets
│       ├── images/              # Directory - image assets
│       ├── rst/                 # Directory - documentation assets
│       │   ├── installation.rst # File - documentation
│       │   └── usage.rst        # File - documentation
│       ├── scripts/             # Directory - local automation scripts
│       ├── static/              # Directory - custom CSS style-sheets
│       └── templates/           # Directory - custom structural HTML overrides
├── .gitignore                   # File - defensive tracking-shield
├── LICENSE                      # File - shared software license
└── README.md                    # File - main repository document
```

The **sphinx-split-guest** repository:
```text
sphinx-split-guest/ # Directory - your contents
├── codebase/       # Directory - your example content
│   └── example.py  # File - Python module with reST docstrings
├── .gitignore      # File - defensive tracking shield
├── LICENSE         # File - shared software license
└── README.md       # File - main repository document
```
See a live example on GitHub: [https://github.com/sphinx-playground/sphinx-split-guest](https://github.com/sphinx-playground/sphinx-split-guest)

## License
```text
MIT License

Copyright (c) 2026 Elliria

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
For more information, see  [The MIT License](https://opensource.org/license/MIT).
