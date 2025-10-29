# "Oversimplified & Accentuated" Theme for "Windows 11 Notification Center Styler"

A cleaner, more refined Windows Notification Center (& Control Center) theme - removing unnecessary elements and offering better **Accent Color** integration.

> ⚠️ **Note:** This theme is optimized for Windows in **Dark Mode** and may not display correctly in **Light Mode**.

### ✨ Features
- Removed unnecessary text and lines
- Enlarged icons  
- Enhanced Accent Color Presence (Automatically Updates with Windows Accent Color)
- Improved Transparency Effects
- Added Subtle, Neat Border Reveal Effects
- Took Fallback Colors (Colors in Battery Mode) into consideration
- Added useful Accesss Keys ([ Alt + Key ] Shorcuts):
  - Notification Center
    - Toggle DoNotDisturb → [ Alt + D ]
    - "Clear All" Button → [ Alt + C ]
    - Expand/Collapse Calender → [ Alt + E ]
   - Control Center
     - Button in Position #1 → [ Alt + 1 ]
     - Button in Position #2 → [ Alt + 2 ]
     - Button in Position #3 → [ Alt + 3 ]
     - Button in Position #4 → [ Alt + 4 ]
     - Button in Position #5 → [ Alt + 5 ]
     - Button in Position #6 → [ Alt + 6 ]
     - Button in Position #7 → [ Alt + 7 ]
     - Button in Position #8 → [ Alt + 8 ]
     - Button in Position #9 → [ Alt + 9 ]
     - Button in Position #10 → [ Alt + 0 ]
     - Button in Position #11 → [ Alt + - ]
> ⚠️ **Note:** I am aware that the **Access Key** for the **Nearby Sharing** button in **Control Center** windows is not functional, this is because this button in particular has a slightly different JSON Selector than the rest of the buttons, I'm looking for a work-around for this problem.

> ⚠️ **Note:** if you change the position of a button in **Control Center** you need to restart `ShellHost.exe` for the **Access Keys** to change according to the new buttons layout.

