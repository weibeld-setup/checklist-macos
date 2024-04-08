# Checklist: macOS

![macOS](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/macos.svg)

Checklist for setting a and personalising a new macOS installation.

## Contents

<!-- 1. Vim plugin: https://github.com/mzlogin/vim-markdown-toc              -->
<!-- 2. Remove:     "<DELETE-ME>"                                            -->
<!-- 3. Set:        :let g:vmt_list_item_char = '- [ ]'                      -->
<!--                :let g:vmt_max_level = 2                                 -->
<!-- 4. Save:       ToC is automatically generated on saving of file         -->

<!-- vim-markdown-toc GFM -->

- [ ] [Install updates](#install-updates)
- [ ] [Disable iCloud Drive](#disable-icloud-drive)
- [ ] [Customise trackpad gestures](#customise-trackpad-gestures)
- [ ] [Customise modifier keys](#customise-modifier-keys)
- [ ] [Disable the 🌐 key](#disable-the--key)
- [ ] [Disable startup sound](#disable-startup-sound)
- [ ] [Disable power chime](#disable-power-chime)
- [ ] [Disable floating screenshot thumbnails](#disable-floating-screenshot-thumbnails)
- [ ] [Enable snap-to-grid for Desktop icons](#enable-snap-to-grid-for-desktop-icons)
- [ ] [Customise menu bar](#customise-menu-bar)
- [ ] [Customise Dock](#customise-dock)
- [ ] [Customise Spaces](#customise-spaces)
- [ ] [Customise Finder](#customise-finder)
- [ ] [Customise TextEdit](#customise-textedit)
- [ ] [Enable keyboard brightness adjustment keys (optional)](#enable-keyboard-brightness-adjustment-keys-optional)
- [ ] [Install custom keyboard layout](#install-custom-keyboard-layout)
- [ ] [Install Xcode Command Line Tools](#install-xcode-command-line-tools)
- [ ] [Install Homebrew](#install-homebrew)
- [ ] [Install Homebrew formulas from Brewfile](#install-homebrew-formulas-from-brewfile)
- [ ] [Set Bash as the default shell](#set-bash-as-the-default-shell)
- [ ] [Install dotfiles](#install-dotfiles)
- [ ] [TODO: Install sudoers file](#todo-install-sudoers-file)
- [ ] [Apply iTerm2 settings](#apply-iterm2-settings)
- [ ] [Apply settings of optional tools](#apply-settings-of-optional-tools)
- [ ] [Set up Google Drive](#set-up-google-drive)
- [ ] [Set up Google Chrome](#set-up-google-chrome)
- [ ] [Set up Fluor](#set-up-fluor)
- [ ] [Install eduroam](#install-eduroam)
- [ ] [Install fonts](#install-fonts)

<!-- vim-markdown-toc -->

## Install updates

System updates:

1. Go to _**System Settings → General → Software Update**_
1. Install all available updates

App updates:

1. Go to _**App Store → Updates**_
1. If there are any updates, click on _**Update All**_

[↑ Top](#contents)

## Disable iCloud Drive

1. Go to _**System Settings → Apple ID → iCloud → Apps Using iCloud**_
1. Set _**iCloud Drive**_ to _**Off**_

> This prevents distracting options in file opening and saving dialogs.

[↑ Top](#contents)

## Customise trackpad gestures

Enable tap to click:

1. Go to _**System Preferences → Trackpad**_
1. Make sure that the _**Point & Click**_ tab is open
1. Enable _**Tap to click**_

Disable opening the Notification Centre when swiping left from the right edge of the trackpad with two fingers:

1. Go to _**System Preferences → Trackpad**_
1. Open the _**More Gestures**_ tab
1. Disable _**Notification Centre**_

> **Note:** the above gesture is disabled to prevent accidential triggering when swiping between pages.

Enable dragging of windows with three fingers:

1. Go to _**System Preferences → Accessibility → Pointer Control → Trackpad Options...**_
1. Enable _**Use trackpad for dragging**_
1. Set _**Dragging style**_ to _**Three-Finger Drag**_

[↑ Top](#contents)

## Customise modifier keys

1. Go to _**System Preferences → Keyboard → Keyboard Shortcuts... → Modifier Keys**_
1. Set _**Caps Lock (⇪) key**_ to _**⌃ Control**_
1. Set _**Control (⌃) key**_ to _**⇪ Caps Lock**_
1. Set _**Option (⌥) key**_ to _**⌘ Command**_
1. Set _**Command (⌘) key**_ to _**⌥ Option**_

> **Note:** the above must be set separately for every connected keyboard (e.g the built-in keyboard and an external Magic Keyboard) by selecting the appropriate keyboard in the _**Select keyboard**_ dropdown list.

[↑ Top](#contents)

## Disable the 🌐 key

1. Go to _**System Preferences → Keyboard**_
1. Set _**Press 🌐 key to**_ to _**Do Nothing**_

> **Note:** this makes the 🌐 key act like a normal _fn_ (function) key (e.g. for typing F1, F2, etc.). The 🌐 key functionality is not really needed as the input source can always be changed with `Ctr-Space`.

[↑ Top](#contents)

## Disable startup sound

1. Go to _**System Settings → Sound**_
1. Disable _**Play sound on startup**_

[↑ Top](#contents)

## Disable power chime

1. Execute the following:
   ```bash
   defaults write com.apple.PowerChime ChimeOnNoHardware -bool true
   ```
1. Log out of macOS and log in again

> **Note:** the power chime is a sound that plays when connecting a charging cable.

[↑ Top](#contents)

## Disable floating screenshot thumbnails

1. Press `Cmd-Shift-5`
1. Open the _**Options**_ dropdown list
1. Disable _**Show Floating Thumbnail**_

> **Note:** this saves all screenshots immediately to the file system and prevents the floating thumbnail animation in the lower right corner of the screen.

[↑ Top](#contents)

## Enable snap-to-grid for Desktop icons

1. Right-click on the Desktop background
1. Click on _**Show View Options**_
1. Set _**Sort By**_ to _**Snap to Grid**_

[↑ Top](#contents)

## Customise menu bar

1. Go to _**System Preferences → Control Centre**_
1. Set _**Bluetooth**_ to _**Show in Menu Bar**_
1. Set _**Focus**_ to _**Don't Show in Menu Bar**_
1. Set _**Sound**_ to _**Always Show in Menu Bar**_
1. Set _**Spotlight**_ to _**Don't Show in Menu Bar**_
1. Under _**Battery**_, enable _**Show Percentage**_
1. Rearrange the icons in the menu bar by holding the ⌘-key and dragging the icons directly in the menu bar

[↑ Top](#contents)

## Customise Dock

1. Go to _**System Preferences → Desktop & Dock**_
1. Enable _**Automatically hide and show the Dock**_
1. Disable _**Show suggested and recent apps in Dock**_
1. Select which items to include in the Dock by dragging unwanted items to the Bin and dragging wanted apps and directories into the dock

[↑ Top](#contents)

## Customise Spaces 

Disable automatic rearrangement:

1. Go to _**System Preferences → Desktop & Dock**_
1. In the _**Mission Control**_ section, disable _**Automatically rearrange Spaces based on most recent use**_

Create desired number of Spaces:

1. Swipe up with four fingers to open Mission Control
1. Move cursor to the top of the screen to reveal the Spaces strip
1. Click on the + on the right side of the Spaces strip to add the desired number of spaces

[↑ Top](#contents)

## Customise Finder

Customise sidebar:

1. Go to _**Finder → Settings → Sidebar**_
1. In the _**Favourites**_ section, enable only the _**Applications**_, _**Desktop**_, and _**Home**_ items
1. In the _**iCloud**_ section, disable all items
1. In the _**Locations**_ section, enable only the _**Hard disks**_, _**External disks**_, and _**CDs, DVDs and iOS Devices**_ items
1. In the _**Tags**_ section, disable all items

Disable hiding of filename extensions and warnings:

1. Go to _**Finder → Settings → Advanced**_
1. Enable _**Show all filename extensions**_
1. Disable _**Show warning before changing an extension**_

Set default location:

1. Go to _**Finder → Settings → General**_
1. In the _**New Finder windows show:**_ dropdown list, select _**Desktop**_

Restrict search to current folder:

1. Go to _**Finder → Settings → Advanced**_
1. In the _**When performing a search:**_ dropdown list, select _**Search the Current Folder**_

Show Path Bar and Status Bar:

1. Go to _**Finder → View**_
1. Click on _**Show Path Bar**_
1. Click on _**Show Status Bar**_

[↑ Top](#contents)

## Customise TextEdit

Set default window style:

1. Go to _**TextEdit → Settings → New Document**_
1. Set _**Format**_ to _**Plain text**_
1. Set _**Width**_ to _**80**_
1. Set _**Plain text font**_ to _**Menlo Regular 12**_
1. Disable **all** the options under the _**Options**_ section

Disable markup rendering:

1. Go to _**TextEdit → Settings → Open and Save**_
1. Enable _**Display HTML files as HTMl code instead of formatted text**_
1. Enable _**Display RTF files as RTF code instead of formatted text**_

Disable automatic adding of file extensions:

1. Go to _**TextEdit → Settings → Open and Save**_
1. Disable _**Add ".txt" extension to plain text files**_

[↑ Top](#contents)

## Enable keyboard brightness adjustment keys (optional)

> **Note:** this step is only necessary if the built-in keyboard does **not** have dedicated keys for adjusting the keyboard brightness (usually bundled with the F5 and F6 keys).

1. Save the following as **`~/Library/LaunchAgents/com.local.KeyRemappings.plist`**:
   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
   <plist version="1.0">
   <dict>
       <key>Label</key>
       <string>com.local.KeyRemapping</string>
       <key>ProgramArguments</key>
       <array>
           <string>/usr/bin/hidutil</string>
           <string>property</string>
           <string>--set</string>
           <!-- Keys:                                                           -->
           <!--   0xC000000CF:  Dictation                                       -->
           <!--   0x10000009B:  Focus                                           -->
           <!--   0xFF00000008: Keyboard brightness up                          -->
           <!--   0xFF00000009: Keyboard brightness down                        -->
           <string>{"UserKeyMapping":[
               {
                 "HIDKeyboardModifierMappingSrc": 0xC000000CF,
                 "HIDKeyboardModifierMappingDst": 0xFF00000009
               },
               {
                 "HIDKeyboardModifierMappingSrc": 0x10000009B,
                 "HIDKeyboardModifierMappingDst": 0xFF00000008
               }
           ]}</string>
       </array>
       <key>RunAtLoad</key>
       <true/>
   </dict>
   </plist>
   ```
1. Log out of macOS and log in again

> **Background:** traditonally, Apple keyboards had two keys for decreasing and increasing the keyboard brightness bundled with the F5 and F6 key, respectively. However, in newer versions (since the introduction of Apple silicon chips), these keys have been exchanged for the _Dication_ and _Focus_ keys. The above script remaps the functions of these keys back to decreasing and increasing the keyboard brightness, as it used to be on older keyboards.

References: 

- https://www.idownloadblog.com/2022/03/25/bring-back-keyboard-brightness/
- https://github.com/amarsyla/hidutil-key-remapping-generator/issues/33#issuecomment-1431296356

[↑ Top](#contents)

## Install custom keyboard layout

![GitHub Repo: Install](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/github-repo-install.svg)

👉 [**weibeld-setup/install-keyboard-layout**](https://github.com/weibeld-setup/install-keyboard-layout)

[↑ Top](#contents)

## Install Xcode Command Line Tools

1. Execute the following to launch the installation dialog:
   ```bash
   xcode-select --install
   ```
1. Complete the installation through the installation dialog

[↑ Top](#contents)

## Install Homebrew

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

> **Note:** see instructions on [brew.sh](https://brew.sh/).

[↑ Top](#contents)

## Install Homebrew formulas from Brewfile

![GitHub Repo: Install](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/github-repo-install.svg)

👉 [**weibeld-setup/install-brewfile**](https://github.com/weibeld-setup/install-brewfile)

[↑ Top](#contents)

## Set Bash as the default shell

1. Execute the following:
   ```bash
   echo "$HOMEBREW_PREFIX"/bin/bash | sudo tee -a /etc/shells >/dev/null
   chsh -s "$HOMEBREW_PREFIX"/bin/bash
   sudo chsh -s "$HOMEBREW_PREFIX"/bin/bash
   ```
1. Quit the terminal application

> **Note:** the above sets the instance of Bash installed by Homebrew as the default shell, replacing Zsh as the default shell.

[↑ Top](#contents)

## Install dotfiles

![GitHub Repo: Install](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/github-repo-install.svg)

👉 [**weibeld-setup/install-dotfiles**](https://github.com/weibeld-setup/install-dotfiles)

[↑ Top](#contents)

## TODO: Install sudoers file

![GitHub Repo: Install](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/github-repo-install.svg)

👉 [**weibeld-setup/install-sudoers**](https://github.com/weibeld-setup/install-sudoers)

> **TODO:** adapt for macOS.

[↑ Top](#contents)

## Apply iTerm2 settings

![GitHub Repo: Settings](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/github-repo-settings.svg)

👉 [**weibeld-setup/settings-iterm2**](https://github.com/weibeld-setup/settings-iterm2)

[↑ Top](#contents)

## Apply settings of optional tools

### Android Studio

![GitHub Repo: Settings](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/github-repo-settings.svg)

👉 [**weibeld-setup/settings-android-studio**](https://github.com/weibeld-setup/settings-android-studio)

### Visual Studio Code

![GitHub Repo: Settings](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/github-repo-settings.svg)

👉 [**weibeld-setup/settings-vscode**](https://github.com/weibeld-setup/settings-vscode)

## Set up Google Drive

[↑ Top](#contents)

## Set up Google Chrome

[↑ Top](#contents)

## Set up Fluor

[↑ Top](#contents)

## Install eduroam

![GitHub Repo: Install](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/github-repo-install.svg)

👉 [**weibeld-setup/install-eduroam**](https://github.com/weibeld-setup/install-eduroam)

[↑ Top](#contents)

## Install fonts

![GitHub Repo: Install](https://raw.githubusercontent.com/weibeld-setup/.github/main/badge/github-repo-install.svg)

👉 [**weibeld-setup/install-fonts**](https://github.com/weibeld-setup/install-fonts)

[↑ Top](#contents)
