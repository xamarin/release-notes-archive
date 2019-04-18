---
id: 887F4C27-4906-4E0C-8EED-8455B2F98AD7
title: "Xamarin.Forms 1.1"
---

# Xamarin.Forms 1.1.1

1.1.1 is a bug-fix release. There are few features in Xamarin.Forms 1.1.1 over 1.1.0.

## Features

- SearchBar.Text is now BindingMode.TwoWay by default
- iOS VisualElementRenderer can now be subclassed by users
- Small Layout performance boost

## Bug Fixes

- Android cells text now lays out appropriately, centering when no detail is set.
- Android EntryCell no longer vertically squished
- On Android MasterDetailPage.Master now correctly sets icon for back arrow
- ActionBar now hides correctly on KitKat
- Images with a UriImageSource inside of a ListView or TableView should no longer crash
- Performance tweaks for android ViewCells introduced in 1.0.1 and accidentally disabled in 1.1.0 are now re-enabled.
- CarouselPage's using templated item sources should no longer crash when resetting source
- AndroidActivity.SetPage now correctly supports being called multiple times to change page contents
- Fix crash on windows phone with TwoWay binding to ListView.SelectedItem
- iOS toolbar items now use retina icons properly (no more fuzzy)
- Fix binding warning spew when creating listviews from xaml
- GroupHeaderTemplates are no longer bindable as binding and binding made so very little sense
- ToolbarItems now inherit their parent pages binding context
- Setting ToolbarItem.Name in XAML will no longer result in build errors