**Author:** [OsamaJT](https://github.com/OsamaHJT)

![Screenshot](Nofication%20Center.png)

---

## 🎨 Elements Modified
- Notification Center
- Notifications (Active & in Control Center)
- Calender
- Control Center
- Media Panel in Control Center
- Left Click Menus (Jumplists) for Taskbar Apps
- Context Menu
- ToolTip Popup
  
---

## 🧩 Installation

1. Download **[Windhawk](https://windhawk.net/)**.  
2. Install the **“[Windows 11 Notification Center Styler](https://windhawk.net/mods/windows-11-notification-center-styler)”** plugin.  
3. Choose the **“Oversimplified & Accentuated”** theme from the integrated themes list.  
   **OR**  
   Copy the JSON code below and go to:  
   **Windows 11 Taskbar Styler → Details → Advanced → Mod Settings**  
   Paste the code into the "**Mod settings**" box and click **Save**.


---

## 🛠️ Modification Notes

I added an extra comment line at the end of each style group to indicate the target object with common language.  
The aim is to make it easier to modify or debug the theme in the future.


<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "MenuFlyoutPresenter",
  "controlStyles[0].styles[0]": "Background:=$DarkAccent",
  "controlStyles[0].styles[1]": "BorderBrush=Transparent",
  "controlStyles[0].styles[2]": "Shadow:=",
  "controlStyles[0].styles[3]": "//Target= Context Menu",
  
  "controlStyles[1].target": "ToolTip > ContentPresenter#LayoutRoot",
  "controlStyles[1].styles[0]": "Background:=$DarkAccent",
  "controlStyles[1].styles[1]": "BorderBrush:=$Reveal",
  "controlStyles[1].styles[2]": "Shadow:=",
  "controlStyles[1].styles[3]": "//Target= Tooltip Popup",
  
  "controlStyles[2].target": "Grid#NotificationCenterGrid",
  "controlStyles[2].styles[0]": "Background:=$Alt",
  "controlStyles[2].styles[1]": "BorderBrush=Transparent",
  "controlStyles[2].styles[2]": "Shadow:=",
  "controlStyles[2].styles[3]": "//Target= Notification Center Box",
  
  "controlStyles[3].target": "TextBlock#NotificationsTextBlock",
  "controlStyles[3].styles[0]": "Visibility=Collapsed",
  "controlStyles[3].styles[1]": "//Target= Notification Center > \"Notifications\" Text",
  
  "controlStyles[4].target": "Button#ClearAll",
  "controlStyles[4].styles[0]": "AccessKey=C",
  "controlStyles[4].styles[1]": "//Target= \"ClearAll\" Button",
  
  "controlStyles[5].target": "Windows.UI.Xaml.Controls.Primitives.ToggleButton#DoNotDisturbButton",
  "controlStyles[5].styles[0]": "AccessKey=D",
  "controlStyles[5].styles[1]": "//Target= Notifcation Center > DoNotDisturb Button",
  
  "controlStyles[6].target": "Microsoft.UI.Xaml.Controls.AnimatedIcon#DoNotDisturbButtonIcon",
  "controlStyles[6].styles[0]": "Height=16",
  "controlStyles[6].styles[1]": "Width=16",
  "controlStyles[6].styles[2]": "//Target= Notifcation Center > DoNotDisturb Button icon",
  
  "controlStyles[7].target": "Grid#DoNotDisturbSubtext",
  "controlStyles[7].styles[0]": "Background:=$Accent",
  "controlStyles[7].styles[1]": "BorderBrush:=$Reveal",
  "controlStyles[7].styles[2]": "BorderThickness=2",
  "controlStyles[7].styles[3]": "CornerRadius=5",
  "controlStyles[7].styles[4]": "Margin=0,0,0,10",
  "controlStyles[7].styles[5]": "//Target= Notifcation Center > DoNotDisturb Activated Plate",
  
  "controlStyles[8].target": "Grid#DoNotDisturbSubtext > TextBlock[1]",
  "controlStyles[8].styles[0]": "Visibility=Collapsed",
  "controlStyles[8].styles[1]": "//Target= Notifcation Center > DoNotDisturb Activated Plate > DoNotDisturb icon",
  
  "controlStyles[9].target": "Grid#DoNotDisturbSubtext > TextBlock[2]",
  "controlStyles[9].styles[0]": "HorizontalAlignment=Center",
  "controlStyles[9].styles[1]": "FontSize=18",
  "controlStyles[9].styles[2]": "//Target= Notifcation Center > DoNotDisturb Activated Plate > \"Donotdisturbison\" Text",
  
  "controlStyles[10].target": "Grid#DoNotDisturbSubtext > TextBlock[3]",
  "controlStyles[10].styles[0]": "TextAlignment=Center",
  "controlStyles[10].styles[1]": "FontSize=11",
  "controlStyles[10].styles[2]": "//Target= Notifcation Center > DoNotDisturb Activated Plate > \"You'll onlyseebannersforprioritynotificationsandalarams.\" text",
  
  "controlStyles[11].target": "Grid#DoNotDisturbSubtext > Button",
  "controlStyles[11].styles[0]": "HorizontalAlignment=Center",
  "controlStyles[11].styles[1]": "Margin= 0,0,0,0",
  "controlStyles[11].styles[2]": "//Target= Notifcation Center > DoNotDisturb Activated Plate > \"NotificationSettings\" Button in Do Not Disturb Banner",
  
  "controlStyles[12].target": "TextBlock#NotificationSettingsButtonText[Text=Notification settings]",
  "controlStyles[12].styles[0]": "Text=Settings",
  "controlStyles[12].styles[1]": "//Target= Notifcation Center > DoNotDisturb Activated Plate > \"NotificationSettings\" Text in Do Not Disturb Banner",
  
  "controlStyles[13].target": "Border#ItemOpaquePlating",
  "controlStyles[13].styles[0]": "BorderBrush:=$Reveal",
  "controlStyles[13].styles[1]": "//Target= Notification Center > Notifcation Plate",
  
  "controlStyles[14].target": "Border#StandardImageBorder",
  "controlStyles[14].styles[0]": "Height=30",
  "controlStyles[14].styles[1]": "Width=30",
  "controlStyles[14].styles[2]": "//Target= Notification Center > Notifcation App Icon",
  
  "controlStyles[15].target": "Grid#GroupTitleGrid > TextBlock#Title",
  "controlStyles[15].styles[0]": "Visibility=Collapsed",
  "controlStyles[15].styles[1]": "//Target= Notification Center > Notifcation App Name",
  
  "controlStyles[16].target": "Grid > Button#VerbButton",
  "controlStyles[16].styles[0]": "BorderBrush=Transparent",
  "controlStyles[16].styles[1]": "//Target= Notification Center > Notifcation App Buttons",
  
  "controlStyles[17].target": "Border#PopupBorder",
  "controlStyles[17].styles[0]": "Background:=$DarkAccent",
  "controlStyles[17].styles[1]": "Shadow:=",
  "controlStyles[17].styles[2]": "//Target= Notification Center > Notification-In Context Menu",
  
  "controlStyles[18].target": "ProgressBar#progressBar > Grid > Border#DeterminateRoot",
  "controlStyles[18].styles[0]": "Background=Transparent",
  "controlStyles[18].styles[1]": "//Target= Notification Center > Progress Bar > Empty Track",
  
  "controlStyles[19].target": "Border#ToastBackgroundBorder2",
  "controlStyles[19].styles[0]": "Background:=$Alt",
  "controlStyles[19].styles[1]": "BorderBrush=Transparent",
  "controlStyles[19].styles[2]": "CornerRadius=15",
  "controlStyles[19].styles[3]": "Shadow:=",
  "controlStyles[19].styles[4]": "//Target= Active Notification > Notification Plate",
  
  "controlStyles[20].target": "Border#AppLogoBorder2",
  "controlStyles[20].styles[0]": "Height=30",
  "controlStyles[20].styles[1]": "Width=30",
  "controlStyles[20].styles[2]": "//Target= Active Notification > App icon's Container",
  
  "controlStyles[21].target": "Border#AppLogoBorder",
  "controlStyles[21].styles[0]": "Height=30",
  "controlStyles[21].styles[1]": "Width=30",
  "controlStyles[21].styles[2]": "//Target= Active Notification > App icon (Before 24H2 I think)",
  
  "controlStyles[22].target": "Image#AppLogo2",
  "controlStyles[22].styles[0]": "Height=30",
  "controlStyles[22].styles[1]": "Width=30",
  "controlStyles[22].styles[2]": "//Target= Active Notification > App icon",
  
  "controlStyles[23].target": "Grid#ToastTitleBar > TextBlock#SenderName",
  "controlStyles[23].styles[0]": "Visibility=Collapsed",
  "controlStyles[23].styles[1]": "//Target= Active Notification > App Name",
  
  "controlStyles[24].target": "Grid#CalendarCenterGrid",
  "controlStyles[24].styles[0]": "Background:=$Alt",
  "controlStyles[24].styles[1]": "BorderBrush=Transparent",
  "controlStyles[24].styles[2]": "CornerRadius=20",
  "controlStyles[24].styles[3]": "Shadow:=",
  "controlStyles[24].styles[4]": "//Target= Calender Box",
  
  "controlStyles[25].target": "Border#CalendarHeaderMinimizedOverlay",
  "controlStyles[25].styles[0]": "Background=Transparent",
  "controlStyles[25].styles[1]": "//Target= Calender's Header (When Minimized)",
  
  "controlStyles[26].target": "Button#ExpandCollapseButton",
  "controlStyles[26].styles[0]": "Background=Transparent",
  "controlStyles[26].styles[1]": "BorderBrush=Transparent",
  "controlStyles[26].styles[2]": "AccessKey=E",
  "controlStyles[26].styles[3]": "//Target= Calender > Header > Expand/Collapse Button",
  
  "controlStyles[27].target": "ScrollViewer#CalendarControlScrollViewer",
  "controlStyles[27].styles[0]": "Background=Transparent",
  "controlStyles[27].styles[1]": "BorderBrush=Transparent",
  "controlStyles[27].styles[2]": "//Target= Calender's Body",
  
  "controlStyles[28].target": "CalendarViewDayItem",
  "controlStyles[28].styles[0]": "CornerRadius=10",
  "controlStyles[28].styles[1]": "//Target= Calender's Day Container",
  
  "controlStyles[29].target": "CalendarViewDayItem > Border",
  "controlStyles[29].styles[0]": "BorderBrush:= <RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"1\" />",
  "controlStyles[29].styles[1]": "CornerRadius=12",
  "controlStyles[29].styles[2]": "//Target= Calender's Day",
  
  "controlStyles[30].target": "Windows.UI.Xaml.Controls.Primitives.CalendarPanel#YearViewPanel > Control",
  "controlStyles[30].styles[0]": "CornerRadius=12",
  "controlStyles[30].styles[1]": "//Target= Target= Calender's Month's Container",
  
  "controlStyles[31].target": "Windows.UI.Xaml.Controls.Primitives.CalendarPanel#YearViewPanel > Control > Border",
  "controlStyles[31].styles[0]": "BorderBrush:=$Reveal",
  "controlStyles[31].styles[1]": "BorderThickness=2",
  "controlStyles[31].styles[2]": "CornerRadius=12",
  "controlStyles[31].styles[3]": "//Target= Calender's Month",
  
  "controlStyles[32].target": "Windows.UI.Xaml.Controls.Primitives.CalendarPanel#DecadeViewPanel > Control",
  "controlStyles[32].styles[0]": "CornerRadius=12",
  "controlStyles[32].styles[1]": "//Target= Target= Calender's Year's Container",
  
  "controlStyles[33].target": "Windows.UI.Xaml.Controls.Primitives.CalendarPanel#DecadeViewPanel > Control > Border",
  "controlStyles[33].styles[0]": "BorderBrush:=$Reveal",
  "controlStyles[33].styles[1]": "BorderThickness=2",
  "controlStyles[33].styles[2]": "CornerRadius=12",
  "controlStyles[33].styles[3]": "//Target= Calender's Year",
  
  "controlStyles[34].target": "Grid#FocusGrid",
  "controlStyles[34].styles[0]": "Background=Transparent",
  "controlStyles[34].styles[1]": "BorderBrush=Transparent",
  "controlStyles[34].styles[2]": "//Target= Calender > Focus Grid (Calender's Footer)",
  
  "controlStyles[35].target": "Button#IncreaseTimeButton",
  "controlStyles[35].styles[0]": "Background=Transparent",
  "controlStyles[35].styles[1]": "BorderBrush=Transparent",
  "controlStyles[35].styles[2]": "//Target= Calender > Focus Grid > Increase Time Button",
  
  "controlStyles[36].target": "Button#DecreaseTimeButton",
  "controlStyles[36].styles[0]": "Background=Transparent",
  "controlStyles[36].styles[1]": "BorderBrush=Transparent",
  "controlStyles[36].styles[2]": "//Target= Calender > Focus Grid > Decrease Time Button",
  
  "controlStyles[37].target": "Button#StartButton",
  "controlStyles[37].styles[0]": "Background=Transparent",
  "controlStyles[37].styles[1]": "BorderBrush=Transparent",
  "controlStyles[37].styles[2]": "//Target= Calender > Focus Grid > Focus Button ",
  
  "controlStyles[38].target": "Grid#ControlCenterRegion",
  "controlStyles[38].styles[0]": "Background=Transparent",
  "controlStyles[38].styles[1]": "BorderBrush=Transparent",
  "controlStyles[38].styles[2]": "CornerRadius=20",
  "controlStyles[38].styles[3]": "Shadow:=",
  "controlStyles[38].styles[4]": "//Target= Control Center Container",
  
  "controlStyles[39].target": "Grid#L1Grid > Border",
  "controlStyles[39].styles[0]": "Background=Transparent",
  "controlStyles[39].styles[1]": "//Target= Control Center's Overlay Layer",
  
  "controlStyles[40].target": "Grid#L1Grid",
  "controlStyles[40].styles[0]": "Background:=$Alt",
  "controlStyles[40].styles[1]": "BorderBrush=Transparent",
  "controlStyles[40].styles[2]": "CornerRadius=20",
  "controlStyles[40].styles[3]": "//Target= Control Center's Body",
  
  "controlStyles[41].target": "ControlCenter.PaginatedGridView > Grid > GridView#RootGridView",
  "controlStyles[41].styles[0]": "Height=auto",
  "controlStyles[41].styles[1]": "//Target= Control Center's Page (This is to make all buttons in one Page)",
  
  "controlStyles[42].target": "Microsoft.UI.Xaml.Controls.PipsPager#QuickActionsPager",
  "controlStyles[42].styles[0]": "Visibility=Collapsed",
  "controlStyles[42].styles[1]": "//Target= Control Center's Page Indicator",
  
  "controlStyles[43].target": "ContentPresenter#ContentPresenter",
  "controlStyles[43].styles[0]": "BorderBrush=Transparent",
  "controlStyles[43].styles[1]": "//Target= Control Center Buttons' Container",
  
  "controlStyles[44].target": "ControlCenter.PaginatedToggleButton",
  "controlStyles[44].styles[0]": "Height=60",
  "controlStyles[44].styles[1]": "//Target= Control Center's Buttons",
  
  "controlStyles[45].target": "ContentControl > ContentPresenter > Grid > Grid",
  "controlStyles[45].styles[0]": "CornerRadius=12",
  "controlStyles[45].styles[1]": "//Target= Control Center's Buttons",
  
  "controlStyles[46].target": "ControlCenter.PaginatedToggleButton > ContentPresenter#ContentPresenter@CommonStates",
  "controlStyles[46].styles[0]": "Background@Normal:= <AcrylicBrush TintColor=\"{ThemeResource SystemAltHighColor}\" FallbackColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" />",
  "controlStyles[46].styles[1]": "//Background@PointerOver:= </>",
  "controlStyles[46].styles[2]": "//Background@Pressed:= </>",
  "controlStyles[46].styles[3]": "//Background@Disabled= </>",
  "controlStyles[46].styles[4]": "Background@Checked:=$Accent",
  "controlStyles[46].styles[5]": "Background@CheckedPointerOver:= <AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorLight1}\" TintOpacity=\"0.6\" TintLuminosityOpacity=\"0.6\" FallbackColor=\"{ThemeResource SystemAccentColorLight1}\" />",
  "controlStyles[46].styles[6]": "Background@CheckedPressed:= <AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.6\" TintLuminosityOpacity=\"0.6\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "controlStyles[46].styles[7]": "Background@CheckedDisabled:= <AcrylicBrush TintColor=\"red\" TintOpacity=\"0.6\" TintLuminosityOpacity=\"0.6\" FallbackColor=\"red\" />",
  "controlStyles[46].styles[8]": "//Target= Control Center > Buttons States Coloring",
  
  "controlStyles[47].target": "Grid > Microsoft.UI.Xaml.Controls.AnimatedIcon",
  "controlStyles[47].styles[0]": "Height=30",
  "controlStyles[47].styles[1]": "Width=30",
  "controlStyles[47].styles[2]": "//Target= Control Center Buttons' icons",
  
  "controlStyles[48].target": "ContentPresenter#Content > StackPanel > TextBlock",
  "controlStyles[48].styles[0]": "Visibility=Collapsed",
  "controlStyles[48].styles[1]": "//Target= Control Center > Text Under Buttons",
  
  "controlStyles[49].target": "ControlCenter.PaginatedToggleButton#ToggleButton[AutomationProperties.Name=Accessibility]",
  "controlStyles[49].styles[0]": "CornerRadius=10",
  "controlStyles[49].styles[1]": "//Target= Control Center > Accessibility Button",
  
  "controlStyles[50].target": "ControlCenter.PaginatedToggleButton#ToggleButton[AutomationProperties.Name=Cast]",
  "controlStyles[50].styles[0]": "CornerRadius=10",
  "controlStyles[50].styles[1]": "//Target= Control Center > Cast Button",
  
  "controlStyles[51].target": "ControlCenter.PaginatedToggleButton#ToggleButton[AutomationProperties.Name=Project]",
  "controlStyles[51].styles[0]": "CornerRadius=10",
  "controlStyles[51].styles[1]": "//Target= Control Center > Project Button",
  
  "controlStyles[52].target": "ControlCenter.PaginatedGridView > Grid",
  "controlStyles[52].styles[0]": "BorderBrush=Transparent",
  "controlStyles[52].styles[1]": "//Target= Control Center > Volume & Brightness area > Top Border",
  
  "controlStyles[53].target": "Rectangle#HorizontalTrackRect",
  "controlStyles[53].styles[0]": "Opacity=0",
  "controlStyles[53].styles[1]": "//Target= Control Center > Brightness & Volume Empty Track",
  
  "controlStyles[54].target": "Rectangle#HorizontalDecreaseRect",
  "controlStyles[54].styles[0]": "Fill:=$Accent",
  "controlStyles[54].styles[1]": "Height=6",
  "controlStyles[54].styles[2]": "//Target= Control Center > Volume & Brightness Fill Track",
  
  "controlStyles[55].target": "Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb > Border",
  "controlStyles[55].styles[0]": "Visibility=Collapsed",
  "controlStyles[55].styles[1]": "//Target= Control Center > Brightness And Volume Knobs",
  
  "controlStyles[56].target": "Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb",
  "controlStyles[56].styles[0]": "Width=0",
  "controlStyles[56].styles[1]": "//Target= Control Center > Brightness and Volume Tracks Thumb (This may seem not so important but it is)",
  
  "controlStyles[57].target": "Microsoft.UI.Xaml.Controls.AnimatedIcon#BrightnessPlayer",
  "controlStyles[57].styles[0]": "Height=25",
  "controlStyles[57].styles[1]": "Width=25",
  "controlStyles[57].styles[2]": "//Target= Control Center > Brightness Animated icon",
  
  "controlStyles[58].target": "Microsoft.UI.Xaml.Controls.AnimatedIcon#FooterButtonIcon",
  "controlStyles[58].styles[0]": "Height=25",
  "controlStyles[58].styles[1]": "Width=25",
  "controlStyles[58].styles[2]": "//Target= Control Center > Volume Animated  icon",
  
  "controlStyles[59].target": "Button#VolumeL2Button > ContentPresenter > StackPanel > FontIcon[1]",
  "controlStyles[59].styles[0]": "FontSize=20",
  "controlStyles[59].styles[1]": "//Target= Control Center > Sound Output Button icon",
  
  "controlStyles[60].target": "StackPanel > ContentPresenter > ContentControl > ContentPresenter > Button > ContentPresenter > StackPanel > TextBlock#Icon",
  "controlStyles[60].styles[0]": "FontSize=25",
  "controlStyles[60].styles[1]": "//Target= Control Center > Battery icon",
  
  "controlStyles[61].target": "StackPanel > ContentPresenter > ContentControl > ContentPresenter > Button > ContentPresenter > StackPanel > TextBlock[2]",
  "controlStyles[61].styles[0]": "FontSize=16",
  "controlStyles[61].styles[1]": "//Target= Control Center > Battery Percentage Text",
  
  "controlStyles[62].target": "Windows.UI.Xaml.Controls.Primitives.ToggleButton > ContentPresenter > Microsoft.UI.Xaml.Controls.AnimatedIcon",
  "controlStyles[62].styles[0]": "Height=25",
  "controlStyles[62].styles[1]": "Width=25",
  "controlStyles[62].styles[2]": "//Target= Control Center > Settings Animated icon",
  
  "controlStyles[63].target": "Grid#L1Grid > Grid",
  "controlStyles[63].styles[0]": "BorderBrush=Transparent",
  "controlStyles[63].styles[1]": "//Target= Control Center's Fotter's Top Border",
  
  "controlStyles[64].target": "ContentPresenter#PageHeader",
  "controlStyles[64].styles[0]": "Background=Transparent",
  "controlStyles[64].styles[1]": "//Target= Control Center > Sub-Menus' Header",
  
  "controlStyles[65].target": "Grid#FullScreenPageRoot > ContentPresenter#PageHeader > Border > Grid > Button#BackButton",
  "controlStyles[65].styles[0]": "CornerRadius=14",
  "controlStyles[65].styles[1]": "//Target= Control Center > Sub-Menu > Header > Back Button",
  
  "controlStyles[66].target": "ContentPresenter > Grid#FullScreenPageRoot",
  "controlStyles[66].styles[0]": "Background:=$DarkAccent",
  "controlStyles[66].styles[1]": "//Target= Control Center > Sub-Menus' Box",
  
  "controlStyles[67].target": "ContentPresenter#PageContent > Grid > Border",
  "controlStyles[67].styles[0]": "Background=Transparent",
  "controlStyles[67].styles[1]": "//Target= Control Center > Sub-Menus' Bodys (Part1)",
  
  "controlStyles[68].target": "Grid > ScrollViewer#ListContent",
  "controlStyles[68].styles[0]": "Background=Transparent",
  "controlStyles[68].styles[1]": "//Target= Control Center > Sub-Menus' Bodys (Part2)",
  
  "controlStyles[69].target": "Border#SwitchKnobOn",
  "controlStyles[69].styles[0]": "Background=",
  "controlStyles[69].styles[1]": "//Target= Control Center > Wifi & Bluetooth Sub-Menus > On/Off Switch (This used to solve an issue before 24H2)",
  
  "controlStyles[70].target": "StackPanel > ContentPresenter > Border",
  "controlStyles[70].styles[0]": "BorderBrush=Transparent",
  "controlStyles[70].styles[1]": "//Target= Control Center > Sub-Menus (Except Cast & WiFi) > Footer",
  
  "controlStyles[71].target": "Border#WADFeatureFooter",
  "controlStyles[71].styles[0]": "BorderBrush=Transparent",
  "controlStyles[71].styles[1]": "//Target= Control Center > Cast Sub-Menu > Footer",
  
  "controlStyles[72].target": "Grid#MediaTransportControlsRoot",
  "controlStyles[72].styles[0]": "Background=Transparent",
  "controlStyles[72].styles[1]": "//Target= Control Center > Media Panel > Overlay Layer",
  
  "controlStyles[73].target": "Grid#MediaTransportControlsRegion",
  "controlStyles[73].styles[0]": "Background:=$DarkAccent",
  "controlStyles[73].styles[1]": "BorderBrush=Transparent",
  "controlStyles[73].styles[2]": "CornerRadius=20",
  "controlStyles[73].styles[3]": "Height=Auto",
  "controlStyles[73].styles[4]": "Shadow:=",
  "controlStyles[73].styles[5]": "//Target= Control Center > Media Panel",
  
  "controlStyles[74].target": "Grid#MediaTransportControlsRoot > Grid[2]",
  "controlStyles[74].styles[0]": "Margin=-8,0,0,12",
  "controlStyles[74].styles[1]": "//Target= Control Center > Media Panel > App Name & icon",
  
  "controlStyles[75].target": "StackPanel#PrimaryAndSecondaryTextContainer",
  "controlStyles[75].styles[0]": "Visibility=Collapsed",
  "controlStyles[75].styles[1]": "//Target= Control Center > Media Panel > Media Name & Subtitles",
  
  "controlStyles[76].target": "Grid#AlbumTextAndArtContainer",
  "controlStyles[76].styles[0]": "HorizontalAlignment=Center",
  "controlStyles[76].styles[1]": "//Target= Control Center > Media Panel > Media Name & Thumbnail Container",
  
  "controlStyles[77].target": "Grid#ThumbnailImage",
  "controlStyles[77].styles[0]": "CornerRadius=15",
  "controlStyles[77].styles[1]": "Height=300",
  "controlStyles[77].styles[2]": "Width=300",
  "controlStyles[77].styles[3]": "//Target= Control Center > Media Panel > Media Thumbnail",
  
  "controlStyles[78].target": "Border#JumpListRestyledAcrylic",
  "controlStyles[78].styles[0]": "Background:=$DarkAccent",
  "controlStyles[78].styles[1]": "CornerRadius=15",
  "controlStyles[78].styles[2]": "Shadow:=",
  "controlStyles[78].styles[3]": "//Target= Taskbar Apps > Left Click Menu (Jumplist)",
  
  "controlStyles[79].target": "GridViewItem[1] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[79].styles[0]": "AccessKey=1",
  "controlStyles[79].styles[1]": "//Target= Control Center Button#1",
  
  "controlStyles[80].target": "GridViewItem[2] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[80].styles[0]": "AccessKey=2",
  "controlStyles[80].styles[1]": "//Target= Control Center Button#2",
  
  "controlStyles[81].target": "GridViewItem[3] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[81].styles[0]": "AccessKey=3",
  "controlStyles[81].styles[1]": "//Target= Control Center Button#3",
  
  "controlStyles[82].target": "GridViewItem[4] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[82].styles[0]": "AccessKey=4",
  "controlStyles[82].styles[1]": "//Target= Control Center Button#4",
  
  "controlStyles[83].target": "GridViewItem[5] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[83].styles[0]": "AccessKey=5",
  "controlStyles[83].styles[1]": "//Target= Control Center Button#5",
  
  "controlStyles[84].target": "GridViewItem[6] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[84].styles[0]": "AccessKey=6",
  "controlStyles[84].styles[1]": "//Target= Control Center Button#6",
  
  "controlStyles[85].target": "GridViewItem[7] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[85].styles[0]": "AccessKey=7",
  "controlStyles[85].styles[1]": "//Target= Control Center Button#7",
  
  "controlStyles[86].target": "GridViewItem[8] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[86].styles[0]": "AccessKey=8",
  "controlStyles[86].styles[1]": "//Target= Control Center Button#8",
  
  "controlStyles[87].target": "GridViewItem[9] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[87].styles[0]": "AccessKey=9",
  "controlStyles[87].styles[1]": "//Target= Control Center Button#9",
  
  "controlStyles[88].target": "GridViewItem[10] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[88].styles[0]": "AccessKey=0",
  "controlStyles[88].styles[1]": "//Target= Control Center Button#10",
  
  "controlStyles[89].target": "GridViewItem[11] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[89].styles[0]": "AccessKey=-",
  "controlStyles[89].styles[1]": "//Target= Control Center Button#11",
  
  "controlStyles[90].target": "GridViewItem[1] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[90].styles[0]": "AccessKey=1",
  "controlStyles[90].styles[1]": "//Target= Control Center Button#1",
  
  "controlStyles[91].target": "GridViewItem[2] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[91].styles[0]": "AccessKey=2",
  "controlStyles[91].styles[1]": "//Target= Control Center Button#2",
  
  "controlStyles[92].target": "GridViewItem[3] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[92].styles[0]": "AccessKey=3",
  "controlStyles[92].styles[1]": "//Target= Control Center Button#3",
  
  "controlStyles[93].target": "GridViewItem[4] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[93].styles[0]": "AccessKey=4",
  "controlStyles[93].styles[1]": "//Target= Control Center Button#4",
  
  "controlStyles[94].target": "GridViewItem[5] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[94].styles[0]": "AccessKey=5",
  "controlStyles[94].styles[1]": "//Target= Control Center Button#5",
  
  "controlStyles[95].target": "GridViewItem[6] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[95].styles[0]": "AccessKey=6",
  "controlStyles[95].styles[1]": "//Target= Control Center Button#6",
  
  "controlStyles[96].target": "GridViewItem[7] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[96].styles[0]": "AccessKey=7",
  "controlStyles[96].styles[1]": "//Target= Control Center Button#7",
  
  "controlStyles[97].target": "GridViewItem[8] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[97].styles[0]": "AccessKey=8",
  "controlStyles[97].styles[1]": "//Target= Control Center Button#8",
  
  "controlStyles[98].target": "GridViewItem[9] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[98].styles[0]": "AccessKey=9",
  "controlStyles[98].styles[1]": "//Target= Control Center Button#9",
  
  "controlStyles[99].target": "GridViewItem[10] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[99].styles[0]": "AccessKey=0",
  "controlStyles[99].styles[1]": "//Target= Control Center Button#10",
  
  "controlStyles[100].target": "GridViewItem[11] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton",
  "controlStyles[100].styles[0]": "AccessKey=-",
  "controlStyles[100].styles[1]": "//Target= Control Center Button#11",
  
  "controlStyles[101].target": "Grid#RootGrid > QuickActions.ControlCenter.FrameWithContentChanged#L2Frame",
  "controlStyles[101].styles[0]": "Background=Transparent",
  "controlStyles[101].styles[1]": "//Target= (No Idea, used to solve an issue before 24H2)",
  
  "controlStyles[102].target": "QuickActions.ControlCenter.AccessibleWindow#PageWindow",
  "controlStyles[102].styles[0]": "Background=Transparent",
  "controlStyles[102].styles[1]": "//Target= (No Idea, used to solve an issue before 24H2)",
  
  "styleConstants[0]": "Alt = <AcrylicBrush TintColor=\"{ThemeResource SystemAltHighColor}\" TintOpacity=\"0.6\" TintLuminosityOpacity=\"0.6\" FallbackColor=\"{ThemeResource SystemAltHighColor}\" />",
  "styleConstants[1]": "Accent = <AcrylicBrush TintColor=\"{ThemeResource SystemAccentColor}\" TintOpacity=\"0.6\" TintLuminosityOpacity=\"0.6\" FallbackColor=\"{ThemeResource SystemAccentColor}\" />",
  "styleConstants[2]": "DarkAccent = <AcrylicBrush TintColor=\"{ThemeResource SystemAccentColorDark1}\" TintOpacity=\"0.6\" TintLuminosityOpacity=\"0.3\" FallbackColor=\"{ThemeResource SystemAccentColorDark1}\" />",
  "styleConstants[3]": "SolidAccent = <SolidColorBrush Color=\"{ThemeResource SystemAccentColor}\" Opacity=\"1\"/>",
  "styleConstants[4]": "Reveal = <RevealBorderBrush Color=\"Transparent\" TargetTheme=\"1\" Opacity=\"1\" />"
}
```
