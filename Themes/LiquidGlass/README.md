# LiquidGlass theme for Windows 11 Notification Center Styler

**Author**: [PhantomNimbi](https://github.com/PhantomNimbi)

---

### Requirements

* [Windows 11 Notification Center Styler](https://windhawk.net/mods/windows-11-notification-center-styler)

---

### Notification Center

![Screenshot](screenshot.png)

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
  - transparent = Transparent
  - Background = <WindhawkBlur BlurAmount="15" TintColor="{ThemeResource SystemAltLowColor}" TintOpacity="0.4"  />
  - ElementBackground = <WindhawkBlur BlurAmount="20" TintColor="{ThemeResource SystemAltLowColor}" TintOpacity="0.4"  />
  - AccentBackground =<WindhawkBlur BlurAmount="20" TintColor="{ThemeResource SystemAccentColorLight1}" TintOpacity="0.2"  />
  - ElementBackground2 = <WindhawkBlur BlurAmount="15" TintColor="{ThemeResource SystemAltLowColor}" TintOpacity="0.2"  />
  - BorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.25" /><GradientStop Color="#50808080" Offset="1" /></LinearGradientBrush>
  - ElementBorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="1" /><GradientStop Color="#50606060" Offset="0.15" /></LinearGradientBrush>
  - BorderThickness=0.3,1,0.3,0.3
  - ElementBorderThickness=0.3,0.3,0.3,1
  - CornerRadius = 12
  - ElementCornerRadius = 8
controlStyles:
  - target: Grid#NotificationCenterGrid
    styles:
      - Background:=$Background
      - CornerRadius = $CornerRadius
      - Shadow :=
      - BorderThickness = $BorderThickness
      - BorderBrush := $BorderBrush
  - target: Grid#CalendarCenterGrid
    styles:
      - Background:=$Background
      - CornerRadius=$CornerRadius
      - Shadow :=
      - Margin = 0,6,0,6
      - MinHeight = 40
      - BorderThickness = $BorderThickness
      - BorderBrush := $BorderBrush
  - target: ScrollViewer#CalendarControlScrollViewer
    styles:
      - Background := $ElementBackground
      - CornerRadius = $ElementCornerRadius
      - Margin = -10,11,-10,-14
      - Shadow :=
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: Border#CalendarHeaderMinimizedOverlay
    styles:
      - Background := $ElementBackground
      - CornerRadius = $CornerRadius
      - Shadow :=
      - Margin =-10,-6,-10,-8
      - Height = 45
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: ActionCenter.FocusSessionControl#FocusSessionControl > Grid#FocusGrid
    styles:
      - Background := $ElementBackground
      - CornerRadius=$CornerRadius
      - Margin = 6,7,6,6
      - Shadow :=
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: MenuFlyoutPresenter
    styles:
      - Background := $Background
      - BorderThickness = 0,0,0,0
      - CornerRadius = $CornerRadius
      - Padding = 1,2,1,2
      - Shadow :=
      - BorderThickness = $BorderThickness
      - BorderBrush := $BorderBrush
  - target: Border#JumpListRestyledAcrylic
    styles:
      - Background := $Background
      - BorderThickness = 0,0,0,0
      - CornerRadius = $CornerRadius
      - Margin = -2,-2,-2,-2
      - Shadow :=
      - BorderThickness = $BorderThickness
      - BorderBrush := $BorderBrush
  - target: Grid#ControlCenterRegion
    styles:
      - Background := $Background
      - CornerRadius = $CornerRadius
      - BorderThickness = 0,0,0,0
      - Shadow :=
      - Margin = 0,0,0,-6
  - target: ContentPresenter#PageContent
    styles:
      - Background := Transparent
      - Shadow :=
  - target: ContentPresenter#PageContent > Grid > Border
    styles:
      - Background := $ElementBackground
      - CornerRadius=$ElementCornerRadius
      - Margin = 8,0,8,2
      - Shadow :=
  - target: QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot
    styles:
      - Background := Transparent
      - Shadow :=
  - target: QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot > ContentPresenter#PageHeader
    styles:
      - Background := $ElementBackground
      - CornerRadius = $ElementCornerRadius
      - Margin = 7,7,7,7
      - Shadow :=
  - target: ScrollViewer#ListContent
    styles:
      - Background := $ElementBackground
      - CornerRadius = $ElementCornerRadius
      - Margin = 8,0,8,0
      - Shadow :=
  - target: ActionCenter.FlexibleToastView#FlexibleNormalToastView
    styles:
      - Background := Transparent
      - Shadow :=
  - target: Border#ToastBackgroundBorder2
    styles:
      - Background :=$Background
      - BorderThickness = 0,0,0,0
      - CornerRadius = $CornerRadius
      - Shadow :=
  - target: JumpViewUI.SystemItemListViewItem > Grid#LayoutRoot > Border#BackgroundBorder
    styles:
      - Background := $ElementBackground
      - CornerRadius = $ElementCornerRadius
  - target: JumpViewUI.JumpListListViewItem > Grid#LayoutRoot > Border#BackgroundBorder
    styles:
      - CornerRadius = $ElementCornerRadius
  - target: ActionCenter.FlexibleItemView
    styles:
      - CornerRadius = $CornerRadius
      - Shadow :=
  - target: QuickActions.AccessibleToggleButton#ToggleButton
    styles:
      - CornerRadius = $ElementCornerRadius
      - BorderThickness = 0
  - target: QuickActions.AccessibleToggleButton#SplitL2Button
    styles:
      - CornerRadius = $ElementCornerRadius
      - Margin = 4,0,-4,0
      - BorderThickness = 0
  - target: Grid#NotificationCenterTopBanner
    styles:
      - Background := $ElementBackground
      - CornerRadius = $ElementCornerRadius
      - Margin = 6
  - target: Windows.UI.Xaml.Controls.Grid#L1Grid > Border
    styles:
      - Background := Transparent
  - target: Windows.UI.Xaml.Controls.ContentPresenter
    styles:
      - BorderThickness = 0
  - target: Windows.UI.Xaml.Controls.Button#FooterButton[AutomationProperties.Name = Edit quick settings]
    styles:
      - Margin = 0,0,8,0
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.Button[AutomationProperties.AutomationId = Microsoft.QuickAction.Battery]
    styles:
      - Margin = 2,0,0,0
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.Button#FooterButton[AutomationProperties.Name = All settings]
    styles:
      - Margin = 0,0,-1,0
      - CornerRadius = $ElementCornerRadius
      - Background := $Background
  - target: Windows.UI.Xaml.Controls.Button[AutomationProperties.AutomationId = Microsoft.QuickAction.Volume]
    styles:
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.Button#VolumeL2Button[AutomationProperties.Name = Select a sound output]
    styles:
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalTrackRect
    styles:
      - Height = 10
      - Fill := $ElementBackground
      - RadiusY = 3
      - RadiusX = 3
  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalDecreaseRect
    styles:
      - Height =10
      - RadiusY = 3
      - RadiusX = 3
      - Margin = 0
  - target: Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb
    styles:
      - Visibility = 1
  - target: Windows.UI.Xaml.Controls.Grid#MediaTransportControlsRegion
    styles:
      - Height = Auto
      - CornerRadius = $CornerRadius
      - BorderThickness = 0
      - Background := $Background
      - Shadow :=
      - Padding = 0,0,0,12
      - Margin = 0,0,0,12
  - target: Windows.UI.Xaml.Controls.Grid#ThumbnailImage
    styles:
      - Grid.Column = 2
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer
    styles:
      - Grid.Column = 1
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#Title
    styles:
      - TextAlignment = Center
      - FontFamily = Tektur
      - FontSize = 18
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#Subtitle
    styles:
      - TextAlignment = Center
      - FontFamily = Montserrat
      - Margin = 0,3,0,0
      - FontWeight= 600
  - target: Windows.UI.Xaml.Controls.ListView#MediaButtonsListView
    styles:
      - VerticalAlignment = Top
      - Height = 48
      - Margin = 0,12,0,-12
  - target: Windows.UI.Xaml.Controls.Primitives.RepeatButton#PreviousButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Background@Normal := $ElementBackground
      - Background@PointerOver := $AccentBackground
      - Background@Pressed := $ElementBackground2
      - Width = 40
      - Height = 30
      - CornerRadius = $ElementCornerRadius
      - Margin = 15,0,0,0
  - target: Windows.UI.Xaml.Controls.Button#PlayPauseButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Background@Normal := $ElementBackground
      - Background@PointerOver := $AccentBackground
      - Background@Pressed := $ElementBackground2
      - Width = 40
      - Height = 40
      - CornerRadius = $ElementCornerRadius
      - Margin = -10,0,0,0
      - BorderBrush := $ElementBorderBrush
      - BorderThickness = $ElementBorderThickness
  - target: Windows.UI.Xaml.Controls.Primitives.RepeatButton#NextButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Background@Normal := $ElementBackground
      - Background@PointerOver := $AccentBackground
      - Background@Pressed := $ElementBackground2
      - Width = 40
      - Height = 30
      - CornerRadius = $ElementCornerRadius
      - Margin = -20,0,0,0
      - BorderBrush := $ElementBorderBrush
      - BorderThickness = $ElementBorderThickness
  - target: Windows.UI.Xaml.Controls.TextBlock#AppNameText
    styles:
      - FontFamily = Tektur
      - FontSize = 16
  - target: Windows.UI.Xaml.Controls.Image#IconImage
    styles:
      - Height = 20
      - Width = 20
  - target: Grid#MediaTransportControlsRoot
    styles:
      - Background := Transparent
  - target: Grid#ToastPeekRegion
    styles:
      - Background =
      - RenderTransform := <TranslateTransform Y="-495" X="395" />
      - Grid.Column = 0
      - Grid.Row = 2
  - target: Windows.UI.Xaml.Controls.CalendarViewDayItem > Windows.UI.Xaml.Controls.Border
    styles:
      - CornerRadius = $ElementCornerRadius
      - Margin = 1,2,1,2
  - target: Windows.UI.Xaml.Controls.CalendarViewDayItem
    styles:
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.Control > Windows.UI.Xaml.Controls.Border
    styles:
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.Primitives.CalendarViewItem
    styles:
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.ListViewHeaderItem
    styles:
      - Margin = 50,6,50,2
      - CornerRadius = $ElementCornerRadius
      - Height = 35
  - target: Windows.UI.Xaml.Controls.Button#SettingsButton
    styles:
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.Button#DismissButton
    styles:
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.StackPanel#CalendarHeader
    styles:
      - Margin = 6,0,0,0
  - target: Windows.UI.Xaml.Controls.ScrollContentPresenter#ScrollContentPresenter
    styles:
      - Margin = 1,2,1,2
  - target: Windows.UI.Xaml.Controls.Grid#WeekDayNames
    styles:
      - Background := $AccentBackground
      - CornerRadius = $ElementCornerRadius
      - Margin = 4,0,4,0
      - Padding = 0,-5,0,-3
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: Windows.UI.Xaml.Controls.ListViewItem
    styles:
      - CornerRadius = $ElementCornerRadius
  - target: Windows.UI.Xaml.Controls.Grid#RootGrid > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - Background := $AccentBackground
      - CornerRadius = $ElementCornerRadius
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#ItemOpaquePlating
    styles:
      - Background := $ElementBackground2
      - CornerRadius = $ElementCornerRadius
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: Windows.UI.Xaml.Controls.Grid#StandardHeroContainer
    styles:
      - Margin = 12,0,12,0
      - CornerRadius = 0
      - Height = 150
  - target: Windows.UI.Xaml.Controls.Grid#SliderContainer
    styles:
      - Margin = 0-2,0,0
  - target: Windows.UI.Xaml.Controls.Button#BackButton
    styles:
      - CornerRadius = $ElementCornerRadius
      - BorderBrush := $ElementBorderBrush
      - BorderThickness = $ElementBorderThickness
  - target: Windows.UI.Xaml.Shapes.Rectangle#OuterBorder
    styles:
      - RadiusX = 6
      - RadiusY = 6
      - Height = 18
  - target: Windows.UI.Xaml.Shapes.Rectangle#SwitchKnobOff
    styles:
      - RadiusY = 3
      - RadiusX = 3
  - target: Windows.UI.Xaml.Controls.Border#SwitchKnobOn
    styles:
      - CornerRadius = 3
  - target: Windows.UI.Xaml.Shapes.Rectangle#SwitchKnobBounds
    styles:
      - RadiusX = 6
      - RadiusY = 6
      - Height = 18
  - target: ActionCenter.NotificationListViewItem
    styles:
      - Margin = 5,2,5,3
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: Windows.UI.Xaml.Controls.Grid[AutomationProperties.LocalizedLandmarkType = Footer]
    styles:
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: NetworkUX.View.SettingsListViewItem > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root
    styles:
      - CornerRadius = $CornerRadius
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: Windows.UI.Xaml.Controls.ContentPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - BorderThickness = $ElementBorderThickness
      - BorderBrush := $ElementBorderBrush
  - target: Button#ClearAll
    styles:
      - AccessKey=x
  - target: Button#ExpandCollapseButton
    styles:
      - AccessKey=e
```
</details>
