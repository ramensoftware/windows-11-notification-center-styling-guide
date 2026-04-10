# Oversimplified&Accentuated theme for Windows 11 Notification Center Styler

A cleaner, more refined Windows Notification Center (& Control Center) theme - removing unnecessary elements and offering better **accent color** integration.

> [!NOTE]
> This theme is optimized for Windows in **Dark Mode** and may not display correctly in **Light Mode**.

### ✨ Features
- Removed unnecessary text and lines
- Enlarged icons
- Enhanced Accent Color presence (automatically updates with Windows Accent Color)
- Improved transparency effects
- Added subtle, neat border reveal effects
- Took fallback colors (colors in battery mode) into consideration
- Added useful access keys ([ Alt + Key ] shortcuts):
  - Notification Center
    - Toggle DoNotDisturb → [ Alt + D ]
    - "Clear all" button → [ Alt + C ]
    - Expand/Collapse calendar → [ Alt + E ]
  - Control Center
    - Button in position #1 → [ Alt + 1 ]
    - Button in position #2 → [ Alt + 2 ]
    - Button in position #3 → [ Alt + 3 ]
    - Button in position #4 → [ Alt + 4 ]
    - Button in position #5 → [ Alt + 5 ]
    - Button in position #6 → [ Alt + 6 ]
    - Button in position #7 → [ Alt + 7 ]
    - Button in position #8 → [ Alt + 8 ]
    - Button in position #9 → [ Alt + 9 ]
    - Button in position #10 → [ Alt + 0 ]
    - Button in position #11 → [ Alt + - ]

> [!NOTE]
> I am aware that the **Access Key** for the **Nearby Sharing** button in **Control Center** windows is not functional, this is because this button in particular has a slightly different JSON Selector than the rest of the buttons, I'm looking for a work-around for this problem.

> [!NOTE]
> If you change the position of a button in **Control Center**, you need to restart `ShellHost.exe` for the **Access Keys** to change according to the new buttons' layout.

