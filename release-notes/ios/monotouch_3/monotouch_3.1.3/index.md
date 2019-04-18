---
id: 9CB480B0-B753-0E8E-D06F-953C41C8BD1D
title: "MonoTouch 3.1.3"
---

&nbsp;

This is a minor update fixing a few customer reported bugs:

-  HMACSHA1 backend is now always included whenever you use this class (previously it was brought in only if you included http/https support). 
-  Fixed a crash using CGPath.Apply on device.
-  Fixed a invalid data return using CGPath.Apply.
-  Fixed an error in the GKAchievementViewController.Delegate binding.
-  Fixed a number of issues with 3.1.2 and the iOS 3.2 SDK -   Loading the proper simulator.
