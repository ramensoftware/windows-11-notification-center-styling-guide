# LayerMicaUI theme for Windows 11 Notification Center Styler
**Author**: [Nimai-HK](https://github.com/Nimai-HK)

![Preview](screenshot.png)

<table style="width:100%;">
  <tr>
    <td style="height:100%; text-align:center;"><img src="control-center.png" style="width:700px; height:auto; display:block; margin:auto;"></td>
    <td style="height:20%; text-align:center;"><img src="control-center-subpage.png" style="width:980px; height:auto; display:block; margin:auto;"></td>
    <td style="height:100%; text-align:center;"><img src="calendar-grid.png" style="width:700px; height:auto; display:block; margin:auto;"></td>
    <td style="height:100%; text-align:center;"><img src="notification-grid-expanded.png" style="width:700px; height:auto; display:block; margin:auto;"></td>
    <td style="height:100%; text-align:center;"><img src="jump-list.png" style="width:980px; height:auto; display:block; margin:auto;"></td>
  </tr>
</table>

## Notes
- Optimized for Windows 11 **25H2**.
- Fully compatible with both light and dark modes.
- Recommended to enable "Show time in notification center" Setting.

---

## Additional customization
<details>
  <summary>Font Customization (Click to expand)</summary>

- Font to be installed: [Nunito](https://fonts.google.com/specimen/Nunito)
- Add these items to the "Style constants" section of the settings page of the Windows 11 Notification Center Styler Mod

  ```
  ThFntWt=Semibold
  ThHdnWt=Bold
  ```
</details>

<details>
  <summary>Control Center Island Layer Size (Click to expand)</summary>

- This is the layer that is present in the control center, volume and brightness sliders region.
![Guiding Image](control-center-layer.png)
- Some users have a different number of sliders here. To make the theme fit your current setup, choose the appropriate phrase.
- Add these items to the "Style constants" section of the settings page of the Windows 11 Notification Center Styler Mod.\
- To be added:
  ```
  ControlCenterLayer=$<Option>
  ```

- Options:
  ```
  OneSlider
  TwoSlider
  ThreeSlider
  ```

- Usage: An example is provided below:
  ```
  ControlCenterLayer=$TwoSlider
  ```

- If you want to have a custom size for the same element, example:
  ```
  ControlCenterLayer=120
  ```
</details>

## Other LayerMicaUI Themes
- [LayerMicaUI Taskbar Theme](https://github.com/ramensoftware/windows-11-taskbar-styling-guide/tree/main/Themes/LayerMicaUI)

- [LayerMicaUI Start Menu Theme](https://github.com/ramensoftware/windows-11-start-menu-styling-guide/tree/main/Themes/LayerMicaUI)

## Theme selection

The theme is integrated into the mod and can be selected directly from the mod's
settings:

* Open the Windows 11 Notification Center Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Notification Center Styler mod in Windhawk.
* Go to the "Advanced" tab.
* Copy the content below to the text box under "Mod settings" and click "Save".

<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "styleConstants[0]": "ThemeLayer=<AcrylicBrush BackgroundSource=\"Backdrop\" TintColor=\"{ThemeResource SystemChromeMediumColor}\" TintOpacity=\"0.1\" TintLuminosityOpacity=\"0.8\" FallbackColor=\"{ThemeResource SystemChromeMediumColor}\" />",
  "styleConstants[1]": "OuterRadius=10",
  "styleConstants[2]": "InnerRadius=8",
  "styleConstants[3]": "ThemeBorder=<SolidColorBrush Color=\"{ThemeResource Border}\" />",
  "styleConstants[4]": "ThemeControlBorder=<SolidColorBrush Color=\"{ThemeResource ControlBorder}\" />",
  "styleConstants[5]": "ThemeOverlay=<SolidColorBrush Color=\"{ThemeResource Overlay}\" />",
  "styleConstants[6]": "ThFnt=Nunito",
  "styleConstants[7]": "ThFntWt=Normal",
  "styleConstants[8]": "ThHdnWt=Semibold",
  "styleConstants[9]": "ThemeOutBorder=<SolidColorBrush Color=\"#66757575\"/>",
  "styleConstants[10]": "ThemeBtn=<SolidColorBrush Color=\"{ThemeResource Btn}\" />",
  "styleConstants[11]": "ControlCenterLayer=120",
  "styleConstants[12]": "ThemeHover=<SolidColorBrush Color=\"{ThemeResource Hover}\" />",
  "styleConstants[13]": "OneSlider=60",
  "styleConstants[14]": "TwoSlider=120",
  "styleConstants[15]": "ThreeSlider=180",

  "themeResourceVariables[0]": "Overlay@Light=#55FFFFFF",
  "themeResourceVariables[1]": "Overlay@Dark=#09FFFFFF",
  "themeResourceVariables[2]": "Border@Light=#0F000000",
  "themeResourceVariables[3]": "Border@Dark=#19000000",
  "themeResourceVariables[4]": "ControlBorder@Light=#0F000000",
  "themeResourceVariables[5]": "ControlBorder@Dark=#15FFFFFF",
  "themeResourceVariables[6]": "Btn@Light=#90FFFFFF",
  "themeResourceVariables[7]": "Btn@Dark=#20FFFFFF",
  "themeResourceVariables[8]": "Accent1@Dark={ThemeResource SystemAccentColorLight2}",
  "themeResourceVariables[9]": "Accent1@Light={ThemeResource SystemAccentColorDark1}",
  "themeResourceVariables[10]": "Hover@Light=#65FFFFFF",
  "themeResourceVariables[11]": "Hover@Dark=#09FFFFFF",
  
  "controlStyles[0].target": "Microsoft.UI.Xaml.Controls.AnimatedIcon#BrightnessPlayer",
    "controlStyles[0].styles[0]": "Height=22",
    "controlStyles[0].styles[1]": "Width=22",
    "controlStyles[0].styles[2]": "//Control Center > Brightness Animated Icon",

  "controlStyles[1].target": "Grid > Microsoft.UI.Xaml.Controls.AnimatedIcon",
    "controlStyles[1].styles[0]": "Width=18",
    "controlStyles[1].styles[1]": "Height=18",
    "controlStyles[1].styles[2]": "//Control Center > Other Animated Icons in the Quick Actions",

  "controlStyles[2].target": "CalendarViewDayItem > Border",
    "controlStyles[2].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[2].styles[1]": "BorderThickness=2",
    "controlStyles[2].styles[2]": "//Calendar > Day Selector Border",

  "controlStyles[3].target": "Control > Border",
    "controlStyles[3].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[3].styles[1]": "//not sure",

  "controlStyles[4].target": "Grid#JumpListGrid > Border",
    "controlStyles[4].styles[0]": "Background:=$ThemeLayer",
    "controlStyles[4].styles[1]": "BorderBrush:=$ThemeOutBorder",
    "controlStyles[4].styles[2]": "BorderThickness=1",
    "controlStyles[4].styles[3]": "//Jump List > List Background and Border",

  "controlStyles[5].target": "ContentPresenter#PageContent > Grid > Border",
    "controlStyles[5].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[5].styles[1]": "//Page Content Border, not sure which one",

  "controlStyles[6].target": "Border#ItemOpaquePlating",
    "controlStyles[6].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[6].styles[1]": "Margin=6,3,6,3",
    "controlStyles[6].styles[2]": "BorderBrush:=$ThemeBorder",
    "controlStyles[6].styles[3]": "BorderThickness=1",
    "controlStyles[6].styles[4]": "//not sure",

  "controlStyles[7].target": "Border#ToastBackgroundBorder2",
    "controlStyles[7].styles[0]": "BorderThickness=1",
    "controlStyles[7].styles[1]": "BorderBrush:=$ThemeOutBorder",
    "controlStyles[7].styles[2]": "//Notification Toast > Border",

  "controlStyles[8].target": "Border#CalendarHeaderMinimizedOverlay",
    "controlStyles[8].styles[0]": "Margin=-11,-7,-11,-10",
    "controlStyles[8].styles[1]": "CornerRadius=$InnerRadius",
    "controlStyles[8].styles[2]": "BorderThickness=1",
    "controlStyles[8].styles[3]": "BorderBrush:=$ThemeBorder",
    "controlStyles[8].styles[4]": "//Calendar > Minimized Overlay",

  "controlStyles[9].target": "Grid#L1Grid > Border",
    "controlStyles[9].styles[0]": "Margin=6,0,6,0",
    "controlStyles[9].styles[1]": "CornerRadius=$InnerRadius",
    "controlStyles[9].styles[2]": "BorderBrush:=$ThemeBorder",
    "controlStyles[9].styles[3]": "BorderThickness=1",
    "controlStyles[9].styles[4]": "Height=$ControlCenterLayer",
    "controlStyles[9].styles[5]": "VerticalAlignment=Bottom",
    "controlStyles[9].styles[6]": "Background:=$ThemeOverlay",
    "controlStyles[9].styles[7]": "//Control Center > Content region Background",

  "controlStyles[10].target": "ContentPresenter#PageContent > Grid > Border",
    "controlStyles[10].styles[0]": "BorderBrush=Transparent",
    "controlStyles[10].styles[1]": "Background=Transparent",
    "controlStyles[10].styles[2]": "//Page Content Border",

  "controlStyles[11].target": "StackPanel > ContentPresenter > Border",
    "controlStyles[11].styles[0]": "BorderBrush=Transparent",
    "controlStyles[11].styles[1]": "//Control Center Splitting Border",

  "controlStyles[12].target": "Border#WADFeatureFooter",
    "controlStyles[12].styles[0]": "BorderBrush=Transparent",
    "controlStyles[12].styles[1]": "//Footer Border in Control Center or Calendar Grid",

  "controlStyles[13].target": "Border#JumpListRestyledAcrylic",
    "controlStyles[13].styles[0]": "Background:=$ThemeLayer",
    "controlStyles[13].styles[1]": "BorderThickness=1",
    "controlStyles[13].styles[2]": "BorderBrush:=$ThemeOutBorder",
    "controlStyles[13].styles[3]": "//Jump List > Background and Border",

  "controlStyles[14].target": "JumpViewUI.TaskbarJumpListFrame > Grid#JumpListGrid > Grid#SystemItemsContainer > Border",
    "controlStyles[14].styles[0]": "Background:=$ThemeOverlay",
    "controlStyles[14].styles[1]": "CornerRadius=$InnerRadius",
    "controlStyles[14].styles[2]": "Margin=2",
    "controlStyles[14].styles[3]": "BorderBrush:=$ThemeBorder",
    "controlStyles[14].styles[4]": "BorderThickness=1",
    "controlStyles[14].styles[5]": "//Jump List > System (App Actions) Items Container Background",

  "controlStyles[15].target": "JumpViewUI.SystemItemListViewItem > Grid#LayoutRoot@CommonStates > Border#BackgroundBorder",
    "controlStyles[15].styles[0]": "Width=220",
    "controlStyles[15].styles[1]": "Margin=-30,0,27,0",
    "controlStyles[15].styles[2]": "CornerRadius=$InnerRadius",
    "controlStyles[15].styles[3]": "//Jump List > System (App Actions) Items Background",

  "controlStyles[16].target": "ListView#MediaButtonsListView > ItemsPresenter > StackPanel > ListViewItem > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > Border",
    "controlStyles[16].styles[0]": "Background:=$ThemeBtn",
    "controlStyles[16].styles[1]": "CornerRadius=$InnerRadius",
    "controlStyles[16].styles[2]": "BorderBrush:=$ThemeControlBorder",
    "controlStyles[16].styles[3]": "BorderThickness=1",
    "controlStyles[16].styles[4]": "Margin=0",
    "controlStyles[16].styles[5]": "//Media Buttons Background (Previous and Next Buttons)",

  "controlStyles[17].target": "ListView#MediaButtonsListView > ItemsPresenter > StackPanel > ListViewItem[2] > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > Border",
    "controlStyles[17].styles[0]": "Background:=<SolidColorBrush Color=\"{ThemeResource Accent1}\" />",
    "controlStyles[17].styles[1]": "CornerRadius=$InnerRadius",
    "controlStyles[17].styles[2]": "BorderBrush:=$ThemeControlBorder",
    "controlStyles[17].styles[3]": "BorderThickness=1",
    "controlStyles[17].styles[4]": "Margin=25,0,25,0",
    "controlStyles[17].styles[5]": "//Media Buttons Background (Play/Pause Button)",

  "controlStyles[18].target": "ScrollViewer#CalendarControlScrollViewer > Border#Root",
    "controlStyles[18].styles[0]": "BorderBrush:=$ThemeBorder",
    "controlStyles[18].styles[1]": "BorderThickness=1",
    "controlStyles[18].styles[2]": "CornerRadius=$InnerRadius",
    "controlStyles[18].styles[3]": "Background=Transparent",
    "controlStyles[18].styles[4]": "////Calendar Grid > Calendar Background Layer Border",

  "controlStyles[19].target": "ActionCenter.FlexibleItemView > Grid#MainGrid > Grid#ItemGrid > Grid > Border#ItemOpaquePlating",
    "controlStyles[19].styles[0]": "Margin=5,-41,5,6",
    "controlStyles[19].styles[1]": "CornerRadius=$InnerRadius",
    "controlStyles[19].styles[2]": "BorderThickness=1",
    "controlStyles[19].styles[3]": "BorderBrush:=$ThemeBorder",
    "controlStyles[19].styles[4]": "Background:=$ThemeOverlay",
    "controlStyles[19].styles[5]": "//Notification (Main item) Background",

  "controlStyles[20].target": "CalendarView#CalendarControl > Border > Grid > Border",
    "controlStyles[20].styles[0]": "BorderBrush:=$ThemeBorder",
    "controlStyles[20].styles[1]": "Height=2",
    "controlStyles[20].style[2]": "Margin=0,-3,0,6",
    "controlStyles[20].styles[3]": "//Calendar > Border Between Month Labels - Day scroll",

  "controlStyles[21].target": "Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > Border[1]",
    "controlStyles[21].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[21].styles[1]": "//List view presenters background (not sure which one)",

  "controlStyles[22].target": "Button#SettingsButton",
    "controlStyles[22].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[22].styles[1]": "//Settings Button in Control Center",

  "controlStyles[23].target": "Button#DismissButton",
    "controlStyles[23].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[23].styles[1]": "//Dismiss button on notifications",

  "controlStyles[24].target": "Button#BackButton",
    "controlStyles[24].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[24].styles[1]": "Margin=1,0,10,0",
    "controlStyles[24].styles[2]": "//Back button in control Center subpages",

  "controlStyles[25].target": "Grid#DoNotDisturbSubtext > Button",
    "controlStyles[25].styles[0]": "Visibility=1",
    "controlStyles[25].styles[1]": "//Do Not Disturb > Link to notification Settings Button",

  "controlStyles[26].target": "Button#FooterButton[AutomationProperties.Name = Edit quick settings]",
    "controlStyles[26].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[26].styles[1]": "//Edit quick settings button in Control Center footer (older version of windows 11)",

  "controlStyles[27].target": "Button#FooterButton[AutomationProperties.Name = All settings]",
    "controlStyles[27].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[27].styles[1]": "//Settings Button in Control Center footer (older version of windows 11)",

  "controlStyles[28].target": "Button[AutomationProperties.AutomationId = Microsoft.QuickAction.Battery]",
    "controlStyles[28].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[28].styles[1]": "//Battery Button in Control Center footer",

  "controlStyles[29].target": "Button[CornerRadius=6]",
    "controlStyles[29].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[29].styles[1]": "//Changing buttons whose corner radius is 6 to my own radius",

  "controlStyles[30].target": "CalendarView#CalendarControl > Border > Grid > Grid > Button",
    "controlStyles[30].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[30].styles[1]": "//Calendar Grid > Month Scroll Buttons",

  "controlStyles[31].target": "Button#VerbButton",
    "controlStyles[31].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[31].styles[1]": "//Notification Bottom long Button",

  "controlStyles[32].target": "CalendarViewDayItem",
    "controlStyles[32].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[32].styles[1]": "Margin=1",
    "controlStyles[32].styles[2]": "//Calendar > Day selector item",

  "controlStyles[33].target": "Windows.UI.Xaml.Controls.Primitives.CalendarViewItem",
    "controlStyles[33].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[33].styles[1]": "//Calendar > Items Background Radius",

  "controlStyles[34].target": "ContentControl#PageHeaderContentControl",
    "controlStyles[34].styles[0]": "Width=64",
    "controlStyles[34].styles[1]": "//Control Center SubPage Header Width Limiter ( to fix an issue with switches being displaced )",

  "controlStyles[35].target": "ContentPresenter#PageHeader",
    "controlStyles[35].styles[0]": "Margin=5",
    "controlStyles[35].styles[1]": "CornerRadius=$InnerRadius",
    "controlStyles[35].styles[2]": "BorderThickness=1",
    "controlStyles[35].styles[3]": "BorderBrush:=$ThemeBorder",
    "controlStyles[35].styles[4]": "Background:=$ThemeOverlay",
    "controlStyles[35].styles[5]": "Padding=0,-2,0,2",
    "controlStyles[35].styles[6]": "Height=45",
    "controlStyles[35].styles[7]": "//Control Center SubPage Header Layer",

  "controlStyles[36].target": "ControlCenter.PaginatedToggleButton#ToggleButton > ContentPresenter#ContentPresenter",
    "controlStyles[36].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[36].styles[1]": "BorderThickness=1",
    "controlStyles[36].styles[2]": "BorderBrush:=$ThemeControlBorder",
    "controlStyles[36].styles[3]": "//Control Center Quick Actions Toggle Button",

  "controlStyles[37].target": "ControlCenter.PaginatedToggleButton#SplitL2Button > ContentPresenter#ContentPresenter",
    "controlStyles[37].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[37].styles[1]": "BorderThickness=1",
    "controlStyles[37].styles[2]": "BorderBrush:=$ThemeControlBorder",
    "controlStyles[37].styles[3]": "Margin=5,0,0,0",
    "controlStyles[37].styles[4]": "//Control Center Quick Actions Arrow Button (Navigate to subpage)",

  "controlStyles[38].target": "Grid#MediaTransportControlsRoot > ControlCenter.MediaTransportControlsButton#MediaTransportControlsButton > ContentPresenter",
    "controlStyles[38].styles[0]": "Background=Transparent",
    "controlStyles[38].styles[1]": "//Media Transport Controls Buttons background content presenter",

  "controlStyles[39].target": "Button#DateTextButtonWithClock > Grid > Border#Border > ContentPresenter#ContentPresenter",
    "controlStyles[39].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[39].styles[1]": "FontSize=14",
    "controlStyles[39].styles[2]": "//Calendar grid date text",

  "controlStyles[40].target": "Button#BackButton > ContentPresenter#ContentPresenter",
    "controlStyles[40].styles[0]": "Content:=<FontIcon FontSize=\"20\" FontFamily=\"Segoe Fluent Icons\" Glyph=\"&#xE973;\" />",
    "controlStyles[40].styles[1]": "Padding=-2,0,0,0",
    "controlStyles[40].styles[2]": "//Control Center > SubPage Back button icon",

  "controlStyles[41].target": "ListView#MediaButtonsListView > ItemsPresenter > StackPanel > ListViewItem > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > Button > ContentPresenter#ContentPresenter",
    "controlStyles[41].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[41].styles[1]": "//Media Control Buttons (Play/Pause) Background Radius",

  "controlStyles[42].target": "ListView#MediaButtonsListView > ItemsPresenter > StackPanel > ListViewItem > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > Windows.UI.Xaml.Controls.Primitives.RepeatButton > ContentPresenter#ContentPresenter",
    "controlStyles[42].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[42].styles[1]": "//Media Control Buttons (Previous, Repeat, Next) Background Radius",

  "controlStyles[43].target": "Control",
    "controlStyles[43].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[43].styles[1]": "//not sure",

  "controlStyles[44].target": "Windows.UI.Xaml.Controls.Primitives.CalendarPanel#YearViewPanel > Control",
    "controlStyles[44].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[44].styles[1]": "//Calendar Year View Panel controls background",

  "controlStyles[45].target": "ActionCenter.FlexibleItemView",
    "controlStyles[45].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[45].styles[1]": "//not sure",

  "controlStyles[46].target": "Grid#NotificationCenterGrid",
    "controlStyles[46].styles[0]": "CornerRadius=$OuterRadius",
    "controlStyles[46].styles[1]": "//Notification Center Main Grid",

  "controlStyles[47].target": "Grid#CalendarCenterGrid",
    "controlStyles[47].styles[0]": "CornerRadius=$OuterRadius",
    "controlStyles[47].styles[1]": "//Calendar Center Grid",

  "controlStyles[48].target": "Grid#MediaTransportControlsRegion",
    "controlStyles[48].styles[0]": "CornerRadius=$OuterRadius",
    "controlStyles[48].styles[1]": "//Media Controls Region Grid",

  "controlStyles[49].target": "Grid#ControlCenterRegion",
    "controlStyles[49].styles[0]": "CornerRadius=$OuterRadius",
    "controlStyles[49].styles[1]": "//Control Center Region Grid",

  "controlStyles[50].target": "Grid#JumpListGrid",
    "controlStyles[50].styles[0]": "CornerRadius=$OuterRadius",
    "controlStyles[50].styles[1]": "BorderThickness=1",
    "controlStyles[50].styles[2]": "BorderBrush:=$ThemeOutBorder",
    "controlStyles[50].styles[3]": "Width=250",
    "controlStyles[50].styles[4]": "//Jump List Grid",

  "controlStyles[51].target": "Grid#WeekDayNames",
    "controlStyles[51].styles[0]": "Margin=2,-5,2,-8",
    "controlStyles[51].styles[1]": "//Calendar Grid > Week Day Names Grid",

  "controlStyles[52].target": "Grid#FocusGrid",
    "controlStyles[52].styles[0]": "Background=Transparent",
    "controlStyles[52].styles[1]": "BorderBrush=Transparent",
    "controlStyles[52].styles[2]": "//Calendar Grid > Footer > Focus settings grid",

  "controlStyles[53].target": "Grid#DoNotDisturbSubtext",
    "controlStyles[53].styles[0]": "Margin=0,-53,0,0",
    "controlStyles[53].styles[1]": "Canvas.ZIndex=-1",
    "controlStyles[53].styles[2]": "BorderThickness=0,0,0,1",
    "controlStyles[53].styles[3]": "BorderBrush:=$ThemeControlBorder",
    "controlStyles[53].styles[4]": "Background:=$ThemeOverlay",
    "controlStyles[53].styles[5]": "Padding=0,63,0,6",
    "controlStyles[53].styles[6]": "CornerRadius=$OuterRadius,$OuterRadius,12,12",
    "controlStyles[53].styles[7]": "//Notifications > Do Not Disturb Subtext Background",

  "controlStyles[54].target": "ControlCenter.PaginatedGridView > Grid",
    "controlStyles[54].styles[0]": "BorderBrush=Transparent",
    "controlStyles[54].styles[1]": "//Separator borders in control center subpages",

  "controlStyles[55].target": "Grid#L1Grid > Grid",
    "controlStyles[55].styles[0]": "BorderBrush=Transparent",
    "controlStyles[55].styles[1]": "//Control Center Main Grid > Other Separator Borders",

  "controlStyles[56].target": "Grid#MediaTransportControlsRoot",
    "controlStyles[56].styles[0]": "CornerRadius=$OuterRadius",
    "controlStyles[56].styles[1]": "BorderThickness=0",
    "controlStyles[56].styles[2]": "Background=Transparent",
    "controlStyles[56].styles[3]": "//Media Controls Root Grid > Inner Light layer",

  "controlStyles[57].target": "Grid#ThumbnailImage",
    "controlStyles[57].styles[0]": "Height=105",
    "controlStyles[57].styles[1]": "Width=105",
    "controlStyles[57].styles[2]": "Margin=0,0,-8,0",
    "controlStyles[57].styles[3]": "CornerRadius=$InnerRadius",
    "controlStyles[57].styles[4]": "BorderThickness=0",
    "controlStyles[57].styles[5]": "Grid.Column=2",
    "controlStyles[57].styles[6]": "//Media Controls > Playing Item Thumbnail Image",

  "controlStyles[58].target": "Grid#NotificationCenterTopBanner",
    "controlStyles[58].styles[0]": "Margin=5,5,5,0",
    "controlStyles[58].styles[1]": "CornerRadius=$InnerRadius",
    "controlStyles[58].styles[2]": "BorderThickness=1",
    "controlStyles[58].styles[3]": "BorderBrush:=$ThemeBorder",
    "controlStyles[58].styles[4]": "Background:=$ThemeOverlay",
    "controlStyles[58].styles[5]": "Padding=10,-2,8,2",
    "controlStyles[58].styles[6]": "Height=38",
    "controlStyles[58].styles[7]": "//Notifications > Top Grid > Layer Banner Background",

  "controlStyles[59].target": "ScrollViewer#CalendarControlScrollViewer > Border#Root > Grid",
    "controlStyles[59].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[59].styles[1]": "//Calendar Grid > Calendar Background Layer > Inner Grid",

  "controlStyles[60].target": "ActionCenter.FlexibleItemView > Grid#MainGrid > Grid#ItemGrid > Grid#StandardHeroContainer",
    "controlStyles[60].styles[0]": "Margin=5,-3,5,0",
    "controlStyles[60].styles[1]": "Padding=8,0,8,0",
    "controlStyles[60].styles[2]": "MaxHeight=160",
    "controlStyles[60].styles[3]": "//Notification in Notification grid > screenshot or attatched image container",

  "controlStyles[61].target": "ActionCenter.GroupView > Grid#GroupGrid",
    "controlStyles[61].styles[0]": "Margin=5,5,5,-3",
    "controlStyles[61].styles[1]": "Background=Transparent",
    "controlStyles[61].styles[2]": "Padding=0",
    "controlStyles[61].styles[3]": "BorderThickness=0,0,0,2",
    "controlStyles[61].styles[4]": "BorderBrush:=$ThemeBorder",
    "controlStyles[61].styles[5]": "//Notification in Notification grid > App Name Group Header",

  "controlStyles[62].target": "CalendarView#CalendarControl > Border > Grid > Grid[1]",
    "controlStyles[62].styles[0]": "Height=46",
    "controlStyles[62].styles[1]": "Margin=-4,-5,-4,0",
    "controlStyles[62].styles[2]": "Padding=0,-2,0,-2",
    "controlStyles[62].styles[3]": "//Calendar Grid > Calendar Month Name Contrainer Grid",

  "controlStyles[63].target": "Grid#MediaTransportControlsRoot > Grid > Image#IconImage",
    "controlStyles[63].styles[0]": "Opacity=0.8",
    "controlStyles[63].styles[1]": "Margin=-4,0,0,0",
    "controlStyles[63].styles[2]": "//Media Controls > Player or player source icon image",

  "controlStyles[64].target": "ListView#MediaButtonsListView",
    "controlStyles[64].styles[0]": "Margin=-62,-60,62,-20",
    "controlStyles[64].styles[1]": "//Media Controls > Media Buttons List View Grid",

  "controlStyles[65].target": "ListViewItem",
    "controlStyles[65].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[65].styles[1]": "//An Attempt to make all List view items obey radius",

  "controlStyles[66].target": "NetworkUX.View.SettingsListViewItem > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root",
    "controlStyles[66].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[66].styles[1]": "//Control Center > Wifi Subpage > List view Items > Attempt to make them obey radius",

  "controlStyles[67].target": "Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root",
    "controlStyles[67].styles[0]": "PointerOverBackground:=$ThemeHover",
    "controlStyles[67].styles[1]": "PressedBackground:=$ThemeBtn",
    "controlStyles[67].styles[2]": "SelectedBackground:=$ThemeHover",
    "controlStyles[67].styles[3]": "SelectedDisabledBackground:=$ThemeHover",
    "controlStyles[67].styles[4]": "SelectedPointerOverBackground:=$ThemeHover",
    "controlStyles[67].styles[5]": "SelectedPressedBackground:=$ThemeBtn",
    "controlStyles[67].styles[6]": "PlaceholderBackground:=$ThemeHover",
    "controlStyles[67].styles[7]": "//An Attempt to make subpage list view items to use theme colors for background in different states",

  "controlStyles[68].target": "MenuFlyoutPresenter",
    "controlStyles[68].styles[0]": "Background:=$ThemeLayer",
    "controlStyles[68].styles[1]": "CornerRadius=$OuterRadius",
    "controlStyles[68].styles[2]": "BorderThickness=1",
    "controlStyles[68].styles[3]": "BorderBrush:=$ThemeOutBorder",
    "controlStyles[68].styles[4]": "//Menu Flyouts > Background",

  "controlStyles[69].target": "ActionCenter.NotificationContentView#NotificationContentView",
    "controlStyles[69].styles[0]": "Margin=5,3,5,1",
    "controlStyles[69].styles[1]": "//Notification Center > Notification > Main container for notification content, excluding header and buttons",

  "controlStyles[70].target": "ControlCenter.PaginatedToggleButton#ToggleButton",
    "controlStyles[70].styles[0]": "BorderBrush:=$ThemeControlBorder",
    "controlStyles[70].styles[1]": "BorderThickness=1",
    "controlStyles[70].styles[2]": "CornerRadius=$InnerRadius",
    "controlStyles[70].styles[3]": "FocusVisualPrimaryThickness=0",
    "controlStyles[70].styles[4]": "FocusVisualSecondaryThickness=0",
    "controlStyles[70].styles[5]": "//An attempt to remove Focus white box and apply border and radius to Control Center Quick Actions Toggle Button",

  "controlStyles[71].target": "ControlCenter.PaginatedToggleButton#SplitL2Button",
    "controlStyles[71].styles[0]": "BorderBrush:=$ThemeControlBorder",
    "controlStyles[71].styles[1]": "BorderThickness=1",
    "controlStyles[71].styles[2]": "//An attempt to remove Focus white box and apply border and radius to Control Center Quick Actions Arrow (Navigate) Button",

  "controlStyles[72].target": "Rectangle#HorizontalTrackRect",
    "controlStyles[72].styles[0]": "Height=6",
    "controlStyles[72].styles[1]": "RadiusX=3",
    "controlStyles[72].styles[2]": "RadiusY=3",
    "controlStyles[72].styles[3]": "Opacity=0.5",
    "controlStyles[72].styles[4]": "//Control Center > Volume and Brightness Sliders > Grey Track Rectangle",

  "controlStyles[73].target": "Rectangle#HorizontalDecreaseRect",
    "controlStyles[73].styles[0]": "Height=6",
    "controlStyles[73].styles[1]": "RadiusX=3",
    "controlStyles[73].styles[2]": "RadiusY=3",
    "controlStyles[73].styles[3]": "//Control Center > Volume and Brightness Sliders > Adjusting Rectangle",

  "controlStyles[74].target": "ScrollViewer#CalendarControlScrollViewer",
    "controlStyles[74].styles[0]": "Margin=-11,10,-11,-12",
    "controlStyles[74].styles[1]": "CornerRadius=$InnerRadius",
    "controlStyles[74].styles[2]": "//Calendar Grid > Calendar ScrollViewer Layer",

  "controlStyles[75].target": "ScrollViewer#ListContent",
    "controlStyles[75].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[75].styles[1]": "//Another Attempt to make scroll viewer grid to obey radius",

  "controlStyles[76].target": "Grid > ScrollViewer#ListContent",
    "controlStyles[76].styles[0]": "Background=Transparent",
    "controlStyles[76].styles[1]": "//Attempt to make scroll viewer grid whitish overlay (for those having grid > scrollviewer structure)",

  "controlStyles[77].target": "StackPanel#CalendarHeader",
    "controlStyles[77].styles[0]": "Margin=6,-5,0,0",
    "controlStyles[77].styles[1]": "//Calendar Grid > Current Time and date displacement",

  "controlStyles[78].target": "StackPanel#PrimaryAndSecondaryTextContainer",
    "controlStyles[78].styles[0]": "VerticalAlignment=Top",
    "controlStyles[78].styles[1]": "Grid.Column=0",
    "controlStyles[78].styles[2]": "Margin=5,0,0,0",
    "controlStyles[78].styles[3]": "//Media Controls > Playing Item Text Container",

  "controlStyles[79].target": "Grid#DoNotDisturbSubtext > TextBlock[3]",
    "controlStyles[79].styles[0]": "Visibility=1",
    "controlStyles[79].styles[1]": "//Do Not Disturb Subtext > 2nd row TextBlock",

  "controlStyles[80].target": "Grid#DoNotDisturbSubtext > TextBlock[2]",
    "controlStyles[80].styles[0]": "Foreground:=<SolidColorBrush Color=\"{ThemeResource TextFillColorSecondary}\" />",
    "controlStyles[80].styles[1]": "FontSize=15",
    "controlStyles[80].styles[2]": "HorizontalAlignment=Center",
    "controlStyles[80].styles[3]": "FontFamily=$ThFnt",
    "controlStyles[80].styles[4]": "FontWeight=$ThFntWt",
    "controlStyles[80].styles[5]": "//Do Not Disturb Subtext > Main 'Do not Disturb is on' TextBlock ",

  "controlStyles[81].target": "Grid#DoNotDisturbSubtext > TextBlock[1]",
    "controlStyles[81].styles[0]": "Visibility=1",
    "controlStyles[81].styles[1]": "//Do Not Disturb Subtext > Do not disturb Icon glyph TextBlock",

  "controlStyles[82].target": "MenuFlyoutItem > Grid > TextBlock",
    "controlStyles[82].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[82].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[82].styles[2]": "//Menu Flyouts > Items > TextBlock (Labels)",

  "controlStyles[83].target": "StackPanel#PrimaryAndSecondaryTextContainer > TextBlock#Title",
    "controlStyles[83].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[83].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[83].styles[2]": "//Media Controls > Playing Item Title TextBlock (some windows 11 versions have different name for this TextBlock)",

  "controlStyles[84].target": "StackPanel#PrimaryAndSecondaryTextContainer > TextBlock#Subtitle",
    "controlStyles[84].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[84].styles[1]": "//Media Controls > Playing Item Subtitle TextBlock (some windows 11 versions have different name for this TextBlock)",

  "controlStyles[85].target": "TextBlock#StatusText",
    "controlStyles[85].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[85].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[85].styles[2]": "FontSize=12.5",
    "controlStyles[85].styles[3]": "//Control Center > Wifi Subpage > COnnected/Disconnected Status TextBlock",

  "controlStyles[86].target": "TextBlock#TitleText",
    "controlStyles[86].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[86].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[86].styles[2]": "FontSize=12.5",
    "controlStyles[86].styles[3]": "//might be some title TextBlock, not sure",

  "controlStyles[87].target": "ToolTip > ContentPresenter#LayoutRoot > TextBlock",
    "controlStyles[87].styles[0]": "FontWeight=$ThFntWt",
    "controlStyles[87].styles[1]": "FontFamily=$ThFnt",
    "controlStyles[87].styles[2]": "FontSize=13",
    "controlStyles[87].styles[3]": "//Tooltips (Hover Flyout Bubbles) > TextBlock (Labels)",

  "controlStyles[88].target": "Grid#WeekDayNames > TextBlock",
    "controlStyles[88].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[88].styles[1]": "FontWeight=$ThHdnWt",
    "controlStyles[88].styles[2]": "FontSize=12",
    "controlStyles[88].styles[3]": "//Calendar Grid > Week Day Names TextBlocks",

  "controlStyles[89].target": "CalendarViewDayItem > TextBlock",
    "controlStyles[89].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[89].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[89].styles[2]": "//Calendar > Day > TextBlock",

  "controlStyles[90].target": "Button#HeaderButton > ContentPresenter#Text > TextBlock",
    "controlStyles[90].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[90].styles[1]": "FontWeight=$ThHdnWt",
    "controlStyles[90].styles[2]": "FontSize=15",
    "controlStyles[90].styles[3]": "//not sure which header buttom this is",

  "controlStyles[91].target": "TextBlock#ClockWithMeridian",
    "controlStyles[91].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[91].styles[1]": "FontWeight=$ThHdnWt",
    "controlStyles[91].styles[2]": "//Calendar grid > Another attempt to change clock TextBlock font (newer windows 11 versions)",

  "controlStyles[92].target": "TextBlock#DurationTextBlock",
    "controlStyles[92].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[92].styles[1]": "//Calendar grid > Footer > Focus duration TextBlock",

  "controlStyles[93].target": "TextBlock#NotificationsTextBlock",
    "controlStyles[93].styles[0]": "FontWeight=$ThHdnWt",
    "controlStyles[93].styles[1]": "FontFamily=$ThFnt",
    "controlStyles[93].styles[2]": "//Notification Center > Main Title 'Notifications' TextBlock",

  "controlStyles[94].target": "TextBlock#StartButtonText",
    "controlStyles[94].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[94].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[94].styles[2]": "//Calendar Grid > Footer > start Focus session TextBlock",

  "controlStyles[95].target": "TextBlock#NoNotificationsTextBlock",
    "controlStyles[95].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[95].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[95].styles[2]": "FontSize=13",
    "controlStyles[95].styles[3]": "//Notification Center > No new Notifications text ",

  "controlStyles[96].target": "TextBlock[AutomationProperties.AutomationId=TextTopologyTileDescription]",
    "controlStyles[96].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[96].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[96].styles[2]": "//Control Center > Quick Actions > ControlLabels and status TextBlock",

  "controlStyles[97].target": "TextBlock#PageTitleText",
    "controlStyles[97].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[97].styles[1]": "FontWeight=$ThHdnWt",
    "controlStyles[97].styles[2]": "FontSize=15",
    "controlStyles[97].styles[3]": "//Control Center > SubPage Main Title TextBlock",

  "controlStyles[98].target": "TextBlock#PageTitle",
    "controlStyles[98].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[98].styles[1]": "FontWeight=$ThHdnWt",
    "controlStyles[98].styles[2]": "FontSize=15",
    "controlStyles[98].styles[3]": "//Control Center > SubPage Main Title TextBlock (some have different name)",

  "controlStyles[99].target": "Button[AutomationProperties.AutomationId=Microsoft.QuickAction.Battery] > ContentPresenter#ContentPresenter > StackPanel > TextBlock",
    "controlStyles[99].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[99].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[99].styles[2]": "FontSize=12.5",
    "controlStyles[99].styles[3]": "//Control Center > Footer > Battery Button > Percentage TextBlock (Newer Windows 11 versions)",

  "controlStyles[100].target": "Grid#GroupTitleGrid > TextBlock#Title",
    "controlStyles[100].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[100].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[100].styles[2]": "FontSize=13.5",
    "controlStyles[100].styles[3]": "//Control Center > SubPage > groups titles",

  "controlStyles[101].target": "StackPanel#TextContentPanel > TextBlock",
    "controlStyles[101].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[101].styles[1]": "//Notifications > Content TextBlocks",

  "controlStyles[102].target": "TextBlock#TimeStamp",
    "controlStyles[102].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[102].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[102].styles[2]": "//Notification Center > Notification > Timestamp TextBlock",

  "controlStyles[103].target": "TextBlock[AutomationProperties.AutomationId=TextBluetoothDisabled]",
    "controlStyles[103].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[103].styles[1]": "//Control Center > Bluetooth Disabled TextBlock in Bluetooth SubPage",

  "controlStyles[104].target": "TextBlock[AutomationProperties.AutomationId=HeaderBluetoothDisabled]",
    "controlStyles[104].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[104].styles[1]": "//Control Center > Bluetooth Disabled Header TextBlock in Bluetooth SubPage",

  "controlStyles[105].target": "TextBlock[AutomationProperties.AutomationId=YourDevices]",
    "controlStyles[105].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[105].styles[1]": "//Control Center > Bluetooth SubPage > 'Your devices' TextBlock",

  "controlStyles[106].target": "NetworkUX.View.EntityListItemControl#EntityListItemControl > Grid > TextBlock",
    "controlStyles[106].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[106].styles[1]": "//Control Center > Wifi SubPage > List Item TextBlocks",

  "controlStyles[107].target": "ActionCenter.ClearAllButton#ClearAllButtonControl > Button#ClearAll > ContentPresenter#ContentPresenter@CommonStates > TextBlock",
    "controlStyles[107].styles[0]": "Foreground@PointerOver:=<SolidColorBrush Color=\"Red\" Opacity=\"0.7\"/>",
    "controlStyles[107].styles[1]": "Foreground@Pressed:=<SolidColorBrush Color=\"Red\" Opacity=\"0.7\"/>",
    "controlStyles[107].styles[2]": "FontFamily=$ThFnt",
    "controlStyles[107].styles[3]": "FontWeight=$ThFntWt",
    "controlStyles[107].styles[4]": "//Notification Center > Clear All Button > TextBlock",

  "controlStyles[108].target": "StackPanel#OffUxPanel > TextBlock",
    "controlStyles[108].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[108].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[108].styles[2]": "//not sure",

  "controlStyles[109].target": "ContentControl#QuickActionContentControl > ContentPresenter > Grid > StackPanel > TextBlock",
    "controlStyles[109].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[109].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[109].styles[2]": "//Control Center > Quick Actions > TextBlock in Quick Action Button (some of them have different structure so this is for those)",

  "controlStyles[110].target": "NetworkUX.View.EntityListItemControl#EntityListItemControl > Grid > StackPanel > TextBlock",
    "controlStyles[110].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[110].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[110].styles[2]": "//Control Center > Wifi SubPage > List Item TextBlocks (some TextBlocks have different structure so this is for those)",

  "controlStyles[111].target": "Windows.UI.Xaml.Controls.Primitives.RepeatButton > ContentPresenter#ContentPresenter > TextBlock",
    "controlStyles[111].styles[0]": "FontFamily=Segoe Fluent Icons",
    "controlStyles[111].styles[1]": "FontSize=15",
    "controlStyles[111].styles[2]": "//Media Control Grid > Media Control Buttons > Repeat, Next and Previous buttons icons",

  "controlStyles[112].target": "Button#PlayPauseButton > ContentPresenter#ContentPresenter > TextBlock",
    "controlStyles[112].styles[0]": "FontFamily=Segoe Fluent Icons",
    "controlStyles[112].styles[1]": "FontSize=16",
    "controlStyles[112].styles[2]": "Foreground:=<SolidColorBrush Color=\"{ThemeResource TextFillColorInverse}\"/>",
    "controlStyles[112].styles[3]": "//Media Control Grid > Media Control Buttons > Play/Pause button icon",

  "controlStyles[113].target": "StackPanel#PrimaryAndSecondaryTextContainer > TextBlock#TitleText",
    "controlStyles[113].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[113].styles[1]": "FontSize=16.5",
    "controlStyles[113].styles[2]": "FontWeight=$ThHdnWt",
    "controlStyles[113].styles[3]": "Margin=0,0,8,0",
    "controlStyles[113].styles[4]": "Padding=0,0,0,10",
    "controlStyles[113].styles[5]": "//Media Control Grid > Playing Item Title TextBlock",

  "controlStyles[114].target": "StackPanel#PrimaryAndSecondaryTextContainer > TextBlock#SubtitleText",
    "controlStyles[114].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[114].styles[1]": "FontSize=13",
    "controlStyles[114].styles[2]": "Foreground:=<SolidColorBrush Color=\"{ThemeResource TextFillColorSecondary}\" />",
    "controlStyles[114].styles[3]": "Margin=0,0,0,-5",
    "controlStyles[114].styles[4]": "//Media Control Grid > Playing Item Subtitle TextBlock",

  "controlStyles[115].target": "TextBlock#AppNameText",
    "controlStyles[115].styles[0]": "FontSize=12",
    "controlStyles[115].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[115].styles[2]": "FontFamily=$ThFnt",
    "controlStyles[115].styles[3]": "Foreground:=<SolidColorBrush Color=\"{ThemeResource TextFillColorSecondary}\" />",
    "controlStyles[115].styles[4]": "//Media Control Grid > Playing source App Name TextBlock",

  "controlStyles[116].target": "JumpViewUI.SystemItemControl > Grid > TextBlock",
    "controlStyles[116].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[116].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[116].styles[2]": "//JumpList Items > TextBlock",

  "controlStyles[117].target": "JumpViewUI.JumpListItemControl > Grid > Grid > TextBlock",
    "controlStyles[117].styles[0]": "FontWeight=$ThFntWt",
    "controlStyles[117].styles[1]": "FontFamily=$ThFnt",
    "controlStyles[117].styles[2]": "//JumpList Items > TextBlock (for those TextBlocks having different structure)",

  "controlStyles[118].target": "TextBlock[AutomationProperties.AutomationId=TextDeviceListEmpty]",
    "controlStyles[118].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[118].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[118].styles[2]": "//Control Center > Bluetooth/Cast SubPage > 'No devices found' TextBlock",

  "controlStyles[119].target": "TextBlock[AutomationProperties.AutomationId=AvailableDisplaysTextBlock]",
    "controlStyles[119].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[119].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[119].styles[2]": "//Control Center > Cast SubPage > Available Displays TextBlock",

  "controlStyles[120].target": "Grid#RootGrid > ContentPresenter#Content > TextBlock",
    "controlStyles[120].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[120].styles[1]": "//Attempt to apply font to more TextBlocks with this structure",

  "controlStyles[121].target": "TextBlock#MixerGroupTitle",
    "controlStyles[121].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[121].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[121].styles[2]": "FontSize=15",
    "controlStyles[121].styles[3]": "//Control Center > Volume Mixer Subpage > App Volume Mixer Group Title TextBlock",

  "controlStyles[122].target": "TextBlock#SpatialGroupTitle",
    "controlStyles[122].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[122].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[122].styles[2]": "FontSize=15",
    "controlStyles[122].styles[3]": "//Control Center > Volume Mixer Subpage > Spatial Audio Group Title TextBlock",

  "controlStyles[123].target": "TextBlock#OutputGroupTitle",
    "controlStyles[123].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[123].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[123].styles[2]": "FontSize=15",
    "controlStyles[123].styles[3]": "//Control Center > Volume Mixer Subpage > Output Devices Group Title TextBlock",

  "controlStyles[124].target": "Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > Grid > TextBlock#TitleText",
    "controlStyles[124].styles[0]": "FontSize=13.5",
    "controlStyles[124].styles[1]": "Margin=0,1,0,-1",
    "controlStyles[124].styles[2]": "//Another attempt to apply fontsize to a Title TextBlock",

  "controlStyles[125].target": "ContentPresenter#PageContent > Grid > ScrollViewer#ListContent > Border#Root > Grid > ScrollContentPresenter#ScrollContentPresenter > ItemsControl > ItemsPresenter > StackPanel > ContentPresenter > StackPanel > TextBlock",
    "controlStyles[125].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[125].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[125].styles[2]": "FontSize=15",
    "controlStyles[125].styles[3]": "//Some TextBlock that needed a larger target string for styles to apply",

  "controlStyles[126].target": "Button#DisconnectButton > ContentPresenter#ContentPresenter > TextBlock",
    "controlStyles[126].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[126].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[126].styles[2]": "//Control Center > Bluetooth/Wifi SubPage > Disconnect Button > TextBlock",

  "controlStyles[127].target": "StackPanel > StackPanel > CheckBox > Grid#RootGrid > ContentPresenter#ContentPresenter > TextBlock",
    "controlStyles[127].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[127].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[127].styles[2]": "//not sure",

  "controlStyles[128].target": "StackPanel > StackPanel > Button > ContentPresenter#ContentPresenter > TextBlock",
    "controlStyles[128].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[128].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[128].styles[2]": "//An attemp to apply Text styles to more buttons of similar structure",

  "controlStyles[129].target": "TextBlock#ProjectInterfaceDeviceTileTextDeviceStatus",
    "controlStyles[129].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[129].styles[1]": "//Control Center > Casting SubPage > Device Tile > Device name",

  "controlStyles[130].target": "TextBlock#ProjectInterfaceDeviceTileTextDeviceName",
    "controlStyles[130].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[130].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[130].styles[2]": "//Control Center > Casting SubPage > Device Tile > Device status",

  "controlStyles[131].target": "ControlCenter.PaginatedToggleButton#SplitL2Button > ContentPresenter#ContentPresenter > FontIcon > Grid > TextBlock",
    "controlStyles[131].styles[0]": "FontWeight=Normal",
    "controlStyles[131].styles[1]": "FontSize=17",
    "controlStyles[131].styles[2]": "//Control Center > Quick Actions > Arrow (Navigate) Button > Icon TextBlock",

  "controlStyles[132].target": "ControlCenter.PaginatedToggleButton#ToggleButton > ContentPresenter#ContentPresenter > Grid > FontIcon > Grid > TextBlock",
    "controlStyles[132].styles[0]": "FontSize=16",
    "controlStyles[132].styles[1]": "Padding=6,0,0,0",
    "controlStyles[132].styles[2]": "Margin=0,0,-6,0",
    "controlStyles[132].styles[3]": "//Control Center > Quick Actions > Toggle Button > Icon TextBlock",

  "controlStyles[133].target": "Button#DateTextButtonWithClockOld > Grid > Border#Border > ContentPresenter#ContentPresenter > TextBlock",
    "controlStyles[133].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[133].styles[1]": "Margin=-3,0,0,0",
    "controlStyles[133].styles[2]": "//Calendar Grid > Header > Date TextBlock (older windows 11 versions)",

  "controlStyles[134].target": "TextBlock#ClockWithMeridianOld",
    "controlStyles[134].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[134].styles[1]": "//Calendar Grid > Header > Clock TextBlock (older windows 11 versions)",

  "controlStyles[135].target": "Button#VolumeL2Button > ContentPresenter#ContentPresenter > StackPanel > FontIcon[2] > Grid > TextBlock",
    "controlStyles[135].styles[0]": "Visibility=1",
    "controlStyles[135].styles[1]": "//Control Center > Volume Slider > Button beside slider > Arrow Icon (Navigate to Volume Mixer Subpage)",

  "controlStyles[136].target": "Button#VolumeL2Button > ContentPresenter#ContentPresenter > StackPanel > FontIcon[1] > Grid > TextBlock",
    "controlStyles[136].styles[0]": "Text=",
    "controlStyles[136].styles[1]": "//Control Center > Volume Slider > Button beside slider > Main Icon (Navigate to Volume Mixer Subpage)",

  "controlStyles[137].target": "TextBlock#StopButtonText",
    "controlStyles[137].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[137].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[137].styles[2]": "//Calendar Grid > Footer > Focus Timer Stop Button Text",

  "controlStyles[138].target": "StackPanel#MainContent > TextBlock#Title2",
    "controlStyles[138].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[138].styles[1]": "FontWeight=$ThHdnWt",
    "controlStyles[138].styles[2]": "//Notification > Title Topic TextBlock",

  "controlStyles[139].target": "StackPanel#MainContent > TextBlock#MessageText",
    "controlStyles[139].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[139].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[139].styles[2]": "//Notification > Content TextBlock",

  "controlStyles[140].target": "TextBlock#Attribution",
    "controlStyles[140].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[140].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[140].styles[2]": "//Notification > Source/User/Attribute TextBlock",

  "controlStyles[141].target": "TextBlock#SubgroupTitleText",
    "controlStyles[141].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[141].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[141].styles[2]": "//Notification > sub group Title TextBlock",

  "controlStyles[142].target": "TextBlock#SenderName",
    "controlStyles[142].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[142].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[142].styles[2]": "//Notification > Sender Name TextBlock",

  "controlStyles[143].target": "TextBlock#VerbText",
    "controlStyles[143].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[143].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[143].styles[2]": "//Notification > Long Button (Actions) TextBlock",

  "controlStyles[144].target": "StackPanel#MainContent > TextBlock#MessageText2",
    "controlStyles[144].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[144].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[144].styles[2]": "//Notification > Additional Content TextBlock",

  "controlStyles[145].target": "StackPanel#TextContentPanel > TextBlock",
    "controlStyles[145].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[145].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[145].styles[2]": "//Notification > Text Content Panel TextBlock",

  "controlStyles[146].target": "Button#DismissButton > Grid@CommonStates > Border#Border > ContentPresenter#ContentPresenter > TextBlock",
    "controlStyles[146].styles[0]": "Foreground@PointerOver:=<SolidColorBrush Color=\"Red\" Opacity=\"0.7\"/>",
    "controlStyles[146].styles[1]": "FontWeight=$ThHdnWt",
    "controlStyles[146].styles[2]": "Foreground@Pressed:=<SolidColorBrush Color=\"Red\" Opacity=\"0.7\"/>",
    "controlStyles[146].styles[3]": "//Notification Center > Notification > Dismiss Notification Button > TextBlock",

  "controlStyles[147].target": "Button#SettingsButton > Grid@CommonStates > Border#Border > ContentPresenter#ContentPresenter > TextBlock",
    "controlStyles[147].styles[0]": "Foreground@PointerOver:=<SolidColorBrush Color=\"{ThemeResource Accent1}\" />",
    "controlStyles[147].styles[1]": "FontWeight=$ThHdnWt",
    "controlStyles[147].styles[2]": "Foreground@Pressed:=<SolidColorBrush Color=\"{ThemeResource Accent1}\" />",
    "controlStyles[147].styles[3]": "//Notification Center > Notification > Settings Button > TextBlock",

  "controlStyles[148].target": "Grid#FocusControlGrid > Button#StopButton > ContentPresenter#ContentPresenter@CommonStates > StackPanel > FontIcon > Grid > TextBlock",
    "controlStyles[148].styles[0]": "Foreground@PointerOver:=<SolidColorBrush Color=\"Red\" Opacity=\"0.7\"/>",
    "controlStyles[148].styles[1]": "Foreground@Pressed:=<SolidColorBrush Color=\"Red\" Opacity=\"0.7\"/>",
    "controlStyles[148].styles[2]": "//Calendar Grid > Footer > Focus Timer Stop Button > Icon TextBlock",

  "controlStyles[149].target": "Grid#FocusControlGrid > Button#StartButton > ContentPresenter#ContentPresenter@CommonStates > StackPanel > FontIcon > Grid > TextBlock",
    "controlStyles[149].styles[0]": "Foreground@PointerOver:=<SolidColorBrush Color=\"{ThemeResource Accent1}\" />",
    "controlStyles[149].styles[1]": "Foreground@Pressed:=<SolidColorBrush Color=\"{ThemeResource Accent1}\" />",
    "controlStyles[149].styles[2]": "//Calendar Grid > Footer > Focus Timer Start Button > Icon TextBlock",

  "controlStyles[150].target": "Grid#FocusStateGrid > Grid#FocusTimeSelector > Button#IncreaseTimeButton > ContentPresenter#ContentPresenter@CommonStates > FontIcon > Grid > TextBlock",
    "controlStyles[150].styles[0]": "Foreground@PointerOver:=<SolidColorBrush Color=\"Green\" Opacity=\"0.7\"/>",
    "controlStyles[150].styles[1]": "Foreground@Pressed:=<SolidColorBrush Color=\"Green\" Opacity=\"0.7\"/>",
    "controlStyles[150].styles[2]": "//Calendar Grid > Footer > Focus Timer Increase (Plus) Button > Icon TextBlock",

  "controlStyles[151].target": "Grid#FocusStateGrid > Grid#FocusTimeSelector > Button#DecreaseTimeButton > ContentPresenter#ContentPresenter@CommonStates > FontIcon > Grid > TextBlock",
    "controlStyles[151].styles[0]": "Foreground@PointerOver:=<SolidColorBrush Color=\"Red\" Opacity=\"0.7\"/>",
    "controlStyles[151].styles[1]": "Foreground@Pressed:=<SolidColorBrush Color=\"Red\" Opacity=\"0.7\"/>",
    "controlStyles[151].styles[2]": "//Calendar Grid > Footer > Focus Timer Decrease (Minus) Button > Icon TextBlock",

  "controlStyles[152].target": "TextBlock#FocusingText",
    "controlStyles[152].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[152].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[152].styles[2]": "//Calendar Grid > Footer > Focus Mode Active TextBlock",

  "controlStyles[153].target": "Windows.UI.Xaml.Controls.Primitives.CalendarPanel#YearViewPanel > Windows.UI.Xaml.Controls.Primitives.CalendarViewItem > TextBlock",
    "controlStyles[153].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[153].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[153].styles[2]": "//Calendar > Click On month > Year Panel > Year TextBlock",

  "controlStyles[154].target": "NetworkUX.View.CFEWiFiPassKey > StackPanel > TextBlock#WiFiPassKeyLabel",
    "controlStyles[154].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[154].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[154].styles[2]": "//Wifi Subpage > Connect to Network > Password request label",

  "controlStyles[155].target": "NetworkUX.View.CFEConnectionCompletion > StackPanel > TextBlock#ErrorMessageLabel",
    "controlStyles[155].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[155].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[155].styles[2]": "//Wifi Subpage > Connect to Network > Error Connecting label",

  "controlStyles[156].target": "NetworkUX.View.CFEConnectionCompletion > StackPanel > Button > ContentPresenter#ContentPresenter > TextBlock",
    "controlStyles[156].styles[0]": "FontFamily=$ThFnt",
    "controlStyles[156].styles[1]": "FontWeight=$ThFntWt",
    "controlStyles[156].styles[2]": "//Wifi Subpage > Network List Item > Connection/Disconnection/Error Buttons > TextBlock",

  "controlStyles[157].target": "ToolTip",
    "controlStyles[157].styles[0]": "CornerRadius=$OuterRadius",
    "controlStyles[157].styles[1]": "//Hover Tooltip Flyout bubbles > Background Corner Radius",

  "controlStyles[158].target": "NetworkUX.View.CFEWiFiPassKey > StackPanel > PasswordBox#PassKeyPasswordBox",
    "controlStyles[158].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[158].styles[1]": "//Wifi SubPage > Connect to Network > PasswordBox CornerRadius",

  "controlStyles[159].target": "StackPanel > Button",
    "controlStyles[159].styles[0]": "CornerRadius=$InnerRadius",
    "controlStyles[159].styles[1]": "//An attempt to apply corner radius to more buttons with similar stucture"
}
```
</details>

## Credits
 - Thanks [Lockframe](https://github.com/Lockframe) and [OsamaHJT](https://github.com/OsamaHJT) for helping me find the targets