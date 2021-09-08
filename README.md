# 🖌️ Windows Ricing

You are thinking about those linux rices on r/unixporn and you want them on widnows, but you cant have them.. 

Well, welcome to windows ricing. Here you can find guides, programs, rainmeter skins, scripts, xoblite configs and everything you need to get started on your windows ricing journey.

- [Table of Contents](#table-of-contents) <a name="table-of-contents"></a>
  - [Where to get Windows Themes](#where-to-get-themes)
  - [Patching your System](#patching-your-system)
  - [Applying custom themes](#applying-custom-themes)
  - [OldNewExplorer](#old-new-explorer)
  - [FAQ](#faq)
  - [Contributing](#contributing)

## ❓ Where to get Windows Themes <a name="where-to-get-themes"></a>
[DeviantArt](https://deviantart.com/) is the primary platform for windows themes.
⚠️ **WARNING**: Websites other than DE are probably fake (resell paid themes) so just keep an eye for those types of websites.

## 🔧 Patching your System <a name="patching-your-system"></a>
In order to apply third-party windows themes you need to patch your system. For this we recommend either:
[UltraUXThemePatcher](https://mhoefs.eu/software_uxtheme.php?ref=syssel&lang=en)
or
[SecureUXTheme](https://github.com/namazso/SecureUxTheme)

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
If you are using SecureUXTheme, just follow continue with the guide above.

## 🎀 Removing ribbon menu from Explorer <a name="old-new-explorer"></a>
For this, you will have to use a program called [OldNewExplorer](https://tihiy.net/files/OldNewExplorer.rar)
Extract it, and open the exe.
Select the "Use command bar" box and **unselect the last two boxes**.

## 🚧 Something doesn't work? Are you confused? <a name="faq"></a>
Read the handy-dandy FAQ we made!

**My theme doesn't apply!**
  **This is a very common problem**, you probably forgot to put the **theme folder** in the themes directory
Below is an image representing how the files and folders should be placed:
![File and Folder Placement](https://raw.githubusercontent.com/winthemers/windows-ricing/main/file-folder-placement.png)

**Will themes reduce my performance?**
**No!** Every single theme is just a reskin of the original windows theme.

**How to make my own themes?**
  Themes are made by editing the original windows msstyle, you can make a copy of it from your "C:\Windows\Resources\Themes" folder and use a style builder tool like [Windows Style Builder](https://www.vistastylebuilder.com/) **(Keep in mind this is PAID SOFTWARE, it costs $30)**, or a free alternative like [msstyleEditor](https://github.com/nptr/msstyleEditor) in order to change the look and properties of the theme.

**I used OldNewExplorer, but now there's a menu that doesn't go away!**
  Press **Ctrl+Shift+M** to remove this menu, make sure you have the **window focused** before pressing the keys.
  
**Theres another bar at the bottom when using OldNewExplorer!**
  Press **Alt+Shift+P** while having the **window focused**.

**I saw screenshots where people had tabs on their explorer, how?**
  You can do this using a shell extension called **QTTabbar**, which can be downloaded [here](http://qttabbar.wikidot.com/)
 QTTabbar includes other tricks like left navigation panel without folder names, we should have a decent QTTabbar guide written pretty soon.
 
 **I am trying to change my QTTabbar toolbar color but there is a black box around it**
  QTTabbar has a bug where it will only be able to recolor toolbar properly on white variant themes, if your theme applies darkmode by default, these black bars will not come off, sorry.
  
**There is a floating taskbar on the preview of the theme while mine is not**
  For this you would need StartIsBack, which can be downloaded [here](https://www.startisback.com/) **(Keep in mind it is PAID SOFTWARE, it costs 4$)**
After installation follow your theme's instructions in order to apply it's theme to SIB.  

**How do I achieve blank titles on my window titlebar?**
  Use [WinAeroTweaker](https://winaerotweaker.com/) to change titlebar font to blank
You can download the blank font [here](https://cdn.discordapp.com/attachments/763855843476766740/847301543429799956/BLANK.TTF)

## ✨ Contributing <a name="contributing"></a>
We'd love if you could contribute to this project with a few fixes or additions :)
