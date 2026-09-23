# Installing RigSize

RigSize is free to use. Installers for Windows and macOS are on the download page for each version. This guide walks you through downloading, installing and opening the app for the first time. You do not need any developer tools.

> **Download page:** [github.com/Dzazaleo/RigSize-releases/releases](https://github.com/Dzazaleo/RigSize-releases/releases)
>
> Pick the file for your computer:
>
> - Windows (64-bit): `RigSize-<version>-x64.exe`
> - macOS (Apple Silicon): `RigSize-<version>-arm64.dmg`
>
> RigSize works with files made in Spine, so you need your own Spine licence from Esoteric Software.

---

## Windows

**Note:** RigSize does not carry a Microsoft-recognised publisher certificate, so Windows shows a warning the first time you run the installer. Getting past it takes two clicks, and then the installer has three short pages. The installation is just for your user account: **you do not need administrator rights, and Windows will not ask for an administrator password**.

### Installing, step by step

1. **"Windows protected your PC".** Download `RigSize-<version>-x64.exe` from the download page and double-click it. Windows shows a blue window titled **Windows protected your PC**:

   _"Microsoft Defender SmartScreen prevented an unrecognised app from starting. Running this app might put your PC at risk."_

   ![Step 1: the “Windows protected your PC” window. It does not name the app. The only button is Don't run, and the way forward is the small More info link.](docs/install-images/windows-smartscreen-more-info.png)

   This window does **not** name the app. The only button is **Don't run**. To continue, click the small **More info** link.

   _Spelling note:_ the picture comes from a computer set to UK English, which writes _unrecognised_. On US English you will see _unrecognized_. It is the same window.

2. **Run anyway.** After you click **More info**, two lines appear: `Application: RigSize-<version>-x64.exe` and `Publisher: Unknown publisher`, and a **Run anyway** button appears next to **Don't run**.

   ![Step 2: the expanded window naming the file and showing Publisher: Unknown publisher, with Run anyway and Don't run buttons.](docs/install-images/windows-smartscreen-run-anyway.png)

   **Publisher: Unknown publisher** is expected, because RigSize has no publisher certificate. Check that the `Application:` line shows the file you downloaded, then click **Run anyway**.

3. **Installation options.** The **RigSize Setup** window opens on **Choose Installation Options**. _Only for me_ is already selected, and the line below it reads _Fresh install for current user only._ Leave it as it is and click **Next >**.

   ![Step 3: RigSize Setup, Choose Installation Options, with “Only for me” selected and the line “Fresh install for current user only.”](docs/install-images/windows-install-options.png)

4. **Install location.** The **Choose Install Location** page suggests `C:\Users\<you>\AppData\Local\Programs\RigSize`. Leave it as it is and click **Install**.

   ![Step 4: Choose Install Location, suggesting the AppData\Local\Programs\RigSize folder for your user account.](docs/install-images/windows-install-location.png)

5. **Finished.** The **Completing RigSize Setup** page says _RigSize has been installed on your computer._ The **Run RigSize** box is ticked. Click **Finish**.

   ![Step 5: Completing RigSize Setup, with the Run RigSize box ticked.](docs/install-images/windows-install-complete.png)

After this, open RigSize from the Start menu (search for "RigSize"), or from the desktop shortcut if the installer made one.

### If something goes wrong

- **Nothing happens after Run anyway**: the download may be incomplete. Check that the file size matches the one on the download page, and download it again if it does not.
- **Your antivirus blocks the installer**: some antivirus programs flag installers that have no publisher certificate. Allow the file in your antivirus settings, or ask your IT department if your computer is managed by your company.

---

## macOS

**Note:** RigSize is not registered with Apple, so the first time you open it, macOS warns you and asks you to confirm. This takes **four steps**, and the last one asks for an administrator's password. You only do this once: after that, the app opens normally from Applications, Launchpad or Spotlight.

> ⚠️ **Two things to know before you start:**
>
> 1. In steps 1 and 3 below, the highlighted button is **Move to Trash**, which deletes the app. If you press Return out of habit, your download is gone. Read each window before you click.
> 2. Step 4 needs **an administrator's** Touch ID or password. If your account on this Mac is not an administrator, someone who has an administrator account must type their password for you. Windows does not need this (see the Windows section).

### Install

1. Download `RigSize-<version>-arm64.dmg` from the download page.
2. Double-click the downloaded `.dmg` file. A Finder window opens with the RigSize icon next to a shortcut to your Applications folder.
3. Drag **RigSize.app** into **Applications**.

### Opening it the first time (macOS 15 Sequoia and later)

1. **The "Not Opened" window.** Open **Applications** in Finder and double-click **RigSize**. macOS shows a window titled _“RigSize.app” Not Opened_:

   _“Apple could not verify ‘RigSize.app’ is free of malware that may harm your Mac or compromise your privacy.”_

   ![Step 1: the “RigSize.app” Not Opened window. Its only buttons are Move to Trash (highlighted) and Done. Neither one opens the app.](docs/install-images/macos-gatekeeper-blocked.png)

   The only buttons are **Move to Trash** (highlighted) and **Done**. There is **no Open button**, and the window does not tell you what to do next. Click **Done**. Do **not** press Return, because that clicks **Move to Trash** and deletes the app.

2. **System Settings.** Open **System Settings**, go to **Privacy & Security**, and scroll down to the **Security** section near the bottom. You will see a line that says:

   _“RigSize.app” was blocked to protect your Mac._

   ![Step 2: the Security section of System Settings, Privacy & Security, showing the “RigSize.app” was blocked line and its Open Anyway button.](docs/install-images/macos-gatekeeper-open-anyway.png)

   Click **Open Anyway** next to it.

3. **The confirmation window.** A window titled _Open “RigSize.app”?_ appears. Its buttons, from top to bottom, are **Move to Trash** (highlighted), **Open Anyway** and **Done**. The one you want is **Open Anyway**, in the middle. Pressing Return would click **Move to Trash** and delete the app.

   ![Step 3: the Open “RigSize.app”? window. The buttons are Move to Trash (highlighted), Open Anyway and Done. The safe choice is the middle button.](docs/install-images/macos-gatekeeper-confirm-open.png)

   Click **Open Anyway** (the middle button).

4. **Administrator password.** A **Privacy & Security** window asks for **an administrator's Touch ID or password**, with the buttons **Use Password…** (highlighted) and **Cancel**. This is the step that actually opens the app: clicking Open Anyway in step 3 does not open it on its own.

   ![Step 4: the Privacy & Security window asking for an administrator's Touch ID or password, with Use Password… (highlighted) and Cancel. This step is what actually opens the app.](docs/install-images/macos-gatekeeper-admin-auth.png)

   Use an administrator's Touch ID or password. RigSize opens.

From now on, RigSize opens normally: double-click it in Applications, find it with Spotlight (`Cmd+Space`, then type "RigSize"), or use Launchpad. You will need to repeat these steps once for each new version you install.

### Older macOS versions (14 Sonoma and earlier)

On macOS 14 and earlier there is often a shorter way:

1. **Right-click** (or Control-click) the RigSize icon in Applications and choose **Open**.
2. macOS says the developer cannot be verified. Click **Open Anyway** (or **Open**, depending on your macOS version).

If you do not see an Open Anyway option, use the System Settings steps above instead. They work on every macOS version RigSize supports. On macOS 15 and later, right-clicking no longer offers an Open option, so use the four steps.

### If something goes wrong

- **"RigSize is damaged and can't be opened"**: macOS sometimes marks downloaded apps in a way that triggers this message. Open Terminal, paste the line below, press Return, then try opening RigSize again:

  ```bash
  xattr -cr "/Applications/RigSize.app"
  ```

---

## Updates

When RigSize starts, it quietly checks whether a newer version exists, and only shows you a message if there is one. You can also check yourself with **Help → Check for Updates**.

The message has a button that opens the download page. Download the new installer and run it the same way as the first time. On macOS, the warning steps above appear once more for the new version.

---

## Reporting problems

Found a bug? Open an issue at [github.com/Dzazaleo/RigSize-releases/issues](https://github.com/Dzazaleo/RigSize-releases/issues) and include:

- Your system and version (for example macOS 15.4 or Windows 11 24H2).
- The RigSize version (shown in **About RigSize**, or in the name of the installer you ran).
- What you did, what you expected to happen, and what happened instead.
