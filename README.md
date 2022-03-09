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

## ❓ Where to get Windows themes <a name="where-to-get-themes"></a>
[DeviantArt](https://deviantart.com/) is the primary platform for windows themes.
⚠️ **WARNING**: Websites other than DE are probably fake (resell paid themes) so just keep an eye for those types of websites.

## 🔧 Patching your system <a name="patching-your-system"></a>
In order to apply third-party Windows themes you need to patch your system. For this we recommend either:
[UltraUXThemePatcher](https://mhoefs.eu/software_uxtheme.php?ref=syssel&lang=en)
or
[SecureUXTheme](https://github.com/namazso/SecureUxTheme) but SecureUX is preferred because it's the safest one.

Instructions for UltraUXThemePatcher:
Download the exe and run thru the installation process and reboot.

Instructions for SecureUXTheme:
1. Download the exe and open it up, select "Hook LogonUI" then hit install.
2. Reboot your PC
3. Follow the guide below for applying the theme.
4. Open up the exe and find the theme you downloaded in the list of themes.
5. Hit patch then apply
6. **And, voila! You are done!**

## 🎨 Applying custom themes <a name="applying-custom-themes"></a>
In order to apply custom themes you'll need to extract them and copy both the ```.theme``` files and the folder which has the name of the theme to ```C:\Windows\Resources\Themes```. If you are using UltraUXThemePatcher then you'll just need to go to Settings > Personalization > Themes and apply the theme.
If you are using SecureUXTheme, just continue with the guide above.

## 🇦 Changing default system font <a name="changing-default-system-font"></a>
By default, Windows uses the Segoe UI font. To change it, Segoe UI needs to be disabled in the registry, and a fallback font needs to be set, which will be used instead.
Use the following steps:
1. Create a backup of your current ```[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts]``` and ```[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\FontSubstitutes]```, by selecting the keys (folders) in the registry editor, and calling File -> Export. Name the file something recognizable, such as "WindowFonts-DefaultBackup.reg".
2. Create a new file for your font setting, call it something like "WindowsFonts-FontName.reg". Make sure the extension is changed to .reg. In the file, paste the following contents, replacing the FontName with the name of the font you wish to use (make sure it's spelled exactly right, for example, ```"Segoe UI"="Arial"```):
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



## 🎀 Removing ribbon menu from Explorer <a name="old-new-explorer"></a>
For this, you will have to use a program called [OldNewExplorer](https://tihiy.net/files/OldNewExplorer.rar)
Extract it, and open the exe.
Select the "Use command bar" box and **unselect the last two boxes**.

**Note:** In Windows 11, the ribbon menu was replaced by a command bar, displaying buttons for copy, paste etc. To remove it, it needs to be replaced by the ribbon menu first.
In Windows Terminal (or command prompt), call: ```reg.exe add "HKCU\Software\Classes\CLSID\{d93ed569-3b3e-4bff-8355-3c44f6a52bb5}\InprocServer32" /f /ve``` (alternatively, this registry key can be added manually).
The ribbon menu should be back, making it possible to remove it with OldNewExplorer as described above.

## 🚧 Something doesn't work? Are you confused? <a name="faq"></a>
Read the handy-dandy FAQ we made!

**My theme doesn't apply!**
  **This is a very common problem**, you probably forgot to put the **theme folder** in the themes directory
Below is an image representing how the files and folders should be placed:

![File and Folder Placement](https://raw.githubusercontent.com/winthemers/windows-ricing/main/file-folder-placement.png)

**Will themes reduce my performance?**
**No!** Every single theme is just a reskin of the original Windows theme.

**How do I make my own themes?**
  Themes are made by editing the original windows msstyle, you can make a copy of it from your "C:\Windows\Resources\Themes" folder and use a style builder tool like [Windows Style Builder](https://www.vistastylebuilder.com/) **(Keep in mind this is PAID SOFTWARE, it costs $30)**, or a free alternative like [msstyleEditor](https://github.com/nptr/msstyleEditor) in order to change the look and properties of the theme.

**I used OldNewExplorer, but now there's a menu that doesn't go away!**
  Press **Ctrl+Shift+M** to remove this menu, make sure you have the **window focused** before pressing the keys.
  
**There's another bar at the bottom when using OldNewExplorer!**
  Press **Alt+Shift+P** while having the **window focused**.

**I saw screenshots where people had tabs on their Explorer, how?**
  You can do this using a shell extension called **QTTabbar**, which can be downloaded [here](http://qttabbar.wikidot.com/)
 QTTabbar includes other tricks like left navigation panel without folder names, we should have a decent QTTabbar guide written pretty soon.
 
 **I am trying to change my QTTabbar toolbar color but there is a black box around it**
  QTTabbar has a bug where it will only be able to recolor toolbar properly on white variant themes, if your theme applies darkmode by default, these black bars will not come off, sorry.
  
**There is a floating taskbar on the preview of the theme while mine is not**
  For this you would need StartIsBack (StartAllBack for Windows 11), which can be downloaded [here](https://www.startisback.com/) or [here](https://www.startallback.com/) (for Windows 11) **(Keep in mind the software is paid, both of them costing 5$)**
After installation follow your theme's instructions in order to apply it's theme to SIB.  

**How do I achieve blank titles on my window title-bar?**
  Use [WinAeroTweaker](https://winaerotweaker.com/) to change titlebar font to blank
You can download the blank font [here!](https://cdn.discordapp.com/attachments/763855843476766740/847301543429799956/BLANK.TTF)

## ✨ Contributing <a name="contributing"></a>
We'd love if you could contribute to this project with a few fixes or additions! :D
