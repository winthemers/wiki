# 🖌️ Windows Ricing

Are you thinking about those Linux rices on r/unixporn and you want them on Windows, but you can't have them...

Well, welcome to Windows ricing. Here you can find guides, programs, Rainmeter skins, scripts, xoblite configs and everything you need to get started on your Windows ricing journey.

⚠️ **WARNING**: As a rule of thumb, before making any kind of change for the first time, create a system restore point.

- [Table of Contents](#table-of-contents) <a name="table-of-contents"></a>
  - [Where to get Windows Themes](#where-to-get-themes)
  - [Patching your System](#patching-your-system)
  - [Applying custom themes](#applying-custom-themes)
  - [Changing default system font](#changing-default-system-font)
  - [Removing ribbon menu from Explorer](#old-new-explorer)
  - [FAQ](#faq)
  - [Contributing](#contributing)

<br />

## ❓ Where to get Windows themes <a name="where-to-get-themes"></a>

[DeviantArt](https://deviantart.com/) is the primary platform for windows themes.

⚠️ **WARNING**: Websites other than DA are probably fake (resell paid themes) so just keep an eye for those types of websites.

<br />

## 🔧 Patching your system <a name="patching-your-system"></a>

In order to apply third-party Windows themes you need to patch your system. For this we recommend **[SecureUXTheme](https://github.com/namazso/SecureUxTheme)** because it's the **most reliable and safe**. We **DO NOT** recommend UltraUXThemePatcher since nowadays it is quite unreliable and it also doesn't work properly on Windows 11.

How to patch using SecureUXTheme:

1. Download [SecureUXTheme](https://github.com/namazso/SecureUxTheme) and open it AS ADMINISTRATOR (the file might be called `ThemeTool.exe`).
2. **(optional, read below\*)** Enable `Hook LogonUI` then hit `Install`.
3. Reboot your PC.

(You only need to do this once, but might need to repeat it after some Windows updates!)

### About Hook LogonUI*

`Hook LogonUI` and `Rename DefaultColors` both aim to fix colors being reset by LogonUI (for example when going into `ctrl+alt+del`) but of course do so in different ways. The tradeoff is simple:

 - `Rename DefaultColors` may cause issues with updates and you might need to repatch more often.
 - `Hook LogonUI` causes locking your computer to take a few more seconds.

It's up to you what you want to do, but if you just want to patch once and forget about it we suggest you use `Hook LogonUI`.

<br />

## 🎨 Applying custom themes <a name="applying-custom-themes"></a>

Since we only recommend you use SecureUXTheme for patching your system, this is a guide for applying themes with SecureUXTheme.

How to apply themes with SecureUXTheme:

1. Make sure you have patched your system (read above).
2. Install your themes by putting the `.theme` files and the adjacent folders into `C:\Windows\Resources\Themes`.
3. Open [SecureUXTheme](https://github.com/namazso/SecureUxTheme) AS ADMINISTRATOR (the file might be called `ThemeTool.exe`).
4. Find your theme in the list and select it.
5. Click `Patch and Apply`.
6. **And, voila! You are done!**

(You need to do this for all the themes you want to apply!)

<br />

## 🇦 Changing default system font <a name="changing-default-system-font"></a>

By default, Windows uses the Segoe UI font. To change it, Segoe UI needs to be disabled in the registry, and a fallback font needs to be set, which will be used instead.

Use the following steps:
1. Create a backup of your current `[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts]` and `[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\FontSubstitutes]`, by selecting the keys (folders) in the registry editor, and calling File -> Export. Name the file something recognizable, such as "WindowFonts-DefaultBackup.reg".
2. Create a new file for your font setting, call it something like "WindowsFonts-FontName.reg". Make sure the extension is changed to .reg. In the file, paste the following contents, replacing the FontName with the name of the font you wish to use (make sure it's spelled exactly right, for example, `"Segoe UI"="Arial"`):
  ```
  Windows Registry Editor Version 5.00

  [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts]
  "Segoe UI (TrueType)"=""
  "Segoe UI Bold (TrueType)"=""
  "Segoe UI Bold Italic (TrueType)"=""
  "Segoe UI Italic (TrueType)"=""
  "Segoe UI Light (TrueType)"=""
  "Segoe UI Semibold (TrueType)"=""
  "Segoe UI Symbol (TrueType)"=""

  [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\FontSubstitutes]

  "Segoe UI"="FontName"
  ```
3. Right-click on the file, and select "Merge", and agree to the prompt that appears.
4. Restart the computer, and the new font should be applied.

<br />

## 🎀 Removing ribbon menu from Explorer <a name="old-new-explorer"></a>

For this, you will have to use a program called [OldNewExplorer](https://tihiy.net/files/OldNewExplorer.rar)

Extract it, and open the exe.

Select the "Use command bar" box and **unselect the last two boxes**.

**Note:** In Windows 11, the ribbon menu was replaced by a command bar, displaying buttons for copy, paste etc. To remove it, it needs to be replaced by the ribbon menu first.
In Windows Terminal (or command prompt), call: `reg.exe add "HKCU\Software\Classes\CLSID\{d93ed569-3b3e-4bff-8355-3c44f6a52bb5}\InprocServer32" /f /ve` (alternatively, this registry key can be added manually).
The ribbon menu should be back, making it possible to remove it with OldNewExplorer as described above.

<br />

## 🚧 Something doesn't work? Are you confused? <a name="faq"></a>

Read the handy-dandy FAQ we made!

### ❓ My theme doesn't apply!

**This is a very common problem**, you probably simply forgot to put the **theme folder** in the themes directory!

Below is an image representing how the files and folders should be placed:

![File and Folder Placement](https://raw.githubusercontent.com/winthemers/windows-ricing/main/file-folder-placement.png)

### ❓ My theme is broken!

If you patched your system using UltraUX, please try [using SecureUX](#patching-your-system) instead. On numerous occasions we had users complain about themes not looking right and it was fixed with SecureUX. If this does not fix your issue then the theme might be old and/or made for another version of Windows.

### ❓ Will themes reduce my performance?

**No!** Every single theme is just a reskin of the original Windows theme.

### ❓ How do I make my own themes

Themes are made by editing the original Windows `.msstyles`, you can make a copy of it from your `C:\Windows\Resources\Themes` folder and use a style builder tool like [Windows Style Builder](https://www.vistastylebuilder.com/) **(Keep in mind this is PAID SOFTWARE, it costs $30)**, or a free alternative like [msstyleEditor](https://github.com/nptr/msstyleEditor) in order to change the look and properties of the theme.

### ❓ I used OldNewExplorer, but now there's a menu that doesn't go away!

Press **Ctrl+Shift+M** to remove this menu. Make sure you have the **window focused** before pressing the keys.
  
### ❓ There's another bar at the bottom when using OldNewExplorer!

Press **Alt+Shift+P** while having the **window focused**.

### ❓ I saw screenshots where people had tabs on their Explorer, how?

You can do this using a shell extension called **QTTabbar**, which can be downloaded [here](http://qttabbar.wikidot.com/).

QTTabbar includes other tricks like left navigation panel without folder names, we should have a decent QTTabbar guide written pretty soon.
 
### ❓ I am trying to change my QTTabbar toolbar color but there is a black box around it...

QTTabbar has a bug where it will only be able to recolor toolbar properly on white variant themes, if your theme applies darkmode by default, these black bars will not come off, sorry.
  
### ❓ There is a floating taskbar on the preview of the theme while mine is not...

For this you would need StartIsBack (StartAllBack for Windows 11), which can be downloaded [here for Windows 10](https://www.startisback.com/) and [here for Windows 11](https://www.startallback.com/) **(Keep in mind the software is paid, both of them costing 5$)**.

After installation follow your theme's instructions in order to apply it's theme to SIB / SAB.  

### ❓ How do I achieve blank titles on my window title-bar?

Use [WinAeroTweaker](https://winaerotweaker.com/) to change titlebar font to blank.

You can download the blank font [here!](https://cdn.discordapp.com/attachments/763855843476766740/847301543429799956/BLANK.TTF)

<br />

## ✨ Contributing <a name="contributing"></a>
We'd love if you could contribute to this project with a few fixes or additions! :D
