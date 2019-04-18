---
id: 0EE7B1A2-666B-41ED-B506-339FE6AC9891
title: "Xamarin.Forms 1.0"
---

# Xamarin.Forms 1.0.1

##Important Notes

- Android ListView performance improved significantly when using `ViewCell`. More improvements in the works.
- Xamarin.Forms.Platform.WinPhone.ButtonRenderer now public instead of internal.
- Pages added to MasterDetailPage.Master must have their Icon property set or an exception will be thrown when adding.
- Android ActionBar no longer uses a gradient
- EntryCell.Text property is now a default TwoWay binding
- Stepper.Value is now a default TwoWay binding
- More API documentation has been added
- ConcurrentDictionary is no longer exposed in the API

##Bug Fixes

- Easing.BounceIn now plays in the correct direction
- [Xaml] Creation of non-primitives (e.g. Color) from a string now works
- [iOS] Picker types now receive and respond to focus events/methods correctly
- [Andorid] Picker types now receive and respond to focus events/methods correctly
- [Xaml] No longer fail on clr-namespace (allow using external libs correctly)
- TimePicker.FormatProperty declaration no longer declares as a child of DatePicker
- TabbedPage and CarouselPage children now settable in XAML without using <TabbedPage.Children>
- [Android] CarouselPage now properly selects the first page when requested.
- [Windows Phone] Popping a modal page while the master page of MasterDetailPage is open no longer leaves the master page open.
- [iOS] Setting button background color on iOS 6 no longer leaves the top part of the default border in place
- [iOS] No longer crash on empty icon path in ToolbarItem
- [Windows Phone] Properly handled queued pushes at app startup
- [Android] ActionBar no longer clobbers theme background drawable
- [Android] Several memory leaks plugged
- [iOS] Labels no longer truncate when relayed out in a constrained layout such as a Grid
- [Android] SearchBar now reacts to focus members correctly
- [Android] SearchBar no longer auto-focuses causing keyboard to display
- ImageSource now correctly converts absolute path strings into FileImageSource's
- [iOS] NavigationBar hidden/shown transition now incredibly more smooth
- [iOS] EntryCell.IsEnabled works

