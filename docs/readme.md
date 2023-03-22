This folder contains the assets and markdown files, which are used for the [SparkFun Thing Plus - ESP32 WROOM (USB-C) Hookup Guide](https://sparkfun.github.io/SparkFun_Thing_Plus_ESP32_WROOM_C/). The documentation is built with [mkdocs](https://www.mkdocs.org/) utilizing the [Materials theme]( link here.


## File Organization
The documentation files are organized in the following fashion:

* All markdown files with the documentation for the hookup guide should be organized into separate sections.
* All assets utilized in the documentation *(i.e. images, pdf's, example code, etc.)* should be organized in folders.

### File Contents
* `index.md`
    * **Introduction**
        * **Required Materials** section
        * **Suggested Readings** section
* `hardware_overview.md`
    * Normal **Hardware Overview** section
* `hardware_assembly.md`
    * Normal **Hardware Assembly** section
* `software_overview.md`
    * Normal **Software Overview** section
* `troubleshooting_tips.md`
    * Normal **Troubleshooting Tips** section
* `resources.md`
    * Links to resources in the `board_files` folder
        * board dimensions (PDF): `dimensions.pdf`
            * PDF of the board dimensions
        * schematic (PDF): `schematic.pdf`
            * PDF of the board's schematic
        * eagle files (ZIP): `eagle_files.zip`
            * ZIP folder containing the `*.sch` and `*.brd` files
        * graphical datasheet (PDF): `graphical_datasheet.pdf` *(if available)*
            * PDF of the graphical datasheet
    * Links to resources in the `component_documentation` folder
        * The relevant datasheets for the board components in a PDF format
    * Links to our website
        * Product page
        * SparkFun hookup guide page _(if available, old **Learn** website)_
        * Product video
        * Pillar pages (i.e. Qwiic, Thing Plus, MicroMod, etc.)
        * Technical assistance page
    * Links to resources from the manufacturer's website
        * Product page
        * Product resources *(if available)*
        * Contact page
        * Forum
        * Community forum
        * etc.
* `single_page.md`


### Folders

Assets, such as example code, `*.pdf` files, or images that are linked in the documentation, should be organized in folders.

* `board_files` Folder
    * This folder should contain:
        * board dimensions (PDF): `dimensions.pdf`
            * PDF of the board dimensions
        * schematic (PDF): `schematic.pdf`
            * PDF of the board's schematic
        * eagle files (ZIP): `eagle_files.zip`
            * ZIP folder containing the `*.sch` and `*.brd` files
        * graphical datasheet (PDF): `graphical_datasheet.pdf` *(if available)*
            * PDF of the graphical datasheet
* `component_documentation` Folder
    * This folder should contain the relevant datasheets for the board components in a PDF format
        * Including those linked in the documentation
        * Example exception: restrictions by manufacturer
* `github` Folder
    * This folder includes the instructions for GitHub action (i.e. filing an issue and creating a pull request)
        * `file_issue.md` *(use template)*
            * Guidelines/information for filing issues
        * `contribute.md` *(use template)*
            * Guidelines/information for filing pull requests
* `graphical_datasheet` Folder *(if available)*
    * This folder should contain the graphical datasheet for the development board
    * Example exception: board use a third-party SDK
* `img` Folder
    * `sfe_logo_sm.png` - SparkFun flame logo (links to the homepage)
    * `hookup_guide` Folder
        * This folder should contain the images for the hookup guide
    * *other* Folders
        * Any other image files, which may be useful
            * May or may not be included in the documentation
            * May be available for future use