# ![Crow Translate logo](./dist/unix/generic/menuicons/72x72/apps/crow-translate.png) Crow Translate

[![GitHub (pre-)release](https://img.shields.io/github/release/Shatur95/CrowTranslate/all.svg)](https://github.com/Shatur95/CrowTranslate/releases)


**Crow Translate** is a simple and lightweight translator programmed in **C++ / Qt** that allows to translate and say selected text using the Google Translate API.
You may also be interested in my library [QOnlineTranslator](https://github.com/Shatur95/QOnlineTranslator "A library that provides free use of the Google Translate API for Qt5") used in this project. 

## Contents

* [Screenshots](#screenshots)
* [Features](#features)
* [Default keyboard shortcuts](#default-keyboard-shortcuts)
* [Dependencies](#dependencies)
* [Third-party libraries](#third-party-libraries)
* [Installation](#installation)

## Screenshots

**Main window:**

![Main window](./dist/unix/main-window-screenshot.png)
___

**Pop-up window:**

![Pop-up window](./dist/unix/popup-window-screenshot.png)

## Features

* Translate and say text in any application that supports text selection
* Translator window with native interface similar to Google Translate
* Highly customizable shortcuts
* Low memory consumption (~19MB)

## Default keyboard shortcuts

You can change these shortcuts in the settings. Some key sequences may not be available due to OS limitations.

### Global

|  Keys                         | Description             |
|-------------------------------|-------------------------|
| <kbd>Alt</kbd> + <kbd>X</kbd> | Translate selected text |
| <kbd>Alt</kbd> + <kbd>C</kbd> | Show main window        |
| <kbd>Alt</kbd> + <kbd>S</kbd> | Say selected text       |

### In main window

|  Keys                                             | Description               |
|---------------------------------------------------|---------------------------|
| <kbd>Ctrl</kbd> + <kbd>Return</kbd>               | Translate                 |
| <kbd>Ctrl</kbd> + <kbd>S</kbd>                    | Say input text            |
| <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd> | Say translated text       |

## Dependencies

**Arch Linux:** qt5-base qt5-multimedia gst-plugins-good openssl qt5-tools (make)

**Debian:** qt5-default qt5-qmake libqt5x11extras5-dev qtbase5-dev qtbase5-dev-tools qttools5-dev-tools qtmultimedia5-dev gstreamer1.0-fluendo-mp3 qtgstreamer-plugins-qt5 gstreamer1.0-plugins-good gstreamer1.0-alsa

## Third-party libraries

This project uses following third-party libraries:
* [QOnlineTranslator](https://github.com/Shatur95/QOnlineTranslator) - my library that provides free use of the Google Translate API for Qt5.
* [QHotkey](https://github.com/Skycoder42/QHotkey) - A global shortcut/hotkey for Desktop Qt-Applications.
* [SingleApplication](https://github.com/itay-grudev/SingleApplication) - A simple single instance application for Qt.

Therefore, if you want to clone this project, you need to use the `--recursive` option:

```bash
git clone --recursive git@github.com:Shatur95/CrowTranslate.git
```

or you can initialize these modules later:

```bash
git clone git@github.com:Shatur95/CrowTranslate.git
git submodule init
git submodule update
```

## Installation

### Automatic script

You can use the automatic script that builds **Crow Translate** and creates a package for your distribution:

```bash
cd dist/unix
./create-package
```

Than you can install it as usual. The script will tell you where the package will be after the making. Currently, only **Arch Linux**, **Debian** and their derivatives are supported.

### Arch Linux and derivatives

You can install [crow-translate-git](https://aur.archlinux.org/packages/crow-translate-git "A simple and lightweight translator that allows to translate and say the selected text using the Google Translate API") from AUR.

### Manual building

You can build **Crow Translate** by using the following commands:

```bash
qmake
make
make clean
```

Then you can use standalone binary `crow`.