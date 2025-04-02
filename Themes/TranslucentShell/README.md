# TranslucentShell theme for Windows 11 Notification Center Styler

**Author**: [Undisputed00x](https://github.com/Undisputed00x)

![Video](video.gif)

## Theme selection

The theme is integrated into the mod, and can be simply selected from the mod's
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
  "controlStyles[0].target": "Grid#NotificationCenterGrid",
  "controlStyles[0].styles[0]": "Background:=<AcrylicBrush TintOpacity=\"0\" TintColor=\"Black\" TintLuminosityOpacity=\"0.12\" Opacity=\"1\" FallbackColor=\"#70262626\"/>",
  "controlStyles[0].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[0].styles[2]": "CornerRadius=15",
  "controlStyles[1].target": "Grid#CalendarCenterGrid",
  "controlStyles[1].styles[0]": "Background:=<AcrylicBrush TintOpacity=\"0\" TintColor=\"Black\" TintLuminosityOpacity=\"0.12\" Opacity=\"1\" FallbackColor=\"#70262626\"/>",
  "controlStyles[1].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[1].styles[2]": "CornerRadius=15",
  "controlStyles[2].target": "ScrollViewer#CalendarControlScrollViewer",
  "controlStyles[2].styles[0]": "Background:=<AcrylicBrush Opacity=\"0\"/>",
  "controlStyles[3].target": "Border#CalendarHeaderMinimizedOverlay",
  "controlStyles[3].styles[0]": "Background:=<AcrylicBrush Opacity=\"0\"/>",
  "controlStyles[4].target": "ActionCenter.FocusSessionControl#FocusSessionControl > Grid#FocusGrid",
  "controlStyles[4].styles[0]": "Background:=<AcrylicBrush Opacity=\"0\"/>",
  "controlStyles[5].target": "MenuFlyoutPresenter",
  "controlStyles[5].styles[0]": "Background:=<AcrylicBrush TintOpacity=\"0\" TintColor=\"Black\" TintLuminosityOpacity=\"0.12\" Opacity=\"1\" FallbackColor=\"#70262626\"/>",
  "controlStyles[5].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[5].styles[2]": "CornerRadius=15",
  "controlStyles[5].styles[3]": "Padding=2,4,2,4",
  "controlStyles[6].target": "Border#JumpListRestyledAcrylic",
  "controlStyles[6].styles[0]": "Background:=<AcrylicBrush TintOpacity=\"0\" TintColor=\"Black\" TintLuminosityOpacity=\"0.12\" Opacity=\"1\" FallbackColor=\"#70262626\"/>",
  "controlStyles[6].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[6].styles[2]": "CornerRadius=15",
  "controlStyles[6].styles[3]": "Margin=-2,-2,-2,-2",
  "controlStyles[7].target": "Grid#ControlCenterRegion",
  "controlStyles[7].styles[0]": "Background:=<AcrylicBrush TintOpacity=\"0\" TintColor=\"Black\" TintLuminosityOpacity=\"0.12\" Opacity=\"1\" FallbackColor=\"#70262626\"/>",
  "controlStyles[7].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[7].styles[2]": "CornerRadius=15",
  "controlStyles[8].target": "Windows.UI.Xaml.Controls.Grid#L1Grid > Border",
  "controlStyles[8].styles[0]": "Background:=<SolidColorBrush Color=\"Transparent\"/>",
  "controlStyles[9].target": "Windows.UI.Xaml.Controls.Grid#MediaTransportControlsRegion",
  "controlStyles[9].styles[0]": "Background:=<AcrylicBrush TintOpacity=\"0\" TintColor=\"Black\" TintLuminosityOpacity=\"0.12\" Opacity=\"1\" FallbackColor=\"#70262626\"/>",
  "controlStyles[9].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[9].styles[2]": "CornerRadius=15",
  "controlStyles[10].target": "Grid#MediaTransportControlsRoot",
  "controlStyles[10].styles[0]": "Background:=<SolidColorBrush Color=\"Transparent\"/>",
  "controlStyles[11].target": "ContentPresenter#PageContent",
  "controlStyles[11].styles[0]": "Background:=<SolidColorBrush Color=\"Transparent\"/>",
  "controlStyles[12].target": "ContentPresenter#PageContent > Grid > Border",
  "controlStyles[12].styles[0]": "Background:=<SolidColorBrush Color=\"Transparent\"/>",
  "controlStyles[13].target": "QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot",
  "controlStyles[13].styles[0]": "Background:=<SolidColorBrush Color=\"Transparent\"/>",
  "controlStyles[14].target": "QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot > ContentPresenter#PageHeader",
  "controlStyles[14].styles[0]": "Background:=<SolidColorBrush Color=\"Transparent\"/>",
  "controlStyles[15].target": "ScrollViewer#ListContent",
  "controlStyles[15].styles[0]": "Background:=<SolidColorBrush Color=\"Transparent\"/>",
  "controlStyles[16].target": "ActionCenter.FlexibleToastView#FlexibleNormalToastView",
  "controlStyles[16].styles[0]": "Background:=<SolidColorBrush Color=\"Transparent\"/>",
  "controlStyles[17].target": "Border#ToastBackgroundBorder2",
  "controlStyles[17].styles[0]": "Background:=<AcrylicBrush TintOpacity=\"0\" TintColor=\"Black\" TintLuminosityOpacity=\"0.12\" Opacity=\"1\" FallbackColor=\"#70262626\"/>",
  "controlStyles[17].styles[1]": "BorderThickness=0,0,0,0",
  "controlStyles[17].styles[2]": "CornerRadius=15",
  "controlStyles[18].target": "JumpViewUI.SystemItemListViewItem > Grid#LayoutRoot > Border#BackgroundBorder",
  "controlStyles[18].styles[0]": "FocusVisualPrimaryThickness=0,0,0,0",
  "controlStyles[18].styles[1]": "FocusVisualSecondaryThickness=0,0,0,0",
  "controlStyles[19].target": "JumpViewUI.JumpListListViewItem > Grid#LayoutRoot > Border#BackgroundBorder",
  "controlStyles[19].styles[0]": "FocusVisualPrimaryThickness=0,0,0,0",
  "controlStyles[20].target": "ActionCenter.FlexibleItemView",
  "controlStyles[20].styles[0]": "CornerRadius=15",
  "controlStyles[21].target": "ControlCenter.MediaTransportControls#MediaTransportControls > Windows.UI.Xaml.Controls.Grid#MediaTransportControlsRegion",
  "controlStyles[21].styles[0]": "Height=470",
  "controlStyles[22].target": "Windows.UI.Xaml.Controls.Grid#AlbumTextAndArtContainer",
  "controlStyles[22].styles[0]": "Height=350",
  "controlStyles[23].target": "Windows.UI.Xaml.Controls.Grid#ThumbnailImage",
  "controlStyles[23].styles[0]": "Width=300",
  "controlStyles[23].styles[1]": "Height=300",
  "controlStyles[23].styles[2]": "HorizontalAlignment=Center",
  "controlStyles[23].styles[3]": "VerticalAlignment=Top",
  "controlStyles[23].styles[4]": "Grid.Column=1",
  "controlStyles[24].target": "Windows.UI.Xaml.Controls.Grid#ThumbnailImage > Windows.UI.Xaml.Controls.Border",
  "controlStyles[24].styles[0]": "CornerRadius=10",
  "controlStyles[25].target": "Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer",
  "controlStyles[25].styles[0]": "VerticalAlignment=Bottom",
  "controlStyles[25].styles[1]": "Grid.Column=0",
  "controlStyles[26].target": "Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#TitleText",
  "controlStyles[26].styles[0]": "TextAlignment=Center",
  "controlStyles[27].target": "Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#SubtitleText",
  "controlStyles[27].styles[0]": "TextAlignment=Center",
  "theme": "",
  "resourceVariables[0].variableKey": "",
  "resourceVariables[0].value": ""
}
```
</details>
