# WOOL Documentation
This repository contains documentation for the WOOL Language in ASCIIDOC format (www.asciidoc.org) that can be compiled into the documentation website at https://www.woolplatform.eu/docs/ using Antora.

## Documentation Content
The actual documentation content can be found in the /docs/ folder, where the different documentation modules can be found.

## DrawIO Source Files
In the /drawio/ folder, source files for diagrams used in the documentation can be found.

## WOOL Documentation Antora Playbooks
This repository also contains two Antora Playbook files for generating the WOOL Documentation site, as well as the UI Bundle, which is a modification of the Antora Default UI.

See https://docs.antora.org/antora/2.3/ for detailed documentation on using Antora.

In short, if you want to generate the WOOL Documentation yourself:

 - Install Antora Command Line Interface (CLI): https://docs.antora.org/antora/2.3/install/install-antora/
 - Clone this repository to $PATH/wool-documentation
 - Open a terminal in $PATH/wool-documentation
 - Run `antora --fetch antora-playbook.yml`
 - This will generate the `/build/` folder, in which you can find `/build/site/index.html` which is the entry-point for the documentation.

Alternatively, if you are writing new documentation, you may use the `antora-playbook-author-mode.yml` file to use the local repository contents for generating the documentation, without having to commit work-in-progress documentation (see https://docs.antora.org/antora/2.1/playbook/author-mode/).

## Antora "WOOL" UI
The /wool-ui/ folder contains the source for generating the WOOL UI Bundle, which is a fork of the Antora Default UI (https://gitlab.com/antora/antora-ui-default).

For detailed instructions on how to make modifications to the UI and build the ui-bundle.zip file that is used in the Antora Playbook, see: https://docs.antora.org/antora-ui-default/

As a quick reference, use the following commands:
 * `gulp preview` - to launch a preview server (localhost:5252), useful for testing changes
 * `gulp bundle` - to create the ui package (generates a new version of `/wool-ui/build/ui-bundle.zip` (copy this to `/wool-ui/release/ui-bundle.zip` so that it will be used by the Antora Playbooks mentioned above).
