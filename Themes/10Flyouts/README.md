# 10Flyouts theme for Windows 11 Notification Center Styler

**Author**: [Tails](https://github.com/milestprower92)

![Screenshot](screenshot.png)

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
theme: None
controlStyles:
  - target: Windows.UI.Xaml.Controls.Border#LogonFrameBorder
    styles:
      - CornerRadius=0
  - target: QuickActions.QuickToggleButtonDesktopWinuiFluent#QuickActionUserControl > QuickActions.AccessibleToggleButton#ToggleButton > ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Foreground:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" />
      - Background@Normal:=<SolidColorBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.5" />
      - Background@PointerOver:=<RevealBorderBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.8" TargetTheme="1" FallbackColor="{ThemeResource SystemChromeHighColor}" />
      - Background@Pressed:=<RevealBorderBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.3" TargetTheme="1" FallbackColor="{ThemeResource SystemChromeHighColor}" />
      - Background@Checked:=<SolidColorBrush Color="{ThemeResource SystemAccentColor}" />
      - Margin=0
      - Background@CheckedPointerOver:=<RevealBorderBrush Color="{ThemeResource SystemAccentColorLight1}" TargetTheme="1" FallbackColor="{ThemeResource SystemAccentColorLight1}" />
      - Background@CheckedPressed:=<RevealBorderBrush Color="{ThemeResource SystemAccentColorDark1}" TargetTheme="1" FallbackColor="{ThemeResource SystemAccentColorDark1}" />
      - BorderBrush:=<RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" FallbackColor="{ThemeResource SystemChromeHighColor}" />
      - BorderThickness=1
      - CornerRadius=0
      - Foreground@Checked:=<SolidColorBrush Color="White" />
      - Foreground@CheckedPointerOver:=<SolidColorBrush Color="White" />
      - Foreground@CheckedPressed:=<SolidColorBrush Color="White" />
      - BorderBrush@PointerOver:=<RevealBorderBrush Color="{ThemeResource SystemBaseHighColor}" TargetTheme="1" Opacity="0.7" FallbackColor="{ThemeResource SystemChromeHighColor}" />
      - BorderBrush@Pressed:=<RevealBorderBrush Color="{ThemeResource SystemBaseHighColor}" TargetTheme="1" Opacity="0.2" FallbackColor="{ThemeResource SystemChromeHighColor}" />
      - BorderBrush@CheckedPointerOver:=<RevealBorderBrush Color="{ThemeResource SystemBaseHighColor}" TargetTheme="1" Opacity="0.7" FallbackColor="Transparent" />
      - BorderBrush@CheckedPressed:=<RevealBorderBrush Color="{ThemeResource SystemBaseHighColor}" TargetTheme="1" Opacity="0.2" FallbackColor="Transparent" />
      - Margin@Normal=-1
      - Background@Disabled:=<SolidColorBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.5" />
      - Foreground@Disabled:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.5" />
      - Margin@Disabled=-1
      - BorderBrush@Checked:=<RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" FallbackColor="Transparent" />
  - target: NetworkUX.MainPage > Grid#LogonFrameGrid > Border#LogonFrameBorder > Grid#NetworkFlyoutGrid > ContentControl > ContentPresenter > StackPanel > QuickActions.QuickActionControl > Grid > ContentControl#TemplateRoot > ContentPresenter > QuickActions.EditModeContainer#EditModeContainer > Grid#RootGrid > Grid#ContentGrid > ContentControl#QuickActionContentControl > ContentPresenter > QuickActions.QuickToggleButtonDesktopWinuiFluent#QuickActionUserControl > QuickActions.AccessibleToggleButton#ToggleButton > ContentPresenter#ContentPresenter@CommonStates > Grid
    styles:
      - Margin=-4,-2,-4,0
      - Margin@Normal=-3,-1,-3,1
  - target: Windows.UI.Xaml.Controls.TextBlock#SettingsLinkDescription
    styles:
      - Margin=10,0,0,10
      - Visibility=0
  - target: Windows.UI.Xaml.Controls.HyperlinkButton#SettingsLink
    styles:
      - Margin=10,0,0,-3
  - target: Windows.UI.Xaml.Controls.ContentControl > Windows.UI.Xaml.Controls.ContentPresenter > Windows.UI.Xaml.Controls.StackPanel
    styles:
      - Margin=0
  - target: NetworkUX.MainPage > Grid#LogonFrameGrid > Border#LogonFrameBorder > Grid#NetworkFlyoutGrid > ScrollViewer#MainScrollViewer > Border#Root > Grid > ScrollContentPresenter#ScrollContentPresenter > StackPanel#MainScrollViewerStackPanel > ContentControl > ContentPresenter > StackPanel > ContentControl > ContentPresenter > StackPanel > NetworkUX.View.SettingsListView#WiFiNetworkList > Border > ScrollViewer#ScrollViewer > Border#Root > Grid > ScrollContentPresenter#ScrollContentPresenter > ItemsPresenter > ItemsStackPanel > ListViewItem > Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root
    styles:
      - SelectionIndicatorEnabled=0
  - target: ClockFlyoutExperience.MainPage > ScrollViewer#TopScrollViewer > Border
    styles:
      - BorderBrush:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.17" />
      - BorderThickness=1,1,1,0
  - target: MtcUvc.View.MtcUvcView > StackPanel#MainStackPanel
    styles:
      - BorderBrush:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.17" />
      - BorderThickness=1
  - target: MtcUvc.View.MtcUvcView > StackPanel#MainStackPanel > StackPanel > Border#ScrollBarSeparator
    styles:
      - Visibility=1
  - target: BatteryFlyoutExperience.MainPage#RootMainPage > BatteryFlyoutExperience.BatteryMainPane#MainPane
    styles:
      - BorderBrushProtected:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.17" />
      - BorderThicknessProtected=1,1,1,0
  - target: JumpViewUI.TaskbarJumpListFrame > Grid#JumpListGrid
    styles:
      - BorderBrush:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.17" />
      - BorderThickness=1,1,1,0
  - target: ContentPresenter > ContentControl > ContentPresenter > StackPanel > StackPanel > CheckBox > Grid#RootGrid > Grid > Rectangle#NormalRectangle
    styles:
      - RadiusX=0
      - RadiusY=0
      - Fill=Auto
  - target: ContentControl > ContentPresenter > StackPanel > StackPanel > Button
    styles:
      - Style:=
      - Margin=10
      - CornerRadius=0
      - Width=140
  - target: Button#DisconnectButton
    styles:
      - Style:=
      - Margin=5
      - CornerRadius=0
      - Width=140
  - target: Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > Border
    styles:
      - Margin=0
  - target: Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root
    styles:
      - SelectedBackground:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark1}" />
      - SelectedPointerOverBackground:=<SolidColorBrush Color="{ThemeResource SystemAccentColor}" />
      - SelectedPressedBackground:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark1}" />
      - CornerRadius=0
      - SelectionIndicatorBrush=Transparent
      - SelectionIndicatorPointerOverBrush=Transparent
      - SelectionIndicatorPressedBrush=Transparent
      - PointerOverBackground:=<RevealBorderBrush Color="{ThemeResource SystemChromeHighColor}" TargetTheme="1" Opacity="0.5" FallbackColor="{ThemeResource SystemChromeHighColor}" />
      - PressedBackground:=<RevealBorderBrush Color="{ThemeResource SystemChromeHighColor}" TargetTheme="1" Opacity="0.3" FallbackColor="{ThemeResource SystemChromeHighColor}" />
      - SelectedForeground=White
  - target: StackPanel#DefaultClock > StackPanel > TextBlock
    styles:
      - FontFamily=Segoe UI
  - target: ActionCenter.ActionCenterPage > Grid#RootGrid
    styles:
      - BorderBrush:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.2" />
      - BorderThickness=1,0,0,0
      - Background:=<WindhawkBlur BlurAmount="10" TintColor="{ThemeResource SystemAltHighColor}" TintOpacity="0"/>
      - Margin=0,0,0,0
  - target: ActionCenter.VerbView > Grid > Button#VerbButton > ContentPresenter#ContentPresenter > Grid > TextBlock
    styles:
      - FontSize=14
      - Margin=0
  - target: Border > Frame > ContentPresenter > ActionCenter.ActionCenterPage > Grid > Grid
    styles:
      - 'Transitions:=<TransitionCollection>              <ContentThemeTransition HorizontalOffset="500" />           </TransitionCollection> '
  - target: ActionCenter.ActionCenterPage > Grid#RootGrid > Grid#NotificationCenterGrid > Border
    styles:
      - Visibility=0
  - target: ActionCenter.ActionCenterPage > Grid#RootGrid > Grid#ControlCenterGrid > Border
    styles:
      - Visibility=0
  - target: ActionCenter.ActionCenterPage > Grid > Grid#ActionCenterBackground
    styles:
      - Visibility=1
  - target: ActionCenter.ToastCenterView
    styles:
      - 'Transitions:=<TransitionCollection>              <ContentThemeTransition HorizontalOffset="100000" />           </TransitionCollection> '
  - target: BatteryFlyoutExperience.MainPage#RootMainPage > BatteryFlyoutExperience.BatteryMainPane#MainPane > Border#PowerOverlaySliderPanel
    styles:
      - Visibility=0
  - target: BatteryFlyoutExperience.MainPage#RootMainPage > BatteryFlyoutExperience.BatteryMainPane#MainPane > Border#QuickActionPanel
    styles:
      - Visibility=1
  - target: Grid
    styles:
      - FocusVisualPrimaryThickness=0
      - FocusVisualSecondaryThickness=0
  - target: Button
    styles:
      - FocusVisualPrimaryThickness=0
      - FocusVisualSecondaryThickness=0
  - target: HyperlinkButton
    styles:
      - FocusVisualPrimaryThickness=0
      - FocusVisualSecondaryThickness=0
  - target: Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > StackPanel > ContentControl > ContentPresenter > ContentControl > ContentPresenter > StackPanel > StackPanel > CheckBox
    styles:
      - FocusVisualPrimaryThickness=0
      - FocusVisualSecondaryThickness=0
      - RequestedTheme=1
  - target: ComboBox > Grid#LayoutRoot@CommonStates > Border#Background
    styles:
      - BorderThickness=2
      - Background@Normal:=<SolidColorBrush Color="{ThemeResource SystemAltLowColor}" />
      - BorderBrush:=<SolidColorBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="1" />
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemAltLowColor}" Opacity="0.7" />
      - CornerRadius=0
  - target: Grid#LogonFrameGrid
    styles:
      - Background:=<AcrylicBrush TintColor="{ThemeResource SystemAltHighColor}" TintOpacity="0.6" TintLuminosityOpacity="0" />
      - Margin=43,20,0,0
      - BorderThickness=1,1,1,0
      - BorderBrush:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.17" />
  - target: Microsoft.UI.Xaml.Controls.AnimatedIcon#DropDownGlyph
    styles:
      - Width=15
      - Margin=0,0,10,0
  - target: Border#PopupBorder
    styles:
      - CornerRadius=0
      - Background:=<AcrylicBrush TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.6" TintLuminosityOpacity="0.6" FallbackColor="{ThemeResource SystemChromeMediumColor}" />
      - BorderBrush:=<AcrylicBrush TintColor="{ThemeResource SystemChromeMediumHighColor}" TintOpacity="0.8" TintLuminosityOpacity="0.8" FallbackColor="{ThemeResource SystemChromeLowColor}" />
  - target: ComboBoxItem > Grid@CommonStates
    styles:
      - Background@Selected:=<SolidColorBrush Color="{ThemeResource SystemAccentColor}" />
      - Margin=0
      - CornerRadius=0
      - Background@SelectedPointerOver:=<RevealBorderBrush Color="{ThemeResource SystemAccentColorLight1}" TargetTheme="1" />
      - Background@SelectedPressed:=<RevealBorderBrush Color="{ThemeResource SystemAccentColorDark1}" TargetTheme="1" />
      - Background@PointerOver:=<RevealBorderBrush Color="{ThemeResource SystemChromeMediumHighColor}" Opacity="1" TargetTheme="1" FallbackColor="{ThemeResource SystemChromeMediumHighColor}" />
      - Background@Pressed:=<RevealBorderBrush Color="{ThemeResource SystemChromeMediumHighColor}" Opacity="0.7" TargetTheme="1" FallbackColor="{ThemeResource SystemChromeMediumHighColor}" />
  - target: ComboBoxItem > Grid > Rectangle
    styles:
      - Visibility=1
  - target: PasswordBox#WCNComboPasswordBox > Grid@CommonStates > Border#BorderElement
    styles:
      - BorderThickness=2
      - Background@Normal:=<SolidColorBrush Color="{ThemeResource SystemAltLowColor}" />
      - BorderBrush:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="1" />
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemAltLowColor}" Opacity="0.7" />
      - CornerRadius=0
      - Background@Focused:=<SolidColorBrush Color="White" />
      - BorderBrush@Focused:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark1}" Opacity="1" />
  - target: PasswordBox#WCNComboPasswordBox > Grid@CommonStates
    styles:
      - RequestedTheme@Focused=1
  - target: PasswordBox#PassKeyPasswordBox > Grid@CommonStates > Border#BorderElement
    styles:
      - BorderThickness=2
      - Background@Normal:=<SolidColorBrush Color="{ThemeResource SystemAltLowColor}" />
      - BorderBrush:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="1" />
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemAltLowColor}" Opacity="0.7" />
      - CornerRadius=0
      - Background@Focused:=<SolidColorBrush Color="White" />
      - BorderBrush@Focused:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark1}" Opacity="1" />
  - target: PasswordBox#PassKeyPasswordBox > Grid@CommonStates
    styles:
      - RequestedTheme@Focused=1
  - target: NetworkUX.View.CFEWiFiWCNCombo > StackPanel > StackPanel > Grid > Button
    styles:
      - Style:=
      - Width=144
      - CornerRadius=0
  - target: NetworkUX.View.CFEWiFiPassKey > StackPanel > StackPanel > Grid > Button#NextButton
    styles:
      - Style:=
      - Width=144
      - CornerRadius=0
      - Margin=0,10,0,0
  - target: NetworkUX.MainPage > Grid#LogonFrameGrid > Border#LogonFrameBorder > Grid#NetworkFlyoutGrid > ContentControl > ContentPresenter > StackPanel > QuickActions.QuickActionControl > Grid > ContentControl#TemplateRoot > ContentPresenter > QuickActions.EditModeContainer#EditModeContainer > Grid#RootGrid > Grid#ContentGrid > ContentControl#QuickActionContentControl > ContentPresenter > QuickActions.QuickToggleButtonDesktop#QuickActionUserControl > QuickActions.AccessibleToggleButton#ToggleButton > Grid#RootGrid@CommonStates > Windows.UI.Xaml.Controls.ContentPresenter > Grid > TextBlock
    styles:
      - Foreground@Checked=White
      - Foreground@CheckedPointerOver=White
      - Foreground@CheckedPressed=White
  - target: NetworkUX.MainPage > Grid#LogonFrameGrid > Border#LogonFrameBorder > Grid#NetworkFlyoutGrid > ContentControl > ContentPresenter > StackPanel > QuickActions.QuickActionControl > Grid > ContentControl#TemplateRoot > ContentPresenter > QuickActions.EditModeContainer#EditModeContainer > Grid#RootGrid > Grid#ContentGrid > ContentControl#QuickActionContentControl > ContentPresenter > QuickActions.QuickToggleButtonDesktop#QuickActionUserControl > QuickActions.AccessibleToggleButton#ToggleButton
    styles:
      - CornerRadius=0
  - target: Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > StackPanel > Grid > ContentControl > NetworkUX.View.EntityListItemControl#EntityListItemControl > Grid > TextBlock
    styles:
      - Foreground:=<SolidColorBrush Color="White" Opacity="0.6" />
  - target: Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > StackPanel > Grid > ContentControl > ContentPresenter > HyperlinkButton > ContentPresenter#ContentPresenter > TextBlock
    styles:
      - Foreground=White
  - target: NetworkUX.View.ConnectedNetwork > StackPanel > StackPanel > HyperlinkButton > ContentPresenter#ContentPresenter > TextBlock
    styles:
      - Foreground:=<SolidColorBrush Color="White" Opacity="0.6" />
  - target: ContentControl > ContentPresenter > StackPanel > StackPanel > Button > ContentPresenter@CommonStates
    styles:
      - Background@Normal:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.2"  />
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.5"  />
      - Background@Pressed:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark3}" Opacity="0.2"  />
      - Background@Disabled:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight1}" Opacity="1"  />
      - Foreground=White
      - BorderThickness=0
  - target: Button#DisconnectButton > ContentPresenter@CommonStates
    styles:
      - Background@Normal:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.2"  />
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.5"  />
      - Background@Pressed:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark3}" Opacity="0.2"  />
      - Background@Disabled:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight1}" Opacity="1"  />
      - Foreground=White
      - BorderThickness=0
  - target: NetworkUX.View.CFEWiFiWCNCombo > StackPanel > StackPanel > Grid > Button > ContentPresenter@CommonStates
    styles:
      - Background@Normal:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.2"  />
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.5"  />
      - Background@Pressed:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark3}" Opacity="0.2"  />
      - Background@Disabled:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight1}" Opacity="1"  />
      - Foreground=White
      - BorderThickness=0
  - target: Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > StackPanel > ContentControl > ContentPresenter > ContentControl > ContentPresenter > StackPanel > StackPanel > CheckBox > Grid#RootGrid@CombinedStates > Grid > Rectangle#NormalRectangle
    styles:
      - Fill@CheckedNormal:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.3"  />
      - Fill@CheckedPointerOver:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.5"  />
      - Fill@CheckedPressed:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark3}" Opacity="0.3"  />
      - Stroke=White
      - StrokeThickness@CheckedNormal=0
      - StrokeThickness@CheckedPointerOver=0
      - StrokeThickness@CheckedPressed=0
  - target: Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > StackPanel > ContentControl > ContentPresenter > ContentControl > ContentPresenter > StackPanel > StackPanel > CheckBox > Grid#RootGrid > ContentPresenter#ContentPresenter > TextBlock
    styles:
      - Foreground=White
      - FontSize=15
  - target: Grid#NetworkFlyoutGrid > ScrollViewer#MainScrollViewer > Border#Root > Grid > Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar > Grid#Root > Grid#VerticalRoot > Windows.UI.Xaml.Controls.Primitives.Thumb#VerticalThumb > Rectangle#ThumbVisual
    styles:
      - RadiusX=0
      - Margin=-3,0,-3,0
      - RadiusY=0
      - Opacity=0.6
  - target: Grid#NetworkFlyoutGrid > ScrollViewer#MainScrollViewer > Border#Root > Grid > Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar > Grid#Root > Grid#VerticalRoot > Rectangle
    styles:
      - RadiusX=0
      - RadiusY=0
  - target: Grid#NetworkFlyoutGrid > ScrollViewer#MainScrollViewer > Border#Root > Grid > Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar > Grid#Root > Grid#VerticalRoot > Windows.UI.Xaml.Controls.Primitives.RepeatButton#VerticalSmallIncrease > Grid#Root > FontIcon#Arrow > Grid > TextBlock
    styles:
      - FontFamily=Segoe MDL2 Assets
      - Text=
      - FontSize=7
      - Foreground:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" />
      - FontWeight=SemiBold
  - target: Grid#NetworkFlyoutGrid > ScrollViewer#MainScrollViewer > Border#Root > Grid > Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar > Grid#Root > Grid#VerticalRoot > Windows.UI.Xaml.Controls.Primitives.RepeatButton#VerticalSmallDecrease > Grid#Root > FontIcon#Arrow > Grid > TextBlock
    styles:
      - FontFamily=Segoe MDL2 Assets
      - Text=
      - Foreground:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" />
      - FontSize=7
      - FontWeight=SemiBold
  - target: Grid#NetworkFlyoutGrid > ScrollViewer#MainScrollViewer > Border#Root > Grid > Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar > Grid#Root > Grid#VerticalRoot > Windows.UI.Xaml.Controls.Primitives.RepeatButton#VerticalSmallDecrease > Grid#Root@CommonStates
    styles:
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.4"  />
      - Background@Pressed:=<SolidColorBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.3"  />
      - Background@Disabled:=<SolidColorBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.4"  />
  - target: Grid#NetworkFlyoutGrid > ScrollViewer#MainScrollViewer > Border#Root > Grid > Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar > Grid#Root > Grid#VerticalRoot > Windows.UI.Xaml.Controls.Primitives.RepeatButton#VerticalSmallIncrease > Grid#Root@CommonStates
    styles:
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.4"  />
      - Background@Pressed:=<SolidColorBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.3"  />
      - Background@Disabled:=<SolidColorBrush Color="{ThemeResource SystemChromeHighColor}" Opacity="0.4"  />
  - target: Grid#NetworkFlyoutGrid > ScrollViewer#MainScrollViewer > Border#Root > Grid > Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar > Grid#Root > Grid#VerticalRoot > Windows.UI.Xaml.Controls.Primitives.RepeatButton#VerticalSmallDecrease > Grid#Root > FontIcon#Arrow
    styles:
      - Margin=0,0,0,3
  - target: Grid#NetworkFlyoutGrid > ScrollViewer#MainScrollViewer > Border#Root > Grid > Windows.UI.Xaml.Controls.Primitives.ScrollBar#VerticalScrollBar > Grid#Root > Grid#VerticalRoot > Windows.UI.Xaml.Controls.Primitives.RepeatButton#VerticalSmallIncrease > Grid#Root > FontIcon#Arrow
    styles:
      - Margin=0,3,0,0
  - target: Button#NextButton > ContentPresenter@CommonStates
    styles:
      - Background@Normal:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.2"  />
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.5"  />
      - Background@Pressed:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark3}" Opacity="0.2"  />
      - Background@Disabled:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight2}" Opacity="1"  />
      - Foreground=White
      - BorderThickness=0
  - target: NetworkUX.View.CFEWiFiPassKey > StackPanel > StackPanel > Grid > Button
    styles:
      - Style:=
      - Width=144
      - CornerRadius=0
      - Margin=0,10,0,0
  - target: NetworkUX.View.CFEWiFiPassKey > StackPanel > StackPanel > Grid > Button > ContentPresenter@CommonStates
    styles:
      - Background@Normal:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.2"  />
      - Background@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="0.5"  />
      - Background@Pressed:=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark3}" Opacity="0.2"  />
      - Background@Disabled:=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight2}" Opacity="1"  />
      - Foreground=White
      - BorderThickness=0
  - target: TextBlock
    styles:
      - FontFamily=Segoe UI, Segoe MDL2 Assets, Core UX MDL2 Assets
  - target: FontIcon > Grid > TextBlock
    styles:
      - FontFamily=Segoe MDL2 Assets
  - target: NetworkUX.View.EntityListItemControl#EntityListItemControl > Grid > ContentControl > ContentPresenter > Grid > FontIcon > Grid > TextBlock
    styles:
      - FontFamily=Segoe Fluent Icons
  - target: Windows.UI.Xaml.Controls.Grid#JumpListGrid
    styles:
      - Margin=0,0,0,0
      - CornerRadius=0
      - Width=256
  - target: Windows.UI.Xaml.Controls.Border#JumpListRestyledAcrylic
    styles:
      - Visibility=1
  - target: JumpViewUI.SystemItemListView#SystemItemList
    styles:
      - Width=256
  - target: JumpViewUI.TaskbarJumpListFrame
    styles:
      - Width=256
  - target: JumpViewUI.JumpListListView#ItemList
    styles:
      - Width=256
      - Padding=0,5,0,5
  - target: JumpViewUI.JumpListItemControl > Grid#GridForContextMenuInvoke_MustHave_No_Columns_Or_Rows > Grid#LayoutRoot > Button
    styles:
      - Width=30
      - Height=30
  - target: JumpViewUI.JumpListListViewItem
    styles:
      - Margin=0,0,0,0
      - Height=30
  - target: JumpViewUI.SystemItemListViewItem
    styles:
      - Margin=0,0,0,0
      - Height=30
  - target: JumpViewUI.SystemItemListViewItem > Windows.UI.Xaml.Controls.Grid#LayoutRoot@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=0
      - Background@PointerOver:=<RevealBorderBrush Color="{ThemeResource SystemListMediumColor}" TargetTheme="1" Opacity="0.8" FallbackColor="{ThemeResource SystemListLowColor}"/>
      - Background@Pressed:=<RevealBorderBrush Color="{ThemeResource SystemListMediumColor}" TargetTheme="1" Opacity="0.6" FallbackColor="{ThemeResource SystemListLowColor}" />
      - BorderBrush@PointerOver:=<RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" />
      - BorderBrush@Pressed:=<RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" />
      - BorderThickness=1,1,1,1
  - target: JumpViewUI.JumpListListViewItem > Windows.UI.Xaml.Controls.Grid#LayoutRoot@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=0
      - Background@PointerOver:=<RevealBorderBrush Color="{ThemeResource SystemListMediumColor}" TargetTheme="1" Opacity="0.8" FallbackColor="{ThemeResource SystemListLowColor}"/>
      - Background@Pressed:=<RevealBorderBrush Color="{ThemeResource SystemListMediumColor}" TargetTheme="1" Opacity="0.6" FallbackColor="{ThemeResource SystemListLowColor}" />
      - BorderBrush@PointerOver:=<RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" />
      - BorderBrush@Pressed:=<RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" />
      - BorderThickness=1,1,1,1
  - target: JumpViewUI.JumpListItemControl > Grid#GridForContextMenuInvoke_MustHave_No_Columns_Or_Rows > Grid#LayoutRoot > Button > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Grid#SystemItemsContainer > Windows.UI.Xaml.Shapes.Rectangle
    styles:
      - Visibility=1
  - target: Windows.UI.Xaml.Controls.Grid#SystemItemsContainer
    styles:
      - Padding=0,5,0,5
  - target: JumpViewUI.JumpListListViewItem > Windows.UI.Xaml.Controls.Grid#LayoutRoot > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter > Windows.UI.Xaml.Controls.Grid#LayoutRoot > Windows.UI.Xaml.Shapes.Rectangle
    styles:
      - Margin=12,4,12,4
  - target: JumpViewUI.JumpListControl#JumpList
    styles:
      - Margin=0,0,0,0
  - target: Windows.UI.Xaml.Controls.Button#PinButton > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - Background@PointerOver:=<AcrylicBrush TintColor="{ThemeResource SystemListLowColor}" TintOpacity="1" Opacity="0.5" FallbackColor="{ThemeResource SystemListLowColor}"/>
      - Background@Pressed:=<AcrylicBrush TintColor="{ThemeResource SystemListLowColor}" TintOpacity="1" Opacity="0.9" FallbackColor="{ThemeResource SystemListMediumColor}"/>
      - CornerRadius=0
  - target: Windows.UI.Xaml.Controls.Border#JumpListAcrylic
    styles:
      - Visibility=0
  - target: Windows.UI.Xaml.Controls.Grid#SystemItemsContainer > Windows.UI.Xaml.Controls.Border#SystemItemsAcrylic
    styles:
      - Visibility=0
      - Margin=0,-5,0,-5
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - CornerRadius=0
      - Background:=<AcrylicBrush TintColor="{ThemeResource SystemAltHighColor}" TintOpacity="0.85" FallbackColor="{ThemeResource SystemChromeMediumColor}" />
  - target: Windows.UI.Xaml.Controls.MenuFlyoutItem
    styles:
      - CornerRadius=0
  - target: Windows.UI.Xaml.Controls.MenuFlyoutItem > Grid
    styles:
      - BorderThickness=1,1,1,1
      - Margin=0
  - target: JumpViewUI.SystemItemControl > Grid > Grid > TextBlock
    styles:
      - Margin=0,-2,0,0
  - target: Windows.UI.Xaml.Controls.TextBlock#DisplayNameTextBlock
    styles:
      - FontSize=12
  - target: JumpViewUI.JumpListCategoryHeaderControl > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBlock#HeadingTextBlock
    styles:
      - Margin=12,10,12,6
  - target: MenuFlyoutItem > Grid@CommonStates
    styles:
      - CornerRadius=0
      - Background@PointerOver:=<RevealBorderBrush Color="{ThemeResource SystemListMediumColor}" TargetTheme="1" Opacity="0.8" FallbackColor="{ThemeResource SystemListLowColor}"/>
      - Background@Pressed:=<RevealBorderBrush Color="{ThemeResource SystemListMediumColor}" TargetTheme="1" Opacity="0.6" FallbackColor="{ThemeResource SystemListLowColor}" />
      - BorderBrush@PointerOver:=<RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" />
      - BorderBrush@Pressed:=<RevealBorderBrush Color="Transparent" TargetTheme="1" Opacity="1" />
      - BorderThickness=1,1,1,1
  - target: Grid#NetworkFlyoutGrid > HyperlinkButton#SettingsLink > ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Background=Transparent
      - Foreground@PointerOver:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.8" />
      - Foreground@Pressed:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.4" />
  - target: Border#DevicesFlowFrameRepaintHeader > Grid > StackPanel > Border > FontIcon > Grid
    styles:
      - Background:=<ImageBrush Stretch="UniformToFill" ImageSource="C:\Windows\System32\@WLOGO_96x96.png" />
      - Margin=-.5,1,0,0
      - RenderTransform:=<ScaleTransform ScaleX="1.2" ScaleY="1.1" />
  - target: ClockFlyoutExperience.FirstRunView#FirstRunControl > Grid > FontIcon > Grid > TextBlock
    styles:
      - Text=
      - FontFamily=Segoe MDL2 Assets
      - FontWeight=SemiBold
      - FontSize=23.4
  - target: Border#DevicesFlowFrameRepaintHeader > Grid > StackPanel > Border > FontIcon
    styles:
      - Foreground=Transparent
  - target: MenuFlyoutSeparator > Rectangle
    styles:
      - Margin=12,5,12,5
      - Fill:=<SolidColorBrush Color="{ThemeResource SystemBaseHighColor}" Opacity="0.4" />
  - target: ToolTip
    styles:
      - CornerRadius=0
styleConstants:
  - ''
themeResourceVariables:
  - ''
```
</details>
