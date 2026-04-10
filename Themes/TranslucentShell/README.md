# TranslucentShell theme for Windows 11 Notification Center Styler

**Author**: [Undisputed00x](https://github.com/Undisputed00x)

![Video](video.gif)

## Thumbnail image size

The default media control thumbnail size is 300x300, which might be too large
for small screens. You can change it by setting the value
`thumbnailImageSize=200`, where `200` is the desired size, in the "Style
constants" section of the mod's settings.

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
  - CommonBgBrush=<WindhawkBlur BlurAmount="25" TintColor="#25323232"/>
  - thumbnailImageSize=300
controlStyles:
  - target: Grid#NotificationCenterGrid
    styles:
      - Background:=$CommonBgBrush
      - BorderThickness=0,0,0,0
      - CornerRadius=15
  - target: Grid#CalendarCenterGrid
    styles:
      - Background:=$CommonBgBrush
      - BorderThickness=0,0,0,0
      - CornerRadius=15
  - target: ScrollViewer#CalendarControlScrollViewer
    styles:
      - Background=Transparent
  - target: Border#CalendarHeaderMinimizedOverlay
    styles:
      - Background=Transparent
  - target: ActionCenter.FocusSessionControl#FocusSessionControl > Grid#FocusGrid
    styles:
      - Background=Transparent
  - target: MenuFlyoutPresenter > Border
    styles:
      - Background:=<WindhawkBlur BlurAmount="25" TintColor="#00000000"/>
      - BorderThickness=0,0,0,0
      - CornerRadius=15
      - Padding=2,4,2,4
  - target: Border#JumpListRestyledAcrylic
    styles:
      - Background:=$CommonBgBrush
      - BorderThickness=0,0,0,0
      - CornerRadius=15
      - Margin=-2,-2,-2,-2
  - target: Grid#ControlCenterRegion
    styles:
      - Background:=$CommonBgBrush
      - BorderThickness=0,0,0,0
      - CornerRadius=15
  - target: Windows.UI.Xaml.Controls.Grid#L1Grid > Border
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: Windows.UI.Xaml.Controls.Grid#MediaTransportControlsRegion
    styles:
      - Background:=$CommonBgBrush
      - BorderThickness=0,0,0,0
      - CornerRadius=15
  - target: Grid#MediaTransportControlsRoot
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: ContentPresenter#PageContent
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: ContentPresenter#PageContent > Grid > Border
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot > ContentPresenter#PageHeader
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: ScrollViewer#ListContent
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: ActionCenter.FlexibleToastView#FlexibleNormalToastView
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: Border#ToastBackgroundBorder2
    styles:
      - Background:=$CommonBgBrush
      - BorderThickness=0,0,0,0
      - CornerRadius=15
  - target: JumpViewUI.SystemItemListViewItem > Grid#LayoutRoot > Border#BackgroundBorder
    styles:
      - FocusVisualPrimaryThickness=0,0,0,0
      - FocusVisualSecondaryThickness=0,0,0,0
  - target: JumpViewUI.JumpListListViewItem > Grid#LayoutRoot > Border#BackgroundBorder
    styles:
      - FocusVisualPrimaryThickness=0,0,0,0
  - target: ActionCenter.FlexibleItemView
    styles:
      - CornerRadius=15
  - target: ControlCenter.MediaTransportControls#MediaTransportControls > Windows.UI.Xaml.Controls.Grid#MediaTransportControlsRegion
    styles:
      - Height=Auto
  - target: Windows.UI.Xaml.Controls.Grid#ThumbnailImage
    styles:
      - Width=$thumbnailImageSize
      - Height=$thumbnailImageSize
      - HorizontalAlignment=Center
      - VerticalAlignment=Top
      - Grid.Column=1
      - Margin=0,2,0,45
  - target: Windows.UI.Xaml.Controls.Grid#ThumbnailImage > Windows.UI.Xaml.Controls.Border
    styles:
      - CornerRadius=10
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer
    styles:
      - VerticalAlignment=Bottom
      - Grid.Column=0
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#TitleText
    styles:
      - TextAlignment=Center
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#SubtitleText
    styles:
      - TextAlignment=Center
```
</details>
