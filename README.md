# IDM Resetter Script

An open-source tool used to activate and reset the trial period of **Internet Download Manager (IDM)**.

## Disclaimer

I want to clarify that I am not the original author of this script. I created this repository mainly to simplify the process for Chinese users. Also, out of respect for the original author’s work, I made sure to properly credit them.

## Features

* IDM trial freeze and activation using registry key locking method
* Activation and trial remain even after installing IDM updates
* IDM trial reset
* Completely open-source
* Based on transparent batch scripts

## IAS Latest Version

Latest version – **v1.2 (12-Feb-2024)**
GitHub: [https://github.com/SajibWh0/IDM-Resetter](https://github.com/SajibWh0/IDM-Resetter)

## Download / How to use it?

First install the latest version of **Internet Download Manager**.
If you have any previous cracks or patches installed, make sure to remove or uninstall them.

Then follow the steps below to activate it.

## Log

📌 The activation option is currently not working in the script. Please use the **Freeze Trial** option to lock the 30-day trial permanently.

## Method 1 – PowerShell (Recommended)

* Right-click the Windows Start menu and select **PowerShell** or **Terminal** (do NOT select CMD).
* Copy and paste the following code and press Enter:

```shell
iex(irm is.gd/iAS)
```

or

```shell
iwr -useb https://raw.githubusercontent.com/SajibWh0/IDM-Resetter/main/IAS.ps1 | iex
```

or

```shell
iwr -useb https://is.gd/iAS | iex
```

* You will see activation options. Follow the on-screen instructions.
* That’s it.

## Method 2 – Traditional

* Download the file from GitHub:
  [https://github.com/SajibWh0/IDM-Resetter/archive/refs/heads/main.zip](https://github.com/SajibWh0/IDM-Resetter/archive/refs/heads/main.zip)
* Right-click the downloaded ZIP file and extract it
* Right-click and run `IAS.cmd`
* You will see activation options. Follow the instructions.
* That’s it.

## Information

### Freeze Trial

* IDM provides a 30-day trial period. You can use this script to lock this trial permanently so it never expires.
* Internet connection is required when applying this method.
* IDM updates can be installed without freezing again.

### Activation (**currently not working**)

* This script uses a registry locking method to activate IDM.
* Internet connection is required during activation.
* IDM updates can be installed without reactivation.
* If IDM shows activation warnings later, simply run the activation option again. No need to reset.

### Reset IDM Activation/Trial

* IDM provides a 30-day trial which you can reset anytime using this script.
* This option can also fix fake serial key errors and similar problems.

## Operating System Requirements

* Supports Windows 7/8/8.1/10/11 and corresponding server versions.
* PowerShell method supported on Windows 8 and above.

## Advanced Information

* To activate in unattended mode use parameter:

```
/act
```

* To freeze trial in unattended mode use:

```
/frz
```

* To reset in unattended mode use:

```
/res
```

## How does it work?

IDM stores trial and activation data in various registry keys. Some of these keys are locked to prevent modification, and the data is stored in specific patterns to track fake serial numbers and remaining trial days.

To activate it, the script triggers some downloads in IDM to generate these registry entries, identifies them, and locks them so IDM cannot edit or read them. This prevents IDM from showing fake serial number warnings.

## Troubleshooting

Browser integration fixes:

Chrome:
[https://www.internetdownloadmanager.com/register/new_faq/bi9.html](https://www.internetdownloadmanager.com/register/new_faq/bi9.html)

Firefox:
[https://www.internetdownloadmanager.com/register/new_faq/bi4.html](https://www.internetdownloadmanager.com/register/new_faq/bi4.html)

## Changelog

### v1.2

* Added activation option with randomly generated name, email and key in registration details.
* Warning added that activation may not work for some users.
* Recommended option is Freeze Trial.

### v1.1

* After IDM 6.42b3 update, fake serial popup started appearing.
* Activation option removed and replaced with Freeze Trial option.
* Script now disables Quick Edit mode in CMD using PowerShell.
* Script restart via conhost.exe merged into Quick Edit disabling code.

### v1.0

* Added code to restart script via conhost.exe when run from terminal.
* Fixed issue with getting current user SID.

### v0.9

* Fixed activation/reset issues for non-admin users.
* Fixed false activation status display.
* Fixed fake serial popup issues.
* Registry scanning and locking rewritten in PowerShell.
* Added update checker.
* Script now temporarily disables Quick Edit mode.
* CLSID registry keys now backed up before modification.
* Added more error checks.

### v0.8

* Project moved to GitHub
* Minor bug fixes
* Added info message when deleting large numbers of empty registry keys.

## Screenshots
<a href="https://imgbb.com/"><img src="https://i.ibb.co.com/yF4W4tcn/image.png" alt="image" border="0" /></a>



## Credits

| Name          | Contribution                                                |
| ------------- | ----------------------------------------------------------- |
| Dukun Cabul   | Original researcher of IDM trial reset and activation logic |
| AveYo (BAU)   | Registry snippet                                            |
| abbodi1406    | Coding help                                                 |
| WindowsAddict | Original IAS author                                         |
| SajibWh0      | Bug Fixing                                                  |

Thanks to IAS users for their attention, feedback, and support.

---

Made with love ❤️
