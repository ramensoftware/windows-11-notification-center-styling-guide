# Borderless theme for Windows 11 Notification Center Styler

Removes all borders and drop shadows from notification center, quick settings and taskbar jump lists as well (thus the name), with the added bonus of a top-aligned notification center, so it fits dock layouts. Also, desktop toasts are resized to 348 for consistency with the notification center toasts.

**Author**: [Ali Cool](https://github.com/AliCool412)

![Screenshot](screenshot.png)
<!--
## Theme selection

The theme is integrated into the mod and can be selected directly from the mod's
settings:

* Open the Windows 11 Notification Center Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:
-->
## Manual installation

The theme styles can be imported manually. To do that, follow these steps:

* Open the Windows 11 Notification Center Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

<details>
<summary>Content to import (click to expand)</summary>

```yaml
controlStyles:
  - target: ActionCenter.FocusSessionControl
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Grid
    styles:
      - Shadow:=
      - BorderThickness=0
  - target: Windows.UI.Xaml.Controls.Border
    styles:
      - Shadow:=
      - BorderThickness=0
  - target: Windows.UI.Xaml.Controls.Grid#NotificationCenterGrid
    styles:
      - Height=Auto
      - VerticalAlignment=Stretch
      - Margin=0
  - target: Windows.UI.Xaml.Controls.TextBlock#NoNotificationsTextBlock
    styles:
      - Text=¯\_(ツ)_/¯
      - FontSize=16
  - target: Windows.UI.Xaml.Controls.Button#ExpandCollapseButton
    styles:
      - BorderThickness=0
  - target: Windows.UI.Xaml.Controls.Grid#DoNotDisturbSubtext > Windows.UI.Xaml.Controls.Button
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Button#ClearAll > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter > Windows.UI.Xaml.Controls.TextBlock
    styles:
      - Text=
      - FontFamily=Segoe Fluent Icons
      - FontSize=8
  - target: Windows.UI.Xaml.Controls.TextBlock
    styles:
      - FontWeight=Normal
  - target: Windows.UI.Xaml.Controls.Grid#CalendarSection
    styles:
      - Height=300
  - target: Windows.UI.Xaml.Controls.Button#PreviousButton
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Button#NextButton
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Button#HeaderButton
    styles:
      - Width=Auto
      - HorizontalAlignment=Left
  - target: Windows.UI.Xaml.Controls.Grid#WeekDayNames
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - BorderThickness=0
  - target: Windows.UI.Xaml.Controls.Button#ExpandCollapseButton
    styles:
      - Visibility=Collapsed
  - target: Grid#CalendarCenterGrid
    styles:
      - Margin=0,10,0,160
  - target: Windows.UI.Xaml.Controls.Button#ClearAll
    styles:
      - Width=24
      - Height=24
  - target: Windows.UI.Xaml.Controls.Primitives.ToggleButton#DoNotDisturbButton
    styles:
      - Height=24
      - Width=24
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#DoNotDisturbButtonIcon
    styles:
      - Height=12
      - Width=12
  - target: Windows.UI.Xaml.Controls.Border#CalendarHeaderMinimizedOverlay
    styles:
      - Visibility=Collapsed
  - target: ActionCenter.NotificationCenterView#NotificationCenterView
    styles:
      - Margin=16,0,16,20
  - target: Windows.UI.Xaml.Controls.Grid#L1Grid > Windows.UI.Xaml.Controls.Border
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Grid#MediaTransportControlsRoot
    styles:
      - Background:=
  - target: Windows.UI.Xaml.Controls.ScrollViewer#CalendarControlScrollViewer
    styles:
      - Background:=
  - target: ContentPresenter#PageContent > Grid > Border
    styles:
      - Background:=
  - target: ContentPresenter#PageHeader
    styles:
      - Background:=
  - target: Windows.UI.Xaml.Controls.Grid#ToastCenterMainGrid
    styles:
      - MaxWidth=348
  - target: ScrollViewer#ListContent
    styles:
      - Background:=
  - target: Windows.UI.Xaml.Controls.StackPanel#SharePickerHeader > Windows.UI.Xaml.Shapes.Rectangle
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.StackPanel#PreviewComponentPanel
    styles:
      - Background:=
  - target: Windows.UI.Xaml.Controls.Border#ItemOpaquePlating
    styles:
      - Opacity=0.7
  - target: ActionCenter.ToastCenterView
    styles:
      - MaxWidth=348
```
</details>
