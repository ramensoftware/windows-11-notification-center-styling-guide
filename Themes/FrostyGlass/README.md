# ❄️ FrostyGlass theme for Windows 11 Notification Center Styler

A refined, translucent "Frosty" experience for the Windows 11 Notification Center via Windhawk.

**Author**: [Guido Lamanna](https://github.com/guidolamanna)

[![Windhawk](https://img.shields.io/badge/Requires-Windhawk-blue?style=flat-square)](https://windhawk.net/)
[![Style](https://img.shields.io/badge/Style-Frosty_Glass-lightgrey?style=flat-square)](#)

This configuration provides a modern **Frosty Glass** aesthetic for your Notification Center, Calendar, and Control Center. It utilizes custom translucent `AcrylicBrush` effects to create a soft, blurred interface that feels perfectly integrated with the desktop environment.

## 📸 Showcase

*Here is the Frosty Glass aesthetic in action across the different flyouts:*

### 📅 Notifications & Calendar

![Notification & Calendar](notification-and-calendar.png)

### 🎛️ Control Center (Compact / No Media Player)

![Control Center (Compact / No Media Player)](control-center-compact.png)

### 🎛️ Control Center (With Media Player)

![Control Center with Media Player](control-center-with-media-player.png)

## 🔗 Related Projects

Complete the look across your entire UI! Check out my other Frosty Glass styling repositories:
* [❄️ Frosty Glass Taskbar Styler](https://github.com/guidolamanna/windows-11-taskbar-styling-guide/blob/main/Themes/FrostyGlass/README.md) to apply this exact same aesthetic to your Taskbar, Alt+Tab menu, volume sliders, and more!
* [❄️ Frosty Glass Start Menu Styler](https://github.com/guidolamanna/windows-11-start-menu-styling-guide/blob/main/Themes/FrostyGlass/README.md) to apply this exact same aesthetic to your Start Menu and Lock Screen!

## 🙌 Credits & Inspiration

A huge thank you to [Ramen Software](https://github.com/ramensoftware) for creating Windhawk. This configuration was heavily inspired by the official [Windows 11 Notification Center Styling Guide](https://github.com/ramensoftware/windows-11-notification-center-styling-guide) and the Windhawk modding community.

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
  - Background=<AcrylicBrush TintColor="#1000000F"/>
  - BorderBrush2=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="{ThemeResource SystemChromeHighColor}" Offset="0.0" /><GradientStop Color="{ThemeResource SystemChromeLowColor}" Offset="0.25" /><GradientStop Color="{ThemeResource SystemChromeHighColor}" Offset="1" /></LinearGradientBrush>
  - BorderThickness=1
  - CornerRadius=10
  - BorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.25" /><GradientStop Color="#50808080" Offset="1" /></LinearGradientBrush>
  - Background2=<AcrylicBrush TintColor="{ThemeResource SystemChromeAltHighColor}" TintOpacity="0.3" FallbackColor="{ThemeResource SystemChromeAltHighColor}" />
  - TrayPadding=2
  - ElementBG=<SolidColorBrush Color="{ThemeResource SystemChromeAltHighColor}" Opacity="0.3" />
  - ElementBorderThickness=1
  - ElementBorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="1" /><GradientStop Color="#50606060" Offset="0.15" /></LinearGradientBrush>
  - ElementCornerRadius=10
  - thumbnailImageSize=300
controlStyles:
  - target: Grid#NotificationCenterGrid
    styles:
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
      - Background:=$Background
      - BorderBrush:=$BorderBrush
  - target: Grid#CalendarCenterGrid
    styles:
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
      - BorderBrush:=$BorderBrush
      - Background:=$Background
  - target: Grid#ControlCenterRegion
    styles:
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
      - Background:=$Background
      - BorderBrush:=$BorderBrush
  - target: Grid#MediaTransportControlsRegion
    styles:
      - CornerRadius:=$CornerRadius
      - BorderThickness:=$BorderThickness
      - Background:=$Background
      - BorderBrush:=$BorderBrush
  - target: MenuFlyoutPresenter
    styles:
      - CornerRadius:=$CornerRadius
      - BorderThickness:=$BorderThickness
      - Background:=$Background
      - BorderBrush:=$BorderBrush
  - target: Button#ClearAll
    styles:
      - AccessKey=x
  - target: Button#ExpandCollapseButton
    styles:
      - AccessKey=c
  - target: Windows.UI.Xaml.Controls.Grid#ThumbnailImage
    styles:
      - Width:=$thumbnailImageSize
      - Height:=$thumbnailImageSize
      - HorizontalAlignment=Center
      - VerticalAlignment=Top
      - Grid.Column=1
      - Margin=0,2,0,55
  - target: ControlCenter.MediaTransportControls#MediaTransportControls > Windows.UI.Xaml.Controls.Grid#MediaTransportControlsRegion
    styles:
      - Height=Auto
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer
    styles:
      - VerticalAlignment=Bottom
      - Grid.Column=0
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#TitleText
    styles:
      - TextAlignment=Center
      - Margin=0,0,0,0
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#SubtitleText
    styles:
      - TextAlignment=Center
      - Margin=0,0,0,5
  - target: Windows.UI.Xaml.Controls.Grid#ThumbnailImage > Windows.UI.Xaml.Controls.Border
    styles:
      - CornerRadius:=$CornerRadius
  - target: Grid#MediaTransportControlsRoot
    styles:
      - Background:=Transparent
  - target: ContentControl > ContentPresenter > Grid > Grid
    styles:
      - BorderBrush:=Transparent
  - target: ContentPresenter#ContentPresenter
    styles:
      - BorderBrush:=$BorderBrush
      - BorderThinkness:=$BorderThickness
      - Background:=$Background
  - target: Border#WADFeatureFooter
    styles:
      - BorderBrush:=Transparent
  - target: StackPanel > ContentPresenter > Border
    styles:
      - BorderBrush:=Transparent
      - BorderThickness:=0
  - target: Windows.UI.Xaml.Controls.Grid[AutomationProperties.LocalizedLandmarkType=Footer]
    styles:
      - BorderBrush:=Transparent
  - target: Microsoft.UI.Xaml.Controls.PipsPager#QuickActionsPager
    styles:
      - Visibility=1
  - target: JumpViewUI.JumpListListViewItem > Grid#LayoutRoot > Border#BackgroundBorder
    styles:
      - CornerRadius:=4.5
  - target: JumpViewUI.SystemItemListViewItem > Grid#LayoutRoot > Border#BackgroundBorder
    styles:
      - CornerRadius:=4.5
  - target: Grid#NotificationCenterGrid
    styles:
      - VerticalAlignment:=2
  - target: Border#ToastBackgroundBorder2
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - CornerRadius:=$CornerRadius
  - target: ScrollViewer#CalendarControlScrollViewer
    styles:
      - Background:=Transparent
      - BorderThickness=0,0,0,0
  - target: Border#CalendarHeaderMinimizedOverlay
    styles:
      - Background:=Transparent
      - BorderThickness=0,0,0,0
  - target: Grid#L1Grid > Border
    styles:
      - Background:=Transparent
      - BorderThickness=0,0,0,0
  - target: ContentPresenter#PageContent
    styles:
      - Background:=Transparent
  - target: ContentPresenter#PageContent > Grid > Border
    styles:
      - Background:=Transparent
  - target: QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot
    styles:
      - Background:=Transparent
  - target: QuickActions.ControlCenter.AccessibleWindow#PageWindow > ContentPresenter > Grid#FullScreenPageRoot > ContentPresenter#PageHeader
    styles:
      - Background:=Transparent
  - target: ScrollViewer#ListContent
    styles:
      - Background:=Transparent
  - target: ActionCenter.FlexibleToastView#FlexibleNormalToastView
    styles:
      - Background:=Transparent
  - target: ActionCenter.FlexibleItemView
    styles:
      - CornerRadius=$CornerRadius
  - target: ContentControl#TogglesGroup > ContentPresenter > ControlCenter.PaginatedGridView > Grid
    styles:
      - BorderThickness=0,0,0,0
  - target: Grid#FooterGrid
    styles:
      - BorderThickness=0,0,0,0
  - target: ActionCenter.FocusSessionControl#FocusSessionControl > Grid#FocusGrid
    styles:
      - Background:=Transparent
      - BorderThickness=0,0,0,0
  - target: ContentPresenter#PageContent
    styles:
      - Background:=Transparent
  - target: Windows.UI.Xaml.Controls.Border#ToastBackgroundBorder
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - CornerRadius:=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#ItemOpaquePlating
    styles:
      - CornerRadius:=7
      - Visibility=0
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
  - target: Windows.UI.Xaml.Controls.ListViewItem
    styles:
      - Margin=0,0,0,3
  - target: Windows.UI.Xaml.Controls.Grid#StandardHeroContainer > Windows.UI.Xaml.Controls.Image
    styles:
      - Opacity=1
  - target: Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar
    styles:
      - Visibility=1
  - target: MenuFlyoutPresenter > Border
    styles:
      - Background:=$Background
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - CornerRadius:=$CornerRadius
  - target: Border#JumpListRestyledAcrylic
    styles:
      - Background:=$Background
      - BorderThickness:=$BorderThickness
      - BorderBrush:=$BorderBrush
      - CornerRadius:=$CornerRadius
      - Margin=-4.5,-2,-4.5,-2
      - Height=Auto
  - target: Windows.UI.Xaml.Controls.ScrollViewer#JumpListScroller
    styles:
      - Margin=-2
  - target: Windows.UI.Xaml.Controls.Grid#SystemItemsContainer > Windows.UI.Xaml.Controls.Border > JumpViewUI.SystemItemListView#SystemItemList
    styles:
      - Margin:=0,3,0,0
```
</details>
