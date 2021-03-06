---
id: 8958BDDC-11E5-4735-9FE3-CD82031BEDDE
title: "Xamarin.Forms 1.2"
---

# Xamarin.Forms 1.2.3

## Important Notes
In this release we have changed the base class of Entry from a ViewRenderer<Entry, Canvas> to a ViewRenderer<Entry, Grid>. While it is unlikely anyone depends on this behavior, if you do you will need to update your code.

Further in 1.3.0 (the next major release) we will be changing the default Grid row and column definitions to use Star instead of Auto. While it is unlikely, if you currently depend on the default of Auto, you should hardcode the value in preparation for the change.

## Enhancements:

### Android

- Image/ImageCell will no longer reload images when the ImageSource instance is the same for a reused element.
- Minor memory improvements when reusing elements (ListView).
- ListView performance increase. Especially when dealing with lots of labels or nested layouts.

## Bug fixes:

### Core

- Fixed an NullReferenceException creating a ResourceDictionary.
- Fixed layout issues in Grid with ColSpan/RowSpan ([Bugzilla 23152](https://bugzilla.xamarin.com/show_bug.cgi?id=23152)).
- Entry no longer clears one way bindings when the user enters text
- BindableObject.ClearValue now properly triggers INPC

### iOS

- ImageCells no longer occasionally get reused for TextCells.
- Fixed an NullReferenceException for Editor.
- Fixed calling PopToRootAsync throwing NullReferenceException ([Bugzilla 23234](https://bugzilla.xamarin.com/show_bug.cgi?id=23234)).
- Fixed SearchButtonPressed firing for Cancel ([Bugzilla 23235](https://bugzilla.xamarin.com/show_bug.cgi?id=23235)).
- Fixed ListView not respecting BackgroundColor ([Bugzilla 23056](https://bugzilla.xamarin.com/show_bug.cgi?id=23056)).
- Fixed a crash with DisplayActionSheet on iOS 8 ([Bugzilla 23358](https://bugzilla.xamarin.com/show_bug.cgi?id=23358)).
- Fixed ScrollView measurement.
- Fixed intermittent rotation layout issues with MasterDetailPage ([Bugzilla 21950](https://bugzilla.xamarin.com/show_bug.cgi?id=21950)).
- ActionSheet no longer fails to send result in some situations
- Pushing pages from custom renderers using native APIs no longer confuses the NavigationRenderer
- Editor.Focus now works correctly
- Editor.UnFocus now works correctly
- Editor.IsEnabled now properly disables editing
- Fix crash introduced in 1.2.3-pre2 when navigating using MasterDetailPage
- Fix memory leak when changing pages using Master pane in MasterDetailPage
- Secondary toolbar items will now clear properly and are sorted correctly
- MapRenderer is now public
- ScrollView will no longer exceed its bounds (extension of previous fix to include more cases)
- Resolve a major memory leak when popping pages from Navigation stack
- ContentPage inside of a NavigationPage inside of TabbedPage will no longer incorrectly set the tab title from the ContentPage

### Android
- Fixed Focused/Unfocused events for SearchBar ([Bugzilla 23296](https://bugzilla.xamarin.com/show_bug.cgi?id=23296)).
- Fixed issue with label truncation.
- Fixed a crash with ScrollViews instances being reused.
- Fixed software keyboard not responding to Focus ([Bugzilla 21862](https://bugzilla.xamarin.com/show_bug.cgi?id=21862)).
- SwitchRenderer no longer causes crashing with Navigation
- ListView selected background color now properly cleared
- Image loading reset on ImageCell
- Fix edge case where images were not loaded asynchronously in ListView
- Images no longer trigger useless layout cycle when re-used in ListView
- Minor ListView performance improvements
- ListView background color will no longer throw a NotFoundException in some cases
- Fix a GREF leak when dismissing keyboard (performance and memory leak)
- Keyboard now properly hides when calling Entry.Unfocus
- ScrollView will no longer crash when inside of a ViewCell
- ListView background and divider color is now based on the theme color
- ScrollView children will no longer flow outside of ScrollView bounds
- Setting MasterDetailPage.Detail should now dispose old Detail properly
- Reshowing an existing ListView will no longer crash on selection
- Fix crash in ImageRenderer during dispose cycle

### Windows Phone

- Fixed RotationX/Y to match Android/iOS.
- Fixed MapType ([Bugzilla 22737](https://bugzilla.xamarin.com/show_bug.cgi?id=22737)).
- Fixed too many toolbars crash.
- Switch.IsEnabled property now works correctly
- Secondary toolbar items no longer occasionally duplicate themselves
- MapRenderer is now public
- Calling Picker.Items.Clear no longer crashes
- Entry's inside of a ViewCell will no longer incorrectly horizontally minimize
- Add support for ApplicationId and AuthToken to FormsMaps.Init (string, string), old overload remains for testing
- EntryCell now properly supports IsEnabled

### XAML

- Fix error when saving xaml file in Xamarin Studio on Windows where the file is locked by another process
- BindableObject can now be used as a root element in XAML, not just VisualElements. Allows creating ViewCells as root objects.

