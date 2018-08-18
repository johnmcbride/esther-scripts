# Getting started 

This guide will show you how to build this repository into a script package and an RSS feed for use within the [Citrix Developer Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=CitrixDeveloper.citrixdeveloper-vscode)

## Pre-requisites

In order to create the script packages and RSS feed you will need to install two Citrix npm packages.

- [citrix-script-packager](https://www.npmjs.com/package/citrix-script-packager)

    This is the tool that helps you create the initial package and packages up the files into a vsix file

    ```sh
    npm install -g citrix-script-packager
    ```

- [citrix-script-feed](https://www.npmjs.com/package/citrix-script-feed)

    This tool helps create an RSS feed, that can then be used within the Citrix Developer extension. The RSS feed can be hosted anywhere, network share, web server, github, etc.

    ```sh
    npm install -g citrix-script-feed
    ```

## Build Instructions

You can follow the steps below to create a new VSIX script package, for example if you would like to add a new script or update an existing script.

### Adding a new script

- Create a new folder under the packages/[friendlyname]/ folder

- Copy you new script(s) into this new folder

### Updating existing script

- Override the existing script in the correct folder under the packages/[friendlyname]/ folder with the new one you have created.

### Building package

Once you have all the files you need in the packages/[friendlyname] run the following commands

- Change into the root of the project directory

- Package the scripts into a vsix with the following command

    ```sh
    citrix-script-packager -p
    ```

    This will create a single vsix file with all the scripts you have added to the packages directory in the output directory.

- Once you have the vsix created you can then either.

    - Create an RSS feed
    - Install the visx manually

## Creating RSS feed (if needed)

## Citrix Extension Developer Instructions