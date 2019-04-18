---
id: 6420E690-0023-9445-1D09-057A9160D703
title: "From 3.1.3 to 3.2"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

&nbsp;

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif" style=""></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public const string Version = "3.1.3";
```

Added:

```
public const string Version = "3.2.0";
        public const string ImageIOLibrary = "/System/Library/Frameworks/ImageIO.framework/ImageIO";
        public const string AssetsLibraryLibrary = "/System/Library/Frameworks/AssetLibrary.framework/AssetLibrary";
        public const string CoreVideoLibrary = "/System/Library/Frameworks/CoreVideo.framework/CoreVideo";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAsset

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual bool ProtectedContent {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetExportSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetExportSession

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static MonoTouch.Foundation.NSString Preset1280x720 {
                get;
        }
        public static MonoTouch.Foundation.NSString Preset640x480 {
                get;
        }
        public static MonoTouch.Foundation.NSString Preset960x540 {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetAppleM4A {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetHighestQuality {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetLowQuality {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetMediumQuality {
                get;
        }
        public static MonoTouch.Foundation.NSString PresetPassthrough {
                get;
        }
        public virtual MonoTouch.Foundation.NSError Error {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetExportSessionStatus" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetExportSessionStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
Waiting,
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMetadataItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMetadataItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual MonoTouch.CoreMedia.CMTime Duration {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableMetadataItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMutableMetadataItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual MonoTouch.CoreMedia.CMTime Duration {
                get;
        }
```

 <a name="Namespace:_MonoTouch.AddressBookUI" class="injected"></a>


# Namespace: MonoTouch.AddressBookUI

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationControllerDelegate 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public override void DidShowViewController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewController viewController, bool animated);
        public override void WillShowViewController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewController viewController, bool animated);
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.AssetsLibrary.ALAsset" class="injected"></a>


## New Type: MonoTouch.AssetsLibrary.ALAsset

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class ALAsset : MonoTouch.Foundation.NSObject {
        
        public ALAsset ();
        public ALAsset (MonoTouch.Foundation.NSCoder coder);
        public ALAsset (MonoTouch.Foundation.NSObjectFlag t);
        public ALAsset (IntPtr handle);
        
        public virtual ALAssetRepresentation RepresentationForUti (string uti);
        public virtual MonoTouch.Foundation.NSObject ValueForProperty (MonoTouch.Foundation.NSString property);
        
        public ALAssetType AssetType {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public MonoTouch.Foundation.NSDate Date {
                get;
        }
        public virtual ALAssetRepresentation DefaultRepresentation {
                get;
        }
        public double Duration {
                get;
        }
        public MonoTouch.CoreLocation.CLLocation Location {
                get;
        }
        public ALAssetOrientation Orientation {
                get;
        }
        public string [] Representations {
                get;
        }
        public virtual MonoTouch.CoreGraphics.CGImage Thumbnail {
                get;
        }
        public MonoTouch.Foundation.NSDictionary UtiToUrlDictionary {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AssetsLibrary.ALAssetOrientation" class="injected"></a>


## New Type: MonoTouch.AssetsLibrary.ALAssetOrientation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum ALAssetOrientation {
        Up,
        Down,
        Left,
        Right,
        UpMirrored,
        DownMirrored,
        LeftMirrored,
        RightMirrored
}
```

 <a name="New_Type:_MonoTouch.AssetsLibrary.ALAssetRepresentation" class="injected"></a>


## New Type: MonoTouch.AssetsLibrary.ALAssetRepresentation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class ALAssetRepresentation : MonoTouch.Foundation.NSObject {
        
        public ALAssetRepresentation ();
        public ALAssetRepresentation (MonoTouch.Foundation.NSCoder coder);
        public ALAssetRepresentation (MonoTouch.Foundation.NSObjectFlag t);
        public ALAssetRepresentation (IntPtr handle);
        
        public virtual uint GetBytes (IntPtr buffer, long offset, uint length, out MonoTouch.Foundation.NSError error);
        public virtual MonoTouch.CoreGraphics.CGImage GetFullScreenImage ();
        public virtual MonoTouch.CoreGraphics.CGImage GetImage ();
        public virtual MonoTouch.CoreGraphics.CGImage GetImage (MonoTouch.Foundation.NSDictionary options);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary Metadata {
                get;
        }
        public virtual ALAssetOrientation Orientation {
                get;
        }
        public virtual float Scale {
                get;
        }
        public virtual long Size {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl Url {
                get;
        }
        public virtual string Uti {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AssetsLibrary.ALAssetsEnumerator" class="injected"></a>


## New Type: MonoTouch.AssetsLibrary.ALAssetsEnumerator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public delegate void ALAssetsEnumerator (ALAsset result, int index, ref bool stop);
```

 <a name="New_Type:_MonoTouch.AssetsLibrary.ALAssetsFilter" class="injected"></a>


## New Type: MonoTouch.AssetsLibrary.ALAssetsFilter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class ALAssetsFilter : MonoTouch.Foundation.NSObject {
        
        public ALAssetsFilter ();
        public ALAssetsFilter (MonoTouch.Foundation.NSCoder coder);
        public ALAssetsFilter (MonoTouch.Foundation.NSObjectFlag t);
        public ALAssetsFilter (IntPtr handle);
        
        public static ALAssetsFilter AllAssets {
                get;
        }
        public static ALAssetsFilter AllPhotos {
                get;
        }
        public static ALAssetsFilter AllVideos {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AssetsLibrary.ALAssetsGroup" class="injected"></a>


## New Type: MonoTouch.AssetsLibrary.ALAssetsGroup

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class ALAssetsGroup : MonoTouch.Foundation.NSObject {
        
        public ALAssetsGroup ();
        public ALAssetsGroup (MonoTouch.Foundation.NSCoder coder);
        public ALAssetsGroup (MonoTouch.Foundation.NSObjectFlag t);
        public ALAssetsGroup (IntPtr handle);
        
        public virtual void Enumerate (ALAssetsEnumerator result);
        public virtual void Enumerate (MonoTouch.Foundation.NSEnumerationOptions options, ALAssetsEnumerator result);
        public virtual void Enumerate (MonoTouch.Foundation.NSIndexSet indexSet, MonoTouch.Foundation.NSEnumerationOptions options, ALAssetsEnumerator result);
        public virtual void SetAssetsFilter (ALAssetsFilter filter);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual int Count {
                get;
        }
        public MonoTouch.Foundation.NSString Name {
                get;
        }
        public string PersistentID {
                get;
        }
        public virtual MonoTouch.CoreGraphics.CGImage PosterImage {
                get;
        }
        public ALAssetsGroupType Type {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AssetsLibrary.ALAssetsGroupType" class="injected"></a>


## New Type: MonoTouch.AssetsLibrary.ALAssetsGroupType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
[Flags]
public enum ALAssetsGroupType : uint {
        Library,
        Album,
        Event,
        Faces,
        SavedPhotos,
        All
}
```

 <a name="New_Type:_MonoTouch.AssetsLibrary.ALAssetType" class="injected"></a>


## New Type: MonoTouch.AssetsLibrary.ALAssetType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum ALAssetType {
        Video,
        Photo,
        Unknown
}
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioBuffer" class="injected"></a>


## New Type: MonoTouch.AudioToolbox.AudioBuffer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public struct AudioBuffer {
        
        public override string ToString ();
        
        public int NumberChannels;
        public int DataByteSize;
        public IntPtr Data;
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioBufferList" class="injected"></a>


## New Type: MonoTouch.AudioToolbox.AudioBufferList

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class AudioBufferList {
        
        public AudioBufferList ();
        
        public override string ToString ();
        
        public int BufferCount {
                get;
        }
        public AudioBuffer[] Buffers {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AudioToolbox.MutableAudioBufferList" class="injected"></a>


## New Type: MonoTouch.AudioToolbox.MutableAudioBufferList

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class MutableAudioBufferList : AudioBufferList, IDisposable {
        
        public MutableAudioBufferList (int nubuffers, int bufferSize);
        
        public void Dispose ();
        public virtual void Dispose (bool disposing);
        protected override void Finalize ();
}
```

 <a name="Namespace:_MonoTouch.AudioUnit" class="injected"></a>


# Namespace: MonoTouch.AudioUnit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.AudioUnit.AudioComponent" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioComponent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class AudioComponent : MonoTouch.ObjCRuntime.INativeObject {
        
        public static AudioComponent FindComponent (AudioComponentDescription cd);
        public static AudioComponent FindComponent (AudioTypeConverter conveter);
        public static AudioComponent FindComponent (AudioTypeEffect effect);
        public static AudioComponent FindComponent (AudioTypeGenerator generator);
        public static AudioComponent FindComponent (AudioTypeMixer mixer);
        public static AudioComponent FindComponent (AudioTypeMusicDevice musicDevice);
        public static AudioComponent FindComponent (AudioTypeOutput output);
        public static AudioComponent FindComponent (AudioTypePanner panner);
        public static AudioComponent FindNextComponent (AudioComponent cmp, AudioComponentDescription cd);
        public AudioUnit CreateAudioUnit ();
        
        public AudioComponentDescription Description {
                get;
        }
        public IntPtr Handle {
                get;
        }
        public string Name {
                get;
        }
        public Version Version {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioComponentDescription" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioComponentDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class AudioComponentDescription {
        
        public AudioComponentDescription ();
        
        public static AudioComponentDescription CreateConverter (AudioTypeConverter converter);
        public static AudioComponentDescription CreateEffect (AudioTypeEffect effect);
        public static AudioComponentDescription CreateGenerator (AudioTypeGenerator generator);
        public static AudioComponentDescription CreateGeneric (AudioComponentType type, int subType);
        public static AudioComponentDescription CreateMixer (AudioTypeMixer mixer);
        public static AudioComponentDescription CreateMusicDevice (AudioTypeMusicDevice musicDevice);
        public static AudioComponentDescription CreateOutput (AudioTypeOutput outputType);
        public static AudioComponentDescription CreatePanner (AudioTypePanner panner);
        public override string ToString ();
        
        public AudioComponentType ComponentType;
        public int ComponentSubType;
        public AudioComponentManufacturerType ComponentManufacturer;
        public int ComponentFlags;
        public int ComponentFlagsMask;
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioComponentManufacturerType" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioComponentManufacturerType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioComponentManufacturerType {
        Apple
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioComponentType" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioComponentType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioComponentType {
        Output,
        MusicDevice,
        MusicEffect,
        FormatConverter,
        Effect,
        Mixer,
        Panner,
        OfflineEffect,
        Generator
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioGraphEventArgs" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioGraphEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class AudioGraphEventArgs : AudioUnitEventArgs {
        
        public AudioGraphEventArgs (AudioUnitRenderActionFlags actionFlags, MonoTouch.AudioToolbox.AudioTimeStamp timeStamp, int busNumber, int numberFrames, MonoTouch.AudioToolbox.AudioBufferList data);
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioTypeConverter" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioTypeConverter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioTypeConverter {
        AU,
        AUiPodTime
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioTypeEffect" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioTypeEffect

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioTypeEffect {
        AUiPodEQ
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioTypeGenerator" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioTypeGenerator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioTypeGenerator {
        
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioTypeMixer" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioTypeMixer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioTypeMixer {
        MultiChannel,
        Embedded3D
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioTypeMusicDevice" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioTypeMusicDevice

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioTypeMusicDevice {
        None
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioTypeOutput" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioTypeOutput

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioTypeOutput {
        Generic,
        Remote,
        VoiceProcessingIO
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioTypePanner" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioTypePanner

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioTypePanner {
        
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioUnit" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioUnit

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class AudioUnit : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public AudioUnit (AudioComponent component);
        
        public void Dispose ();
        public void Dispose (bool disposing);
        public MonoTouch.AudioToolbox.AudioStreamBasicDescription GetAudioFormat (AudioUnitScopeType scope, uint audioUnitElement);
        public int Initialize ();
        public void Render (AudioUnitRenderActionFlags flags, MonoTouch.AudioToolbox.AudioTimeStamp timeStamp, int outputBusnumber, int numberFrames, MonoTouch.AudioToolbox.AudioBufferList data);
        public void SetAudioFormat (MonoTouch.AudioToolbox.AudioStreamBasicDescription audioFormat, AudioUnitScopeType scope, uint audioUnitElement);
        public void SetEnableIO (bool enableIO, AudioUnitScopeType scope, uint audioUnitElement);
        public void Start ();
        public void Stop ();
        public AudioUnitStatus TryRender (AudioUnitRenderActionFlags flags, MonoTouch.AudioToolbox.AudioTimeStamp timeStamp, int outputBusnumber, int numberFrames, MonoTouch.AudioToolbox.AudioBufferList data);
        public int Uninitialize ();
        
        public AudioComponent Component {
                get;
        }
        public IntPtr Handle {
                get;
        }
        public bool IsPlaying {
                get;
        }
        
        public event EventHandler<audiouniteventargs> RenderCallback; } </audiouniteventargs>
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioUnitEventArgs" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioUnitEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class AudioUnitEventArgs : EventArgs {
        
        public AudioUnitEventArgs (AudioUnitRenderActionFlags actionFlags, MonoTouch.AudioToolbox.AudioTimeStamp timestamp, int busNumber, int frames, MonoTouch.AudioToolbox.AudioBufferList data);
        
        public readonly AudioUnitRenderActionFlags ActionFlags;
        public readonly MonoTouch.AudioToolbox.AudioTimeStamp TimeStamp;
        public readonly int BusNumber;
        public readonly int NumberFrames;
        public readonly MonoTouch.AudioToolbox.AudioBufferList Data;
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioUnitException" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioUnitException

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class AudioUnitException : Exception {
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioUnitPropertyIDType" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioUnitPropertyIDType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioUnitPropertyIDType {
        ClassInfo,
        MakeConnection,
        SampleRate,
        ParameterList,
        ParameterInfo,
        StreamFormat,
        ElementCount,
        Latency,
        SupportedNumChannels,
        MaximumFramesPerSlice,
        AudioChannelLayout,
        TailTime,
        BypassEffect,
        LastRenderError,
        SetRenderCallback,
        FactoryPresets,
        RenderQuality,
        InPlaceProcessing,
        ElementName,
        SupportedChannelLayoutTags,
        PresentPreset,
        ShouldAllocateBuffer,
        CurrentDevice,
        ChannelMap,
        EnableIO,
        StartTime,
        SetInputCallback,
        HasIO,
        StartTimestampsAtZero
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioUnitRenderActionFlags" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioUnitRenderActionFlags

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
[Flags]
public enum AudioUnitRenderActionFlags {
        PreRender,
        PostRender,
        OutputIsSilence,
        OfflinePreflight,
        OfflineRender,
        OfflineComplete,
        PostRenderError
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioUnitScopeType" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioUnitScopeType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioUnitScopeType {
        Global,
        Input,
        Output
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioUnitStatus" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioUnitStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum AudioUnitStatus {
        NoError,
        ParameterError,
        InvalidProperty,
        InvalidParameter,
        InvalidElement,
        NoConnection,
        FailedInitialization,
        TooManyFramesToProcess,
        InvalidFile,
        FormatNotSupported,
        Uninitialized,
        InvalidScope,
        PropertyNotWritable,
        CannotDoInCurrentContext,
        InvalidPropertyValue,
        PropertyNotInUse,
        Initialized,
        InvalidOfflineRender,
        Unauthorized
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AudioUnitUtils" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AudioUnitUtils

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public static class AudioUnitUtils {
        
        public static MonoTouch.AudioToolbox.AudioStreamBasicDescription AUCanonicalASBD (double sampleRate, int channel);
        public static void SetOverrideCategoryDefaultToSpeaker (bool isSpeaker);
        
        public const int SampleFractionBits = 24;
}
```

 <a name="New_Type:_MonoTouch.AudioUnit.AUGraph" class="injected"></a>


## New Type: MonoTouch.AudioUnit.AUGraph

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class AUGraph : IDisposable {
        
        public AUGraph ();
        
        public int AddNode (AudioComponentDescription cd);
        public void ConnnectNodeInput (int inSourceNode, uint inSourceOutputNumber, int inDestNode, uint inDestInputNumber);
        public void Dispose ();
        public virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public AudioUnit GetNodeInfo (int node);
        public void Initialize ();
        public void Open ();
        public void Start ();
        public void Stop ();
        public int TryOpen ();
        
        public IntPtr Handler {
                get;
        }
        
        public event EventHandler<audiographeventargs> RenderCallback; } </audiographeventargs>
```

 <a name="New_Type:_MonoTouch.AudioUnit.ExtAudioFile" class="injected"></a>


## New Type: MonoTouch.AudioUnit.ExtAudioFile

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class ExtAudioFile : IDisposable {
        
        public static ExtAudioFile CreateWithUrl (MonoTouch.CoreFoundation.CFUrl url, MonoTouch.AudioToolbox.AudioFileType fileType, MonoTouch.AudioToolbox.AudioStreamBasicDescription inStreamDesc, MonoTouch.AudioToolbox.AudioFileFlags flag);
        public static ExtAudioFile OpenUrl (MonoTouch.CoreFoundation.CFUrl url);
        public void Dispose ();
        public long FileTell ();
        public int Read (int numberFrames, MonoTouch.AudioToolbox.AudioBufferList data);
        public void Seek (long frameOffset);
        public void WriteAsync (int numberFrames, MonoTouch.AudioToolbox.AudioBufferList data);
        
        public MonoTouch.AudioToolbox.AudioStreamBasicDescription ClientDataFormat {
                set;
        }
        public MonoTouch.AudioToolbox.AudioStreamBasicDescription FileDataFormat {
                get;
        }
        public long FileLengthFrames {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.AudioUnitWrapper" class="injected"></a>


# Namespace: MonoTouch.AudioUnitWrapper

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.AudioUnitWrapper._AudioConverter" class="injected"></a>


## New Type: MonoTouch.AudioUnitWrapper._AudioConverter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class _AudioConverter : IDisposable {
        
        public static _AudioConverter CreateInstance (MonoTouch.AudioToolbox.AudioStreamBasicDescription srcFormat, MonoTouch.AudioToolbox.AudioStreamBasicDescription destFormat);
        public void Dispose ();
        public void FillBuffer (MonoTouch.AudioToolbox.AudioBufferList data, uint numberFrames, MonoTouch.AudioToolbox.AudioStreamPacketDescription[] packetDescs);
        
        public byte [] DecompressionMagicCookie {
                set;
        }
        
        public event EventHandler<_AudioConverterEventArgs> EncoderCallback;
}
```

 <a name="New_Type:_MonoTouch.AudioUnitWrapper._AudioConverterEventArgs" class="injected"></a>


## New Type: MonoTouch.AudioUnitWrapper._AudioConverterEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class _AudioConverterEventArgs : EventArgs {
        
        public _AudioConverterEventArgs (uint _NumberDataPackets, MonoTouch.AudioToolbox.AudioBufferList _Data, MonoTouch.AudioToolbox.AudioStreamPacketDescription[] _DataPacketDescription);
        
        public uint NumberDataPackets;
        public readonly MonoTouch.AudioToolbox.AudioBufferList Data;
        public readonly MonoTouch.AudioToolbox.AudioStreamPacketDescription[] DataPacketDescription;
}
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.CoreAnimation.CAEdgeAntialiasingMask" class="injected"></a>


## New Type: MonoTouch.CoreAnimation.CAEdgeAntialiasingMask

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
[Flags]
public enum CAEdgeAntialiasingMask {
        LeftEdge,
        RightEdge,
        BottomEdge,
        TopEdge,
        All,
        LeftRightEdges,
        TopBottomEdges
}
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CALayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CALayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual uint EdgeAntialiasingMask {
```

Added:

```
public virtual CAEdgeAntialiasingMask EdgeAntialiasingMask {
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAMediaTimingFunction" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAMediaTimingFunction

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static MonoTouch.Foundation.NSString EaseIn {
                get;
        }
        public static MonoTouch.Foundation.NSString EaseInEaseOut {
                get;
        }
        public static MonoTouch.Foundation.NSString EaseOut {
                get;
        }
        public static MonoTouch.Foundation.NSString Linear {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAShapeLayer" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAShapeLayer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual float StrokeEnd {
                get;
                set;
        }
        public virtual float StrokeStart {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAValueFunction" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAValueFunction

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual CAValueFunction FromName (string name);
```

Added:

```
public static CAValueFunction FromName (string name);
```

 <a name="Namespace:_MonoTouch.CoreData" class="injected"></a>


# Namespace: MonoTouch.CoreData

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.CoreData.NSEntityDescription" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSEntityDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public static NSEntityDescription InsertNewObjectForEntityForName (string entityName, NSManagedObjectContext context);
```

Added:

```
public static MonoTouch.Foundation.NSObject InsertNewObjectForEntityForName (string entityName, NSManagedObjectContext context);
```

 <a name="Namespace:_MonoTouch.CoreFoundation" class="injected"></a>


# Namespace: MonoTouch.CoreFoundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.CoreFoundation.CFType" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CFType {
        
        public CFType ();
        
        public static int GetTypeID (IntPtr typeRef);
}
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGFont" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGFont

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static CGFont CreateFromProvider (CGDataProvider provider);
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGPDFArray" class="injected"></a>


## New Type: MonoTouch.CoreGraphics.CGPDFArray

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CGPDFArray : MonoTouch.ObjCRuntime.INativeObject {
        
        public bool GetArray (int idx, out CGPDFArray array);
        public bool GetBoolean (int idx, out bool result);
        public bool GetDictionary (int idx, out CGPDFArray result);
        public bool GetFloat (int idx, out float result);
        public bool GetInt (int idx, out int result);
        public bool GetName (int idx, out string result);
        public bool GetStream (int idx, out CGPDFStream result);
        
        public int Count {
                get;
        }
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGPDFDictionary" class="injected"></a>


## New Type: MonoTouch.CoreGraphics.CGPDFDictionary

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CGPDFDictionary : MonoTouch.ObjCRuntime.INativeObject {
        
        public bool GetArray (string key, out CGPDFArray array);
        public bool GetBoolean (string key, out bool result);
        public bool GetDictionary (string key, out CGPDFDictionary result);
        public bool GetFloat (string key, out float result);
        public bool GetInt (string key, out int result);
        public bool GetName (string key, out string result);
        public bool GetStream (string key, out CGPDFStream result);
        
        public int Count {
                get;
        }
        public IntPtr Handle {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFDocument" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFDocument

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public CGPDFPage GetPage (int page);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFPage" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFPage

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public CGPDFDictionary Dictionary {
                get;
        }
```

 <a name="New_Type:_MonoTouch.CoreGraphics.CGPDFStream" class="injected"></a>


## New Type: MonoTouch.CoreGraphics.CGPDFStream

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CGPDFStream : MonoTouch.ObjCRuntime.INativeObject {
        
        public MonoTouch.Foundation.NSData Data {
                get;
        }
        public CGPDFDictionary Dictionary {
                get;
        }
        public IntPtr Handle {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreLocation" class="injected"></a>


# Namespace: MonoTouch.CoreLocation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.CoreLocation.CLAuthorizationStatus" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLAuthorizationStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum CLAuthorizationStatus {
        NotDetermined,
        Restricted,
        Denied,
        Authorized
}
```

 <a name="New_Type:_MonoTouch.CoreLocation.CLAuthroziationChangedEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreLocation.CLAuthroziationChangedEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CLAuthroziationChangedEventArgs : EventArgs {
        
        public CLAuthroziationChangedEventArgs (CLAuthorizationStatus status);
        
        public CLAuthorizationStatus Status {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocation" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public CLLocation (CLLocationCoordinate2D coordinate, double altitude, double hAccuracy, double vAccuracy, double course, double speed, MonoTouch.Foundation.NSDate timestamp);
        public static readonly double AccurracyBestForNavigation;
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManager" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static CLAuthorizationStatus Status {
                get;
        }
        public event EventHandler<CLAuthroziationChangedEventArgs> AuthorizationChanged;
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManagerDelegate" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManagerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual void AuthorizationChanged (CLLocationManager manager, CLAuthorizationStatus status);
```

 <a name="Namespace:_MonoTouch.CoreText" class="injected"></a>


# Namespace: MonoTouch.CoreText

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.CoreText.CTFont" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFont

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public CTFont (MonoTouch.CoreGraphics.CGFont font, float size, MonoTouch.CoreGraphics.CGAffineTransform transform, CTFontDescriptor descriptor);
        public CTFont (MonoTouch.CoreGraphics.CGFont font, float size, CTFontDescriptor descriptor);
        public CTFont (MonoTouch.CoreGraphics.CGFont font, float size, MonoTouch.CoreGraphics.CGAffineTransform transform);
        public void DrawGlyphs (MonoTouch.CoreGraphics.CGContext context, ushort [] glyphs, System.Drawing.PointF [] positions);
        public int GetLigatureCaretPositions (ushort glyph, float [] positions);
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFontTable" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFontTable

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
VerticalMetrics
```

Added:

```
VerticalMetrics,
        SBitmapData,
        SExtendedBitmapData
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFrameAttributeKey" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFrameAttributeKey

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static readonly MonoTouch.Foundation.NSString PathFillRule;
        public static readonly MonoTouch.Foundation.NSString PathWidth;
```

 <a name="Type_Changed:_MonoTouch.CoreText.CTFramePathFillRule" class="injected"></a>


## Type Changed: MonoTouch.CoreText.CTFramePathFillRule

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
[Serializable]
 public enum CTFramePathFillRule {
        EvenOdd,
        WindingNumber
 }
```

 <a name="Namespace:_MonoTouch.EventKit" class="injected"></a>


# Namespace: MonoTouch.EventKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.EventKit.EKErrorCode" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKErrorCode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

   
   
 Added:

```
InvalidSpan
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKEventViewAction" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEventViewAction

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
[Serializable]
 public enum EKEventViewAction {
        Done,
        Responded,
        Deleted
 }
```

 <a name="Namespace:_MonoTouch.EventKitUI" class="injected"></a>


# Namespace: MonoTouch.EventKitUI

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.EventKitUI.EKEventViewController" class="injected"></a>


## Type Changed: MonoTouch.EventKitUI.EKEventViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public EKEventViewDelegate Delegate {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler<EKEventViewEventArgs> Completed;
```

 <a name="New_Type:_MonoTouch.EventKitUI.EKEventViewDelegate" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKEventViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public abstract class EKEventViewDelegate : MonoTouch.Foundation.NSObject {
        
        public EKEventViewDelegate ();
        public EKEventViewDelegate (MonoTouch.Foundation.NSCoder coder);
        public EKEventViewDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public EKEventViewDelegate (IntPtr handle);
        
        public abstract void Completed (EKEventViewController controller, MonoTouch.EventKit.EKEventViewAction action);
}
```

 <a name="New_Type:_MonoTouch.EventKitUI.EKEventViewEventArgs" class="injected"></a>


## New Type: MonoTouch.EventKitUI.EKEventViewEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class EKEventViewEventArgs : EventArgs {
        
        public EKEventViewEventArgs (MonoTouch.EventKit.EKEventViewAction action);
        
        public MonoTouch.EventKit.EKEventViewAction Action {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSBundle" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSBundle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static bool LoadNib (string nibName, NSObject owner);
        public virtual NSDictionary InfoDictionary {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static NSDate DistantFuture {
                get;
        }
        public static NSDate DistantPast {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDictionary" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDictionary

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public IntPtr LowlevelObjectForKey (IntPtr key);
```

 <a name="New_Type:_MonoTouch.Foundation.NSEnumerationOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSEnumerationOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
[Flags]
public enum NSEnumerationOptions {
        SortConcurrent,
        Reverse
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSKeyValueChange" class="injected"></a>


## New Type: MonoTouch.Foundation.NSKeyValueChange

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum NSKeyValueChange {
        Setting,
        Insertion,
        Removal,
        Replacement
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSKeyValueObservingOptions" class="injected"></a>


## New Type: MonoTouch.Foundation.NSKeyValueObservingOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
[Flags]
public enum NSKeyValueObservingOptions {
        New,
        Old,
        OldNew,
        Initial,
        Prior
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSKeyValueSetMutationKind" class="injected"></a>


## New Type: MonoTouch.Foundation.NSKeyValueSetMutationKind

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum NSKeyValueSetMutationKind {
        UnionSet,
        MinusSet,
        IntersectSet,
        SetSet
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableAttributedString

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual void AddAttribute (string name, NSObject value, NSRange range);
```

Added:

```
public virtual void AddAttribute (NSString attributeName, NSObject value, NSRange range);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableDictionary" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableDictionary

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static NSMutableDictionary LowlevelFromObjectAndKey (IntPtr obj, IntPtr key);
        public void LowlevelSetObject (IntPtr obj, IntPtr key);
        public void LowlevelSetObject (NSObject obj, IntPtr key);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSObject

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static bool AutomaticallyNotifiesObserversForKey (string key);
        public static NSSet GetKeyPathsForValuesAffecting (NSString key);
        public virtual void AccessibilityDecrement ();
        public virtual void AccessibilityIncrement ();
        public virtual bool AccessibilityScroll (MonoTouch.UIKit.UIAccessibilityScrollDirection direction);
        public virtual void AddObserver (NSObject observer, NSString keyPath, NSKeyValueObservingOptions options, IntPtr context);
        public virtual void DidChange (NSKeyValueChange changeKind, NSIndexSet indexes, NSString forKey);
        public virtual void DidChange (NSString forKey, NSKeyValueSetMutationKind mutationKind, NSSet objects);
        public virtual void DidChangeValue (string forKey);
        public virtual NSDictionary GetDictionaryOfValuesFromKeys (NSString[] keys);
        public virtual void ObserveValue (NSString keyPath, NSObject ofObject, NSDictionary change, IntPtr context);
        public virtual void RemoveObserver (NSObject observer, NSString keyPath);
        public virtual void SetNilValueForKey (NSString key);
        public virtual void SetValueForKey (NSObject value, NSString key);
        public virtual void SetValueForKeyPath (NSObject value, NSString keyPath);
        public virtual void SetValueForUndefinedKey (NSObject value, NSString undefinedKey);
        public virtual void SetValuesForKeysWithDictionary (NSDictionary keyedValues);
        public virtual NSObject ValueForKey (NSString key);
        public virtual NSObject ValueForKeyPath (NSString keyPath);
        public virtual NSObject ValueForUndefinedKey (NSString key);
        public virtual void WillChange (NSKeyValueChange changeKind, NSIndexSet indexes, NSString forKey);
        public virtual void WillChange (NSString forKey, NSKeyValueSetMutationKind mutationKind, NSSet objects);
        public virtual void WillChangeValue (string forKey);
        public static NSString ChangeIndexesKey {
                get;
        }
        public static NSString ChangeKindKey {
                get;
        }
        public static NSString ChangeNewKey {
                get;
        }
        public static NSString ChangeNotificationIsPriorKey {
                get;
        }
        public static NSString ChangeOldKey {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRunLoop" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRunLoop

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static NSString NSDefaultRunLoopMode {
                get;
        }
        public static NSString NSRunLoopCommonModes {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSStream" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSStream

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual NSObject Delegate {
```

Added:

```
public virtual void Open ();
        public static NSString NetworkServiceTypeVoIP {
                get;
        }
        public NSStreamDelegate Delegate {
        public virtual NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler<NSStreamEventArgs> OnEvent;
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSStreamDelegate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSStreamDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
Could not find MonoTouch.Foundation.NSStreamDelegate
```

Added:

```
public class NSStreamDelegate : NSObject {
        
        public NSStreamDelegate ();
        public NSStreamDelegate (NSCoder coder);
        public NSStreamDelegate (NSObjectFlag t);
        public NSStreamDelegate (IntPtr handle);
        
        public virtual void HandleEvent (NSStream theStream, NSStreamEvent streamEvent);
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSStreamEvent" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSStreamEvent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
Could not find MonoTouch.Foundation.NSStreamEvent
```

Added:

```
[Serializable]
 public enum NSStreamEvent : uint {
        None,
        OpenCompleted,
        HasBytesAvailable,
        HasSpaceAvailable,
        ErrorOccurred,
        EndEncountered
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSStreamEventArgs" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSStreamEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
Could not find MonoTouch.Foundation.NSStreamEventArgs
```

Added:

```
public class NSStreamEventArgs : EventArgs {
        
        public NSStreamEventArgs (NSStreamEvent streamEvent);
        
        public NSStreamEvent StreamEvent {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSString

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public System.Drawing.SizeF DrawString (System.Drawing.PointF point, float width, MonoTouch.UIKit.UIFont font, float minFontSize, float actualFontSize, MonoTouch.UIKit.UILineBreakMode breakMode, MonoTouch.UIKit.UIBaselineAdjustment adjustment);
        public System.Drawing.SizeF DrawString (System.Drawing.PointF point, float width, MonoTouch.UIKit.UIFont font, float fontSize, MonoTouch.UIKit.UILineBreakMode breakMode, MonoTouch.UIKit.UIBaselineAdjustment adjustment);
        public System.Drawing.SizeF DrawString (System.Drawing.PointF point, float width, MonoTouch.UIKit.UIFont font, MonoTouch.UIKit.UILineBreakMode breakMode);
        public System.Drawing.SizeF DrawString (System.Drawing.PointF point, MonoTouch.UIKit.UIFont font);
        public System.Drawing.SizeF DrawString (System.Drawing.RectangleF rect, MonoTouch.UIKit.UIFont font);
        public System.Drawing.SizeF DrawString (System.Drawing.RectangleF rect, MonoTouch.UIKit.UIFont font, MonoTouch.UIKit.UILineBreakMode mode);
        public System.Drawing.SizeF DrawString (System.Drawing.RectangleF rect, MonoTouch.UIKit.UIFont font, MonoTouch.UIKit.UILineBreakMode mode, MonoTouch.UIKit.UITextAlignment alignment);
        public static explicit operator NSString (string str);
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievement" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievement

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual bool Hidden {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementDescription" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
set;
                set;
                set;
                set;
                set;
                set;
                set;
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKError" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
InvalidParameter
```

 <a name="New_Type:_MonoTouch.GameKit.GKFriendRequestComposeViewController" class="injected"></a>


## New Type: MonoTouch.GameKit.GKFriendRequestComposeViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class GKFriendRequestComposeViewController : MonoTouch.UIKit.UINavigationController {
        
        public GKFriendRequestComposeViewController ();
        public GKFriendRequestComposeViewController (MonoTouch.Foundation.NSCoder coder);
        public GKFriendRequestComposeViewController (MonoTouch.Foundation.NSObjectFlag t);
        public GKFriendRequestComposeViewController (IntPtr handle);
        
        public virtual void AddRecipientsFromAliases (string [] aliases);
        public virtual void AddRecipientsFromEmails (string [] emailAddresses);
        public virtual void AddRecipientsFromPlayerIDs (string [] emailAddresses);
        
        public static int MaxNumberOfRecipients {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public GKFriendRequestComposeViewControllerDelegate ComposeViewDelegate {
                get;
                set;
        }
        public virtual string Message {
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakComposeViewDelegate {
                get;
                set;
        }
        
        public event EventHandler DidFinish;
}
```

 <a name="" class="injected"></a>


## New Type: MonoTouch.GameKit.GKFriendRequestComposeViewControllerDelegate 

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public abstract class GKFriendRequestComposeViewControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public GKFriendRequestComposeViewControllerDelegate ();
        public GKFriendRequestComposeViewControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public GKFriendRequestComposeViewControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public GKFriendRequestComposeViewControllerDelegate (IntPtr handle);
        
        public abstract void DidFinish (GKFriendRequestComposeViewController viewController);
}
```

 <a name="Namespace:_MonoTouch.ImageIO" class="injected"></a>


# Namespace: MonoTouch.ImageIO

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.ImageIO.CGImageDestination" class="injected"></a>


## New Type: MonoTouch.ImageIO.CGImageDestination

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CGImageDestination : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public static CGImageDestination FromData (MonoTouch.Foundation.NSData data, string typeIdentifier, int imageCount);
        public static CGImageDestination FromData (MonoTouch.Foundation.NSData data, string typeIdentifier, int imageCount, CGImageDestinationOptions options);
        public static CGImageDestination FromUrl (MonoTouch.Foundation.NSUrl url, string typeIdentifier, int imageCount);
        public static CGImageDestination FromUrl (MonoTouch.Foundation.NSUrl url, string typeIdentifier, int imageCount, CGImageDestinationOptions options);
        public static int GetTypeID ();
        public void AddImage (MonoTouch.CoreGraphics.CGImage image, MonoTouch.Foundation.NSDictionary properties);
        public void AddImage (CGImageSource source, int index, MonoTouch.Foundation.NSDictionary properties);
        public void Close ();
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public void SetProperties (MonoTouch.Foundation.NSDictionary properties);
        
        public static string [] TypeIdentifiers {
                get;
        }
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.ImageIO.CGImageDestinationOptions" class="injected"></a>


## New Type: MonoTouch.ImageIO.CGImageDestinationOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CGImageDestinationOptions {
        
        public CGImageDestinationOptions ();
        
        public MonoTouch.CoreGraphics.CGColor DestinationBackgroundColor {
                get;
                set;
        }
        public Nullable<float> LossyCompressionQuality {          get;            set;    } } </float>
```

 <a name="New_Type:_MonoTouch.ImageIO.CGImageOptions" class="injected"></a>


## New Type: MonoTouch.ImageIO.CGImageOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CGImageOptions {
        
        public CGImageOptions ();
        
        public string BestGuessTypeIdentifier {
                get;
                set;
        }
        public bool ShouldAllowFloat {
                get;
                set;
        }
        public bool ShouldCache {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.ImageIO.CGImageSource" class="injected"></a>


## New Type: MonoTouch.ImageIO.CGImageSource

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CGImageSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public static CGImageSource CreateIncremental (CGImageOptions options);
        public static CGImageSource FromData (MonoTouch.Foundation.NSData data);
        public static CGImageSource FromData (MonoTouch.Foundation.NSData data, CGImageOptions options);
        public static CGImageSource FromDataProvider (MonoTouch.CoreGraphics.CGDataProvider provider);
        public static CGImageSource FromDataProvider (MonoTouch.CoreGraphics.CGDataProvider provider, CGImageOptions options);
        public static CGImageSource FromUrl (MonoTouch.Foundation.NSUrl url);
        public static CGImageSource FromUrl (MonoTouch.Foundation.NSUrl url, CGImageOptions options);
        public static int GetTypeID ();
        public MonoTouch.Foundation.NSDictionary CopyProperties (MonoTouch.Foundation.NSDictionary dict);
        public MonoTouch.Foundation.NSDictionary CopyProperties (MonoTouch.Foundation.NSDictionary dict, int imageIndex);
        public MonoTouch.CoreGraphics.CGImage CreateImage (int index, CGImageOptions options);
        public MonoTouch.CoreGraphics.CGImage CreateThumbnail (int index, CGImageThumbnailOptions options);
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public CGImageSourceStatus GetStatus ();
        public CGImageSourceStatus GetStatus (int index);
        public void UpdateData (MonoTouch.Foundation.NSData data, bool final);
        public void UpdateDataProvider (MonoTouch.CoreGraphics.CGDataProvider provider);
        
        public static string [] TypeIdentifiers {
                get;
        }
        public IntPtr Handle {
                get;
        }
        public int ImageCount {
                get;
        }
        public string TypeIdentifier {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.ImageIO.CGImageSourceStatus" class="injected"></a>


## New Type: MonoTouch.ImageIO.CGImageSourceStatus

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum CGImageSourceStatus {
        Complete,
        Incomplete,
        ReadingHeader,
        UnknownType,
        InvalidData,
        UnexpectedEOF
}
```

 <a name="New_Type:_MonoTouch.ImageIO.CGImageThumbnailOptions" class="injected"></a>


## New Type: MonoTouch.ImageIO.CGImageThumbnailOptions

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class CGImageThumbnailOptions : CGImageOptions {
        
        public CGImageThumbnailOptions ();
        
        public bool CreateThumbnailFromImageAlways {
                get;
                set;
        }
        public bool CreateThumbnailFromImageIfAbsent {
                get;
                set;
        }
        public bool CreateThumbnailWithTransform {
                get;
                set;
        }
        public Nullable<int> MaxPixelSize {               get;            set;    } } </int>
```

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


# Namespace: MonoTouch.MapKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.MapKit.MKAnnotationView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKAnnotationView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual void SetDragState (MKAnnotationViewDragState newDragState, bool animated);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKCircle" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKCircle

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual bool Intersects (MKMapRect rect);
        public virtual MKMapRect BoundingMapRect {
                get;
        }
        public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                get;
                set;
        }
        public virtual string Subtitle {
                get;
        }
        public virtual string Title {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapPoint" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapPoint

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static MKMapPoint FromCoordinate (MonoTouch.CoreLocation.CLLocationCoordinate2D coordinate);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual MonoTouch.Foundation.NSSet GetAnnotations (MKMapRect mapRect);
```

 <a name="New_Type:_MonoTouch.MapKit.MKOverlay" class="injected"></a>


## New Type: MonoTouch.MapKit.MKOverlay

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class MKOverlay : MKAnnotation {
        
        public MKOverlay ();
        public MKOverlay (MonoTouch.Foundation.NSCoder coder);
        public MKOverlay (MonoTouch.Foundation.NSObjectFlag t);
        public MKOverlay (IntPtr handle);
        
        public virtual bool Intersects (MKMapRect rect);
        
        public virtual MKMapRect BoundingMapRect {
                get;
        }
        public override MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                get;
                set;
        }
        public override string Subtitle {
                get;
        }
        public override string Title {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPlacemark" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPlacemark

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public class MKPlacemark : MonoTouch.Foundation.NSObject {
```

Added:

```
public class MKPlacemark : MKAnnotation {
        public override MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                get;
                set;
        }
        public override string Subtitle {
                get;
        }
        public override string Title {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPointAnnotation" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPointAnnotation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolygon" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolygon

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual bool Intersects (MKMapRect rect);
        public virtual MKMapRect BoundingMapRect {
                get;
        }
        public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                get;
                set;
        }
        public virtual string Subtitle {
                get;
        }
        public virtual string Title {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPolyline" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPolyline

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual bool Intersects (MKMapRect rect);
        public virtual MKMapRect BoundingMapRect {
                get;
        }
        public virtual MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                get;
                set;
        }
        public virtual string Subtitle {
                get;
        }
        public virtual string Title {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKShape" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKShape

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public class MKShape : MonoTouch.Foundation.NSObject {
        public virtual string Subtitle {
        public virtual string Title {
                set;
```

Added:

```
public class MKShape : MKAnnotation {
        public override MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
        public override string Subtitle {
                get;
        }
        public override string Title {
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKUserLocation" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKUserLocation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public class MKUserLocation : MonoTouch.Foundation.NSObject {
        public virtual string Subtitle {
                set;
        public virtual string Title {
                set;
```

Added:

```
public class MKUserLocation : MKAnnotation {
        public override MonoTouch.CoreLocation.CLLocationCoordinate2D Coordinate {
                get;
                set;
        }
        public override string Subtitle {
        public override string Title {
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItem" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItem

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static string GetPersistentIDProperty (MPMediaGrouping groupingType);
        public static string GetTitleProperty (MPMediaGrouping groupingType);
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItemProperty" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItemProperty

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public const string PersistendID = "persistendID";
```

Added:

```
public const string PersistentID = "persistentID";
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaPlaylistProperty" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaPlaylistProperty

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public const string PersistendID = "playlistPersistentID";
```

Added:

```
public const string PersistentID = "playlistPersistentID";
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaQuery" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaQuery

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual MPMediaQuerySection[] CollectionSections {
                get;
        }
        public virtual MPMediaQuerySection[] ItemSections {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaQuerySection" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaQuerySection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
Could not find MonoTouch.MediaPlayer.MPMediaQuerySection
```

Added:

```
public class MPMediaQuerySection : MonoTouch.Foundation.NSObject {
        
        public MPMediaQuerySection ();
        public MPMediaQuerySection (MonoTouch.Foundation.NSCoder coder);
        public MPMediaQuerySection (MonoTouch.Foundation.NSObjectFlag t);
        public MPMediaQuerySection (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSRange Range {
                get;
        }
        public virtual string Title {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPVolumeView" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPVolumeView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual bool ShowsRouteButton {
                get;
                set;
        }
        public virtual bool ShowsVolumeSlider {
                get;
                set;
        }
```

 <a name="Namespace:_MonoTouch.MessageUI" class="injected"></a>


# Namespace: MonoTouch.MessageUI

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.MessageUI.MFMailComposeViewControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.MessageUI.MFMailComposeViewControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public override void DidShowViewController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewController viewController, bool animated);
        public override void WillShowViewController (MonoTouch.UIKit.UINavigationController navigationController, MonoTouch.UIKit.UIViewController viewController, bool animated);
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static bool bool_objc_msgSend_int (IntPtr receiver, IntPtr selector, int arg1);
        public static bool bool_objc_msgSendSuper_int (IntPtr receiver, IntPtr selector, int arg1);
        public static IntPtr IntPtr_objc_msgSend_CLLocationCoordinate2D_Double_Double_Double_Double_Double_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2, double arg3, double arg4, double arg5, double arg6, IntPtr arg7);
        public static IntPtr IntPtr_objc_msgSend_SizeF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, IntPtr arg2);
        public static IntPtr IntPtr_objc_msgSendSuper_CLLocationCoordinate2D_Double_Double_Double_Double_Double_IntPtr (IntPtr receiver, IntPtr selector, MonoTouch.CoreLocation.CLLocationCoordinate2D arg1, double arg2, double arg3, double arg4, double arg5, double arg6, IntPtr arg7);
        public static IntPtr IntPtr_objc_msgSendSuper_SizeF_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.SizeF arg1, IntPtr arg2);
        public static uint UInt32_objc_msgSend_IntPtr_Int64_UInt32_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, long arg2, uint arg3, IntPtr arg4);
        public static uint UInt32_objc_msgSendSuper_IntPtr_Int64_UInt32_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, long arg2, uint arg3, IntPtr arg4);
        public static void void_objc_msgSend_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3);
        public static void void_objc_msgSend_int_RectangleF (IntPtr receiver, IntPtr selector, int arg1, System.Drawing.RectangleF arg2);
        public static void void_objc_msgSend_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
        public static void void_objc_msgSend_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4);
        public static void void_objc_msgSend_RectangleF_int (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, int arg2);
        public static void void_objc_msgSend_RectangleF_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_int_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, int arg1, IntPtr arg2, IntPtr arg3);
        public static void void_objc_msgSendSuper_int_RectangleF (IntPtr receiver, IntPtr selector, int arg1, System.Drawing.RectangleF arg2);
        public static void void_objc_msgSendSuper_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, bool arg2, IntPtr arg3);
        public static void void_objc_msgSendSuper_IntPtr_IntPtr_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, int arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_RectangleF_int (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, int arg2);
        public static void void_objc_msgSendSuper_RectangleF_IntPtr_Boolean_IntPtr (IntPtr receiver, IntPtr selector, System.Drawing.RectangleF arg1, IntPtr arg2, bool arg3, IntPtr arg4);
```

 <a name="Namespace:_MonoTouch.OpenGLES" class="injected"></a>


# Namespace: MonoTouch.OpenGLES

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Namespace:_MonoTouch.QuickLook" class="injected"></a>


# Namespace: MonoTouch.QuickLook

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Namespace:_MonoTouch.Security" class="injected"></a>


# Namespace: MonoTouch.Security

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.Security.SecAccessible" class="injected"></a>


## New Type: MonoTouch.Security.SecAccessible

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum SecAccessible {
        WhenUnlocked,
        AfterFirstUnlock,
        Always,
        WhenUnlockedThisDeviceOnly,
        AfterFirstUnlockThisDeviceOnly,
        AlwaysThisDeviceOnly
}
```

 <a name="New_Type:_MonoTouch.Security.SecAuthenticationType" class="injected"></a>


## New Type: MonoTouch.Security.SecAuthenticationType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum SecAuthenticationType {
        Ntlm,
        Msn,
        Dpa,
        Rpa,
        HttpBasic,
        HttpDigest,
        HtmlForm,
        Default
}
```

 <a name="New_Type:_MonoTouch.Security.SecCertificate" class="injected"></a>


## New Type: MonoTouch.Security.SecCertificate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class SecCertificate : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public SecCertificate (MonoTouch.Foundation.NSData data);
        
        public static int GetTypeID ();
        public void Dispose ();
        public virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public MonoTouch.Foundation.NSData DerData {
                get;
        }
        public IntPtr Handle {
                get;
        }
        public string SubjectSummary {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Security.SecIdentity" class="injected"></a>


## New Type: MonoTouch.Security.SecIdentity

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class SecIdentity : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public static int GetTypeID ();
        public void Dispose ();
        public virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public SecCertificate Certificate {
                get;
        }
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Security.SecKey" class="injected"></a>


## New Type: MonoTouch.Security.SecKey

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class SecKey : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public static SecStatusCode GenerateKeyPair (MonoTouch.Foundation.NSDictionary parameters, out SecKey publicKey, out SecKey privateKey);
        public static int GetTypeID ();
        public SecStatusCode Decrypt (SecPadding padding, byte [] cipherText, byte [] plainText);
        public SecStatusCode Decrypt (SecPadding padding, IntPtr cipherText, int cipherLen, IntPtr plainText, int playLen);
        public void Dispose ();
        public virtual void Dispose (bool disposing);
        public SecStatusCode Encrypt (SecPadding padding, byte [] plainText, byte [] cipherText);
        public SecStatusCode Encrypt (SecPadding padding, IntPtr plainText, int playLen, IntPtr cipherText, int cipherLen);
        protected override void Finalize ();
        public SecStatusCode RawVerify (SecPadding padding, byte [] signedData, byte [] signature);
        public SecStatusCode RawVerify (SecPadding padding, IntPtr signedData, int signedDataLen, IntPtr signature, int signatureLen);
        
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Security.SecKeyChain" class="injected"></a>


## New Type: MonoTouch.Security.SecKeyChain

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public static class SecKeyChain {
        
        public static SecStatusCode Add (SecRecord record);
        public static object QueryAsConcreteType (SecRecord query, out SecStatusCode result);
        public static MonoTouch.Foundation.NSData QueryAsData (SecRecord query);
        public static MonoTouch.Foundation.NSData[] QueryAsData (SecRecord query, bool wantPersistentReference, int max, out SecStatusCode status);
        public static MonoTouch.Foundation.NSData QueryAsData (SecRecord query, bool wantPersistentReference, out SecStatusCode status);
        public static MonoTouch.Foundation.NSData[] QueryAsData (SecRecord query, int max);
        public static SecRecord[] QueryAsRecord (SecRecord query, int max, out SecStatusCode result);
        public static SecRecord QueryAsRecord (SecRecord query, out SecStatusCode result);
        public static SecStatusCode Remove (SecRecord record);
        public static SecStatusCode Update (SecRecord query, SecRecord newAttributes);
}
```

 <a name="New_Type:_MonoTouch.Security.SecKeyClass" class="injected"></a>


## New Type: MonoTouch.Security.SecKeyClass

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum SecKeyClass {
        Public,
        Private,
        Symmetric
}
```

 <a name="New_Type:_MonoTouch.Security.SecKeyType" class="injected"></a>


## New Type: MonoTouch.Security.SecKeyType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum SecKeyType {
        RSA,
        EC
}
```

 <a name="New_Type:_MonoTouch.Security.SecKind" class="injected"></a>


## New Type: MonoTouch.Security.SecKind

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum SecKind {
        InternetPassword,
        GenericPassword,
        Certificate,
        Key,
        Identity
}
```

 <a name="New_Type:_MonoTouch.Security.SecMatchLimit" class="injected"></a>


## New Type: MonoTouch.Security.SecMatchLimit

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public static class SecMatchLimit {
        
        public static IntPtr MatchLimitAll {
                get;
        }
        public static IntPtr MatchLimitOne {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Security.SecPadding" class="injected"></a>


## New Type: MonoTouch.Security.SecPadding

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum SecPadding {
        None,
        PKCS1,
        OAEP,
        PKCS1MD2,
        PKCS1MD5,
        PKCS1SHA1
}
```

 <a name="New_Type:_MonoTouch.Security.SecPolicy" class="injected"></a>


## New Type: MonoTouch.Security.SecPolicy

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class SecPolicy : MonoTouch.Foundation.NSObject {
        
        public static int GetTypeID ();
        public override bool Equals (object other);
        public override int GetHashCode ();
        
        public static bool operator == (SecPolicy a, SecPolicy b);
        public static bool operator != (SecPolicy a, SecPolicy b);
}
```

 <a name="New_Type:_MonoTouch.Security.SecProtocol" class="injected"></a>


## New Type: MonoTouch.Security.SecProtocol

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum SecProtocol {
        Ftp,
        FtpAccount,
        Http,
        Irc,
        Nntp,
        Pop3,
        Smtp,
        Socks,
        Imap,
        Ldap,
        AppleTalk,
        Afp,
        Telnet,
        Ssh,
        Ftps,
        Https,
        HttpProxy,
        HttpsProxy,
        FtpProxy,
        Smb,
        Rtsp,
        RtspProxy,
        Daap,
        Eppc,
        Ipp,
        Nntps,
        Ldaps,
        Telnets,
        Imaps,
        Ircs,
        Pop3s
}
```

 <a name="New_Type:_MonoTouch.Security.SecRecord" class="injected"></a>


## New Type: MonoTouch.Security.SecRecord

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class SecRecord : IDisposable {
        
        public SecRecord (SecKind secKind);
        
        public SecRecord Clone ();
        public void Dispose ();
        public virtual void Dispose (bool disposing);
        protected override void Finalize ();
        
        public string AccessGroup {
                get;
                set;
        }
        public SecAccessible Accessible {
                get;
                set;
        }
        public string Account {
                get;
                set;
        }
        public string ApplicationLabel {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData ApplicationTag {
                get;
                set;
        }
        public SecAuthenticationType AuthenticationType {
                get;
                set;
        }
        public bool CanDecrypt {
                get;
                set;
        }
        public bool CanDerive {
                get;
                set;
        }
        public bool CanEncrypt {
                get;
                set;
        }
        public bool CanSign {
                get;
                set;
        }
        public bool CanUnwrap {
                get;
                set;
        }
        public bool CanVerify {
                get;
                set;
        }
        public bool CanWrap {
                get;
                set;
        }
        public MonoTouch.Foundation.NSNumber CertificateEncoding {
                get;
        }
        public MonoTouch.Foundation.NSNumber CertificateType {
                get;
        }
        public string Comment {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDate CreationDate {
                get;
                set;
        }
        public int Creator {
                get;
                set;
        }
        public int CreatorType {
                get;
                set;
        }
        public string Description {
                get;
                set;
        }
        public int EffectiveKeySize {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData Generic {
                get;
                set;
        }
        public bool Invisible {
                get;
                set;
        }
        public bool IsNegative {
                get;
                set;
        }
        public bool IsPermanent {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData Issuer {
                get;
        }
        public SecKeyClass KeyClass {
                get;
                set;
        }
        public int KeySizeInBits {
                get;
                set;
        }
        public SecKeyType KeyType {
                get;
                set;
        }
        public string Label {
                get;
                set;
        }
        public bool MatchCaseInsensitive {
                get;
                set;
        }
        public string MatchEmailAddressIfPresent {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData[] MatchIssuers {
                set;
        }
        public MonoTouch.Foundation.NSArray MatchItemList {
                get;
                set;
        }
        public SecPolicy MatchPolicy {
                get;
                set;
        }
        public string MatchSubjectContains {
                get;
                set;
        }
        public bool MatchTrustedOnly {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDate MatchValidOnDate {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDate ModificationDate {
                get;
                set;
        }
        public string Path {
                get;
                set;
        }
        public int Port {
                get;
                set;
        }
        public SecProtocol Protocol {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData PublicKeyHash {
                get;
        }
        public string SecurityDomain {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData SerialNumber {
                get;
        }
        public string Server {
                get;
                set;
        }
        public string Service {
                get;
                set;
        }
        public string Subject {
                get;
        }
        public MonoTouch.Foundation.NSData SubjectKeyID {
                get;
        }
        public MonoTouch.Foundation.NSData ValueData {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.Security.SecStatusCode" class="injected"></a>


## New Type: MonoTouch.Security.SecStatusCode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum SecStatusCode {
        Success,
        Unimplemented,
        Param,
        Allocate,
        NotAvailable,
        ReadOnly,
        AuthFailed,
        NoSuchKeyChain,
        InvalidKeyChain,
        DuplicateKeyChain,
        DuplicateItem,
        ItemNotFound,
        InteractionNotAllowed,
        Decode
}
```

 <a name="New_Type:_MonoTouch.Security.SecTrust" class="injected"></a>


## New Type: MonoTouch.Security.SecTrust

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class SecTrust : MonoTouch.Foundation.NSObject {
        
        public SecTrust ();
        
        public static int GetTypeID ();
}
```

 <a name="New_Type:_MonoTouch.Security.SecurityException" class="injected"></a>


## New Type: MonoTouch.Security.SecurityException

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class SecurityException : Exception {
        
        public SecurityException (SecStatusCode code);
}
```

 <a name="Namespace:_MonoTouch.StoreKit" class="injected"></a>


# Namespace: MonoTouch.StoreKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.StoreKit.SKError" class="injected"></a>


## New Type: MonoTouch.StoreKit.SKError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum SKError {
        Unknown,
        ClientInvalid,
        PaymentCancelled,
        PaymentInvalid,
        PaymentNotAllowed
}
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKProductsRequest" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKProductsRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public event EventHandler<SKProductsRequestResponseEventArgs> ReceivedResponse;
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKProductsRequestDelegate" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKProductsRequestDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public override void RequestFailed (SKRequest request, MonoTouch.Foundation.NSError error);
        public override void RequestFinished (SKRequest request);
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKProductsRequestResponseEventArgs" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKProductsRequestResponseEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
Could not find MonoTouch.StoreKit.SKProductsRequestResponseEventArgs
```

Added:

```
public class SKProductsRequestResponseEventArgs : EventArgs {
        
        public SKProductsRequestResponseEventArgs (SKProductsResponse response);
        
        public SKProductsResponse Response {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKRequest" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public event EventHandler<SKRequestErrorEventArgs> RequestFailed;
        public event EventHandler RequestFinished;
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKRequestDelegate" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKRequestDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual void RequedFailed (SKRequest request, MonoTouch.Foundation.NSError error);
```

Added:

```
public virtual void RequestFailed (SKRequest request, MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.StoreKit.SKRequestErrorEventArgs" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKRequestErrorEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
Could not find MonoTouch.StoreKit.SKRequestErrorEventArgs
```

Added:

```
public class SKRequestErrorEventArgs : EventArgs {
        
        public SKRequestErrorEventArgs (MonoTouch.Foundation.NSError error);
        
        public MonoTouch.Foundation.NSError Error {
                get;
                set;
        }
 }
```

 <a name="Namespace:_MonoTouch.SystemConfiguration" class="injected"></a>


# Namespace: MonoTouch.SystemConfiguration

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="New_Type:_MonoTouch.UIKit.UIAccessibilityScrollDirection" class="injected"></a>


## New Type: MonoTouch.UIKit.UIAccessibilityScrollDirection

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum UIAccessibilityScrollDirection {
        Right,
        Left,
        Up,
        Down
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplication

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual bool SetKeepAliveTimout (double timeout, MonoTouch.Foundation.NSAction handler);
```

Added:

```
public virtual bool SetKeepAliveTimeout (double timeout, MonoTouch.Foundation.NSAction handler);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplicationDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplicationDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual void OpenUrl (UIApplication application, MonoTouch.Foundation.NSUrl url, string sourceApplication, MonoTouch.Foundation.NSObject annotation);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDevice" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDevice

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual void PlayInputClick ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDocumentInteractionController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDocumentInteractionController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public virtual UIImage Icons {
```

Added:

```
public virtual UIImage[] Icons {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIGestureRecognizer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public class Token : MonoTouch.Foundation.NSObject {
                
                public void Activated ();
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public override void DidShowViewController (UINavigationController navigationController, UIViewController viewController, bool animated);
        public override void WillShowViewController (UINavigationController navigationController, UIViewController viewController, bool animated);
```

 <a name="New_Type:_MonoTouch.UIKit.UIMarkupTextPrintFormatter" class="injected"></a>


## New Type: MonoTouch.UIKit.UIMarkupTextPrintFormatter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class UIMarkupTextPrintFormatter : UIPrintFormatter {
        
        public UIMarkupTextPrintFormatter ();
        public UIMarkupTextPrintFormatter (MonoTouch.Foundation.NSCoder coder);
        public UIMarkupTextPrintFormatter (MonoTouch.Foundation.NSObjectFlag t);
        public UIMarkupTextPrintFormatter (IntPtr handle);
        public UIMarkupTextPrintFormatter (string text);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string MarkupText {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPickerViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPickerViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Changed:

```
public virtual string GetView (UIPickerView pickerView, int row, int component, UIView view);
```

New signature:

```
public virtual UIView GetView (UIPickerView pickerView, int row, int component, UIView view);
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrint" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrint

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public static class UIPrint {
        
        public static MonoTouch.Foundation.NSString ErrorDomain {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintError" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintError

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum UIPrintError {
        NotAvailable,
        NoContent,
        UnknownImageFormat,
        JobFailed
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintFormatter" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintFormatter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class UIPrintFormatter : MonoTouch.Foundation.NSObject {
        
        public UIPrintFormatter ();
        public UIPrintFormatter (MonoTouch.Foundation.NSCoder coder);
        public UIPrintFormatter (MonoTouch.Foundation.NSObjectFlag t);
        public UIPrintFormatter (IntPtr handle);
        
        public virtual void DrawRect (System.Drawing.RectangleF rect, int pageIndex);
        public virtual System.Drawing.RectangleF RectangleForPage (int pageIndex);
        public virtual void RemoveFromPrintPageRenderer ();
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIEdgeInsets ContentInsets {
                get;
                set;
        }
        public virtual float MaximumContentHeight {
                get;
                set;
        }
        public virtual float MaximumContentWidth {
                get;
                set;
        }
        public virtual int PageCount {
                get;
        }
        public virtual UIPrintPageRenderer PrintPageRenderer {
                get;
        }
        public virtual int StartPage {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintInfo" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintInfo

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class UIPrintInfo : MonoTouch.Foundation.NSObject {
        
        public UIPrintInfo ();
        public UIPrintInfo (MonoTouch.Foundation.NSCoder coder);
        public UIPrintInfo (MonoTouch.Foundation.NSObjectFlag t);
        public UIPrintInfo (IntPtr handle);
        
        public static UIPrintInfo FromDictionary (MonoTouch.Foundation.NSDictionary dictionary);
        
        public static UIPrintInfo PrintInfo {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIPrintInfoDuplex Duplex {
                get;
                set;
        }
        public virtual string JobName {
                get;
                set;
        }
        public virtual UIPrintInfoOrientation Orientation {
                get;
                set;
        }
        public virtual UIPrintInfoOutputType OutputType {
                get;
                set;
        }
        public virtual string PrinterID {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary ToDictionary {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintInfoDuplex" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintInfoDuplex

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum UIPrintInfoDuplex {
        None,
        LongEdge,
        ShortEdge
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintInfoOrientation" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintInfoOrientation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum UIPrintInfoOrientation {
        Portrait,
        Landscape
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintInfoOutputType" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintInfoOutputType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public enum UIPrintInfoOutputType {
        General,
        Photo,
        Grayscale
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintInteraction" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintInteraction

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public delegate UIViewController UIPrintInteraction (UIPrintInteractionController printInteractionController);
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintInteractionCompletionHandler" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintInteractionCompletionHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public delegate void UIPrintInteractionCompletionHandler (UIPrintInteractionController printInteractionController, bool completed, MonoTouch.Foundation.NSError error);
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintInteractionController" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintInteractionController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class UIPrintInteractionController : MonoTouch.Foundation.NSObject {
        
        public UIPrintInteractionController ();
        public UIPrintInteractionController (MonoTouch.Foundation.NSCoder coder);
        public UIPrintInteractionController (MonoTouch.Foundation.NSObjectFlag t);
        public UIPrintInteractionController (IntPtr handle);
        
        public static bool CanPrint (MonoTouch.Foundation.NSData data);
        public static bool CanPrint (MonoTouch.Foundation.NSUrl url);
        public virtual void Dismiss (bool animated);
        public virtual void Present (bool animated, UIPrintInteractionCompletionHandler completion);
        public virtual void PresentFromBarButtonItem (UIBarButtonItem item, bool animated, UIPrintInteractionCompletionHandler completion);
        public virtual void PresentFromRectInView (System.Drawing.RectangleF rect, UIView view, bool animated, UIPrintInteractionCompletionHandler completion);
        
        public static MonoTouch.Foundation.NSSet PrintableUTIs {
                get;
        }
        public static bool PrintingAvailable {
                get;
        }
        public static UIPrintInteractionController SharedPrintController {
                get;
        }
        public UIPrintInteractionPaperList ChoosePaper {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public UIPrintInteractionControllerDelegate Delegate {
                get;
                set;
        }
        public UIPrintInteraction GetViewController {
                get;
                set;
        }
        public virtual UIPrintFormatter PrintFormatter {
                get;
                set;
        }
        public virtual UIPrintInfo PrintInfo {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject[] PrintingItems {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject PrintItem {
                get;
                set;
        }
        public virtual UIPrintPageRenderer PrintPageRenderer {
                get;
                set;
        }
        public virtual UIPrintPaper PrintPaper {
                get;
        }
        public virtual bool ShowsPageRange {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSObject WeakDelegate {
                get;
                set;
        }
        
        public event EventHandler DidDismissPrinterOptions;
        public event EventHandler DidFinishJob;
        public event EventHandler DidPresentPrinterOptions;
        public event EventHandler WillDismissPrinterOptions;
        public event EventHandler WillPresentPrinterOptions;
        public event EventHandler WillStartJob;
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintInteractionControllerDelegate" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintInteractionControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class UIPrintInteractionControllerDelegate : MonoTouch.Foundation.NSObject {
        
        public UIPrintInteractionControllerDelegate ();
        public UIPrintInteractionControllerDelegate (MonoTouch.Foundation.NSCoder coder);
        public UIPrintInteractionControllerDelegate (MonoTouch.Foundation.NSObjectFlag t);
        public UIPrintInteractionControllerDelegate (IntPtr handle);
        
        public virtual UIPrintPaper ChoosePaper (UIPrintInteractionController printInteractionController, UIPrintPaper[] paperList);
        public virtual void DidDismissPrinterOptions (UIPrintInteractionController printInteractionController);
        public virtual void DidFinishJob (UIPrintInteractionController printInteractionController);
        public virtual void DidPresentPrinterOptions (UIPrintInteractionController printInteractionController);
        public virtual UIViewController GetViewController (UIPrintInteractionController printInteractionController);
        public virtual void WillDismissPrinterOptions (UIPrintInteractionController printInteractionController);
        public virtual void WillPresentPrinterOptions (UIPrintInteractionController printInteractionController);
        public virtual void WillStartJob (UIPrintInteractionController printInteractionController);
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintInteractionPaperList" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintInteractionPaperList

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
[Serializable]
public delegate UIPrintPaper UIPrintInteractionPaperList (UIPrintInteractionController printInteractionController, UIPrintPaper[] paperList);
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintPageRenderer" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintPageRenderer

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class UIPrintPageRenderer : MonoTouch.Foundation.NSObject {
        
        public UIPrintPageRenderer ();
        public UIPrintPageRenderer (MonoTouch.Foundation.NSCoder coder);
        public UIPrintPageRenderer (MonoTouch.Foundation.NSObjectFlag t);
        public UIPrintPageRenderer (IntPtr handle);
        
        public virtual void AddPrintFormatter (UIPrintFormatter formatter, int pageIndex);
        public virtual void DrawContentForPage (int index, System.Drawing.RectangleF contentRect);
        public virtual void DrawFooterForPage (int index, System.Drawing.RectangleF footerRect);
        public virtual void DrawHeaderForPage (int index, System.Drawing.RectangleF headerRect);
        public virtual void DrawPage (int index, System.Drawing.RectangleF pageRect);
        public virtual void DrawPrintFormatterForPage (UIPrintFormatter printFormatter, int index);
        public virtual void PrepareForDrawingPages (MonoTouch.Foundation.NSRange range);
        public virtual UIPrintFormatter[] PrintFormattersForPage (int index);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual float FooterHeight {
                get;
                set;
        }
        public virtual float HeaderHeight {
                get;
                set;
        }
        public virtual int NumberOfPages {
                get;
        }
        public virtual System.Drawing.RectangleF PaperRect {
                get;
        }
        public virtual System.Drawing.RectangleF PrintableRect {
                get;
        }
        public virtual UIPrintFormatter[] PrintFormatters {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIPrintPaper" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPrintPaper

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class UIPrintPaper : MonoTouch.Foundation.NSObject {
        
        public UIPrintPaper ();
        public UIPrintPaper (MonoTouch.Foundation.NSCoder coder);
        public UIPrintPaper (MonoTouch.Foundation.NSObjectFlag t);
        public UIPrintPaper (IntPtr handle);
        
        public static UIPrintPaper ForPageSize (System.Drawing.SizeF pageSize, UIPrintPaper[] paperList);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual System.Drawing.SizeF PaperSize {
                get;
        }
        public virtual System.Drawing.RectangleF PrintableRect {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBar

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public event EventHandler<UISearchBarButtonIndexEventArgs> SelectedScopeButtonIndexChanged;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBarButtonIndexEventArgs" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBarButtonIndexEventArgs

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
Could not find MonoTouch.UIKit.UISearchBarButtonIndexEventArgs
```

Added:

```
public class UISearchBarButtonIndexEventArgs : EventArgs {
        
        public UISearchBarButtonIndexEventArgs (int selectedScope);
        
        public int SelectedScope {
                get;
                set;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBarDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBarDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual void SelectedScopeButtonIndexChanged (UISearchBar searchBar, int selectedScope);
```

 <a name="New_Type:_MonoTouch.UIKit.UISimpleTextPrintFormatter" class="injected"></a>


## New Type: MonoTouch.UIKit.UISimpleTextPrintFormatter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class UISimpleTextPrintFormatter : UIPrintFormatter {
        
        public UISimpleTextPrintFormatter ();
        public UISimpleTextPrintFormatter (MonoTouch.Foundation.NSCoder coder);
        public UISimpleTextPrintFormatter (MonoTouch.Foundation.NSObjectFlag t);
        public UISimpleTextPrintFormatter (IntPtr handle);
        public UISimpleTextPrintFormatter (string text);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIColor Color {
                get;
                set;
        }
        public virtual UIFont Font {
                get;
                set;
        }
        public virtual UILineBreakMode LineBreakMode {
                get;
                set;
        }
        public virtual string Text {
                get;
                set;
        }
        public virtual UITextAlignment TextAlignment {
                get;
                set;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewDataSource" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewDataSource

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
public abstract int RowsInSection (UITableView tableview, int section);
```

Added:

```
public abstract int RowsInSection (UITableView tableView, int section);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public override void DecelerationEnded (UIScrollView scrollView);
        public override void DecelerationStarted (UIScrollView scrollView);
        public override void DidZoom (UIScrollView scrollView);
        public override void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
        public override void DraggingStarted (UIScrollView scrollView);
        public override void ScrollAnimationEnded (UIScrollView scrollView);
        public override void Scrolled (UIScrollView scrollView);
        public override void ScrolledToTop (UIScrollView scrollView);
        public override bool ShouldScrollToTop (UIScrollView scrollView);
        public override UIView ViewForZoomingInScrollView (UIScrollView scrollView);
        public override void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
        public override void ZoomingStarted (UIScrollView scrollView, UIView view);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITableViewSource" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableViewSource

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public override void DecelerationEnded (UIScrollView scrollView);
        public override void DecelerationStarted (UIScrollView scrollView);
        public override void DidZoom (UIScrollView scrollView);
        public override void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
        public override void DraggingStarted (UIScrollView scrollView);
        public override void ScrollAnimationEnded (UIScrollView scrollView);
        public override void Scrolled (UIScrollView scrollView);
        public override void ScrolledToTop (UIScrollView scrollView);
        public override bool ShouldScrollToTop (UIScrollView scrollView);
        public override UIView ViewForZoomingInScrollView (UIScrollView scrollView);
        public override void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
        public override void ZoomingStarted (UIScrollView scrollView, UIView view);
```

 <a name="New_Type:_MonoTouch.UIKit.UITextInputMode" class="injected"></a>


## New Type: MonoTouch.UIKit.UITextInputMode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

```
public class UITextInputMode : MonoTouch.Foundation.NSObject {
        
        public UITextInputMode ();
        public UITextInputMode (MonoTouch.Foundation.NSCoder coder);
        public UITextInputMode (MonoTouch.Foundation.NSObjectFlag t);
        public UITextInputMode (IntPtr handle);
        
        public static UITextInputMode CurrentInputMode {
                get;
        }
        public static MonoTouch.Foundation.NSString CurrentInputModeDidChangeNotification {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string PrimaryLanguage {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextViewDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextViewDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public override void DecelerationEnded (UIScrollView scrollView);
        public override void DecelerationStarted (UIScrollView scrollView);
        public override void DidZoom (UIScrollView scrollView);
        public override void DraggingEnded (UIScrollView scrollView, bool willDecelerate);
        public override void DraggingStarted (UIScrollView scrollView);
        public override void ScrollAnimationEnded (UIScrollView scrollView);
        public override void Scrolled (UIScrollView scrollView);
        public override void ScrolledToTop (UIScrollView scrollView);
        public override bool ShouldScrollToTop (UIScrollView scrollView);
        public override UIView ViewForZoomingInScrollView (UIScrollView scrollView);
        public override void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
        public override void ZoomingStarted (UIScrollView scrollView, UIView view);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIVideoEditorControllerDelegate" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIVideoEditorControllerDelegate

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public override void DidShowViewController (UINavigationController navigationController, UIViewController viewController, bool animated);
        public override void WillShowViewController (UINavigationController navigationController, UIViewController viewController, bool animated);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public virtual void DrawRect (System.Drawing.RectangleF area, UIViewPrintFormatter formatter);
        public virtual bool EnableInputClicksWhenVisible {
                get;
        }
        public virtual UIViewPrintFormatter ViewPrintFormatter {
                get;
        }
        
        public event MonoTouch.Foundation.NSAction AnimationWillEnd;
        public event MonoTouch.Foundation.NSAction AnimationWillStart;
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewController

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Removed:

```
set;
```

Added:

```
public virtual UISplitViewController SplitViewController {
                get;
        }
        public virtual UITabBarController TabBarController {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIViewPrintFormatter" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIViewPrintFormatter

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public class UIViewPrintFormatter : UIPrintFormatter {
        
        public UIViewPrintFormatter ();
        public UIViewPrintFormatter (MonoTouch.Foundation.NSCoder coder);
        public UIViewPrintFormatter (MonoTouch.Foundation.NSObjectFlag t);
        public UIViewPrintFormatter (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual UIView View {
                get;
        }
 }
```

 <a name="Namespace:_MonoTouch.iAd" class="injected"></a>


# Namespace: MonoTouch.iAd

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_MonoTouch.iAd.ADBannerView" class="injected"></a>


## Type Changed: MonoTouch.iAd.ADBannerView

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
public static MonoTouch.Foundation.NSString SizeIdentifierLandscape {
                get;
        }
        public static MonoTouch.Foundation.NSString SizeIdentifierPortrait {
                get;
        }
```

 <a name="Namespace:_System.Drawing" class="injected"></a>


# Namespace: System.Drawing

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

 <a name="Type_Changed:_System.Drawing.RectangleFExt" class="injected"></a>


## Type Changed: System.Drawing.RectangleFExt

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.1.3_to_3.2/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.2#)

Added:

```
// Extension methods for RectangleF 
 public static class RectangleFExt {
        
        public static void DivideRect (this RectangleF rect, out RectangleF slice, out RectangleF rem, float amount, Edge edge);
        public static RectangleF Inset (this RectangleF rect, float dx, float dy);
        public static RectangleF IntegralRect (this RectangleF rect);
        
        [Serializable]
        public enum Edge {
                MinX,
                MinY,
                MaxX,
                MaxY
        }
 }
```
