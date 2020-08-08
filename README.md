[![license](https://img.shields.io/badge/license-Apache%20License%202.0-blue.svg?style=flat)](http://www.apache.org/licenses/LICENSE-2.0)

# CUBA Translations Add-on

This project includes all available translations in the [translations](https://github.com/cuba-platform/translations) project in a single add-on. The goal is to help new users evaluating the platform in their native language (when available) because not all languages have a dedicated addon.

* This project only wraps CUBA-Platform translation project as an addon. Any changes in the translation values should be done in the translation project.
* English and Russian translations are removed because they are already included in CUBA-Platform by default.



## Available Translations

Translations availability depends on the content of the [translations](https://github.com/cuba-platform/translations) project. The following translations are currently available:



**Platform Version 7.2:**

| Component / Addon | Languages                                                    |
| ----------------- | ------------------------------------------------------------ |
| cuba              | Greek (el)<br />French (fr)<br />Brazilian Portuguese (pt_BR)<br />Romanian (ro) |
| bpm               | French (fr)                                                  |
| charts            | French (fr)<br />Brazilian Portuguese (pt_BR)                |
| fts               | French (fr)<br />Romanian (ro)                               |
| reports           | French (fr)<br />Romanian (ro)                               |



**Platform Version 7.1:**

| Component / Add-on | Languages                                                    |
| ------------------ | ------------------------------------------------------------ |
| cuba               | Danish (da)<br />German (de)<br />Spanish (es)<br />French (fr)<br />Italian (it)<br />Dutch (nl)<br />Portuguese (pt)<br />Brazilian Portuguese (pt_BR)<br />Romanian (ro)<br />Slovak (sk)<br />Turkish (tr)<br />Simplified Chinese (zh_CN) |
| bpm                | Danish (da)<br />German (de)<br />Spanish (es)<br />French (fr)<br />Italian (it)<br />Simplified Chinese (zh_CN) |
| charts             | German (de)<br />Spanish (es)<br />French (fr)<br />Italian (it)<br />Brazilian Portuguese (pt_BR)<br />Simplified Chinese (zh_CN) |
| fts                | German (de)<br />Spanish (es)<br />French (fr)<br />Italian (it)<br />Romanian (ro)<br />Turkish (tr)<br />Simplified Chinese (zh_CN) |
| reports            | Danish (da)<br />German (de)<br />Spanish (es)<br />French (fr)<br />Italian (it)<br />Romanian (ro)<br />Simplified Chinese (zh_CN) |
| bproc              | German (de)                                                  |
| idp                | Spanish (es)<br />French (fr)<br />Italian (it)<br />Turkish (tr) |

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
| 7.1.*            | 7.1.2          | br.com.petersonbr.translations:cuba-translations-addon-global:7.1.2 |
| 7.2.*            | 7.2.1          | br.com.petersonbr.translations:cuba-translations-addon-global:7.2.1 |

The latest stable version is: `7.2.1`



## Supported DBMS engines

_N/A_ - This component does not need any data



## Created tables

_NONE_



## Implementation Details

This project includes the [translations](https://github.com/cuba-platform/translations) project as a git submodule only to copy its content to the correct folders when installing locally or publishing to Bintray.

Two gradle taks have been created to automate the process:

* updateSubmodules: create and/or update the submodule contents
* copyTranslations: filter and copy the correct translation files to their correct folders in the addon