**Author:** [OsamaJT](https://github.com/OsamaHJT)

![Screenshot](Notification%20Center.png)

---

## 🎨 Elements modified
- Notification Center
- Notifications (active & in Control Center)
- Calendar
- Control Center
- Media panel in Control Center
- Left click menus (Jumplists) for taskbar apps
- Context menu
- Tooltip popup

---

## Theme selection

The theme is integrated into the mod and can be selected directly from the mod's
settings:

* Open the Windows 11 Notification Center Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Notification Center Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

<details>
<summary>Content to import (click to expand)</summary>

```yaml
styleConstants:
  - Alt = <AcrylicBrush TintColor="{ThemeResource SystemAltHighColor}" TintOpacity="0.6" TintLuminosityOpacity="0.6" FallbackColor="{ThemeResource SystemAltHighColor}" />
  - Accent = <AcrylicBrush TintColor="{ThemeResource SystemAccentColor}" TintOpacity="0.6" TintLuminosityOpacity="0.6" FallbackColor="{ThemeResource SystemAccentColor}" />
  - DarkAccent = <AcrylicBrush TintColor="{ThemeResource SystemAccentColorDark1}" TintOpacity="0.6" TintLuminosityOpacity="0.3" FallbackColor="{ThemeResource SystemAccentColorDark1}" />
  - SolidAccent = <SolidColorBrush Color="{ThemeResource SystemAccentColor}" Opacity="1"/>
  - Reveal = <RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" />
controlStyles:
  - target: MenuFlyoutPresenter
    styles:
      - Background:=$DarkAccent
      - BorderBrush=Transparent
      - Shadow:=
      - //Target= Context Menu
  - target: ToolTip > ContentPresenter#LayoutRoot
    styles:
      - Background:=$DarkAccent
      - BorderBrush:=$Reveal
      - Shadow:=
      - //Target= Tooltip Popup
  - target: Grid#NotificationCenterGrid
    styles:
      - Background:=$Alt
      - BorderBrush=Transparent
      - Shadow:=
      - //Target= Notification Center Box
  - target: TextBlock#NotificationsTextBlock
    styles:
      - Visibility=Collapsed
      - //Target= Notification Center > "Notifications" Text
  - target: Button#ClearAll
    styles:
      - AccessKey=C
      - //Target= "ClearAll" Button
  - target: Windows.UI.Xaml.Controls.Primitives.ToggleButton#DoNotDisturbButton
    styles:
      - AccessKey=D
      - //Target= Notification Center > DoNotDisturb Button
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#DoNotDisturbButtonIcon
    styles:
      - Height=16
      - Width=16
      - //Target= Notification Center > DoNotDisturb Button icon
  - target: Grid#DoNotDisturbSubtext
    styles:
      - Background:=$Accent
      - BorderBrush:=$Reveal
      - BorderThickness=2
      - CornerRadius=5
      - Margin=0,0,0,10
      - //Target= Notification Center > DoNotDisturb Activated Plate
  - target: Grid#DoNotDisturbSubtext > TextBlock[1]
    styles:
      - Visibility=Collapsed
      - //Target= Notification Center > DoNotDisturb Activated Plate > DoNotDisturb icon
  - target: Grid#DoNotDisturbSubtext > TextBlock[2]
    styles:
      - HorizontalAlignment=Center
      - FontSize=18
      - //Target= Notification Center > DoNotDisturb Activated Plate > "Donotdisturbison" Text
  - target: Grid#DoNotDisturbSubtext > TextBlock[3]
    styles:
      - TextAlignment=Center
      - FontSize=11
      - //Target= Notification Center > DoNotDisturb Activated Plate > "You'll onlyseebannersforprioritynotificationsandalarams." text
  - target: Grid#DoNotDisturbSubtext > Button
    styles:
      - HorizontalAlignment=Center
      - Margin= 0,0,0,0
      - //Target= Notification Center > DoNotDisturb Activated Plate > "NotificationSettings" Button in Do Not Disturb Banner
  - target: TextBlock#NotificationSettingsButtonText[Text=Notification settings]
    styles:
      - Text=Settings
      - //Target= Notification Center > DoNotDisturb Activated Plate > "NotificationSettings" Text in Do Not Disturb Banner
  - target: Border#ItemOpaquePlating
    styles:
      - BorderBrush:=$Reveal
      - //Target= Notification Center > Notification Plate
  - target: Border#StandardImageBorder
    styles:
      - Height=30
      - Width=30
      - //Target= Notification Center > Notification App Icon
  - target: Grid#GroupTitleGrid > TextBlock#Title
    styles:
      - Visibility=Collapsed
      - //Target= Notification Center > Notification App Name
  - target: Grid > Button#VerbButton
    styles:
      - BorderBrush=Transparent
      - //Target= Notification Center > Notification App Buttons
  - target: Border#PopupBorder
    styles:
      - Background:=$DarkAccent
      - Shadow:=
      - //Target= Notification Center > Notification-In Context Menu
  - target: ProgressBar#progressBar > Grid > Border#DeterminateRoot
    styles:
      - Background=Transparent
      - //Target= Notification Center > Progress Bar > Empty Track
  - target: Border#ToastBackgroundBorder2
    styles:
      - Background:=$Alt
      - BorderBrush=Transparent
      - CornerRadius=15
      - Shadow:=
      - //Target= Active Notification > Notification Plate
  - target: Border#AppLogoBorder2
    styles:
      - Height=30
      - Width=30
      - //Target= Active Notification > App icon's Container
  - target: Border#AppLogoBorder
    styles:
      - Height=30
      - Width=30
      - //Target= Active Notification > App icon (Before 24H2 I think)
  - target: Image#AppLogo2
    styles:
      - Height=30
      - Width=30
      - //Target= Active Notification > App icon
  - target: Grid#ToastTitleBar > TextBlock#SenderName
    styles:
      - Visibility=Collapsed
      - //Target= Active Notification > App Name
  - target: Grid#CalendarCenterGrid
    styles:
      - Background:=$Alt
      - BorderBrush=Transparent
      - CornerRadius=20
      - Shadow:=
      - //Target= Calendar Box
  - target: Border#CalendarHeaderMinimizedOverlay
    styles:
      - Background=Transparent
      - //Target= Calendar's Header (When Minimized)
  - target: Button#ExpandCollapseButton
    styles:
      - Background=Transparent
      - BorderBrush=Transparent
      - AccessKey=E
      - //Target= Calendar > Header > Expand/Collapse Button
  - target: ScrollViewer#CalendarControlScrollViewer
    styles:
      - Background=Transparent
      - BorderBrush=Transparent
      - //Target= Calendar's Body
  - target: CalendarViewDayItem
    styles:
      - CornerRadius=10
      - //Target= Calendar's Day Container
  - target: CalendarViewDayItem > Border
    styles:
      - BorderBrush:= <RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" />
      - CornerRadius=12
      - //Target= Calendar's Day
  - target: Windows.UI.Xaml.Controls.Primitives.CalendarPanel#YearViewPanel > Control
    styles:
      - CornerRadius=12
      - //Target= Target= Calendar's Month's Container
  - target: Windows.UI.Xaml.Controls.Primitives.CalendarPanel#YearViewPanel > Control > Border
    styles:
      - BorderBrush:=$Reveal
      - BorderThickness=2
      - CornerRadius=12
      - //Target= Calendar's Month
  - target: Windows.UI.Xaml.Controls.Primitives.CalendarPanel#DecadeViewPanel > Control
    styles:
      - CornerRadius=12
      - //Target= Target= Calendar's Year's Container
  - target: Windows.UI.Xaml.Controls.Primitives.CalendarPanel#DecadeViewPanel > Control > Border
    styles:
      - BorderBrush:=$Reveal
      - BorderThickness=2
      - CornerRadius=12
      - //Target= Calendar's Year
  - target: Grid#FocusGrid
    styles:
      - Background=Transparent
      - BorderBrush=Transparent
      - //Target= Calendar > Focus Grid (Calendar's Footer)
  - target: Button#IncreaseTimeButton
    styles:
      - Background=Transparent
      - BorderBrush=Transparent
      - //Target= Calendar > Focus Grid > Increase Time Button
  - target: Button#DecreaseTimeButton
    styles:
      - Background=Transparent
      - BorderBrush=Transparent
      - //Target= Calendar > Focus Grid > Decrease Time Button
  - target: Button#StartButton
    styles:
      - Background=Transparent
      - BorderBrush=Transparent
      - //Target= Calendar > Focus Grid > Focus Button
  - target: Grid#ControlCenterRegion
    styles:
      - Background=Transparent
      - BorderBrush=Transparent
      - CornerRadius=20
      - Shadow:=
      - //Target= Control Center Container
  - target: Grid#L1Grid > Border
    styles:
      - Background=Transparent
      - //Target= Control Center's Overlay Layer
  - target: Grid#L1Grid
    styles:
      - Background:=$Alt
      - BorderBrush=Transparent
      - CornerRadius=20
      - //Target= Control Center's Body
  - target: ControlCenter.PaginatedGridView > Grid > GridView#RootGridView
    styles:
      - Height=auto
      - //Target= Control Center's Page (This is to make all buttons in one Page)
  - target: Microsoft.UI.Xaml.Controls.PipsPager#QuickActionsPager
    styles:
      - Visibility=Collapsed
      - //Target= Control Center's Page Indicator
  - target: ContentPresenter#ContentPresenter
    styles:
      - BorderBrush=Transparent
      - //Target= Control Center Buttons' Container
  - target: ControlCenter.PaginatedToggleButton
    styles:
      - Height=60
      - //Target= Control Center's Buttons
  - target: ContentControl > ContentPresenter > Grid > Grid
    styles:
      - CornerRadius=12
      - //Target= Control Center's Buttons
  - target: ControlCenter.PaginatedToggleButton > ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Background@Normal:= <AcrylicBrush TintColor="{ThemeResource SystemAltHighColor}" FallbackColor="{ThemeResource CardStrokeColorDefaultSolid}" />
      - //Background@PointerOver:= </>
      - //Background@Pressed:= </>
      - //Background@Disabled= </>
      - Background@Checked:=$Accent
      - Background@CheckedPointerOver:= <AcrylicBrush TintColor="{ThemeResource SystemAccentColorLight1}" TintOpacity="0.6" TintLuminosityOpacity="0.6" FallbackColor="{ThemeResource SystemAccentColorLight1}" />
      - Background@CheckedPressed:= <AcrylicBrush TintColor="{ThemeResource SystemAccentColorDark1}" TintOpacity="0.6" TintLuminosityOpacity="0.6" FallbackColor="{ThemeResource SystemAccentColorDark1}" />
      - Background@CheckedDisabled:= <AcrylicBrush TintColor="red" TintOpacity="0.6" TintLuminosityOpacity="0.6" FallbackColor="red" />
      - //Target= Control Center > Buttons States Coloring
  - target: Grid > Microsoft.UI.Xaml.Controls.AnimatedIcon
    styles:
      - Height=30
      - Width=30
      - //Target= Control Center Buttons' icons
  - target: ContentPresenter#Content > StackPanel > TextBlock
    styles:
      - Visibility=Collapsed
      - //Target= Control Center > Text Under Buttons
  - target: ControlCenter.PaginatedToggleButton#ToggleButton[AutomationProperties.Name=Accessibility]
    styles:
      - CornerRadius=10
      - //Target= Control Center > Accessibility Button
  - target: ControlCenter.PaginatedToggleButton#ToggleButton[AutomationProperties.Name=Cast]
    styles:
      - CornerRadius=10
      - //Target= Control Center > Cast Button
  - target: ControlCenter.PaginatedToggleButton#ToggleButton[AutomationProperties.Name=Project]
    styles:
      - CornerRadius=10
      - //Target= Control Center > Project Button
  - target: ControlCenter.PaginatedGridView > Grid
    styles:
      - BorderBrush=Transparent
      - //Target= Control Center > Volume & Brightness area > Top Border
  - target: Rectangle#HorizontalTrackRect
    styles:
      - Opacity=0
      - //Target= Control Center > Brightness & Volume Empty Track
  - target: Rectangle#HorizontalDecreaseRect
    styles:
      - Fill:=$Accent
      - Height=6
      - //Target= Control Center > Volume & Brightness Fill Track
  - target: Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb > Border
    styles:
      - Visibility=Collapsed
      - //Target= Control Center > Brightness And Volume Knobs
  - target: Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb
    styles:
      - Width=0
      - //Target= Control Center > Brightness and Volume Tracks Thumb (This may seem not so important but it is)
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#BrightnessPlayer
    styles:
      - Height=25
      - Width=25
      - //Target= Control Center > Brightness Animated icon
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#FooterButtonIcon
    styles:
      - Height=25
      - Width=25
      - //Target= Control Center > Volume Animated  icon
  - target: Button#VolumeL2Button > ContentPresenter > StackPanel > FontIcon[1]
    styles:
      - FontSize=20
      - //Target= Control Center > Sound Output Button icon
  - target: StackPanel > ContentPresenter > ContentControl > ContentPresenter > Button > ContentPresenter > StackPanel > TextBlock#Icon
    styles:
      - FontSize=25
      - //Target= Control Center > Battery icon
  - target: StackPanel > ContentPresenter > ContentControl > ContentPresenter > Button > ContentPresenter > StackPanel > TextBlock[2]
    styles:
      - FontSize=16
      - //Target= Control Center > Battery Percentage Text
  - target: Windows.UI.Xaml.Controls.Primitives.ToggleButton > ContentPresenter > Microsoft.UI.Xaml.Controls.AnimatedIcon
    styles:
      - Height=25
      - Width=25
      - //Target= Control Center > Settings Animated icon
  - target: Grid#L1Grid > Grid
    styles:
      - BorderBrush=Transparent
      - //Target= Control Center's Footer's Top Border
  - target: ContentPresenter#PageHeader
    styles:
      - Background=Transparent
      - //Target= Control Center > Sub-Menus' Header
  - target: Grid#FullScreenPageRoot > ContentPresenter#PageHeader > Border > Grid > Button#BackButton
    styles:
      - CornerRadius=14
      - //Target= Control Center > Sub-Menu > Header > Back Button
  - target: ContentPresenter > Grid#FullScreenPageRoot
    styles:
      - Background:=$DarkAccent
      - //Target= Control Center > Sub-Menus' Box
  - target: ContentPresenter#PageContent > Grid > Border
    styles:
      - Background=Transparent
      - //Target= Control Center > Sub-Menus' Bodys (Part1)
  - target: Grid > ScrollViewer#ListContent
    styles:
      - Background=Transparent
      - //Target= Control Center > Sub-Menus' Bodys (Part2)
  - target: Border#SwitchKnobOn
    styles:
      - Background=
      - //Target= Control Center > Wifi & Bluetooth Sub-Menus > On/Off Switch (This used to solve an issue before 24H2)
  - target: StackPanel > ContentPresenter > Border
    styles:
      - BorderBrush=Transparent
      - //Target= Control Center > Sub-Menus (Except Cast & WiFi) > Footer
  - target: Border#WADFeatureFooter
    styles:
      - BorderBrush=Transparent
      - //Target= Control Center > Cast Sub-Menu > Footer
  - target: Grid#MediaTransportControlsRoot
    styles:
      - Background=Transparent
      - //Target= Control Center > Media Panel > Overlay Layer
  - target: Grid#MediaTransportControlsRegion
    styles:
      - Background:=$DarkAccent
      - BorderBrush=Transparent
      - CornerRadius=20
      - Height=Auto
      - Shadow:=
      - //Target= Control Center > Media Panel
  - target: Grid#MediaTransportControlsRoot > Grid[2]
    styles:
      - Margin=-8,0,0,12
      - //Target= Control Center > Media Panel > App Name & icon
  - target: StackPanel#PrimaryAndSecondaryTextContainer
    styles:
      - Visibility=Collapsed
      - //Target= Control Center > Media Panel > Media Name & Subtitles
  - target: Grid#AlbumTextAndArtContainer
    styles:
      - HorizontalAlignment=Center
      - //Target= Control Center > Media Panel > Media Name & Thumbnail Container
  - target: Grid#ThumbnailImage
    styles:
      - CornerRadius=15
      - Height=300
      - Width=300
      - //Target= Control Center > Media Panel > Media Thumbnail
  - target: Border#JumpListRestyledAcrylic
    styles:
      - Background:=$DarkAccent
      - CornerRadius=15
      - Shadow:=
      - //Target= Taskbar Apps > Left Click Menu (Jumplist)
  - target: GridViewItem[1] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=1
      - //Target= Control Center Button#1
  - target: GridViewItem[2] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=2
      - //Target= Control Center Button#2
  - target: GridViewItem[3] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=3
      - //Target= Control Center Button#3
  - target: GridViewItem[4] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=4
      - //Target= Control Center Button#4
  - target: GridViewItem[5] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=5
      - //Target= Control Center Button#5
  - target: GridViewItem[6] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=6
      - //Target= Control Center Button#6
  - target: GridViewItem[7] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=7
      - //Target= Control Center Button#7
  - target: GridViewItem[8] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=8
      - //Target= Control Center Button#8
  - target: GridViewItem[9] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=9
      - //Target= Control Center Button#9
  - target: GridViewItem[10] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=0
      - //Target= Control Center Button#10
  - target: GridViewItem[11] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=-
      - //Target= Control Center Button#11
  - target: GridViewItem[1] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=1
      - //Target= Control Center Button#1
  - target: GridViewItem[2] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=2
      - //Target= Control Center Button#2
  - target: GridViewItem[3] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=3
      - //Target= Control Center Button#3
  - target: GridViewItem[4] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=4
      - //Target= Control Center Button#4
  - target: GridViewItem[5] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=5
      - //Target= Control Center Button#5
  - target: GridViewItem[6] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=6
      - //Target= Control Center Button#6
  - target: GridViewItem[7] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=7
      - //Target= Control Center Button#7
  - target: GridViewItem[8] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=8
      - //Target= Control Center Button#8
  - target: GridViewItem[9] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=9
      - //Target= Control Center Button#9
  - target: GridViewItem[10] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=0
      - //Target= Control Center Button#10
  - target: GridViewItem[11] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > ContentControl > ContentPresenter > Grid > ControlCenter.PaginatedToggleButton#ToggleButton
    styles:
      - AccessKey=-
      - //Target= Control Center Button#11
  - target: Grid#RootGrid > QuickActions.ControlCenter.FrameWithContentChanged#L2Frame
    styles:
      - Background=Transparent
      - //Target= (No Idea, used to solve an issue before 24H2)
  - target: QuickActions.ControlCenter.AccessibleWindow#PageWindow
    styles:
      - Background=Transparent
      - //Target= (No Idea, used to solve an issue before 24H2)
```
</details>

### Modification notes

I added an extra comment line at the end of each style group to indicate the target object with common language.  
The aim is to make it easier to modify or debug the theme in the future.
