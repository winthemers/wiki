# 🖌️ Windows Ricing

You think how those linux rices on r/unixporn are so beautiful, but you cant have them on windows.. 

Well, welcome to windows ricing. Here you can find guides, programs, rainmeter skins, scripts, xoblite configs and everything you need to get started on your windows ricing journey.

- [Table of Contents](#table-of-contents) <a name="table-of-contents"></a>
  - [Where to get Windows Themes](#where-to-get-themes)
  - [Patching your System](#patching-your-system)
  - [Applying custom themes](#applying-custom-themes)

## ❓ Where to get Windows Themes <a name="where-to-get-themes"></a>
[DeviantArt](https://deviantart.com/) 
DeviantArt is the primary platform for windows themes and the one which has the most themes.
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

## Removing ribbon menu from Explorer
For this, you will have to use a program called [OldNewExplorer](https://tihiy.net/files/OldNewExplorer.rar)
Extract it, and open the exe.
Select the "Use command bar" box and **unselect the last two boxes**.

## 🚧 Something doesn't work? You are confused, having problems?
Read the handy-dandy FAQ we made!

**Will themes reduce my performance?**
**No!** Every single theme is just a reskin of the original windows theme.

**How to make my own themes?**
Themes are made by editing the original windows msstyle, you can make a copy of it from your "C:\Windows\Resources\Themes" folder and use a style builder tool like [Windows Style Builder](https://www.vistastylebuilder.com/) in order to change the look and properties of the theme.
