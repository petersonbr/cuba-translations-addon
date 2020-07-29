[![license](https://img.shields.io/badge/license-Apache%20License%202.0-blue.svg?style=flat)](http://www.apache.org/licenses/LICENSE-2.0)

# CUBA Translations Add-on

This project includes all available translations in the [translations](https://github.com/cuba-platform/translations) project in a single add-on. The goal is to help new users evaluating the platform in their native language (when available) because not all languages have a dedicated addon.

* This project only wraps CUBA-Platform translation project as an addon. Any changes in the translation values should be done in the translation project.
* English and Russian translations are removed because they are already included in CUBA-Platform by default.
* Some translations have a different folder hierarchy and will not work (IDP for example).



## Installation

1. Add the component repository to your `build.gradle` file:

```
repositories {
    maven {
        url  "https://dl.bintray.com/petersonbr/cuba-components" 
    }
}
```

2. Add the component [using Studio](https://doc.cuba-platform.com/manual-latest/app_components_usage.html#app_components_usage_by_studio) using a compatible version of the add-on:

| Platform Version | Add-on Version | Coordinates                                                  |
| ---------------- | -------------- | ------------------------------------------------------------ |
| 7.1.*            | 7.1.0          | br.com.petersonbr.translations:cuba-translations-addon-global:7.1.0 |
| 7.2.*            | 7.2.0          | br.com.petersonbr.translations:cuba-translations-addon-global:7.2.0 |

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