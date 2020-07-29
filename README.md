[![license](https://img.shields.io/badge/license-Apache%20License%202.0-blue.svg?style=flat)](http://www.apache.org/licenses/LICENSE-2.0)

# CUBA Translations Add-on

This project includes all available translations in the [translations](https://github.com/cuba-platform/translations) project in a single add-on. The goal is to help new users evaluating the platform in their native language (when available) because not all languages have a dedicated addon.

## Installation

**NOTE**: This add-on's repository is officially linked to the main CUBA repository.

You can use **CUBA Studio** / **IntelliJ IDEA** to add it to your project: choose the `CUBA -> Marketplace...` menu item,
find the *Italian Translation* add-on, then click on the `Install` button.

The following table shows which version of the add-on is compatible with which version of the framework:

| Platform Version | Add-on Version | Coordinates
| ---------------- | -------------- | ------------
| 7.1.*            | 7.1.0          | br.com.petersonbr.translations:cuba-translations-addon-global:7.1.0
| 7.2.*            | 7.2.0          | br.com.petersonbr.translations:cuba-translations-addon-global:7.2.1

The latest stable version is: `7.2.0`

## Supported DBMS engines

_N/A_ - This component does not need any data

## Created tables

_NONE_

## Implementation Details

This project includes the [translations](https://github.com/cuba-platform/translations) project as a git submodule only to copy its content to the correct folders when installing locally or publishing to Bintray.

Two gradle taks have been created to automate the process:

* updateSubmodules: create and/or update the submodule contents
* copyTranslations: filter and copy the correct translation files to their correct folders in the addon