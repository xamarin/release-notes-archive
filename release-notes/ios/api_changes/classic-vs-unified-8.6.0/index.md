---
id: 0D9811DB-3A4D-4786-8179-D9E90AF6BF1A
title: "classic vs unified 8.6.0"
---

# Classic (monotouch.dll) vs Unified (Xamarin.iOS.dll) API differences

## Namespace Accelerate

### Type Changed: Accelerate.Pixel8888

Modified fields:

```
public readonly Pixel8888 Zero;
```

### Type Changed: Accelerate.PixelARGB16S

Modified fields:

```
public readonly PixelARGB16S Zero;
```

### Type Changed: Accelerate.PixelARGB16U

Modified fields:

```
public readonly PixelARGB16U Zero;
```

### Type Changed: Accelerate.PixelFFFF

Modified fields:

```
public readonly PixelFFFF Zero;
```

### Type Changed: Accelerate.vImage

Removed methods:

```
[Obsolete ("Use the overload with 'short[][] kernels' instead")]
	public static vImageError ConvolveMultiKernelARGB8888 (ref vImageBuffer src, ref vImageBuffer dest, IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, short[] kernels, uint kernel_height, uint kernel_width, int[] divisors, int[] biases, Pixel8888 backgroundColor, vImageFlags flags);

	[Obsolete ("Use the overload with 'float[][] kernels' instead")]
	public static vImageError ConvolveMultiKernelARGBFFFF (ref vImageBuffer src, ref vImageBuffer dest, IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, float[] kernels, uint kernel_height, uint kernel_width, float[] biases, PixelFFFF backgroundColor, vImageFlags flags);

	[Obsolete ("Use the overload with 'float[][] kernels' instead")]
	public static vImageError ConvolveMultiKernelARGBFFFF (ref vImageBuffer src, ref vImageBuffer dest, IntPtr tempBuffer, int srcOffsetToROI_X, int srcOffsetToROI_Y, float[] kernels, uint kernel_height, uint kernel_width, float[] biases, ref PixelFFFF backgroundColor, vImageFlags flags);
```

## Namespace Accounts

### Type Changed: Accounts.ACAccount

Modified constructors:

```
public protected ACAccount (Foundation.NSObjectFlag t)
	public protected ACAccount (IntPtr handle)
```

### Type Changed: Accounts.ACAccountCredential

Modified constructors:

```
public protected ACAccountCredential (Foundation.NSObjectFlag t)
	public protected ACAccountCredential (IntPtr handle)
```

### Type Changed: Accounts.ACAccountStore

Modified constructors:

```
public protected ACAccountStore (Foundation.NSObjectFlag t)
	public protected ACAccountStore (IntPtr handle)
```

Removed methods:

```
protected virtual System.Threading.Tasks.Task<bool> RequestAccessAsync (ACAccountType accountType, Foundation.NSDictionary options);
	public System.Threading.Tasks.Task<bool> RequestAccessAsync (ACAccountType accountType, AccountStoreOptions options);
	public virtual System.Threading.Tasks.Task<bool> RequestAccessAsync (ACAccountType accountType);
	public virtual System.Threading.Tasks.Task<bool> SaveAccountAsync (ACAccount account);
```

Added methods:

```
protected virtual System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> RequestAccessAsync (ACAccountType accountType, Foundation.NSDictionary options);
	public System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> RequestAccessAsync (ACAccountType accountType, AccountStoreOptions options);
	public virtual System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> RequestAccessAsync (ACAccountType accountType);
	public virtual System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> SaveAccountAsync (ACAccount account);
```

### Type Changed: Accounts.ACAccountType

Modified constructors:

```
public protected ACAccountType (Foundation.NSObjectFlag t)
	public protected ACAccountType (IntPtr handle)
```

## Namespace AddressBook

### Type Changed: AddressBook.ABPerson

Removed methods:

```
[Obsolete ("Use GetAllAddresses")]
	public AddressBook.ABMultiValue<Foundation.NSDictionary> GetAddresses ();

	[Obsolete ("Use GetInstantMessageServices")]
	public AddressBook.ABMultiValue<Foundation.NSDictionary> GetInstantMessages ();

	[Obsolete ("Use GetSocialProfiles")]
	public AddressBook.ABMultiValue<Foundation.NSDictionary> GetSocialProfile ();
```

### Type Changed: AddressBook.ABSource

Removed field:

```
[Obsolete ("Use ABSourceType.SearchableMask")]
	public static const int SearchableMask;
```

### Type Changed: AddressBook.InstantMessageService

Removed property:

```
public Foundation.NSString Service { set; }
```

### Type Changed: AddressBook.SocialProfile

Removed property:

```
public Foundation.NSString Service { set; }
```

## Namespace AddressBookUI

### Type Changed: AddressBookUI.ABNewPersonViewController

Modified constructors:

```
public protected ABNewPersonViewController (Foundation.NSObjectFlag t)
	public protected ABNewPersonViewController (IntPtr handle)
```

Modified properties:

```
public ABNewPersonViewControllerDelegate IABNewPersonViewControllerDelegate Delegate { get; set; }
```

### Type Changed: AddressBookUI.ABNewPersonViewControllerDelegate

Modified constructors:

```
public protected ABNewPersonViewControllerDelegate ()
	public protected ABNewPersonViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected ABNewPersonViewControllerDelegate (IntPtr handle)
```

Removed method:

```
public virtual void DidCompleteWithNewPerson (ABNewPersonViewController controller, IntPtr person);
```

Added method:

```
public virtual void DidCompleteWithNewPerson (ABNewPersonViewController controller, AddressBook.ABPerson person);
```

### Type Changed: AddressBookUI.ABPeoplePickerNavigationController

Modified constructors:

```
public protected ABPeoplePickerNavigationController (Foundation.NSObjectFlag t)
	public protected ABPeoplePickerNavigationController (IntPtr handle)
```

Modified properties:

```
public ABPeoplePickerNavigationControllerDelegate IABPeoplePickerNavigationControllerDelegate Delegate { get; set; }
```

### Type Changed: AddressBookUI.ABPeoplePickerNavigationControllerDelegate

Modified constructors:

```
public protected ABPeoplePickerNavigationControllerDelegate (Foundation.NSObjectFlag t)
	public protected ABPeoplePickerNavigationControllerDelegate (IntPtr handle)
```

Removed methods:

```
public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, AddressBook.ABPerson selectedPerson, int propertyId, IntPtr abMultiValueIdentifier);
	public override void DidShowViewController (UIKit.UINavigationController navigationController, UIKit.UIViewController viewController, bool animated);
	public override UIKit.IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UIKit.UINavigationController navigationController, UIKit.UINavigationControllerOperation operation, UIKit.UIViewController fromViewController, UIKit.UIViewController toViewController);
	public override UIKit.IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UIKit.UINavigationController navigationController, UIKit.IUIViewControllerAnimatedTransitioning animationController);
	public override UIKit.UIInterfaceOrientation GetPreferredInterfaceOrientation (UIKit.UINavigationController navigationController);
	public virtual bool ShouldContinue (ABPeoplePickerNavigationController peoplePicker, IntPtr selectedPerson);
	public virtual bool ShouldContinue (ABPeoplePickerNavigationController peoplePicker, IntPtr selectedPerson, int propertyId, int identifier);
	public override UIKit.UIInterfaceOrientationMask SupportedInterfaceOrientations (UIKit.UINavigationController navigationController);
	public override void WillShowViewController (UIKit.UINavigationController navigationController, UIKit.UIViewController viewController, bool animated);
```

Added methods:

```
public virtual void DidSelectPerson (ABPeoplePickerNavigationController peoplePicker, AddressBook.ABPerson selectedPerson, int propertyId, int identifier);
	public virtual bool ShouldContinue (ABPeoplePickerNavigationController peoplePicker, AddressBook.ABPerson selectedPerson);
	public virtual bool ShouldContinue (ABPeoplePickerNavigationController peoplePicker, AddressBook.ABPerson selectedPerson, int propertyId, int identifier);
```

### Type Changed: AddressBookUI.ABPeoplePickerNavigationControllerDelegate_Extensions

Removed methods:

```
public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, AddressBook.ABPerson selectedPerson, int propertyId, IntPtr abMultiValueIdentifier);
	public static bool ShouldContinue (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, IntPtr selectedPerson);
	public static bool ShouldContinue (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, IntPtr selectedPerson, int propertyId, int identifier);
```

Added methods:

```
public static void DidSelectPerson (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, AddressBook.ABPerson selectedPerson, int propertyId, int identifier);
	public static bool ShouldContinue (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, AddressBook.ABPerson selectedPerson);
	public static bool ShouldContinue (IABPeoplePickerNavigationControllerDelegate This, ABPeoplePickerNavigationController peoplePicker, AddressBook.ABPerson selectedPerson, int propertyId, int identifier);
```

### Type Changed: AddressBookUI.ABPersonViewController

Modified constructors:

```
public protected ABPersonViewController (Foundation.NSObjectFlag t)
	public protected ABPersonViewController (IntPtr handle)
```

Modified properties:

```
public ABPersonViewControllerDelegate IABPersonViewControllerDelegate Delegate { get; set; }
```

Removed method:

```
[Obsolete ("Use SetHighlightedItemForProperty(ABPersonProperty,int?).")]
	public virtual void SetHighlightedItemForProperty (int property, int identifier);
```

### Type Changed: AddressBookUI.ABPersonViewControllerDelegate

Modified constructors:

```
public protected ABPersonViewControllerDelegate ()
	public protected ABPersonViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected ABPersonViewControllerDelegate (IntPtr handle)
```

Removed method:

```
public virtual bool ShouldPerformDefaultActionForPerson (ABPersonViewController personViewController, IntPtr person, int propertyId, int identifier);
```

Added method:

```
public virtual bool ShouldPerformDefaultActionForPerson (ABPersonViewController personViewController, AddressBook.ABPerson person, int propertyId, int identifier);
```

### Type Changed: AddressBookUI.ABUnknownPersonViewController

Modified constructors:

```
public protected ABUnknownPersonViewController (Foundation.NSObjectFlag t)
	public protected ABUnknownPersonViewController (IntPtr handle)
```

Modified properties:

```
public ABUnknownPersonViewControllerDelegate IABUnknownPersonViewControllerDelegate Delegate { get; set; }
```

### Type Changed: AddressBookUI.ABUnknownPersonViewControllerDelegate

Modified constructors:

```
public protected ABUnknownPersonViewControllerDelegate ()
	public protected ABUnknownPersonViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected ABUnknownPersonViewControllerDelegate (IntPtr handle)
```

Removed methods:

```
public virtual void DidResolveToPerson (ABUnknownPersonViewController unknownPersonView, IntPtr person);
	public virtual bool ShouldPerformDefaultActionForPerson (ABUnknownPersonViewController personViewController, IntPtr person, int propertyId, int identifier);
```

Added methods:

```
public virtual void DidResolveToPerson (ABUnknownPersonViewController unknownPersonView, AddressBook.ABPerson person);
	public virtual bool ShouldPerformDefaultActionForPerson (ABUnknownPersonViewController personViewController, AddressBook.ABPerson person, int propertyId, int identifier);
```

### Type Changed: AddressBookUI.ABUnknownPersonViewControllerDelegate_Extensions

Removed methods:

```
public static void DidResolveToPerson (IABUnknownPersonViewControllerDelegate This, ABUnknownPersonViewController unknownPersonView, IntPtr person);
	public static bool ShouldPerformDefaultActionForPerson (IABUnknownPersonViewControllerDelegate This, ABUnknownPersonViewController personViewController, IntPtr person, int propertyId, int identifier);
```

Added method:

```
public static bool ShouldPerformDefaultActionForPerson (IABUnknownPersonViewControllerDelegate This, ABUnknownPersonViewController personViewController, AddressBook.ABPerson person, int propertyId, int identifier);
```

### Type Changed: AddressBookUI.IABNewPersonViewControllerDelegate

Added method:

```
public virtual void DidCompleteWithNewPerson (ABNewPersonViewController controller, AddressBook.ABPerson person);
```

### Type Changed: AddressBookUI.IABPersonViewControllerDelegate

Added method:

```
public virtual bool ShouldPerformDefaultActionForPerson (ABPersonViewController personViewController, AddressBook.ABPerson person, int propertyId, int identifier);
```

### Type Changed: AddressBookUI.IABUnknownPersonViewControllerDelegate

Added method:

```
public virtual void DidResolveToPerson (ABUnknownPersonViewController unknownPersonView, AddressBook.ABPerson person);
```

### Removed Type AddressBookUI.ABNewPersonViewControllerDelegate_Extensions ### Removed Type AddressBookUI.ABPersonViewControllerDelegate_Extensions 



## Namespace AdSupport

### Type Changed: AdSupport.ASIdentifierManager

Modified constructors:

```
public protected ASIdentifierManager (Foundation.NSObjectFlag t)
	public protected ASIdentifierManager (IntPtr handle)
```

## Namespace AssetsLibrary

### Type Changed: AssetsLibrary.ALAsset

Modified constructors:

```
public protected ALAsset (Foundation.NSObjectFlag t)
	public protected ALAsset (IntPtr handle)
```

Removed methods:

```
public virtual void SetImageData (Foundation.NSData imageData, Foundation.NSDictionary metadata, ALAssetsLibraryWriteCompletionDelegate completionBlock);
	public virtual void SetVideoAtPath (Foundation.NSUrl videoPathURL, ALAssetsLibraryWriteCompletionDelegate completionBlock);
	public virtual void WriteModifiedImageToSavedToPhotosAlbum (Foundation.NSData imageData, Foundation.NSDictionary metadata, ALAssetsLibraryWriteCompletionDelegate completionBlock);
	public virtual void WriteModifiedVideoToSavedPhotosAlbum (Foundation.NSUrl videoPathURL, ALAssetsLibraryWriteCompletionDelegate completionBlock);
```

Added methods:

```
public virtual void SetImageData (Foundation.NSData imageData, Foundation.NSDictionary metadata, System.Action<Foundation.NSUrl,Foundation.NSError> completionBlock);
	public virtual void SetVideoAtPath (Foundation.NSUrl videoPathURL, System.Action<Foundation.NSUrl,Foundation.NSError> completionBlock);
	public virtual void WriteModifiedImageToSavedToPhotosAlbum (Foundation.NSData imageData, Foundation.NSDictionary metadata, System.Action<Foundation.NSUrl,Foundation.NSError> completionBlock);
	public virtual void WriteModifiedVideoToSavedPhotosAlbum (Foundation.NSUrl videoPathURL, System.Action<Foundation.NSUrl,Foundation.NSError> completionBlock);
```

### Type Changed: AssetsLibrary.ALAssetRepresentation

Modified constructors:

```
public protected ALAssetRepresentation (Foundation.NSObjectFlag t)
	public protected ALAssetRepresentation (IntPtr handle)
```

### Type Changed: AssetsLibrary.ALAssetsFilter

Modified constructors:

```
public protected ALAssetsFilter (Foundation.NSObjectFlag t)
	public protected ALAssetsFilter (IntPtr handle)
```

### Type Changed: AssetsLibrary.ALAssetsGroup

Modified constructors:

```
public protected ALAssetsGroup (Foundation.NSObjectFlag t)
	public protected ALAssetsGroup (IntPtr handle)
```

### Type Changed: AssetsLibrary.ALAssetsLibrary

Modified constructors:

```
public protected ALAssetsLibrary (Foundation.NSObjectFlag t)
	public protected ALAssetsLibrary (IntPtr handle)
```

Removed methods:

```
public virtual void AddAssetsGroupAlbum (string name, ALAssetsLibraryGroupResult resultBlock, ALAssetsLibraryAccessFailure failureBlock);
	public virtual void AssetForUrl (Foundation.NSUrl assetURL, ALAssetsLibraryAssetForURLResultDelegate resultBlock, ALAssetsLibraryAccessFailureDelegate failureBlock);
	public virtual void Enumerate (ALAssetsGroupType types, ALAssetsLibraryGroupsEnumerationResultsDelegate enumerationBlock, ALAssetsLibraryAccessFailureDelegate failureBlock);
	public virtual void GroupForUrl (Foundation.NSUrl groupURL, ALAssetsLibraryGroupResult resultBlock, ALAssetsLibraryAccessFailure failureBlock);
	public virtual void WriteImageToSavedPhotosAlbum (CoreGraphics.CGImage imageData, ALAssetOrientation orientation, ALAssetsLibraryWriteCompletionDelegate completionBlock);
	public virtual void WriteImageToSavedPhotosAlbum (CoreGraphics.CGImage imageData, Foundation.NSDictionary metadata, ALAssetsLibraryWriteCompletionDelegate completionBlock);
	public virtual void WriteImageToSavedPhotosAlbum (Foundation.NSData imageData, Foundation.NSDictionary metadata, ALAssetsLibraryWriteCompletionDelegate completionBlock);

	[Obsolete ("Use the overload that takes a CGImage instead")]
	public virtual void WriteImageToSavedPhotosAlbum (UIKit.UIImage imageData, Foundation.NSDictionary metadata, ALAssetsLibraryWriteCompletionDelegate completionBlock);

	[Obsolete ("Use the overload that takes a CGImage instead")]
	public virtual void WriteImageToSavedPhotosAlbum (UIKit.UIImage imageData, ALAssetOrientation orientation, ALAssetsLibraryWriteCompletionDelegate completionBlock);
	public virtual void WriteVideoToSavedPhotosAlbum (Foundation.NSUrl videoPathURL, ALAssetsLibraryWriteCompletionDelegate completionBlock);
```

Added methods:

```
public virtual void AddAssetsGroupAlbum (string name, System.Action<ALAssetsGroup> resultBlock, System.Action<Foundation.NSError> failureBlock);
	public virtual void AssetForUrl (Foundation.NSUrl assetURL, System.Action<ALAsset> resultBlock, System.Action<Foundation.NSError> failureBlock);
	public virtual void Enumerate (ALAssetsGroupType types, ALAssetsLibraryGroupsEnumerationResultsDelegate enumerationBlock, System.Action<Foundation.NSError> failureBlock);
	public virtual void GroupForUrl (Foundation.NSUrl groupURL, System.Action<ALAssetsGroup> resultBlock, System.Action<Foundation.NSError> failureBlock);
	public virtual void WriteImageToSavedPhotosAlbum (CoreGraphics.CGImage imageData, ALAssetOrientation orientation, System.Action<Foundation.NSUrl,Foundation.NSError> completionBlock);
	public virtual void WriteImageToSavedPhotosAlbum (CoreGraphics.CGImage imageData, Foundation.NSDictionary metadata, System.Action<Foundation.NSUrl,Foundation.NSError> completionBlock);
	public virtual void WriteImageToSavedPhotosAlbum (Foundation.NSData imageData, Foundation.NSDictionary metadata, System.Action<Foundation.NSUrl,Foundation.NSError> completionBlock);
	public virtual void WriteVideoToSavedPhotosAlbum (Foundation.NSUrl videoPathURL, System.Action<Foundation.NSUrl,Foundation.NSError> completionBlock);
```

### Removed Type AssetsLibrary.ALAssetsLibraryAccessFailure ### Removed Type AssetsLibrary.ALAssetsLibraryAccessFailureDelegate ### Removed Type AssetsLibrary.ALAssetsLibraryAssetForURLResultDelegate ### Removed Type AssetsLibrary.ALAssetsLibraryGroupResult ### Removed Type AssetsLibrary.ALAssetsLibraryWriteCompletionDelegate 



## Namespace AudioToolbox



### Type Changed: AudioToolbox.AudioFile

Removed field:

```
protected IntPtr handle;
```

Removed method:

```
[Obsolete ("Use ReadPacketData instead")]
	public AudioFileError ReadPackets (bool useCache, out int numBytes, AudioStreamPacketDescription[] packetDescriptions, long startingPacket, ref int numPackets, IntPtr buffer);
```

### Type Changed: AudioToolbox.AudioQueue

Removed methods:

```
[Obsolete ("Use CreateProcessingTap (AudioQueueProcessingTapDelegate, AudioQueueProcessingTapFlags, out AudioQueueStatus) instead")]
	public AudioQueueProcessingTap CreateProcessingTap (AudioQueueProcessingTapCallback processingCallback, AudioQueueProcessingTapFlags flags, out AudioQueueStatus status);
	public virtual void Dispose (bool disposing, bool immediate);
```

Added method:

```
protected virtual void Dispose (bool disposing);
```

### Type Changed: AudioToolbox.AudioQueueProcessingTap

Removed method:

```
[Obsolete ("Use overload with AudioBuffers")]
	public AudioQueueStatus GetSourceAudio (uint numberOfFrames, ref AudioTimeStamp timeStamp, out AudioQueueProcessingTapFlags flags, out uint parentNumberOfFrames, AudioBufferList data);
```

### Type Changed: AudioToolbox.AudioQueueTimeline

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: AudioToolbox.MusicSequence

Removed methods:

```
public MusicPlayerStatus BarBeatTimeToBeats (CoreAnimation.CABarBeatTime barBeatTime, out double beats);

	[Obsolete ("Use overload with an out 'double beats'")]
	public MusicPlayerStatus BarBeatTimeToBeats (CoreAnimation.CABarBeatTime barBeatTime);
	public MusicPlayerStatus BeatsToBarBeatTime (double beats, int subbeatDivisor, out CoreAnimation.CABarBeatTime barBeatTime);

	[Obsolete ("Use GetTrackIndex(MusicTrack, out int) to distinguish between the track or an error code")]
	public int GetTrackIndex (MusicTrack track);
```

Added methods:

```
public MusicPlayerStatus BarBeatTimeToBeats (CABarBeatTime barBeatTime, out double beats);
	public MusicPlayerStatus BeatsToBarBeatTime (double beats, int subbeatDivisor, out CABarBeatTime barBeatTime);
```

### Type Changed: AudioToolbox.OutputAudioQueue

Removed event:

```
public event System.EventHandler<OutputCompletedEventArgs> OutputCompleted;
```

Added event:

```
public event System.EventHandler<BufferCompletedEventArgs> BufferCompleted;
```

Removed method:

```
protected virtual void OnOutputCompleted (IntPtr audioQueueBuffer);
```

Added method:

```
protected virtual void OnBufferCompleted (IntPtr audioQueueBuffer);
```

### Type Changed: AudioToolbox.SoundBank

Removed constructor:

```
public SoundBank ();
```

### Removed Type AudioToolbox.AudioBufferList ### Removed Type AudioToolbox.AudioQueueProcessingTapCallback ### Removed Type AudioToolbox.MutableAudioBufferList ### Removed Type AudioToolbox.OutputCompletedEventArgs ### New Type AudioToolbox.BufferCompletedEventArgs

```
public class BufferCompletedEventArgs : System.EventArgs {
	// constructors
	public BufferCompletedEventArgs (IntPtr audioQueueBuffer);
	public BufferCompletedEventArgs (AudioQueueBuffer* audioQueueBuffer);
	// properties
	public IntPtr IntPtrBuffer { get; }
	public AudioQueueBuffer* UnsafeBuffer { get; set; }
}
```

### New Type AudioToolbox.CABarBeatTime

```
public struct CABarBeatTime {
	// fields
	public int Bar;
	public ushort Beat;
	public ushort Reserved;
	public ushort Subbeat;
	public ushort SubbeatDivisor;
}
```





## Namespace AudioUnit



### Type Changed: AudioUnit.AudioComponent

Modified properties:

```
public AudioComponentDescription AudioComponentDescription? Description { get; }
```

Removed methods:

```
[Obsolete ("Use the overload that accept a ref to the AudioComponentDescription parameter")]
	public static AudioComponent FindComponent (AudioComponentDescription cd);

	[Obsolete ("Use the overload that accept a ref to the AudioComponentDescription parameter")]
	public static AudioComponent FindNextComponent (AudioComponent cmp, AudioComponentDescription cd);
```

### Type Changed: AudioUnit.AudioComponentDescription

Removed constructor:

```
public AudioComponentDescription ();
```

### Type Changed: AudioUnit.AudioTypeMusicDevice

Removed value:

```
[Obsolete]
	None = 0,
```

### Type Changed: AudioUnit.AudioUnit

Removed event:

```
[Obsolete ("Use SetRenderCallback")]
	public event System.EventHandler<AudioUnitEventArgs> RenderCallback;
```

Removed methods:

```
[Obsolete]
	public void Render (AudioUnitRenderActionFlags flags, AudioToolbox.AudioTimeStamp timeStamp, int outputBusnumber, int numberFrames, AudioToolbox.AudioBufferList data);

	[Obsolete]
	public AudioUnitStatus TryRender (AudioUnitRenderActionFlags flags, AudioToolbox.AudioTimeStamp timeStamp, int outputBusnumber, int numberFrames, AudioToolbox.AudioBufferList data);
```

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: AudioUnit.AudioUnitUtils

Removed methods:

```
[Obsolete ("Use AudioStreamBasicDescription::CreateLinearPCM instead")]
	public static AudioToolbox.AudioStreamBasicDescription AUCanonicalASBD (double sampleRate, int channel);

	[Obsolete ("Use AudioSession::OverrideCategoryDefaultToSpeaker instead")]
	public static void SetOverrideCategoryDefaultToSpeaker (bool isSpeaker);
```

### Type Changed: AudioUnit.AUGraph

Removed property:

```
[Obsolete ("Use Handle property instead")]
	public IntPtr Handler { get; }
```

Removed event:

```
public event System.EventHandler<AudioGraphEventArgs> RenderCallback;
```

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: AudioUnit.ExtAudioFile

Removed methods:

```
[Obsolete ("Use overload with AudioBuffers")]
	public int Read (int numberFrames, AudioToolbox.AudioBufferList data);

	[Obsolete ("Use overload with AudioBuffers")]
	public void WriteAsync (int numberFrames, AudioToolbox.AudioBufferList data);
```

### Removed Type AudioUnit.AudioComponentDescriptionNative ### Removed Type AudioUnit.AudioGraphEventArgs ### Removed Type AudioUnit.AudioUnitEventArgs 



## Namespace AVFoundation



### Type Changed: AVFoundation.AudioSettings

Modified properties:

```
public float? double? SampleRate { get; set; }
```

### Type Changed: AVFoundation.AVAsset

Modified constructors:

```
public protected AVAsset (Foundation.NSObjectFlag t)
	public protected AVAsset (IntPtr handle)
```

Removed method:

```
public virtual void LoadValuesAsynchronously (string[] keys, Foundation.NSAction handler);
```

Added method:

```
public virtual void LoadValuesAsynchronously (string[] keys, System.Action handler);
```

### Type Changed: AVFoundation.AVAssetExportSession

Modified constructors:

```
public protected AVAssetExportSession (Foundation.NSObjectFlag t)
	public protected AVAssetExportSession (IntPtr handle)
```

Modified properties:

```
public virtual AVVideoCompositing IAVVideoCompositing CustomVideoCompositor { get; }
```

Removed method:

```
public virtual void ExportAsynchronously (AVCompletionHandler handler);
```

Added method:

```
public virtual void ExportAsynchronously (System.Action handler);
```

### Type Changed: AVFoundation.AVAssetImageGenerator

Modified constructors:

```
public protected AVAssetImageGenerator (Foundation.NSObjectFlag t)
	public protected AVAssetImageGenerator (IntPtr handle)
```

Modified properties:

```
public virtual AVVideoCompositing IAVVideoCompositing CustomVideoCompositor { get; }
```

Removed method:

```
[Obsolete ("Use the overload that takes NSValue[] instead")]
	public virtual void GenerateCGImagesAsynchronously (Foundation.NSValue cmTimesRequestedTimes, AVAssetImageGeneratorCompletionHandler handler);
```

### Type Changed: AVFoundation.AVAssetReader

Modified constructors:

```
public protected AVAssetReader (Foundation.NSObjectFlag t)
	public protected AVAssetReader (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetReaderAudioMixOutput

Modified constructors:

```
public protected AVAssetReaderAudioMixOutput (Foundation.NSObjectFlag t)
	public protected AVAssetReaderAudioMixOutput (IntPtr handle)
```

Removed property:

```
public virtual Foundation.NSDictionary AudioSettings { get; }
```

Removed method:

```
public static AVAssetReaderAudioMixOutput FromTracks (AVAssetTrack[] audioTracks, Foundation.NSDictionary audioSettings);
```

### Type Changed: AVFoundation.AVAssetReaderOutput

Modified constructors:

```
public protected AVAssetReaderOutput (Foundation.NSObjectFlag t)
	public protected AVAssetReaderOutput (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetReaderOutputMetadataAdaptor

Modified constructors:

```
public protected AVAssetReaderOutputMetadataAdaptor (Foundation.NSObjectFlag t)
	public protected AVAssetReaderOutputMetadataAdaptor (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetReaderSampleReferenceOutput

Modified constructors:

```
public protected AVAssetReaderSampleReferenceOutput (Foundation.NSObjectFlag t)
	public protected AVAssetReaderSampleReferenceOutput (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetReaderTrackOutput

Modified constructors:

```
public protected AVAssetReaderTrackOutput (Foundation.NSObjectFlag t)
	public protected AVAssetReaderTrackOutput (IntPtr handle)
```

Removed method:

```
public static AVAssetReaderTrackOutput FromTrack (AVAssetTrack track, Foundation.NSDictionary outputSettings);
```

### Type Changed: AVFoundation.AVAssetReaderVideoCompositionOutput

Removed constructors:

```
[Obsolete ("Use overload with PixelBufferAttributes")]
	public AVAssetReaderVideoCompositionOutput (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
```

Modified constructors:

```
public protected AVAssetReaderVideoCompositionOutput (Foundation.NSObjectFlag t)
	public protected AVAssetReaderVideoCompositionOutput (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use UncompressedVideoSettings property")]
	public AVVideoSettings VideoSettings { get; }
```

Modified properties:

```
public virtual AVVideoCompositing IAVVideoCompositing CustomVideoCompositor { get; }
```

Removed methods:

```
[Obsolete ("Use Create method or constructor")]
	public AVAssetReaderVideoCompositionOutput FromTracks (AVAssetTrack[] videoTracks, AVVideoSettings videoSettings);
	public static AVAssetReaderVideoCompositionOutput WeakFromTracks (AVAssetTrack[] videoTracks, Foundation.NSDictionary videoSettings);
```

### Type Changed: AVFoundation.AVAssetResourceLoader

Removed constructors:

```
public AVAssetResourceLoader ();
```

Modified constructors:

```
public protected AVAssetResourceLoader (Foundation.NSObjectFlag t)
	public protected AVAssetResourceLoader (IntPtr handle)
```

Modified properties:

```
public virtual AVAssetResourceLoaderDelegate IAVAssetResourceLoaderDelegate Delegate { get; }
```

Removed method:

```
public virtual void SetDelegate (AVAssetResourceLoaderDelegate resourceLoaderDelegate, CoreFoundation.DispatchQueue delegateQueue);
```

Added method:

```
public virtual void SetDelegate (IAVAssetResourceLoaderDelegate resourceLoaderDelegate, CoreFoundation.DispatchQueue delegateQueue);
```

### Type Changed: AVFoundation.AVAssetResourceLoaderDelegate

Modified constructors:

```
public protected AVAssetResourceLoaderDelegate ()
	public protected AVAssetResourceLoaderDelegate (Foundation.NSObjectFlag t)
	public protected AVAssetResourceLoaderDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetResourceLoadingContentInformationRequest

Removed constructors:

```
public AVAssetResourceLoadingContentInformationRequest ();
```

Modified constructors:

```
public protected AVAssetResourceLoadingContentInformationRequest (Foundation.NSObjectFlag t)
	public protected AVAssetResourceLoadingContentInformationRequest (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetResourceLoadingDataRequest

Removed constructors:

```
[Obsolete ("Type is not meant to be created by user code")]
	public AVAssetResourceLoadingDataRequest ();
```

Modified constructors:

```
public protected AVAssetResourceLoadingDataRequest (Foundation.NSObjectFlag t)
	public protected AVAssetResourceLoadingDataRequest (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetResourceLoadingRequest

Removed constructors:

```
public AVAssetResourceLoadingRequest ();
```

Modified constructors:

```
public protected AVAssetResourceLoadingRequest (Foundation.NSObjectFlag t)
	public protected AVAssetResourceLoadingRequest (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetResourceRenewalRequest

Modified constructors:

```
public protected AVAssetResourceRenewalRequest (Foundation.NSObjectFlag t)
	public protected AVAssetResourceRenewalRequest (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetTrack

Modified constructors:

```
public protected AVAssetTrack (Foundation.NSObjectFlag t)
	public protected AVAssetTrack (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetTrackGroup

Modified constructors:

```
public protected AVAssetTrackGroup (Foundation.NSObjectFlag t)
	public protected AVAssetTrackGroup (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetTrackSegment

Modified constructors:

```
public protected AVAssetTrackSegment (Foundation.NSObjectFlag t)
	public protected AVAssetTrackSegment (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetWriter

Modified constructors:

```
public protected AVAssetWriter (Foundation.NSObjectFlag t)
	public protected AVAssetWriter (IntPtr handle)
```

Removed method:

```
public virtual void FinishWriting (Foundation.NSAction completionHandler);
```

Added method:

```
public virtual void FinishWriting (System.Action completionHandler);
```

### Type Changed: AVFoundation.AVAssetWriterInput

Modified constructors:

```
public protected AVAssetWriterInput (string mediaType, Foundation.NSDictionary outputSettings)
	public protected AVAssetWriterInput (IntPtr handle)
	public protected AVAssetWriterInput (Foundation.NSObjectFlag t)
```

Removed methods:

```
public static AVAssetWriterInput FromType (string mediaType, Foundation.NSDictionary outputSettings);
	public virtual void RequestMediaData (CoreFoundation.DispatchQueue queue, Foundation.NSAction action);
```

Added method:

```
public virtual void RequestMediaData (CoreFoundation.DispatchQueue queue, System.Action action);
```

### Type Changed: AVFoundation.AVAssetWriterInputGroup

Modified constructors:

```
public protected AVAssetWriterInputGroup (Foundation.NSObjectFlag t)
	public protected AVAssetWriterInputGroup (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetWriterInputMetadataAdaptor

Modified constructors:

```
public protected AVAssetWriterInputMetadataAdaptor (Foundation.NSObjectFlag t)
	public protected AVAssetWriterInputMetadataAdaptor (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetWriterInputPassDescription

Modified constructors:

```
public protected AVAssetWriterInputPassDescription (Foundation.NSObjectFlag t)
	public protected AVAssetWriterInputPassDescription (IntPtr handle)
```

### Type Changed: AVFoundation.AVAssetWriterInputPixelBufferAdaptor

Modified constructors:

```
public protected AVAssetWriterInputPixelBufferAdaptor (Foundation.NSObjectFlag t)
	public protected AVAssetWriterInputPixelBufferAdaptor (IntPtr handle)
```

### Type Changed: AVFoundation.AVAsynchronousKeyValueLoading

Modified constructors:

```
public protected AVAsynchronousKeyValueLoading ()
	public protected AVAsynchronousKeyValueLoading (Foundation.NSObjectFlag t)
	public protected AVAsynchronousKeyValueLoading (IntPtr handle)
```

Removed method:

```
public virtual void LoadValuesAsynchronously (string[] keys, Foundation.NSAction handler);
```

Added method:

```
public virtual void LoadValuesAsynchronously (string[] keys, System.Action handler);
```

### Type Changed: AVFoundation.AVAsynchronousVideoCompositionRequest

Modified constructors:

```
public protected AVAsynchronousVideoCompositionRequest (Foundation.NSObjectFlag t)
	public protected AVAsynchronousVideoCompositionRequest (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudio3DMixing

Modified constructors:

```
public protected AVAudio3DMixing ()
	public protected AVAudio3DMixing (Foundation.NSObjectFlag t)
	public protected AVAudio3DMixing (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioBuffer

Modified constructors:

```
public protected AVAudioBuffer (Foundation.NSObjectFlag t)
	public protected AVAudioBuffer (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioChannelLayout

Modified constructors:

```
public protected AVAudioChannelLayout (Foundation.NSObjectFlag t)
	public protected AVAudioChannelLayout (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioEngine

Modified constructors:

```
public protected AVAudioEngine (Foundation.NSObjectFlag t)
	public protected AVAudioEngine (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioEnvironmentDistanceAttenuationParameters

Modified constructors:

```
public protected AVAudioEnvironmentDistanceAttenuationParameters (Foundation.NSObjectFlag t)
	public protected AVAudioEnvironmentDistanceAttenuationParameters (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioEnvironmentNode

Modified constructors:

```
public protected AVAudioEnvironmentNode (Foundation.NSObjectFlag t)
	public protected AVAudioEnvironmentNode (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioEnvironmentReverbParameters

Modified constructors:

```
public protected AVAudioEnvironmentReverbParameters (Foundation.NSObjectFlag t)
	public protected AVAudioEnvironmentReverbParameters (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioFile

Modified constructors:

```
public protected AVAudioFile (IntPtr handle)
	public protected AVAudioFile (Foundation.NSObjectFlag t)
```

### Type Changed: AVFoundation.AVAudioFormat

Modified constructors:

```
public protected AVAudioFormat (IntPtr handle)
	public protected AVAudioFormat (Foundation.NSObjectFlag t)
```

### Type Changed: AVFoundation.AVAudioInputNode

Modified constructors:

```
public protected AVAudioInputNode (Foundation.NSObjectFlag t)
	public protected AVAudioInputNode (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioIONode

Modified constructors:

```
public protected AVAudioIONode (Foundation.NSObjectFlag t)
	public protected AVAudioIONode (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioMix

Modified constructors:

```
public protected AVAudioMix (Foundation.NSObjectFlag t)
	public protected AVAudioMix (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioMixerNode

Modified constructors:

```
public protected AVAudioMixerNode (Foundation.NSObjectFlag t)
	public protected AVAudioMixerNode (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioMixInputParameters

Modified constructors:

```
public protected AVAudioMixInputParameters (Foundation.NSObjectFlag t)
	public protected AVAudioMixInputParameters (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioNode

Modified constructors:

```
public protected AVAudioNode (Foundation.NSObjectFlag t)
	public protected AVAudioNode (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioOutputNode

Modified constructors:

```
public protected AVAudioOutputNode (Foundation.NSObjectFlag t)
	public protected AVAudioOutputNode (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioPcmBuffer

Modified constructors:

```
public protected AVAudioPcmBuffer (Foundation.NSObjectFlag t)
	public protected AVAudioPcmBuffer (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioPlayer

Removed constructors:

```
[Obsolete ("This method had an invalid signature in MonoMac 1.0.3, use AVAudioPlayer.FromUrl instead")]
	public AVAudioPlayer (Foundation.NSUrl url, Foundation.NSError error);

	[Obsolete ("This method had an invalid signature in MonoMac 1.0.3, use AVAudioPlayer.FromData instead")]
	public AVAudioPlayer (Foundation.NSData data, Foundation.NSError error);
```

Modified constructors:

```
public protected AVAudioPlayer (Foundation.NSObjectFlag t)
	public protected AVAudioPlayer (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use SoundSettings")]
	public AVAudioPlayerSettings Settings { get; }
```

Modified properties:

```
public AVAudioPlayerDelegate IAVAudioPlayerDelegate Delegate { get; set; }
```

Removed method:

```
[Obsolete ("This method was incorrectly named, use PlayAtTime instead")]
	public bool PlayAtTimetime (double time);
```

### Type Changed: AVFoundation.AVAudioPlayerDelegate

Modified constructors:

```
public protected AVAudioPlayerDelegate (Foundation.NSObjectFlag t)
	public protected AVAudioPlayerDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioPlayerNode

Modified constructors:

```
public protected AVAudioPlayerNode (Foundation.NSObjectFlag t)
	public protected AVAudioPlayerNode (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioRecorder

Removed constructors:

```
[Obsolete ("Use static Create method as this method had an invalid signature up to MonoMac 1.4.4")]
	public AVAudioRecorder (Foundation.NSUrl url, Foundation.NSDictionary settings, Foundation.NSError outError);
```

Modified constructors:

```
public protected AVAudioRecorder (Foundation.NSObjectFlag t)
	public protected AVAudioRecorder (IntPtr handle)
```

Removed property:

```
public AudioSettings AudioSettings { get; }
```

Modified properties:

```
public AVAudioRecorderDelegate IAVAudioRecorderDelegate Delegate { get; set; }
	public virtual Foundation.NSDictionary AudioSettings Settings { get; }
```

Added property:

```
public virtual Foundation.NSDictionary WeakSettings { get; }
```

Removed methods:

```
[Obsolete ("Use Create method")]
	public static AVAudioRecorder ToUrl (Foundation.NSUrl url, Foundation.NSDictionary settings, out Foundation.NSError error);

	[Obsolete ("Use Create method")]
	public static AVAudioRecorder ToUrl (Foundation.NSUrl url, AVAudioRecorderSettings settings, out Foundation.NSError error);
```

### Type Changed: AVFoundation.AVAudioRecorderDelegate

Modified constructors:

```
public protected AVAudioRecorderDelegate (Foundation.NSObjectFlag t)
	public protected AVAudioRecorderDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioSession

Removed constructors:

```
[Obsolete ("Please use the static SharedInstance property as this type is not meant to be created")]
	public AVAudioSession ();
```

Modified constructors:

```
public protected AVAudioSession (Foundation.NSObjectFlag t)
	public protected AVAudioSession (IntPtr handle)
```

Removed properties:

```
public static Foundation.NSString LocationLower { get; }
	public static Foundation.NSString LocationUpper { get; }
	public static Foundation.NSString OrientationBack { get; }
	public static Foundation.NSString OrientationBottom { get; }
	public static Foundation.NSString OrientationFront { get; }
	public static Foundation.NSString OrientationTop { get; }
	public static Foundation.NSString PolarPatternCardioid { get; }
	public static Foundation.NSString PolarPatternOmnidirectional { get; }
	public static Foundation.NSString PolarPatternSubcardioid { get; }
```

Modified properties:

```
public AVAudioSessionDelegate IAVAudioSessionDelegate Delegate { get; set; }
```

Removed methods:

```
[Obsolete ("Use SetActive(bool, out NSError) instead")]
	public bool SetActive (bool beActive, Foundation.NSError outError);

	[Obsolete ("Use SetCategory(bool, out NSError) instead")]
	public bool SetCategory (Foundation.NSString theCategory, Foundation.NSError outError);

	[Obsolete ("Use SetPreferredSampleRate(bool, out NSError) on iOS 6.0 instead")]
	public bool SetPreferredHardwareSampleRate (double sampleRate, Foundation.NSError outError);

	[Obsolete ("Use SetPreferredIOBufferDuration(bool, out NSError) instead")]
	public bool SetPreferredIOBufferDuration (double duration, Foundation.NSError outError);
```

### Type Changed: AVFoundation.AVAudioSessionChannelDescription

Modified constructors:

```
public protected AVAudioSessionChannelDescription (Foundation.NSObjectFlag t)
	public protected AVAudioSessionChannelDescription (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioSessionDataSourceDescription

Modified constructors:

```
public protected AVAudioSessionDataSourceDescription (Foundation.NSObjectFlag t)
	public protected AVAudioSessionDataSourceDescription (IntPtr handle)
```

Modified properties:

```
public virtual string AVAudioDataSourceLocation Location { get; }
	public virtual string AVAudioDataSourceOrientation Orientation { get; }
	public virtual Foundation.NSString AVAudioDataSourcePolarPattern PreferredPolarPattern { get; }
	public virtual Foundation.NSString AVAudioDataSourcePolarPattern SelectedPolarPattern { get; }
	public virtual Foundation.NSString[] AVAudioDataSourcePolarPattern[] SupportedPolarPatterns { get; }
```

Removed method:

```
public virtual bool SetPreferredPolarPattern (Foundation.NSString pattern, out Foundation.NSError outError);
```

Added method:

```
public bool SetPreferredPolarPattern (AVAudioDataSourcePolarPattern pattern, out Foundation.NSError outError);
```

### Type Changed: AVFoundation.AVAudioSessionDelegate

Modified constructors:

```
public protected AVAudioSessionDelegate (Foundation.NSObjectFlag t)
	public protected AVAudioSessionDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioSessionPortDescription

Modified constructors:

```
public protected AVAudioSessionPortDescription (Foundation.NSObjectFlag t)
	public protected AVAudioSessionPortDescription (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioSessionRouteDescription

Modified constructors:

```
public protected AVAudioSessionRouteDescription (Foundation.NSObjectFlag t)
	public protected AVAudioSessionRouteDescription (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioStereoMixing

Modified constructors:

```
public protected AVAudioStereoMixing ()
	public protected AVAudioStereoMixing (Foundation.NSObjectFlag t)
	public protected AVAudioStereoMixing (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioTime

Modified constructors:

```
public protected AVAudioTime (IntPtr handle)
	public protected AVAudioTime (Foundation.NSObjectFlag t)
```

### Type Changed: AVFoundation.AVAudioUnit

Modified constructors:

```
public protected AVAudioUnit (Foundation.NSObjectFlag t)
	public protected AVAudioUnit (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitDelay

Modified constructors:

```
public protected AVAudioUnitDelay (Foundation.NSObjectFlag t)
	public protected AVAudioUnitDelay (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitDistortion

Modified constructors:

```
public protected AVAudioUnitDistortion (Foundation.NSObjectFlag t)
	public protected AVAudioUnitDistortion (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitEffect

Modified constructors:

```
public AVAudioUnitEffect (AudioUnit.AudioComponentDescription desc audioComponentDescription)
	public protected AVAudioUnitEffect (Foundation.NSObjectFlag t)
	public protected AVAudioUnitEffect (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitEQ

Modified constructors:

```
public protected AVAudioUnitEQ (Foundation.NSObjectFlag t)
	public protected AVAudioUnitEQ (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitEQFilterParameters

Modified constructors:

```
public protected AVAudioUnitEQFilterParameters (Foundation.NSObjectFlag t)
	public protected AVAudioUnitEQFilterParameters (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitGenerator

Modified constructors:

```
public AVAudioUnitGenerator (AudioUnit.AudioComponentDescription desc audioComponentDescription)
	public protected AVAudioUnitGenerator (Foundation.NSObjectFlag t)
	public protected AVAudioUnitGenerator (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitMidiInstrument

Modified constructors:

```
public AVAudioUnitMidiInstrument (AudioUnit.AudioComponentDescription desc audioComponentDescription)
	public protected AVAudioUnitMidiInstrument (Foundation.NSObjectFlag t)
	public protected AVAudioUnitMidiInstrument (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitReverb

Modified constructors:

```
public protected AVAudioUnitReverb (Foundation.NSObjectFlag t)
	public protected AVAudioUnitReverb (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitSampler

Modified constructors:

```
public protected AVAudioUnitSampler (Foundation.NSObjectFlag t)
	public protected AVAudioUnitSampler (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitTimeEffect

Modified constructors:

```
public AVAudioUnitTimeEffect (AudioUnit.AudioComponentDescription desc audioComponentDescription)
	public protected AVAudioUnitTimeEffect (Foundation.NSObjectFlag t)
	public protected AVAudioUnitTimeEffect (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitTimePitch

Modified constructors:

```
public AVAudioUnitTimePitch (AudioUnit.AudioComponentDescription desc audioComponentDescription)
	public protected AVAudioUnitTimePitch (Foundation.NSObjectFlag t)
	public protected AVAudioUnitTimePitch (IntPtr handle)
```

### Type Changed: AVFoundation.AVAudioUnitVarispeed

Modified constructors:

```
public AVAudioUnitVarispeed (AudioUnit.AudioComponentDescription desc audioComponentDescription)
	public protected AVAudioUnitVarispeed (Foundation.NSObjectFlag t)
	public protected AVAudioUnitVarispeed (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureAudioChannel

Modified constructors:

```
public protected AVCaptureAudioChannel (Foundation.NSObjectFlag t)
	public protected AVCaptureAudioChannel (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureAudioDataOutput

Modified constructors:

```
public protected AVCaptureAudioDataOutput (Foundation.NSObjectFlag t)
	public protected AVCaptureAudioDataOutput (IntPtr handle)
```

Modified properties:

```
public virtual AVCaptureAudioDataOutputSampleBufferDelegate IAVCaptureAudioDataOutputSampleBufferDelegate SampleBufferDelegate { get; }
```

Removed method:

```
public virtual void SetSampleBufferDelegatequeue (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, CoreFoundation.DispatchQueue sampleBufferCallbackDispatchQueue);
```

Added method:

```
public virtual void SetSampleBufferDelegateQueue (AVCaptureAudioDataOutputSampleBufferDelegate sampleBufferDelegate, CoreFoundation.DispatchQueue sampleBufferCallbackDispatchQueue);
```

### Type Changed: AVFoundation.AVCaptureAudioDataOutputSampleBufferDelegate

Modified constructors:

```
public protected AVCaptureAudioDataOutputSampleBufferDelegate (Foundation.NSObjectFlag t)
	public protected AVCaptureAudioDataOutputSampleBufferDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureAutoExposureBracketedStillImageSettings

Modified constructors:

```
public protected AVCaptureAutoExposureBracketedStillImageSettings (Foundation.NSObjectFlag t)
	public protected AVCaptureAutoExposureBracketedStillImageSettings (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureBracketedStillImageSettings

Modified constructors:

```
public protected AVCaptureBracketedStillImageSettings (Foundation.NSObjectFlag t)
	public protected AVCaptureBracketedStillImageSettings (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureConnection

Modified constructors:

```
public protected AVCaptureConnection (Foundation.NSObjectFlag t)
	public protected AVCaptureConnection (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use InputPorts")]
	public AVCaptureInputPort[] inputPorts { get; }
```

### Type Changed: AVFoundation.AVCaptureDevice

Modified constructors:

```
public protected AVCaptureDevice (Foundation.NSObjectFlag t)
	public protected AVCaptureDevice (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureDeviceFormat

Modified constructors:

```
public protected AVCaptureDeviceFormat (Foundation.NSObjectFlag t)
	public protected AVCaptureDeviceFormat (IntPtr handle)
```

Modified properties:

```
public virtual System.Drawing.Size CoreMedia.CMVideoDimensions HighResolutionStillImageDimensions { get; }
```

### Type Changed: AVFoundation.AVCaptureDeviceInput

Removed constructors:

```
[Obsolete ("Use AVCaptureDeviceInput (AVCaptureDevice, out NSError) instead")]
	public AVCaptureDeviceInput (AVCaptureDevice device, IntPtr handle);
```

Modified constructors:

```
public protected AVCaptureDeviceInput (Foundation.NSObjectFlag t)
	public protected AVCaptureDeviceInput (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use FromDevice (AVCaptureDevice, out NSError) instead")]
	public static AVCaptureDeviceInput FromDevice (AVCaptureDevice device, IntPtr handle);
```

### Type Changed: AVFoundation.AVCaptureFileOutput

Modified constructors:

```
public protected AVCaptureFileOutput (Foundation.NSObjectFlag t)
	public protected AVCaptureFileOutput (IntPtr handle)
```

Removed method:

```
public virtual void StartRecordingToOutputFile (Foundation.NSUrl outputFileUrl, AVCaptureFileOutputRecordingDelegate recordingDelegate);
```

Added method:

```
public virtual void StartRecordingToOutputFile (Foundation.NSUrl outputFileUrl, IAVCaptureFileOutputRecordingDelegate recordingDelegate);
```

### Type Changed: AVFoundation.AVCaptureFileOutputRecordingDelegate

Modified constructors:

```
public protected AVCaptureFileOutputRecordingDelegate ()
	public protected AVCaptureFileOutputRecordingDelegate (Foundation.NSObjectFlag t)
	public protected AVCaptureFileOutputRecordingDelegate (IntPtr handle)
```

Modified methods:

```
public abstract void FinishedRecording (AVCaptureFileOutput captureOutput, Foundation.NSUrl outputFileUrl, Foundation.NSObject[] connections, Foundation.NSError error)
```

### Type Changed: AVFoundation.AVCaptureFileOutputRecordingDelegate_Extensions

Removed method:

```
public static void FinishedRecording (IAVCaptureFileOutputRecordingDelegate This, AVCaptureFileOutput captureOutput, Foundation.NSUrl outputFileUrl, Foundation.NSObject[] connections, Foundation.NSError error);
```

### Type Changed: AVFoundation.AVCaptureFocusMode

Removed values:

```
[Obsolete ("use AutoFocus instead")]
	ModeAutoFocus = 1,

	[Obsolete ("use ContinuousAutoFocus instead")]
	ModeContinuousAutoFocus = 2,

	[Obsolete ("use Locked instead")]
	ModeLocked = 0,
```

### Type Changed: AVFoundation.AVCaptureInput

Modified constructors:

```
public protected AVCaptureInput (Foundation.NSObjectFlag t)
	public protected AVCaptureInput (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureInputPort

Modified constructors:

```
public protected AVCaptureInputPort (Foundation.NSObjectFlag t)
	public protected AVCaptureInputPort (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureManualExposureBracketedStillImageSettings

Modified constructors:

```
public protected AVCaptureManualExposureBracketedStillImageSettings (Foundation.NSObjectFlag t)
	public protected AVCaptureManualExposureBracketedStillImageSettings (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureMetadataOutput

Modified constructors:

```
public protected AVCaptureMetadataOutput (Foundation.NSObjectFlag t)
	public protected AVCaptureMetadataOutput (IntPtr handle)
```

Modified properties:

```
public virtual Foundation.NSString[] AVMetadataObjectType AvailableMetadataObjectTypes { get; }
	public virtual AVCaptureMetadataOutputObjectsDelegate IAVCaptureMetadataOutputObjectsDelegate Delegate { get; }
	public virtual Foundation.NSString[] AVMetadataObjectType MetadataObjectTypes { get; set; }
```

Added properties:

```
public virtual Foundation.NSString[] WeakAvailableMetadataObjectTypes { get; }
	public virtual Foundation.NSString[] WeakMetadataObjectTypes { get; set; }
```

Removed method:

```
public virtual void SetDelegate (AVCaptureMetadataOutputObjectsDelegate objectsDelegate, CoreFoundation.DispatchQueue objectsCallbackQueue);
```

Added method:

```
public virtual void SetDelegate (IAVCaptureMetadataOutputObjectsDelegate objectsDelegate, CoreFoundation.DispatchQueue objectsCallbackQueue);
```

### Type Changed: AVFoundation.AVCaptureMetadataOutputObjectsDelegate

Modified constructors:

```
public protected AVCaptureMetadataOutputObjectsDelegate (Foundation.NSObjectFlag t)
	public protected AVCaptureMetadataOutputObjectsDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureMovieFileOutput

Modified constructors:

```
public protected AVCaptureMovieFileOutput (Foundation.NSObjectFlag t)
	public protected AVCaptureMovieFileOutput (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureOutput

Modified constructors:

```
public protected AVCaptureOutput (Foundation.NSObjectFlag t)
	public protected AVCaptureOutput (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureSession

Modified constructors:

```
public protected AVCaptureSession (Foundation.NSObjectFlag t)
	public protected AVCaptureSession (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureStillImageOutput

Modified constructors:

```
public protected AVCaptureStillImageOutput (Foundation.NSObjectFlag t)
	public protected AVCaptureStillImageOutput (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureVideoDataOutput

Modified constructors:

```
public protected AVCaptureVideoDataOutput (Foundation.NSObjectFlag t)
	public protected AVCaptureVideoDataOutput (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use Compressed or Uncompressed property")]
	public AVVideoSettings VideoSettings { get; set; }
```

Modified properties:

```
public virtual AVCaptureVideoDataOutputSampleBufferDelegate IAVCaptureVideoDataOutputSampleBufferDelegate SampleBufferDelegate { get; }
```

Removed method:

```
[Obsolete ("Use SetSampleBufferDelegate")]
	public void SetSampleBufferDelegateAndQueue (AVCaptureVideoDataOutputSampleBufferDelegate sampleBufferDelegate, CoreFoundation.DispatchQueue queue);
```

### Type Changed: AVFoundation.AVCaptureVideoDataOutputSampleBufferDelegate

Modified constructors:

```
public protected AVCaptureVideoDataOutputSampleBufferDelegate (Foundation.NSObjectFlag t)
	public protected AVCaptureVideoDataOutputSampleBufferDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVCaptureVideoPreviewLayer

Modified constructors:

```
public protected AVCaptureVideoPreviewLayer (Foundation.NSObjectFlag t)
	public protected AVCaptureVideoPreviewLayer (IntPtr handle)
```

Removed property:

```
public AVLayerVideoGravity LayerVideoGravity { get; set; }
```

Modified properties:

```
public string AVLayerVideoGravity VideoGravity { get; set; }
```

### Type Changed: AVFoundation.AVComposition

Modified constructors:

```
public protected AVComposition (Foundation.NSObjectFlag t)
	public protected AVComposition (IntPtr handle)
```

### Type Changed: AVFoundation.AVCompositionTrack

Modified constructors:

```
public protected AVCompositionTrack (Foundation.NSObjectFlag t)
	public protected AVCompositionTrack (IntPtr handle)
```

### Type Changed: AVFoundation.AVCompositionTrackSegment

Modified constructors:

```
public protected AVCompositionTrackSegment (Foundation.NSObjectFlag t)
	public protected AVCompositionTrackSegment (IntPtr handle)
```

### Type Changed: AVFoundation.AVFrameRateRange

Modified constructors:

```
public protected AVFrameRateRange (Foundation.NSObjectFlag t)
	public protected AVFrameRateRange (IntPtr handle)
```

### Type Changed: AVFoundation.AVMediaSelectionGroup

Modified constructors:

```
public protected AVMediaSelectionGroup (Foundation.NSObjectFlag t)
	public protected AVMediaSelectionGroup (IntPtr handle)
```

### Type Changed: AVFoundation.AVMediaSelectionOption

Modified constructors:

```
public protected AVMediaSelectionOption (Foundation.NSObjectFlag t)
	public protected AVMediaSelectionOption (IntPtr handle)
```

### Type Changed: AVFoundation.AVMetadataFaceObject

Modified constructors:

```
public protected AVMetadataFaceObject (Foundation.NSObjectFlag t)
	public protected AVMetadataFaceObject (IntPtr handle)
```

### Type Changed: AVFoundation.AVMetadataItem

Modified constructors:

```
public protected AVMetadataItem (Foundation.NSObjectFlag t)
	public protected AVMetadataItem (IntPtr handle)
```

Removed method:

```
public virtual void LoadValuesAsynchronously (string[] keys, Foundation.NSAction handler);
```

Added method:

```
public virtual void LoadValuesAsynchronously (string[] keys, System.Action handler);
```

### Type Changed: AVFoundation.AVMetadataItemFilter

Removed constructors:

```
[Obsolete ("Please use the static ForSharing factory method as this type is not meant to be created directly")]
	public AVMetadataItemFilter ();
```

Modified constructors:

```
public protected AVMetadataItemFilter (Foundation.NSObjectFlag t)
	public protected AVMetadataItemFilter (IntPtr handle)
```

### Type Changed: AVFoundation.AVMetadataMachineReadableCodeObject

Modified constructors:

```
public protected AVMetadataMachineReadableCodeObject (Foundation.NSObjectFlag t)
	public protected AVMetadataMachineReadableCodeObject (IntPtr handle)
```

Modified properties:

```
public virtual Foundation.NSDictionary[] System.Drawing.PointF[] Corners { get; }
```

Added property:

```
public virtual Foundation.NSDictionary[] WeakCorners { get; }
```

### Type Changed: AVFoundation.AVMetadataObject

Modified constructors:

```
public protected AVMetadataObject (Foundation.NSObjectFlag t)
	public protected AVMetadataObject (IntPtr handle)
```

Modified properties:

```
public virtual Foundation.NSString AVMetadataObjectType Type { get; }
```

Added property:

```
public virtual Foundation.NSString WeakType { get; }
```

### Type Changed: AVFoundation.AVMidiPlayer

Modified constructors:

```
public protected AVMidiPlayer (Foundation.NSObjectFlag t)
	public protected AVMidiPlayer (IntPtr handle)
```

### Type Changed: AVFoundation.AVMutableAudioMix

Modified constructors:

```
public protected AVMutableAudioMix (Foundation.NSObjectFlag t)
	public protected AVMutableAudioMix (IntPtr handle)
```

### Type Changed: AVFoundation.AVMutableAudioMixInputParameters

Modified constructors:

```
public protected AVMutableAudioMixInputParameters (Foundation.NSObjectFlag t)
	public protected AVMutableAudioMixInputParameters (IntPtr handle)
```

### Type Changed: AVFoundation.AVMutableComposition

Modified constructors:

```
public protected AVMutableComposition (Foundation.NSObjectFlag t)
	public protected AVMutableComposition (IntPtr handle)
```

### Type Changed: AVFoundation.AVMutableCompositionTrack

Modified constructors:

```
public protected AVMutableCompositionTrack (Foundation.NSObjectFlag t)
	public protected AVMutableCompositionTrack (IntPtr handle)
```

### Type Changed: AVFoundation.AVMutableMetadataItem

Modified constructors:

```
public protected AVMutableMetadataItem (Foundation.NSObjectFlag t)
	public protected AVMutableMetadataItem (IntPtr handle)
```

### Type Changed: AVFoundation.AVMutableTimedMetadataGroup

Modified constructors:

```
public protected AVMutableTimedMetadataGroup (Foundation.NSObjectFlag t)
	public protected AVMutableTimedMetadataGroup (IntPtr handle)
```

### Type Changed: AVFoundation.AVMutableVideoComposition

Modified constructors:

```
public protected AVMutableVideoComposition (Foundation.NSObjectFlag t)
	public protected AVMutableVideoComposition (IntPtr handle)
```

### Type Changed: AVFoundation.AVMutableVideoCompositionInstruction

Modified constructors:

```
public protected AVMutableVideoCompositionInstruction (Foundation.NSObjectFlag t)
	public protected AVMutableVideoCompositionInstruction (IntPtr handle)
```

### Type Changed: AVFoundation.AVMutableVideoCompositionLayerInstruction

Modified constructors:

```
public protected AVMutableVideoCompositionLayerInstruction (Foundation.NSObjectFlag t)
	public protected AVMutableVideoCompositionLayerInstruction (IntPtr handle)
```

### Type Changed: AVFoundation.AVOutputSettingsAssistant

Modified constructors:

```
public protected AVOutputSettingsAssistant (Foundation.NSObjectFlag t)
	public protected AVOutputSettingsAssistant (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayer

Modified constructors:

```
public protected AVPlayer (Foundation.NSObjectFlag t)
	public protected AVPlayer (IntPtr handle)
```

Removed methods:

```
public virtual Foundation.NSObject AddBoundaryTimeObserver (Foundation.NSValue[] times, CoreFoundation.DispatchQueue queue, Foundation.NSAction handler);
	public virtual Foundation.NSObject AddPeriodicTimeObserver (CoreMedia.CMTime interval, CoreFoundation.DispatchQueue queue, AVTimeHandler handler);

	[Obsolete ("Use Seek(CMTime, CMTime, CMTIme, AVCompletion) instead, the callback contains a `bool finished' parameter")]
	public void Seek (CoreMedia.CMTime time, CoreMedia.CMTime toleranceBefore, CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);

	[Obsolete ("Use Seek(CMTime, AVCompletion) instead, the callback contains a `bool finished' parameter")]
	public void Seek (CoreMedia.CMTime time, AVCompletionHandler completion);
```

Added methods:

```
public virtual Foundation.NSObject AddBoundaryTimeObserver (Foundation.NSValue[] times, CoreFoundation.DispatchQueue queue, System.Action handler);
	public virtual Foundation.NSObject AddPeriodicTimeObserver (CoreMedia.CMTime interval, CoreFoundation.DispatchQueue queue, System.Action<CoreMedia.CMTime> handler);
```

### Type Changed: AVFoundation.AVPlayerItem

Modified constructors:

```
public protected AVPlayerItem (Foundation.NSObjectFlag t)
	public protected AVPlayerItem (IntPtr handle)
```

Modified properties:

```
public virtual AVVideoCompositing IAVVideoCompositing CustomVideoCompositor { get; }
```

Removed method:

```
[Obsolete ("Use Seek(CMTime, CMTime, CMTIme, AVCompletion) instead, the callback contains a `bool finished' parameter")]
	public void Seek (CoreMedia.CMTime time, CoreMedia.CMTime toleranceBefore, CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
```

### Type Changed: AVFoundation.AVPlayerItemAccessLog

Modified constructors:

```
public protected AVPlayerItemAccessLog (Foundation.NSObjectFlag t)
	public protected AVPlayerItemAccessLog (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayerItemAccessLogEvent

Modified constructors:

```
public protected AVPlayerItemAccessLogEvent (Foundation.NSObjectFlag t)
	public protected AVPlayerItemAccessLogEvent (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayerItemErrorLog

Modified constructors:

```
public protected AVPlayerItemErrorLog (Foundation.NSObjectFlag t)
	public protected AVPlayerItemErrorLog (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayerItemErrorLogEvent

Modified constructors:

```
public protected AVPlayerItemErrorLogEvent (Foundation.NSObjectFlag t)
	public protected AVPlayerItemErrorLogEvent (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayerItemLegibleOutput

Modified constructors:

```
public protected AVPlayerItemLegibleOutput (Foundation.NSObjectFlag t)
	public protected AVPlayerItemLegibleOutput (IntPtr handle)
```

Modified properties:

```
public virtual AVPlayerItemLegibleOutputPushDelegate IAVPlayerItemLegibleOutputPushDelegate Delegate { get; }
```

Removed method:

```
public virtual void SetDelegate (AVPlayerItemLegibleOutputPushDelegate delegateObject, CoreFoundation.DispatchQueue delegateQueue);
```

Added method:

```
public virtual void SetDelegate (IAVPlayerItemLegibleOutputPushDelegate delegateObject, CoreFoundation.DispatchQueue delegateQueue);
```

### Type Changed: AVFoundation.AVPlayerItemLegibleOutputPushDelegate

Modified constructors:

```
public protected AVPlayerItemLegibleOutputPushDelegate (Foundation.NSObjectFlag t)
	public protected AVPlayerItemLegibleOutputPushDelegate (IntPtr handle)
```

Removed method:

```
public override void OutputSequenceWasFlushed (AVPlayerItemOutput output);
```

### Type Changed: AVFoundation.AVPlayerItemMetadataOutput

Modified constructors:

```
public protected AVPlayerItemMetadataOutput (Foundation.NSObjectFlag t)
	public protected AVPlayerItemMetadataOutput (IntPtr handle)
```

Modified properties:

```
public AVPlayerItemMetadataOutputPushDelegate IAVPlayerItemMetadataOutputPushDelegate Delegate { get; }
```

Removed method:

```
public virtual void SetDelegate (AVPlayerItemMetadataOutputPushDelegate pushDelegate, CoreFoundation.DispatchQueue delegateQueue);
```

Added method:

```
public virtual void SetDelegate (IAVPlayerItemMetadataOutputPushDelegate pushDelegate, CoreFoundation.DispatchQueue delegateQueue);
```

### Type Changed: AVFoundation.AVPlayerItemMetadataOutputPushDelegate

Modified constructors:

```
public protected AVPlayerItemMetadataOutputPushDelegate (Foundation.NSObjectFlag t)
	public protected AVPlayerItemMetadataOutputPushDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayerItemOutput

Modified constructors:

```
public protected AVPlayerItemOutput (Foundation.NSObjectFlag t)
	public protected AVPlayerItemOutput (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayerItemOutputPullDelegate

Modified constructors:

```
public protected AVPlayerItemOutputPullDelegate (Foundation.NSObjectFlag t)
	public protected AVPlayerItemOutputPullDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayerItemOutputPushDelegate

Modified constructors:

```
public protected AVPlayerItemOutputPushDelegate (Foundation.NSObjectFlag t)
	public protected AVPlayerItemOutputPushDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayerItemTrack

Modified constructors:

```
public protected AVPlayerItemTrack (Foundation.NSObjectFlag t)
	public protected AVPlayerItemTrack (IntPtr handle)
```

### Type Changed: AVFoundation.AVPlayerItemVideoOutput

Modified constructors:

```
public protected AVPlayerItemVideoOutput (Foundation.NSObjectFlag t)
	public protected AVPlayerItemVideoOutput (IntPtr handle)
```

Modified properties:

```
public AVPlayerItemOutputPullDelegate IAVPlayerItemOutputPullDelegate Delegate { get; }
```

Removed method:

```
public virtual void SetDelegate (AVPlayerItemOutputPullDelegate delegateClass, CoreFoundation.DispatchQueue delegateQueue);
```

Added method:

```
public virtual void SetDelegate (IAVPlayerItemOutputPullDelegate delegateClass, CoreFoundation.DispatchQueue delegateQueue);
```

### Type Changed: AVFoundation.AVPlayerLayer

Modified constructors:

```
public protected AVPlayerLayer (Foundation.NSObjectFlag t)
	public protected AVPlayerLayer (IntPtr handle)
```

Removed property:

```
public AVLayerVideoGravity LayerVideoGravity { get; set; }
```

Modified properties:

```
public string AVLayerVideoGravity VideoGravity { get; set; }
```

### Type Changed: AVFoundation.AVPlayerMediaSelectionCriteria

Modified constructors:

```
public protected AVPlayerMediaSelectionCriteria (Foundation.NSObjectFlag t)
	public protected AVPlayerMediaSelectionCriteria (IntPtr handle)
```

### Type Changed: AVFoundation.AVQueuePlayer

Modified constructors:

```
public protected AVQueuePlayer (Foundation.NSObjectFlag t)
	public protected AVQueuePlayer (IntPtr handle)
```

### Type Changed: AVFoundation.AVSampleBufferDisplayLayer

Modified constructors:

```
public protected AVSampleBufferDisplayLayer (Foundation.NSObjectFlag t)
	public protected AVSampleBufferDisplayLayer (IntPtr handle)
```

### Type Changed: AVFoundation.AVSpeechSynthesisVoice

Modified constructors:

```
public protected AVSpeechSynthesisVoice (Foundation.NSObjectFlag t)
	public protected AVSpeechSynthesisVoice (IntPtr handle)
```

### Type Changed: AVFoundation.AVSpeechSynthesizer

Modified constructors:

```
public protected AVSpeechSynthesizer (Foundation.NSObjectFlag t)
	public protected AVSpeechSynthesizer (IntPtr handle)
```

Modified properties:

```
public AVSpeechSynthesizerDelegate IAVSpeechSynthesizerDelegate Delegate { get; set; }
```

### Type Changed: AVFoundation.AVSpeechSynthesizerDelegate

Modified constructors:

```
public protected AVSpeechSynthesizerDelegate (Foundation.NSObjectFlag t)
	public protected AVSpeechSynthesizerDelegate (IntPtr handle)
```

### Type Changed: AVFoundation.AVSpeechUtterance

Modified constructors:

```
public protected AVSpeechUtterance (Foundation.NSObjectFlag t)
	public protected AVSpeechUtterance (IntPtr handle)
```

### Type Changed: AVFoundation.AVSynchronizedLayer

Modified constructors:

```
public protected AVSynchronizedLayer (Foundation.NSObjectFlag t)
	public protected AVSynchronizedLayer (IntPtr handle)
```

### Type Changed: AVFoundation.AVTextStyleRule

Modified constructors:

```
public protected AVTextStyleRule (IntPtr handle)
	public protected AVTextStyleRule (Foundation.NSObjectFlag t)
```

### Type Changed: AVFoundation.AVTimedMetadataGroup

Modified constructors:

```
public protected AVTimedMetadataGroup (Foundation.NSObjectFlag t)
	public protected AVTimedMetadataGroup (IntPtr handle)
```

### Type Changed: AVFoundation.AVUrlAsset

Modified constructors:

```
public protected AVUrlAsset (Foundation.NSObjectFlag t)
	public protected AVUrlAsset (IntPtr handle)
```

Removed method:

```
public static AVUrlAsset FromUrl (Foundation.NSUrl url, Foundation.NSDictionary options);
```

### Type Changed: AVFoundation.AVVideoCompositing

Modified constructors:

```
public protected AVVideoCompositing ()
	public protected AVVideoCompositing (Foundation.NSObjectFlag t)
	public protected AVVideoCompositing (IntPtr handle)
```

### Type Changed: AVFoundation.AVVideoComposition

Modified constructors:

```
public protected AVVideoComposition (Foundation.NSObjectFlag t)
	public protected AVVideoComposition (IntPtr handle)
```

Removed method:

```
public virtual bool IsValidForAsset (AVAsset asset, CoreMedia.CMTimeRange timeRange, AVVideoCompositionValidationHandling validationDelegate);
```

Added method:

```
public virtual bool IsValidForAsset (AVAsset asset, CoreMedia.CMTimeRange timeRange, IAVVideoCompositionValidationHandling validationDelegate);
```

### Type Changed: AVFoundation.AVVideoCompositionCoreAnimationTool

Modified constructors:

```
public protected AVVideoCompositionCoreAnimationTool (Foundation.NSObjectFlag t)
	public protected AVVideoCompositionCoreAnimationTool (IntPtr handle)
```

### Type Changed: AVFoundation.AVVideoCompositionInstruction

Modified constructors:

```
public protected AVVideoCompositionInstruction (Foundation.NSObjectFlag t)
	public protected AVVideoCompositionInstruction (IntPtr handle)
```

### Type Changed: AVFoundation.AVVideoCompositionLayerInstruction

Modified constructors:

```
public protected AVVideoCompositionLayerInstruction (Foundation.NSObjectFlag t)
	public protected AVVideoCompositionLayerInstruction (IntPtr handle)
```

### Type Changed: AVFoundation.AVVideoCompositionRenderContext

Modified constructors:

```
public protected AVVideoCompositionRenderContext (Foundation.NSObjectFlag t)
	public protected AVVideoCompositionRenderContext (IntPtr handle)
```

### Type Changed: AVFoundation.AVVideoCompositionValidationHandling

Modified constructors:

```
public protected AVVideoCompositionValidationHandling (Foundation.NSObjectFlag t)
	public protected AVVideoCompositionValidationHandling (IntPtr handle)
```

### Type Changed: AVFoundation.AVVideoSettingsCompressed

Modified properties:

```
public int? float? AverageNonDroppableFrameRate { get; set; }
	public int? float? ExpectedSourceFrameRate { get; set; }
```

### Type Changed: AVFoundation.IAVAsynchronousKeyValueLoading

Removed method:

```
public virtual void LoadValuesAsynchronously (string[] keys, Foundation.NSAction handler);
```

Added method:

```
public virtual void LoadValuesAsynchronously (string[] keys, System.Action handler);
```

### Type Changed: AVFoundation.IAVCaptureFileOutputRecordingDelegate

Added method:

```
public virtual void FinishedRecording (AVCaptureFileOutput captureOutput, Foundation.NSUrl outputFileUrl, Foundation.NSObject[] connections, Foundation.NSError error);
```

### Removed Type AVFoundation.AVAsynchronousKeyValueLoading_Extensions ### Removed Type AVFoundation.AVAudio3DMixing_Extensions ### Removed Type AVFoundation.AVAudioMixing_Extensions ### Removed Type AVFoundation.AVAudioPlayerSettings ### Removed Type AVFoundation.AVAudioRecorderSettings ### Removed Type AVFoundation.AVAudioStereoMixing_Extensions ### Removed Type AVFoundation.AVCompletionHandler ### Removed Type AVFoundation.AVTimeHandler ### Removed Type AVFoundation.AVVideoSettings ### New Type AVFoundation.AVAudioDataSourceLocation

```
[Serializable]
public enum AVAudioDataSourceLocation {
	Lower = 2,
	Unknown = 0,
	Upper = 1,
}
```

### New Type AVFoundation.AVAudioDataSourceOrientation

```
[Serializable]
public enum AVAudioDataSourceOrientation {
	Back = 4,
	Bottom = 2,
	Front = 3,
	Left = 5,
	Right = 6,
	Top = 1,
	Unknown = 0,
}
```

### New Type AVFoundation.AVAudioDataSourcePolarPattern

```
[Serializable]
public enum AVAudioDataSourcePolarPattern {
	Cardioid = 2,
	Omnidirectional = 1,
	Subcardioid = 3,
	Unknown = 0,
}
```





## Namespace AVKit



### Type Changed: AVKit.AVPlayerViewController

Modified constructors:

```
public protected AVPlayerViewController (Foundation.NSObjectFlag t)
	public protected AVPlayerViewController (IntPtr handle)
```

## Namespace CloudKit



### Type Changed: CloudKit.CKAsset

Modified constructors:

```
public protected CKAsset (Foundation.NSObjectFlag t)
	public protected CKAsset (IntPtr handle)
```

### Type Changed: CloudKit.CKContainer

Modified constructors:

```
public protected CKContainer (Foundation.NSObjectFlag t)
	public protected CKContainer (IntPtr handle)
```

### Type Changed: CloudKit.CKDatabase

Modified constructors:

```
public protected CKDatabase (Foundation.NSObjectFlag t)
	public protected CKDatabase (IntPtr handle)
```

### Type Changed: CloudKit.CKDatabaseOperation

Modified constructors:

```
public protected CKDatabaseOperation (Foundation.NSObjectFlag t)
	public protected CKDatabaseOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKDiscoverAllContactsOperation

Modified constructors:

```
public protected CKDiscoverAllContactsOperation (Foundation.NSObjectFlag t)
	public protected CKDiscoverAllContactsOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKDiscoveredUserInfo

Modified constructors:

```
public protected CKDiscoveredUserInfo (Foundation.NSObjectFlag t)
	public protected CKDiscoveredUserInfo (IntPtr handle)
```

### Type Changed: CloudKit.CKDiscoverUserInfosOperation

Modified constructors:

```
public protected CKDiscoverUserInfosOperation (Foundation.NSObjectFlag t)
	public protected CKDiscoverUserInfosOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKFetchNotificationChangesOperation

Modified constructors:

```
public protected CKFetchNotificationChangesOperation (Foundation.NSObjectFlag t)
	public protected CKFetchNotificationChangesOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKFetchRecordChangesOperation

Modified constructors:

```
public protected CKFetchRecordChangesOperation (Foundation.NSObjectFlag t)
	public protected CKFetchRecordChangesOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKFetchRecordsOperation

Modified constructors:

```
public protected CKFetchRecordsOperation (Foundation.NSObjectFlag t)
	public protected CKFetchRecordsOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKFetchRecordZonesOperation

Modified constructors:

```
public protected CKFetchRecordZonesOperation (Foundation.NSObjectFlag t)
	public protected CKFetchRecordZonesOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKFetchSubscriptionsOperation

Modified constructors:

```
public protected CKFetchSubscriptionsOperation (Foundation.NSObjectFlag t)
	public protected CKFetchSubscriptionsOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKLocationSortDescriptor

Modified constructors:

```
public protected CKLocationSortDescriptor (Foundation.NSObjectFlag t)
	public protected CKLocationSortDescriptor (IntPtr handle)
```

### Type Changed: CloudKit.CKMarkNotificationsReadOperation

Modified constructors:

```
public protected CKMarkNotificationsReadOperation (Foundation.NSObjectFlag t)
	public protected CKMarkNotificationsReadOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKModifyBadgeOperation

Modified constructors:

```
public protected CKModifyBadgeOperation (Foundation.NSObjectFlag t)
	public protected CKModifyBadgeOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKModifyRecordsOperation

Modified constructors:

```
public protected CKModifyRecordsOperation (Foundation.NSObjectFlag t)
	public protected CKModifyRecordsOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKModifyRecordZonesOperation

Modified constructors:

```
public protected CKModifyRecordZonesOperation (Foundation.NSObjectFlag t)
	public protected CKModifyRecordZonesOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKModifySubscriptionsOperation

Modified constructors:

```
public protected CKModifySubscriptionsOperation (Foundation.NSObjectFlag t)
	public protected CKModifySubscriptionsOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKNotification

Modified constructors:

```
public protected CKNotification (Foundation.NSObjectFlag t)
	public protected CKNotification (IntPtr handle)
```

### Type Changed: CloudKit.CKNotificationID

Modified constructors:

```
public protected CKNotificationID (Foundation.NSObjectFlag t)
	public protected CKNotificationID (IntPtr handle)
```

### Type Changed: CloudKit.CKNotificationInfo

Modified constructors:

```
public protected CKNotificationInfo (Foundation.NSObjectFlag t)
	public protected CKNotificationInfo (IntPtr handle)
```

### Type Changed: CloudKit.CKOperation

Modified constructors:

```
public protected CKOperation (Foundation.NSObjectFlag t)
	public protected CKOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKQuery

Modified constructors:

```
public protected CKQuery (Foundation.NSObjectFlag t)
	public protected CKQuery (IntPtr handle)
```

### Type Changed: CloudKit.CKQueryCursor

Modified constructors:

```
public protected CKQueryCursor (Foundation.NSObjectFlag t)
	public protected CKQueryCursor (IntPtr handle)
```

### Type Changed: CloudKit.CKQueryNotification

Modified constructors:

```
public protected CKQueryNotification (Foundation.NSObjectFlag t)
	public protected CKQueryNotification (IntPtr handle)
```

### Type Changed: CloudKit.CKQueryOperation

Modified constructors:

```
public protected CKQueryOperation (Foundation.NSObjectFlag t)
	public protected CKQueryOperation (IntPtr handle)
```

### Type Changed: CloudKit.CKRecord

Modified constructors:

```
public protected CKRecord (Foundation.NSObjectFlag t)
	public protected CKRecord (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use Id instead")]
	public virtual CKRecordID RecordId { get; }
```

Modified properties:

```
public virtual CKRecordID Id { get; }
```

### Type Changed: CloudKit.CKRecordID

Modified constructors:

```
public protected CKRecordID (Foundation.NSObjectFlag t)
	public protected CKRecordID (IntPtr handle)
```

### Type Changed: CloudKit.CKRecordValue

Modified constructors:

```
public protected CKRecordValue (Foundation.NSObjectFlag t)
	public protected CKRecordValue (IntPtr handle)
```

### Type Changed: CloudKit.CKRecordZone

Modified constructors:

```
public protected CKRecordZone (Foundation.NSObjectFlag t)
	public protected CKRecordZone (IntPtr handle)
```

### Type Changed: CloudKit.CKRecordZoneID

Modified constructors:

```
public protected CKRecordZoneID (Foundation.NSObjectFlag t)
	public protected CKRecordZoneID (IntPtr handle)
```

### Type Changed: CloudKit.CKRecordZoneNotification

Modified constructors:

```
public protected CKRecordZoneNotification (Foundation.NSObjectFlag t)
	public protected CKRecordZoneNotification (IntPtr handle)
```

### Type Changed: CloudKit.CKReference

Modified constructors:

```
public protected CKReference (Foundation.NSObjectFlag t)
	public protected CKReference (IntPtr handle)
```

### Type Changed: CloudKit.CKServerChangeToken

Modified constructors:

```
public protected CKServerChangeToken (Foundation.NSObjectFlag t)
	public protected CKServerChangeToken (IntPtr handle)
```

### Type Changed: CloudKit.CKSubscription

Modified constructors:

```
public protected CKSubscription (Foundation.NSObjectFlag t)
	public protected CKSubscription (IntPtr handle)
```

### Removed Type CloudKit.CKRecordValue_Extensions 

## Namespace CoreAnimation



### Type Changed: CoreAnimation.CAAction

Modified constructors:

```
public protected CAAction (Foundation.NSObjectFlag t)
	public protected CAAction (IntPtr handle)
```

Modified methods:

```
public abstract void RunAction (string eventKey, Foundation.NSObject obj, Foundation.NSDictionary arguments)
```

### Type Changed: CoreAnimation.CAAnimation

Modified constructors:

```
public protected CAAnimation (Foundation.NSObjectFlag t)
	public protected CAAnimation (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use BeginTime instead")]
	public double CFTimeInterval { get; set; }
```

### Type Changed: CoreAnimation.CAAnimationDelegate

Modified constructors:

```
public protected CAAnimationDelegate (Foundation.NSObjectFlag t)
	public protected CAAnimationDelegate (IntPtr handle)
```

### Type Changed: CoreAnimation.CAAnimationGroup

Modified constructors:

```
public protected CAAnimationGroup (Foundation.NSObjectFlag t)
	public protected CAAnimationGroup (IntPtr handle)
```

### Type Changed: CoreAnimation.CABasicAnimation

Modified constructors:

```
public protected CABasicAnimation (Foundation.NSObjectFlag t)
	public protected CABasicAnimation (IntPtr handle)
```

### Type Changed: CoreAnimation.CADisplayLink

Modified constructors:

```
public protected CADisplayLink (Foundation.NSObjectFlag t)
	public protected CADisplayLink (IntPtr handle)
```

Removed method:

```
public static CADisplayLink Create (Foundation.NSAction action);
```

Added method:

```
public static CADisplayLink Create (System.Action action);
```

### Type Changed: CoreAnimation.CAEAGLLayer

Modified constructors:

```
public protected CAEAGLLayer (Foundation.NSObjectFlag t)
	public protected CAEAGLLayer (IntPtr handle)
```

### Type Changed: CoreAnimation.CAEmitterBehavior

Modified constructors:

```
public protected CAEmitterBehavior (Foundation.NSObjectFlag t)
	public protected CAEmitterBehavior (IntPtr handle)
```

### Type Changed: CoreAnimation.CAEmitterCell

Modified constructors:

```
public protected CAEmitterCell (Foundation.NSObjectFlag t)
	public protected CAEmitterCell (IntPtr handle)
```

### Type Changed: CoreAnimation.CAEmitterLayer

Modified constructors:

```
public protected CAEmitterLayer (Foundation.NSObjectFlag t)
	public protected CAEmitterLayer (IntPtr handle)
```

### Type Changed: CoreAnimation.CAFillMode

Removed constructor:

```
public CAFillMode ();
```

Removed property:

```
public static Foundation.NSString Frozen { get; }
```

### Type Changed: CoreAnimation.CAGradientLayer

Modified constructors:

```
public protected CAGradientLayer (Foundation.NSObjectFlag t)
	public protected CAGradientLayer (IntPtr handle)
```

### Type Changed: CoreAnimation.CAKeyFrameAnimation

Modified constructors:

```
public protected CAKeyFrameAnimation (Foundation.NSObjectFlag t)
	public protected CAKeyFrameAnimation (IntPtr handle)
```

Removed properties:

```
public static Foundation.NSString CalculationDiscrete { get; }
	public static Foundation.NSString CalculationLinear { get; }
	public static Foundation.NSString CalculationPaced { get; }
```

Removed method:

```
[Obsolete ("This method in the future will return a CAKeyFrameAnimation, update your source, or use GetFromKeyPath to avoid this warning for now")]
	public static CAPropertyAnimation FromKeyPath (string path);
```

Added method:

```
public static CAKeyFrameAnimation FromKeyPath (string path);
```

### Type Changed: CoreAnimation.CALayer

Modified constructors:

```
public protected CALayer (Foundation.NSObjectFlag t)
	public protected CALayer (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use BeginTime instead")]
	public double CFTimeInterval { get; set; }
```

Modified properties:

```
public CALayerDelegate ICALayerDelegate Delegate { get; set; }
```

Removed method:

```
[Obsolete ("Use ConvertRectFromLayer instead")]
	public System.Drawing.RectangleF ConvertRectfromLayer (System.Drawing.RectangleF rect, CALayer layer);
```

### Type Changed: CoreAnimation.CALayerDelegate

Modified constructors:

```
public protected CALayerDelegate (Foundation.NSObjectFlag t)
	public protected CALayerDelegate (IntPtr handle)
```

### Type Changed: CoreAnimation.CAMediaTiming

Modified constructors:

```
public protected CAMediaTiming ()
	public protected CAMediaTiming (Foundation.NSObjectFlag t)
	public protected CAMediaTiming (IntPtr handle)
```

Modified properties:

```
public abstract bool AutoReverses { get; set; }
	public abstract double BeginTime { get; set; }
	public abstract double Duration { get; set; }
	public abstract string FillMode { get; set; }
	public abstract float RepeatCount { get; set; }
	public abstract double RepeatDuration { get; set; }
	public abstract float Speed { get; set; }
	public abstract double TimeOffset { get; set; }
```

### Type Changed: CoreAnimation.CAMediaTimingFunction

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CAMediaTimingFunction ();
```

Modified constructors:

```
public protected CAMediaTimingFunction (Foundation.NSObjectFlag t)
	public protected CAMediaTimingFunction (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use FromName(NSString) with one of the CAMediaTimingFunction fields")]
	public static CAMediaTimingFunction FromName (string name);
```

### Type Changed: CoreAnimation.CAMetalLayer

Modified constructors:

```
public protected CAMetalLayer (Foundation.NSObjectFlag t)
	public protected CAMetalLayer (IntPtr handle)
```

### Type Changed: CoreAnimation.CAPropertyAnimation

Modified constructors:

```
public protected CAPropertyAnimation (Foundation.NSObjectFlag t)
	public protected CAPropertyAnimation (IntPtr handle)
```

### Type Changed: CoreAnimation.CAReplicatorLayer

Modified constructors:

```
public protected CAReplicatorLayer (Foundation.NSObjectFlag t)
	public protected CAReplicatorLayer (IntPtr handle)
```

### Type Changed: CoreAnimation.CAScrollLayer

Modified constructors:

```
public protected CAScrollLayer (Foundation.NSObjectFlag t)
	public protected CAScrollLayer (IntPtr handle)
```

### Type Changed: CoreAnimation.CAShapeLayer

Modified constructors:

```
public protected CAShapeLayer (Foundation.NSObjectFlag t)
	public protected CAShapeLayer (IntPtr handle)
```

### Type Changed: CoreAnimation.CATextLayer

Modified constructors:

```
public protected CATextLayer (Foundation.NSObjectFlag t)
	public protected CATextLayer (IntPtr handle)
```

Modified properties:

```
public virtual Foundation.NSAttributedString AttributedString { get; set; }
```

### Type Changed: CoreAnimation.CATiledLayer

Modified constructors:

```
public protected CATiledLayer (Foundation.NSObjectFlag t)
	public protected CATiledLayer (IntPtr handle)
```

### Type Changed: CoreAnimation.CATransaction

Modified constructors:

```
public protected CATransaction (Foundation.NSObjectFlag t)
	public protected CATransaction (IntPtr handle)
```

Modified properties:

```
public Foundation.NSAction System.Action CompletionBlock { get; set; }
```

### Type Changed: CoreAnimation.CATransformLayer

Modified constructors:

```
public protected CATransformLayer (Foundation.NSObjectFlag t)
	public protected CATransformLayer (IntPtr handle)
```

### Type Changed: CoreAnimation.CATransition

Modified constructors:

```
public protected CATransition (Foundation.NSObjectFlag t)
	public protected CATransition (IntPtr handle)
```

Removed property:

```
[Obsolete ("The name has been fixed, use Filter instead")]
	public Foundation.NSObject filter { get; set; }
```

### Type Changed: CoreAnimation.CAValueFunction

Modified constructors:

```
public protected CAValueFunction (Foundation.NSObjectFlag t)
	public protected CAValueFunction (IntPtr handle)
```

### Type Changed: CoreAnimation.ICAAction

Added method:

```
public virtual void RunAction (string eventKey, Foundation.NSObject obj, Foundation.NSDictionary arguments);
```

### Type Changed: CoreAnimation.ICAMediaTiming

Added properties:

```
public virtual bool AutoReverses { get; set; }
	public virtual double BeginTime { get; set; }
	public virtual double Duration { get; set; }
	public virtual string FillMode { get; set; }
	public virtual float RepeatCount { get; set; }
	public virtual double RepeatDuration { get; set; }
	public virtual float Speed { get; set; }
	public virtual double TimeOffset { get; set; }
```

### Removed Type CoreAnimation.CAAction_Extensions ### Removed Type CoreAnimation.CABarBeatTime ### Removed Type CoreAnimation.CAMediaTiming_Extensions ### Removed Type CoreAnimation.CAMetalDrawable_Extensions 



## Namespace CoreAudioKit



### Type Changed: CoreAudioKit.CABTMidiCentralViewController

Modified constructors:

```
public protected CABTMidiCentralViewController (Foundation.NSObjectFlag t)
	public protected CABTMidiCentralViewController (IntPtr handle)
```

### Type Changed: CoreAudioKit.CABTMidiLocalPeripheralViewController

Modified constructors:

```
public protected CABTMidiLocalPeripheralViewController (Foundation.NSObjectFlag t)
	public protected CABTMidiLocalPeripheralViewController (IntPtr handle)
```

### Type Changed: CoreAudioKit.CAInterAppAudioSwitcherView

Modified constructors:

```
public protected CAInterAppAudioSwitcherView (Foundation.NSObjectFlag t)
	public protected CAInterAppAudioSwitcherView (IntPtr handle)
```

### Type Changed: CoreAudioKit.CAInterAppAudioTransportView

Modified constructors:

```
public protected CAInterAppAudioTransportView (Foundation.NSObjectFlag t)
	public protected CAInterAppAudioTransportView (IntPtr handle)
```

## Namespace CoreBluetooth



### Type Changed: CoreBluetooth.CBATTRequest

Removed constructors:

```
[Obsolete ("This type is not meant to be created by user code.")]
	public CBATTRequest ();
```

Modified constructors:

```
public protected CBATTRequest (Foundation.NSObjectFlag t)
	public protected CBATTRequest (IntPtr handle)
```

### Type Changed: CoreBluetooth.CBAttribute

Modified constructors:

```
public protected CBAttribute (Foundation.NSObjectFlag t)
	public protected CBAttribute (IntPtr handle)
```

### Type Changed: CoreBluetooth.CBCentral

Removed constructors:

```
[Obsolete ("This type is not meant to be created by user code.")]
	public CBCentral ();
```

Modified constructors:

```
public protected CBCentral (Foundation.NSObjectFlag t)
	public protected CBCentral (IntPtr handle)
```

Removed property:

```
public virtual IntPtr UUID { get; }
```

### Type Changed: CoreBluetooth.CBCentralManager

Removed constructors:

```
public CBCentralManager (CBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue, Foundation.NSDictionary options);
	public CBCentralManager (CBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue);
	public CBCentralManager (CBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue, CBCentralInitOptions options);
```

Modified constructors:

```
public protected CBCentralManager (IntPtr handle)
	public protected CBCentralManager (Foundation.NSObjectFlag t)
```

Added constructors:

```
public CBCentralManager (ICBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue);
	public CBCentralManager (ICBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue, Foundation.NSDictionary options);
	public CBCentralManager (ICBCentralManagerDelegate centralDelegate, CoreFoundation.DispatchQueue queue, CBCentralInitOptions options);
```

Modified properties:

```
public CBCentralManagerDelegate ICBCentralManagerDelegate Delegate { get; set; }
```

Removed methods:

```
[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void RetrievePeripherals (System.Guid peripheralUuid);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void RetrievePeripherals (System.Guid[] peripheralUuids);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid[] serviceUuids, Foundation.NSDictionary options);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid[] serviceUuids, PeripheralScanningOptions options);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid[] serviceUuids);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid serviceUuid, Foundation.NSDictionary options);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void ScanForPeripherals (System.Guid serviceUuid);
```

### Type Changed: CoreBluetooth.CBCentralManagerDelegate

Modified constructors:

```
public protected CBCentralManagerDelegate ()
	public protected CBCentralManagerDelegate (Foundation.NSObjectFlag t)
	public protected CBCentralManagerDelegate (IntPtr handle)
```

### Type Changed: CoreBluetooth.CBCharacteristic

Removed constructors:

```
[Obsolete ("This type is not meant to be created by user code. Use CBMutableCharacteristic")]
	public CBCharacteristic ();
```

Modified constructors:

```
public protected CBCharacteristic (Foundation.NSObjectFlag t)
	public protected CBCharacteristic (IntPtr handle)
```

Removed property:

```
public virtual CBCentral[] SubscribedCentrals { get; }
```

### Type Changed: CoreBluetooth.CBDescriptor

Removed constructors:

```
[Obsolete ("This type is not meant to be created by user code. Use CBMutableDescriptor")]
	public CBDescriptor ();
```

Modified constructors:

```
public protected CBDescriptor (Foundation.NSObjectFlag t)
	public protected CBDescriptor (IntPtr handle)
```

### Type Changed: CoreBluetooth.CBMutableCharacteristic

Removed constructors:

```
[Obsolete ("Use .ctor(CBUUID,CBCharacteristicProperties,NSData,CBAttributePermissions)")]
	public CBMutableCharacteristic ();
```

Modified constructors:

```
public protected CBMutableCharacteristic (Foundation.NSObjectFlag t)
	public protected CBMutableCharacteristic (IntPtr handle)
```

Added property:

```
public virtual CBCentral[] SubscribedCentrals { get; }
```

### Type Changed: CoreBluetooth.CBMutableDescriptor

Removed constructors:

```
[Obsolete ("Use .ctor(CBUUID,NSObject)")]
	public CBMutableDescriptor ();
```

Modified constructors:

```
public protected CBMutableDescriptor (Foundation.NSObjectFlag t)
	public protected CBMutableDescriptor (IntPtr handle)
```

### Type Changed: CoreBluetooth.CBMutableService

Removed constructors:

```
[Obsolete ("Use .ctor (CBUUID,bool)")]
	public CBMutableService ();
```

Modified constructors:

```
public protected CBMutableService (Foundation.NSObjectFlag t)
	public protected CBMutableService (IntPtr handle)
```

### Type Changed: CoreBluetooth.CBPeer

Modified constructors:

```
public protected CBPeer (Foundation.NSObjectFlag t)
	public protected CBPeer (IntPtr handle)
```

Removed property:

```
public virtual CBUUID UUID { get; }
```

### Type Changed: CoreBluetooth.CBPeripheral

Removed constructors:

```
[Obsolete ("This type is not meant to be created by user code.")]
	public CBPeripheral ();
```

Modified constructors:

```
public protected CBPeripheral (Foundation.NSObjectFlag t)
	public protected CBPeripheral (IntPtr handle)
```

Removed property:

```
public virtual IntPtr UUID { get; }
```

Modified properties:

```
public CBPeripheralDelegate ICBPeripheralDelegate Delegate { get; set; }
```

Removed event:

```
public event System.EventHandler<CBServiceEventArgs> DiscoverCharacteristic;
```

Added event:

```
public event System.EventHandler<CBServiceEventArgs> DiscoveredCharacteristic;
```

Removed methods:

```
[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void DiscoverCharacteristics (System.Guid[] charactersticUUIDs, CBService forService);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void DiscoverIncludedServices (System.Guid[] includedServiceUUIDs, CBService forService);

	[Obsolete ("Use the CBUUID overload since Guid internal memory representation is different")]
	public void DiscoverServices (System.Guid[] services);
```

### Type Changed: CoreBluetooth.CBPeripheralDelegate

Modified constructors:

```
public protected CBPeripheralDelegate (Foundation.NSObjectFlag t)
	public protected CBPeripheralDelegate (IntPtr handle)
```

Removed method:

```
public virtual void DiscoverCharacteristic (CBPeripheral peripheral, CBService service, Foundation.NSError error);
```

Added method:

```
public virtual void DiscoveredCharacteristic (CBPeripheral peripheral, CBService service, Foundation.NSError error);
```

### Type Changed: CoreBluetooth.CBPeripheralDelegate_Extensions

Removed method:

```
public static void DiscoverCharacteristic (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService service, Foundation.NSError error);
```

Added method:

```
public static void DiscoveredCharacteristic (ICBPeripheralDelegate This, CBPeripheral peripheral, CBService service, Foundation.NSError error);
```

### Type Changed: CoreBluetooth.CBPeripheralManager

Removed constructors:

```
public CBPeripheralManager (CBPeripheralManagerDelegate peripheralDelegate, CoreFoundation.DispatchQueue queue);
	public CBPeripheralManager (CBPeripheralManagerDelegate peripheralDelegate, CoreFoundation.DispatchQueue queue, Foundation.NSDictionary options);
```

Modified constructors:

```
public protected CBPeripheralManager (Foundation.NSObjectFlag t)
	public protected CBPeripheralManager (IntPtr handle)
```

Added constructors:

```
public CBPeripheralManager (ICBPeripheralManagerDelegate peripheralDelegate, CoreFoundation.DispatchQueue queue);
	public CBPeripheralManager (ICBPeripheralManagerDelegate peripheralDelegate, CoreFoundation.DispatchQueue queue, Foundation.NSDictionary options);
```

Modified properties:

```
public CBPeripheralManagerDelegate ICBPeripheralManagerDelegate Delegate { get; set; }
```

### Type Changed: CoreBluetooth.CBPeripheralManagerDelegate

Modified constructors:

```
public protected CBPeripheralManagerDelegate ()
	public protected CBPeripheralManagerDelegate (Foundation.NSObjectFlag t)
	public protected CBPeripheralManagerDelegate (IntPtr handle)
```

### Type Changed: CoreBluetooth.CBService

Removed constructors:

```
[Obsolete ("This type is not meant to be created by user code. Use CBMutableService")]
	public CBService ();
```

Modified constructors:

```
public protected CBService (Foundation.NSObjectFlag t)
	public protected CBService (IntPtr handle)
```

### Type Changed: CoreBluetooth.CBUUID

Removed constructors:

```
[Obsolete ("Use FromString or FromData to create a valid CBUUID instance")]
	public CBUUID ();
```

Modified constructors:

```
public protected CBUUID (Foundation.NSObjectFlag t)
	public protected CBUUID (IntPtr handle)
```

Removed methods:

```
public override bool Equals (object obj);
	public override int GetHashCode ();
```

### Type Changed: CoreBluetooth.PeripheralConnectionOptions

Removed properties:

```
[Obsolete ("use NotifyOnConnection property instead")]
	public bool NotifyOnConnectionKey { set; }

	[Obsolete ("Use NotifyOnDisconnection property instead")]
	public bool NotifyOnDisconnectionKey { set; }

	[Obsolete ("use NotifyOnNotification property instead")]
	public bool NotifyOnNotificationKey { set; }
```

## Namespace CoreData



### Type Changed: CoreData.NSAsynchronousFetchRequest

Modified constructors:

```
public protected NSAsynchronousFetchRequest (Foundation.NSObjectFlag t)
	public protected NSAsynchronousFetchRequest (IntPtr handle)
```

### Type Changed: CoreData.NSAsynchronousFetchResult

Modified constructors:

```
public protected NSAsynchronousFetchResult (Foundation.NSObjectFlag t)
	public protected NSAsynchronousFetchResult (IntPtr handle)
```

### Type Changed: CoreData.NSAtomicStore

Modified constructors:

```
public protected NSAtomicStore (Foundation.NSObjectFlag t)
	public protected NSAtomicStore (IntPtr handle)
```

### Type Changed: CoreData.NSAtomicStoreCacheNode

Modified constructors:

```
public protected NSAtomicStoreCacheNode (Foundation.NSObjectFlag t)
	public protected NSAtomicStoreCacheNode (IntPtr handle)
```

### Type Changed: CoreData.NSAttributeDescription

Modified constructors:

```
public protected NSAttributeDescription (Foundation.NSObjectFlag t)
	public protected NSAttributeDescription (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use the DefaultValue property")]
	public virtual void SetDefaultValue (Foundation.NSObject value);
```

### Type Changed: CoreData.NSBatchUpdateRequest

Modified constructors:

```
public protected NSBatchUpdateRequest (Foundation.NSObjectFlag t)
	public protected NSBatchUpdateRequest (IntPtr handle)
```

### Type Changed: CoreData.NSBatchUpdateResult

Modified constructors:

```
public protected NSBatchUpdateResult (Foundation.NSObjectFlag t)
	public protected NSBatchUpdateResult (IntPtr handle)
```

### Type Changed: CoreData.NSEntityDescription

Modified constructors:

```
public protected NSEntityDescription (Foundation.NSObjectFlag t)
	public protected NSEntityDescription (IntPtr handle)
```

### Type Changed: CoreData.NSEntityMapping

Modified constructors:

```
public protected NSEntityMapping (Foundation.NSObjectFlag t)
	public protected NSEntityMapping (IntPtr handle)
```

### Type Changed: CoreData.NSEntityMigrationPolicy

Modified constructors:

```
public protected NSEntityMigrationPolicy (Foundation.NSObjectFlag t)
	public protected NSEntityMigrationPolicy (IntPtr handle)
```

### Type Changed: CoreData.NSFetchedPropertyDescription

Modified constructors:

```
public protected NSFetchedPropertyDescription (Foundation.NSObjectFlag t)
	public protected NSFetchedPropertyDescription (IntPtr handle)
```

### Type Changed: CoreData.NSFetchedResultsController

Modified constructors:

```
public protected NSFetchedResultsController (Foundation.NSObjectFlag t)
	public protected NSFetchedResultsController (IntPtr handle)
```

Modified properties:

```
public NSFetchedResultsControllerDelegate INSFetchedResultsControllerDelegate Delegate { get; set; }
```

### Type Changed: CoreData.NSFetchedResultsControllerDelegate

Modified constructors:

```
public protected NSFetchedResultsControllerDelegate (Foundation.NSObjectFlag t)
	public protected NSFetchedResultsControllerDelegate (IntPtr handle)
```

### Type Changed: CoreData.NSFetchedResultsSectionInfo

Modified constructors:

```
public protected NSFetchedResultsSectionInfo ()
	public protected NSFetchedResultsSectionInfo (Foundation.NSObjectFlag t)
	public protected NSFetchedResultsSectionInfo (IntPtr handle)
```

### Type Changed: CoreData.NSFetchRequest

Modified constructors:

```
public protected NSFetchRequest (Foundation.NSObjectFlag t)
	public protected NSFetchRequest (IntPtr handle)
```

### Type Changed: CoreData.NSIncrementalStore

Modified constructors:

```
public protected NSIncrementalStore (Foundation.NSObjectFlag t)
	public protected NSIncrementalStore (IntPtr handle)
```

### Type Changed: CoreData.NSIncrementalStoreNode

Modified constructors:

```
public protected NSIncrementalStoreNode (Foundation.NSObjectFlag t)
	public protected NSIncrementalStoreNode (IntPtr handle)
```

### Type Changed: CoreData.NSManagedObject

Modified constructors:

```
public protected NSManagedObject (Foundation.NSObjectFlag t)
	public protected NSManagedObject (IntPtr handle)
```

Removed methods:

```
public virtual void DidChangeValueForKey (string inKey, NSKeyValueSetMutationKind inMutationKind, Foundation.NSSet inObjects);
	public virtual void WillChangeValueForKey (string inKey, NSKeyValueSetMutationKind inMutationKind, Foundation.NSSet inObjects);
```

Added methods:

```
public virtual void DidChangeValueForKey (string inKey, Foundation.NSKeyValueSetMutationKind inMutationKind, Foundation.NSSet inObjects);
	public virtual void WillChangeValueForKey (string inKey, Foundation.NSKeyValueSetMutationKind inMutationKind, Foundation.NSSet inObjects);
```

### Type Changed: CoreData.NSManagedObjectContext

Modified constructors:

```
public protected NSManagedObjectContext (Foundation.NSObjectFlag t)
	public protected NSManagedObjectContext (IntPtr handle)
```

Removed methods:

```
public virtual void Perform (Foundation.NSAction action);
	public virtual void PerformAndWait (Foundation.NSAction action);
```

Added methods:

```
public virtual void Perform (System.Action action);
	public virtual void PerformAndWait (System.Action action);
```

### Type Changed: CoreData.NSManagedObjectID

Modified constructors:

```
public protected NSManagedObjectID (Foundation.NSObjectFlag t)
	public protected NSManagedObjectID (IntPtr handle)
```

### Type Changed: CoreData.NSManagedObjectModel

Modified constructors:

```
public protected NSManagedObjectModel (Foundation.NSObjectFlag t)
	public protected NSManagedObjectModel (IntPtr handle)
```

### Type Changed: CoreData.NSMappingModel

Modified constructors:

```
public protected NSMappingModel (Foundation.NSObjectFlag t)
	public protected NSMappingModel (IntPtr handle)
```

### Type Changed: CoreData.NSMergeConflict

Modified constructors:

```
public protected NSMergeConflict (Foundation.NSObjectFlag t)
	public protected NSMergeConflict (IntPtr handle)
```

### Type Changed: CoreData.NSMergePolicy

Modified constructors:

```
public protected NSMergePolicy (Foundation.NSObjectFlag t)
	public protected NSMergePolicy (IntPtr handle)
```

### Type Changed: CoreData.NSMigrationManager

Modified constructors:

```
public protected NSMigrationManager (Foundation.NSObjectFlag t)
	public protected NSMigrationManager (IntPtr handle)
```

### Type Changed: CoreData.NSPersistentStore

Modified constructors:

```
public protected NSPersistentStore (Foundation.NSObjectFlag t)
	public protected NSPersistentStore (IntPtr handle)
```

### Type Changed: CoreData.NSPersistentStoreAsynchronousResult

Modified constructors:

```
public protected NSPersistentStoreAsynchronousResult (Foundation.NSObjectFlag t)
	public protected NSPersistentStoreAsynchronousResult (IntPtr handle)
```

### Type Changed: CoreData.NSPersistentStoreCoordinator

Removed constructors:

```
[Obsolete ("Use .ctor(NSManagedObjectModel)")]
	public NSPersistentStoreCoordinator ();
```

Modified constructors:

```
public protected NSPersistentStoreCoordinator (Foundation.NSObjectFlag t)
	public protected NSPersistentStoreCoordinator (IntPtr handle)
```

### Type Changed: CoreData.NSPersistentStoreRequest

Modified constructors:

```
public protected NSPersistentStoreRequest (Foundation.NSObjectFlag t)
	public protected NSPersistentStoreRequest (IntPtr handle)
```

### Type Changed: CoreData.NSPersistentStoreResult

Modified constructors:

```
public protected NSPersistentStoreResult (Foundation.NSObjectFlag t)
	public protected NSPersistentStoreResult (IntPtr handle)
```

### Type Changed: CoreData.NSPropertyDescription

Modified constructors:

```
public protected NSPropertyDescription (Foundation.NSObjectFlag t)
	public protected NSPropertyDescription (IntPtr handle)
```

### Type Changed: CoreData.NSPropertyMapping

Modified constructors:

```
public protected NSPropertyMapping (Foundation.NSObjectFlag t)
	public protected NSPropertyMapping (IntPtr handle)
```

### Type Changed: CoreData.NSRelationshipDescription

Modified constructors:

```
public protected NSRelationshipDescription (Foundation.NSObjectFlag t)
	public protected NSRelationshipDescription (IntPtr handle)
```

### Type Changed: CoreData.NSSaveChangesRequest

Modified constructors:

```
public protected NSSaveChangesRequest (Foundation.NSObjectFlag t)
	public protected NSSaveChangesRequest (IntPtr handle)
```

### Removed Type CoreData.NSFetchedResultsSectionInfo_Extensions ### Removed Type CoreData.NSKeyValueSetMutationKind 



## Namespace CoreFoundation



### Type Changed: CoreFoundation.CFAllocator

Removed method:

```
public IntPtr Allocate (long size, CFAllocatorFlags hint);
```

Added method:

```
public IntPtr Allocate (long size);
```

### Type Changed: CoreFoundation.CFRange

Added constructor:

```
public CFRange (int l, int len);
```

### Type Changed: CoreFoundation.CFReadStream

Removed method:

```
protected override bool DoSetClient (CFStream.CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
```

Added method:

```
protected override bool DoSetClient (CFStream.CFStreamCallback callback, int eventTypes, IntPtr context);
```

### Type Changed: CoreFoundation.CFRunLoop

Removed properties:

```
public static Foundation.NSString CFDefaultRunLoopMode { get; }
	public static Foundation.NSString CFRunLoopCommonModes { get; }
```

Removed methods:

```
public bool RemoveSource (CFRunLoopSource source, Foundation.NSString mode);

	[Obsolete ("Use the NSString version of CFRunLoop.RunInMode() instead.")]
	public CFRunLoopExitReason RunInMode (string mode, double seconds, bool returnAfterSourceHandled);
```

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

Added method:

```
public void RemoveSource (CFRunLoopSource source, Foundation.NSString mode);
```

### Type Changed: CoreFoundation.CFRunLoopSource

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: CoreFoundation.CFRunLoopSourceCustom

Removed methods:

```
protected virtual void OnCancel (CFRunLoop loop, string mode);
	protected virtual void OnSchedule (CFRunLoop loop, string mode);
```

Modified methods:

```
public protected override void Dispose (bool disposing)
```

Added methods:

```
protected virtual void OnCancel (CFRunLoop loop, Foundation.NSString mode);
	protected virtual void OnSchedule (CFRunLoop loop, Foundation.NSString mode);
```

### Type Changed: CoreFoundation.CFStream

Removed method:

```
protected virtual bool DoSetClient (CFStream.CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
```

Added method:

```
protected virtual bool DoSetClient (CFStream.CFStreamCallback callback, int eventTypes, IntPtr context);
```

### Type Changed: CoreFoundation.CFString

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: CoreFoundation.CFWriteStream

Removed method:

```
protected override bool DoSetClient (CFStream.CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
```

Added method:

```
protected override bool DoSetClient (CFStream.CFStreamCallback callback, int eventTypes, IntPtr context);
```

### Type Changed: CoreFoundation.DispatchGroup

Removed methods:

```
public void DispatchAsync (DispatchQueue queue, Foundation.NSAction action);
	public void Notify (DispatchQueue queue, Foundation.NSAction action);
```

Added methods:

```
public void DispatchAsync (DispatchQueue queue, System.Action action);
	public void Notify (DispatchQueue queue, System.Action action);
```

### Type Changed: CoreFoundation.DispatchQueue

Removed methods:

```
public void DispatchAfter (DispatchTime when, Foundation.NSAction action);
	public void DispatchAsync (Foundation.NSAction action);
	public void DispatchSync (Foundation.NSAction action);
```

Added methods:

```
public void DispatchAfter (DispatchTime when, System.Action action);
	public void DispatchAsync (System.Action action);
	public void DispatchSync (System.Action action);
```

### Removed Type CoreFoundation.CFAllocatorFlags ### Removed Type CoreFoundation.CFIndex 



## Namespace CoreGraphics



### Type Changed: CoreGraphics.CGBitmapContext

Modified properties:

```
public uint CGBitmapFlags BitmapInfo { get; }
```

### Type Changed: CoreGraphics.CGColorSpace

Modified fields:

```
public readonly CGColorSpace Null;
```

### Type Changed: CoreGraphics.CGContext

Removed methods:

```
public void BeginTransparencyLayer (System.Drawing.RectangleF rectangle);
	public void BeginTransparencyLayer ();

	[Obsolete ("Use SetFillColor() instead.")]
	public void SetCMYKFillColor (float cyan, float magenta, float yellow, float black, float alpha);

	[Obsolete ("Use SetStrokeColor() instead.")]
	public void SetCMYKStrokeColor (float cyan, float magenta, float yellow, float black, float alpha);

	[Obsolete ("Use SetFillColor() instead.")]
	public void SetFillColorWithColor (CGColor color);

	[Obsolete ("Use SetFillColor() instead.")]
	public void SetGrayFillColor (float gray, float alpha);

	[Obsolete ("Use SetStrokeColor() instead.")]
	public void SetGrayStrokeColor (float gray, float alpha);

	[Obsolete ("Use SetFillColor() instead.")]
	public void SetRGBFillColor (float red, float green, float blue, float alpha);

	[Obsolete ("Use SetStrokeColor() instead.")]
	public void SetRGBStrokeColor (float red, float green, float blue, float alpha);
	public void SetShadow (System.Drawing.SizeF offset, float blur);
	public void SetShadowWithColor (System.Drawing.SizeF offset, float blur, CGColor color);

	[Obsolete ("Use SetStrokeColor() instead.")]
	public void SetStrokeColorWithColor (CGColor color);
```

Modified methods:

```
public void ShowGlyphsAtPositions (ushort[] glyphs, System.Drawing.PointF[] positions, int size_t_count count = -1)
```

Added method:

```
public void SetShadow (System.Drawing.SizeF offset, float blur, CGColor color);
```

### Type Changed: CoreGraphics.CGFont

Removed method:

```
[Obsolete ("Use ToCTFont(GCFloat,CGAffineTransform)")]
	public CoreText.CTFont ToCTFont (float size, ref CGAffineTransform matrix);
```

### Type Changed: CoreGraphics.CGImageProperties

Removed properties:

```
[Obsolete ("Use the DPIHeightF property")]
	public int? DPIHeight { get; set; }

	[Obsolete ("Use the DPIWidthF property")]
	public int? DPIWidth { get; set; }
```

### Type Changed: CoreGraphics.CGPath

Removed methods:

```
[Obsolete ("Use AddEllipseInRect instead")]
	public void AddElipseInRect (CGAffineTransform m, System.Drawing.RectangleF rect);

	[Obsolete ("Use AddEllipseInRect instead")]
	public void AddElipseInRect (System.Drawing.RectangleF rect);

	[Obsolete ("Misnamed method, it's AddLines")]
	public void AddRects (CGAffineTransform m, System.Drawing.PointF[] points, int count);

	[Obsolete ("Misnamed method, it's AddLines")]
	public void AddRects (System.Drawing.PointF[] points, int count);

	[Obsolete ("Use AddLineToPoint instead")]
	public void CGPathAddLineToPoint (CGAffineTransform transform, float x, float y);

	[Obsolete ("Use AddLineToPoint instead")]
	public void CGPathAddLineToPoint (float x, float y);
```

Added methods:

```
public void AddLines (CGAffineTransform m, System.Drawing.PointF[] points, int count);
	public void AddLines (System.Drawing.PointF[] points, int count);
```

### Type Changed: CoreGraphics.CGPDFDictionary

Removed method:

```
[Obsolete ("Use the Apply(Action method")]
	public void Apply (System.Action<System.String,System.Object> callback);
```

### Type Changed: CoreGraphics.CGPDFDocument

Removed methods:

```
public System.Drawing.RectangleF GetArtBox (int page);
	public System.Drawing.RectangleF GetBleedBox (int page);
	public System.Drawing.RectangleF GetCropBox (int page);
	public System.Drawing.RectangleF GetMediaBox (int page);
	public System.Drawing.RectangleF GetTrimBox (int page);
	public bool UnlockWithPassword (string pass);
```

Added method:

```
public bool Unlock (string password);
```

### Type Changed: CoreGraphics.CGPDFStream

Removed property:

```
[Obsolete ("Use GetData(out CGPDFDataFormat) instead")]
	public Foundation.NSData Data { get; }
```

### Type Changed: CoreGraphics.RectangleFExtensions

Removed method:

```
public static void Divide (System.Drawing.RectangleF self, float amount, CGRectEdge edge, out System.Drawing.RectangleF slice, out System.Drawing.RectangleF remainder);
```

Added method:

```
public static void Divide (System.Drawing.RectangleF self, float amount, System.Drawing.RectangleFEdge edge, out System.Drawing.RectangleF slice, out System.Drawing.RectangleF remainder);
```

### Removed Type CoreGraphics.NSDictionaryExtensions ### Removed Type CoreGraphics.PointFExtensions ### New Type CoreGraphics.CGPoint

```
[Serializable]
public struct CGPoint, System.IEquatable<System.Drawing.PointF> {
	// constructors
	public CGPoint (float x, float y);
	public CGPoint (System.Drawing.PointF point);
	// fields
	public static System.Drawing.PointF Empty;
	// properties
	public bool IsEmpty { get; }
	public float X { get; set; }
	public float Y { get; set; }
	// methods
	public static System.Drawing.PointF Add (System.Drawing.PointF point, System.Drawing.SizeF size);
	public virtual bool Equals (System.Drawing.PointF point);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static System.Drawing.PointF op_Addition (System.Drawing.PointF l, System.Drawing.SizeF r);
	public static bool op_Equality (System.Drawing.PointF l, System.Drawing.PointF r);
	public static System.Drawing.Point op_Explicit (System.Drawing.PointF point);
	public static System.Drawing.PointF op_Explicit (System.Drawing.PointF point);
	public static System.Drawing.PointF op_Implicit (System.Drawing.Point point);
	public static System.Drawing.PointF op_Implicit (System.Drawing.PointF point);
	public static bool op_Inequality (System.Drawing.PointF l, System.Drawing.PointF r);
	public static System.Drawing.PointF op_Subtraction (System.Drawing.PointF l, System.Drawing.SizeF r);
	public static System.Drawing.PointF Subtract (System.Drawing.PointF point, System.Drawing.SizeF size);
	public Foundation.NSDictionary ToDictionary ();
	public override string ToString ();
	public static bool TryParse (Foundation.NSDictionary dictionaryRepresentation, out System.Drawing.PointF point);
}
```

### New Type CoreGraphics.CGRect

```
[Serializable]
public struct CGRect, System.IEquatable<System.Drawing.RectangleF> {
	// constructors
	public CGRect (System.Drawing.PointF location, System.Drawing.SizeF size);
	public CGRect (float x, float y, float width, float height);
	// fields
	public static System.Drawing.RectangleF Empty;
	// properties
	public float Bottom { get; }
	public float Height { get; set; }
	public bool IsEmpty { get; }
	public float Left { get; }
	public System.Drawing.PointF Location { get; set; }
	public float Right { get; }
	public System.Drawing.SizeF Size { get; set; }
	public float Top { get; }
	public float Width { get; set; }
	public float X { get; set; }
	public float Y { get; set; }
	// methods
	public bool Contains (System.Drawing.PointF point);
	public bool Contains (float x, float y);
	public bool Contains (System.Drawing.RectangleF rect);
	public override bool Equals (object obj);
	public virtual bool Equals (System.Drawing.RectangleF rect);
	public static System.Drawing.RectangleF FromLTRB (float left, float top, float right, float bottom);
	public override int GetHashCode ();
	public void Inflate (System.Drawing.SizeF size);
	public static System.Drawing.RectangleF Inflate (System.Drawing.RectangleF rect, float x, float y);
	public void Inflate (float x, float y);
	public static System.Drawing.RectangleF Intersect (System.Drawing.RectangleF a, System.Drawing.RectangleF b);
	public void Intersect (System.Drawing.RectangleF rect);
	public bool IntersectsWith (System.Drawing.RectangleF rect);
	public void Offset (float x, float y);
	public void Offset (System.Drawing.PointF pos);
	public static bool op_Equality (System.Drawing.RectangleF left, System.Drawing.RectangleF right);
	public static System.Drawing.Rectangle op_Explicit (System.Drawing.RectangleF rect);
	public static System.Drawing.RectangleF op_Explicit (System.Drawing.RectangleF rect);
	public static System.Drawing.RectangleF op_Implicit (System.Drawing.RectangleF rect);
	public static System.Drawing.RectangleF op_Implicit (System.Drawing.Rectangle rect);
	public static bool op_Inequality (System.Drawing.RectangleF left, System.Drawing.RectangleF right);
	public Foundation.NSDictionary ToDictionary ();
	public override string ToString ();
	public static bool TryParse (Foundation.NSDictionary dictionaryRepresentation, out System.Drawing.RectangleF rect);
	public static System.Drawing.RectangleF Union (System.Drawing.RectangleF a, System.Drawing.RectangleF b);
}
```

### New Type CoreGraphics.CGSize

```
[Serializable]
public struct CGSize, System.IEquatable<System.Drawing.SizeF> {
	// constructors
	public CGSize (float width, float height);
	public CGSize (System.Drawing.SizeF size);
	public CGSize (System.Drawing.PointF point);
	// fields
	public static System.Drawing.SizeF Empty;
	// properties
	public float Height { get; set; }
	public bool IsEmpty { get; }
	public float Width { get; set; }
	// methods
	public static System.Drawing.SizeF Add (System.Drawing.SizeF size1, System.Drawing.SizeF size2);
	public override bool Equals (object obj);
	public virtual bool Equals (System.Drawing.SizeF size);
	public override int GetHashCode ();
	public static System.Drawing.SizeF op_Addition (System.Drawing.SizeF l, System.Drawing.SizeF r);
	public static bool op_Equality (System.Drawing.SizeF l, System.Drawing.SizeF r);
	public static System.Drawing.PointF op_Explicit (System.Drawing.SizeF size);
	public static System.Drawing.Size op_Explicit (System.Drawing.SizeF size);
	public static System.Drawing.SizeF op_Explicit (System.Drawing.SizeF size);
	public static System.Drawing.SizeF op_Implicit (System.Drawing.Size size);
	public static System.Drawing.SizeF op_Implicit (System.Drawing.SizeF size);
	public static bool op_Inequality (System.Drawing.SizeF l, System.Drawing.SizeF r);
	public static System.Drawing.SizeF op_Subtraction (System.Drawing.SizeF l, System.Drawing.SizeF r);
	public static System.Drawing.SizeF Subtract (System.Drawing.SizeF size1, System.Drawing.SizeF size2);
	public System.Drawing.PointF ToCGPoint ();
	public Foundation.NSDictionary ToDictionary ();

	[Obsolete ("Use ToCGPoint instead")]
	public System.Drawing.PointF ToPointF ();
	public System.Drawing.SizeF ToRoundedCGSize ();

	[Obsolete ("Use ToRoundedCGSize instead")]
	public System.Drawing.SizeF ToSize ();
	public override string ToString ();
	public static bool TryParse (Foundation.NSDictionary dictionaryRepresentation, out System.Drawing.SizeF size);
}
```





## Namespace CoreImage



### Type Changed: CoreImage.CIColor

Modified constructors:

```
public protected CIColor (Foundation.NSObjectFlag t)
	public protected CIColor (IntPtr handle)
```

### Type Changed: CoreImage.CIColorKernel

Modified constructors:

```
public protected CIColorKernel (Foundation.NSObjectFlag t)
	public protected CIColorKernel (IntPtr handle)
```

### Type Changed: CoreImage.CIContext

Modified constructors:

```
public protected CIContext (Foundation.NSObjectFlag t)
	public protected CIContext (IntPtr handle)
```

### Type Changed: CoreImage.CIDetector

Modified constructors:

```
public protected CIDetector (Foundation.NSObjectFlag t)
	public protected CIDetector (IntPtr handle)
```

### Type Changed: CoreImage.CIFaceFeature

Modified constructors:

```
public protected CIFaceFeature (Foundation.NSObjectFlag t)
	public protected CIFaceFeature (IntPtr handle)
```

### Type Changed: CoreImage.CIFeature

Modified constructors:

```
public protected CIFeature (Foundation.NSObjectFlag t)
	public protected CIFeature (IntPtr handle)
```

### Type Changed: CoreImage.CIFilter

Modified constructors:

```
public protected CIFilter (Foundation.NSObjectFlag t)
	public protected CIFilter (IntPtr handle)
```

### Type Changed: CoreImage.CIImage

Removed constructors:

```
[Obsolete ("CVImageBuffer is used on OSX, for iOS use CVPixelBuffer")]
	public CIImage (CoreVideo.CVImageBuffer imageBuffer);

	[Obsolete ("CVImageBuffer is used on OSX, for iOS use CVPixelBuffer")]
	public CIImage (CoreVideo.CVImageBuffer imageBuffer, Foundation.NSDictionary dict);

	[Obsolete ("CVImageBuffer is used on OSX, for iOS use CVPixelBuffer")]
	public CIImage (CoreVideo.CVImageBuffer imageBuffer, CIImageInitializationOptions options);

	[Obsolete ("A CIImage cannot be created from a CGLayer on iOS (only OSX)")]
	public CIImage (CoreGraphics.CGLayer layer);

	[Obsolete ("A CIImage cannot be created from a CGLayer on iOS (only OSX)")]
	public CIImage (CoreGraphics.CGLayer layer, Foundation.NSDictionary d);

	[Obsolete ("A CIImage cannot be created from a CGLayer on iOS (only OSX)")]
	public CIImage (CoreGraphics.CGLayer layer, CIImageInitializationOptions options);
```

Modified constructors:

```
public protected CIImage (IntPtr handle)
	public protected CIImage (Foundation.NSObjectFlag t)
```

Removed method:

```
[Obsolete ("Use the overload acceping a CIFormat enum (instead of an int) for pixelFormat")]
	public static CIImage FromData (Foundation.NSData bitmapData, int bytesPerRow, System.Drawing.SizeF size, int pixelFormat, CoreGraphics.CGColorSpace colorSpace);
```

### Type Changed: CoreImage.CIKernel

Modified constructors:

```
public protected CIKernel (Foundation.NSObjectFlag t)
	public protected CIKernel (IntPtr handle)
```

Removed methods:

```
[Obsolete ("Use FromProgramSingle")]
	public static CIKernel FromProgram (string coreImageShaderProgram);

	[Obsolete ("Use FromProgramMultiple")]
	public static CIKernel[] FromPrograms (string coreImageShaderProgram);
```

### Type Changed: CoreImage.CIQRCodeFeature

Modified constructors:

```
public protected CIQRCodeFeature (Foundation.NSObjectFlag t)
	public protected CIQRCodeFeature (IntPtr handle)
```

### Type Changed: CoreImage.CIRectangleFeature

Modified constructors:

```
public protected CIRectangleFeature (Foundation.NSObjectFlag t)
	public protected CIRectangleFeature (IntPtr handle)
```

### Type Changed: CoreImage.CIVector

Modified constructors:

```
public protected CIVector (IntPtr handle)
	public protected CIVector (Foundation.NSObjectFlag t)
```

### Type Changed: CoreImage.CIWarpKernel

Modified constructors:

```
public protected CIWarpKernel (Foundation.NSObjectFlag t)
	public protected CIWarpKernel (IntPtr handle)
```

## Namespace CoreLocation



### Type Changed: CoreLocation.CLBeacon

Modified constructors:

```
public protected CLBeacon (Foundation.NSObjectFlag t)
	public protected CLBeacon (IntPtr handle)
```

### Type Changed: CoreLocation.CLBeaconRegion

Removed constructor:

```
[Obsolete ("Does not return a valid instance on iOS8")]
	public CLBeaconRegion ();
```

Modified constructors:

```
public protected CLBeaconRegion (Foundation.NSObjectFlag t)
	public protected CLBeaconRegion (IntPtr handle)
```

### Type Changed: CoreLocation.CLCircularRegion

Modified constructors:

```
public protected CLCircularRegion (Foundation.NSObjectFlag t)
	public protected CLCircularRegion (IntPtr handle)
```

### Type Changed: CoreLocation.CLFloor

Modified constructors:

```
public protected CLFloor (Foundation.NSObjectFlag t)
	public protected CLFloor (IntPtr handle)
```

### Type Changed: CoreLocation.CLGeocoder

Modified constructors:

```
public protected CLGeocoder (Foundation.NSObjectFlag t)
	public protected CLGeocoder (IntPtr handle)
```

### Type Changed: CoreLocation.CLHeading

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CLHeading ();
```

Modified constructors:

```
public protected CLHeading (Foundation.NSObjectFlag t)
	public protected CLHeading (IntPtr handle)
```

### Type Changed: CoreLocation.CLLocation

Modified constructors:

```
public protected CLLocation (Foundation.NSObjectFlag t)
	public protected CLLocation (IntPtr handle)
```

Removed fields:

```
public static double AccuracyBest;
	public static double AccuracyHundredMeters;
	public static double AccuracyKilometer;
	public static double AccuracyNearestTenMeters;
	public static double AccuracyThreeKilometers;
	public static double AccurracyBestForNavigation;
```

Added properties:

```
public static double AccuracyBest { get; }
	public static double AccuracyHundredMeters { get; }
	public static double AccuracyKilometer { get; }
	public static double AccuracyNearestTenMeters { get; }
	public static double AccuracyThreeKilometers { get; }
	public static double AccurracyBestForNavigation { get; }
```

Removed method:

```
public virtual double Distancefrom (CLLocation location);
```

### Type Changed: CoreLocation.CLLocationManager

Modified constructors:

```
public protected CLLocationManager (Foundation.NSObjectFlag t)
	public protected CLLocationManager (IntPtr handle)
```

Modified properties:

```
public CLLocationManagerDelegate ICLLocationManagerDelegate Delegate { get; set; }
```

### Type Changed: CoreLocation.CLLocationManagerDelegate

Modified constructors:

```
public protected CLLocationManagerDelegate (Foundation.NSObjectFlag t)
	public protected CLLocationManagerDelegate (IntPtr handle)
```

Removed method:

```
[Obsolete ("Do not override this method, override the (CLLocationManager, CLRegion) overload instead.")]
	public virtual void DidStartMonitoringForRegion (CLRegion region);
```

### Type Changed: CoreLocation.CLPlacemark

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CLPlacemark ();
```

Modified constructors:

```
public protected CLPlacemark (Foundation.NSObjectFlag t)
	public protected CLPlacemark (IntPtr handle)
```

### Type Changed: CoreLocation.CLRegion

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CLRegion ();
```

Modified constructors:

```
public protected CLRegion (Foundation.NSObjectFlag t)
	public protected CLRegion (IntPtr handle)
```

### Type Changed: CoreLocation.CLVisit

Modified constructors:

```
public protected CLVisit (Foundation.NSObjectFlag t)
	public protected CLVisit (IntPtr handle)
```

### Removed Type CoreLocation.CLAuthroziationChangedEventArgs 

## Namespace CoreMedia



### Type Changed: CoreMedia.CMFormatDescription

Removed property:

```
[Obsolete ("Use CMVideoFormatDescription")]
	public System.Drawing.Size VideoDimensions { get; }
```

Removed methods:

```
public static Foundation.NSObject[] GetExtensionKeysCommonWithImageBuffers ();

	[Obsolete ("Use CMVideoFormatDescription")]
	public System.Drawing.RectangleF GetVideoCleanAperture (bool originIsAtTopLeft);

	[Obsolete ("Use CMVideoFormatDescription")]
	public System.Drawing.SizeF GetVideoPresentationDimensions (bool usePixelAspectRatio, bool useCleanAperture);
	public bool VideoMatchesImageBuffer (CoreVideo.CVImageBuffer imageBuffer);
```

### Type Changed: CoreMedia.CMMediaType

Removed value:

```
[Obsolete ("Use Metadata instead")]
	TimedMetadata = 1953326452,
```

### Type Changed: CoreMedia.CMSampleBuffer

Modified properties:

```
public CMTime PresentationTimeStamp { get; set; }
```

Removed methods:

```
[Obsolete ("Use GetAudioFormatDescription or GetVideoFormatDescription")]
	public CMFormatDescription GetFormatDescription ();
	public int Invalidate ();
	public int MakeDataReady ();
	public int SetDataBuffer (CMBlockBuffer dataBuffer);
	public int SetDataReady ();
	public int SetOutputPresentationTimeStamp (CMTime outputPresentationTimeStamp);
	public int TrackDataReadiness (CMSampleBuffer bufferToTrack);
```

Added methods:

```
public CMSampleBufferError Invalidate ();
	public CMSampleBufferError MakeDataReady ();
	public CMSampleBufferError SetDataBuffer (CMBlockBuffer dataBuffer);
	public CMSampleBufferError SetDataReady ();
	public CMSampleBufferError TrackDataReadiness (CMSampleBuffer bufferToTrack);
```

### Type Changed: CoreMedia.CMTime

Modified fields:

```
public readonly CMTime Indefinite;
	public readonly CMTime Invalid;
	public readonly CMTime NegativeInfinity;
	public readonly CMTime PositiveInfinity;
	public readonly CMTime Zero;
```

Removed property:

```
[Obsolete ("Use ToDictionary instead")]
	public IntPtr AsDictionary { get; }
```

Removed method:

```
[Obsolete ("Use FromDictionary (NSDictionary) instead")]
	public static CMTime FromDictionary (IntPtr dict);
```

### Type Changed: CoreMedia.CMVideoFormatDescription

Removed constructor:

```
public CMVideoFormatDescription (CMVideoCodecType codecType, System.Drawing.Size size);
```

Added constructor:

```
public CMVideoFormatDescription (CMVideoCodecType codecType, CMVideoDimensions size);
```

Modified properties:

```
public System.Drawing.Size CMVideoDimensions Dimensions { get; }
```

Added methods:

```
public static Foundation.NSObject[] GetExtensionKeysCommonWithImageBuffers ();
	public bool VideoMatchesImageBuffer (CoreVideo.CVImageBuffer imageBuffer);
```

### New Type CoreMedia.CMVideoDimensions

```
public struct CMVideoDimensions {
	// constructors
	public CMVideoDimensions (int width, int height);
	// fields
	public int Height;
	public int Width;
}
```

## Namespace CoreMidi



### Type Changed: CoreMidi.MidiClient

Removed interface:

```
ObjCRuntime.INativeObject
```

Removed method:

```
[Obsolete ("It is better to use CreateVirtualSource (string name, out MidiError statusCode) to flag errors")]
	public MidiEndpoint CreateVirtualSource (string name);
```

Modified methods:

```
public protected override void Dispose (bool disposing)
```

### Type Changed: CoreMidi.MidiDevice

Removed interface:

```
ObjCRuntime.INativeObject
```

### Type Changed: CoreMidi.MidiEndpoint

Removed interface:

```
ObjCRuntime.INativeObject
```

Modified properties:

```
public int bool IsBroadcast { get; set; }
```

Modified methods:

```
public protected override void Dispose (bool disposing)
```

### Type Changed: CoreMidi.MidiEntity

Removed interface:

```
ObjCRuntime.INativeObject
```

Modified properties:

```
public int bool IsBroadcast { get; set; }
```

### Type Changed: CoreMidi.MidiNetworkConnection

Modified constructors:

```
public protected MidiNetworkConnection (Foundation.NSObjectFlag t)
	public protected MidiNetworkConnection (IntPtr handle)
```

### Type Changed: CoreMidi.MidiNetworkHost

Modified constructors:

```
public protected MidiNetworkHost (Foundation.NSObjectFlag t)
	public protected MidiNetworkHost (IntPtr handle)
```

### Type Changed: CoreMidi.MidiNetworkSession

Modified constructors:

```
public protected MidiNetworkSession (Foundation.NSObjectFlag t)
	public protected MidiNetworkSession (IntPtr handle)
```

### Type Changed: CoreMidi.MidiObject

Removed constructor:

```
[Obsolete ("Use the (int) overload instead")]
	public MidiObject (IntPtr handle);
```

Removed interface:

```
ObjCRuntime.INativeObject
```

Modified properties:

```
public virtual final IntPtr int Handle { get; }
```

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: CoreMidi.MidiPort

Removed interface:

```
ObjCRuntime.INativeObject
```

Modified methods:

```
public protected override void Dispose (bool disposing)
```

## Namespace CoreMotion

### Type Changed: CoreMotion.CMAccelerometerData

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CMAccelerometerData ();
```

Modified constructors:

```
public protected CMAccelerometerData (Foundation.NSObjectFlag t)
	public protected CMAccelerometerData (IntPtr handle)
```

### Type Changed: CoreMotion.CMAltimeter

Modified constructors:

```
public protected CMAltimeter (Foundation.NSObjectFlag t)
	public protected CMAltimeter (IntPtr handle)
```

### Type Changed: CoreMotion.CMAltitudeData

Modified constructors:

```
public protected CMAltitudeData (Foundation.NSObjectFlag t)
	public protected CMAltitudeData (IntPtr handle)
```

### Type Changed: CoreMotion.CMAttitude

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CMAttitude ();
```

Modified constructors:

```
public protected CMAttitude (Foundation.NSObjectFlag t)
	public protected CMAttitude (IntPtr handle)
```

### Type Changed: CoreMotion.CMDeviceMotion

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CMDeviceMotion ();
```

Modified constructors:

```
public protected CMDeviceMotion (Foundation.NSObjectFlag t)
	public protected CMDeviceMotion (IntPtr handle)
```

### Type Changed: CoreMotion.CMGyroData

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CMGyroData ();
```

Modified constructors:

```
public protected CMGyroData (Foundation.NSObjectFlag t)
	public protected CMGyroData (IntPtr handle)
```

### Type Changed: CoreMotion.CMLogItem

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CMLogItem ();
```

Modified constructors:

```
public protected CMLogItem (Foundation.NSObjectFlag t)
	public protected CMLogItem (IntPtr handle)
```

### Type Changed: CoreMotion.CMMagnetometerData

Removed constructor:

```
[Obsolete ("This type is not meant to be created by application code")]
	public CMMagnetometerData ();
```

Modified constructors:

```
public protected CMMagnetometerData (Foundation.NSObjectFlag t)
	public protected CMMagnetometerData (IntPtr handle)
```

### Type Changed: CoreMotion.CMMotionActivity

Modified constructors:

```
public protected CMMotionActivity (Foundation.NSObjectFlag t)
	public protected CMMotionActivity (IntPtr handle)
```

### Type Changed: CoreMotion.CMMotionActivityManager

Modified constructors:

```
public protected CMMotionActivityManager (Foundation.NSObjectFlag t)
	public protected CMMotionActivityManager (IntPtr handle)
```

### Type Changed: CoreMotion.CMMotionManager

Modified constructors:

```
public protected CMMotionManager (Foundation.NSObjectFlag t)
	public protected CMMotionManager (IntPtr handle)
```

### Type Changed: CoreMotion.CMPedometer

Modified constructors:

```
public protected CMPedometer (Foundation.NSObjectFlag t)
	public protected CMPedometer (IntPtr handle)
```

### Type Changed: CoreMotion.CMPedometerData

Modified constructors:

```
public protected CMPedometerData (Foundation.NSObjectFlag t)
	public protected CMPedometerData (IntPtr handle)
```

### Type Changed: CoreMotion.CMStepCounter

Modified constructors:

```
public protected CMStepCounter (Foundation.NSObjectFlag t)
	public protected CMStepCounter (IntPtr handle)
```

## Namespace CoreTelephony

### Type Changed: CoreTelephony.CTCall

Modified constructors:

```
public protected CTCall (Foundation.NSObjectFlag t)
	public protected CTCall (IntPtr handle)
```

### Type Changed: CoreTelephony.CTCallCenter

Modified constructors:

```
public protected CTCallCenter (Foundation.NSObjectFlag t)
	public protected CTCallCenter (IntPtr handle)
```

Modified properties:

```
public virtual CTCallEventHandler System.Action<CTCall> CallEventHandler { get; set; }
```

### Type Changed: CoreTelephony.CTCarrier

Modified constructors:

```
public protected CTCarrier (Foundation.NSObjectFlag t)
	public protected CTCarrier (IntPtr handle)
```

### Type Changed: CoreTelephony.CTSubscriber

Modified constructors:

```
public protected CTSubscriber (Foundation.NSObjectFlag t)
	public protected CTSubscriber (IntPtr handle)
```

### Type Changed: CoreTelephony.CTSubscriberInfo

Modified constructors:

```
public protected CTSubscriberInfo (Foundation.NSObjectFlag t)
	public protected CTSubscriberInfo (IntPtr handle)
```

### Type Changed: CoreTelephony.CTTelephonyNetworkInfo

Modified constructors:

```
public protected CTTelephonyNetworkInfo (Foundation.NSObjectFlag t)
	public protected CTTelephonyNetworkInfo (IntPtr handle)
```

Modified properties:

```
public virtual CTCarrierEventHandler System.Action<CTCarrier> CellularProviderUpdatedEventHandler { get; set; }
```

### Removed Type CoreTelephony.CTCallEventHandler ### Removed Type CoreTelephony.CTCarrierEventHandler 



## Namespace CoreText

### Type Changed: CoreText.CTFontDescriptor

Removed methods:

```
[Obsolete ("Use WithFeature with specific selector")]
	public CTFontDescriptor WithFeature (Foundation.NSNumber featureTypeIdentifier, Foundation.NSNumber featureSelectorIdentifier);

	[Obsolete ("Deprecated")]
	public CTFontDescriptor WithFeature (CTFontFeatureLetterCase.Selector featureSelector);
```

### Type Changed: CoreText.CTFontDescriptorAttributes

Modified properties:

```
public Foundation.NSNumber CTFontManagerScope? RegistrationScope { get; set; }
```

### Type Changed: CoreText.CTFontFeatureKey

Removed constructor:

```
public CTFontFeatureKey ();
```

### Type Changed: CoreText.CTFontFeatures

Removed property:

```
[Obsolete ("Use FeatureGroup property instead")]
	public Foundation.NSNumber Identifier { get; set; }
```

### Type Changed: CoreText.CTFontFeatureSelectorKey

Removed constructor:

```
public CTFontFeatureSelectorKey ();
```

### Type Changed: CoreText.CTFontFeatureSelectors

Removed property:

```
[Obsolete ("Use one of descendant classes")]
	public Foundation.NSNumber Identifier { get; set; }
```

### Type Changed: CoreText.CTFontFeatureSettings

Removed constructor:

```
public CTFontFeatureSettings (Foundation.NSDictionary dictionary);
```

Removed properties:

```
[Obsolete ("Use FeatureWeak or FeatureGroup instead")]
	public Foundation.NSNumber SelectorIdentifier { get; set; }

	[Obsolete ("Use FeatureGroup property instead")]
	public Foundation.NSNumber TypeIdentifier { get; set; }
```

### Type Changed: CoreText.CTRunDelegateOperations

Modified methods:

```
public virtual virtual final void Dispose ()
```

Added methods:

```
protected override void ~CTRunDelegateOperations ();
	protected virtual void Dispose (bool disposing);
```

## Namespace CoreVideo

### Type Changed: CoreVideo.CVBuffer

Removed fields:

```
public static Foundation.NSString MovieTimeKey;
	public static Foundation.NSString NonPropagatedAttachmentsKey;
	public static Foundation.NSString PropagatedAttachmentsKey;
	public static Foundation.NSString TimeScaleKey;
	public static Foundation.NSString TimeValueKey;
```

Added properties:

```
public static Foundation.NSString MovieTimeKey { get; }
	public static Foundation.NSString NonPropagatedAttachmentsKey { get; }
	public static Foundation.NSString PropagatedAttachmentsKey { get; }
	public static Foundation.NSString TimeScaleKey { get; }
	public static Foundation.NSString TimeValueKey { get; }
```

Removed methods:

```
public Foundation.NSObject GetAttachment (Foundation.NSString key, out CVAttachmentMode attachmentMode);
	public void SetAttachment (Foundation.NSString key, Foundation.NSObject value, CVAttachmentMode attachmentMode);
```

Added methods:

```
public T GetAttachment<T> (Foundation.NSString key, out CVAttachmentMode attachmentMode);
	public void SetAttachment (Foundation.NSString key, ObjCRuntime.INativeObject value, CVAttachmentMode attachmentMode);
```

### Type Changed: CoreVideo.CVImageBuffer

Removed fields:

```
public static Foundation.NSString AlphaChannelIsOpaque;
	public static Foundation.NSString CGColorSpaceKey;
	public static Foundation.NSString ChromaLocation_Bottom;
	public static Foundation.NSString ChromaLocation_BottomLeft;
	public static Foundation.NSString ChromaLocation_Center;
	public static Foundation.NSString ChromaLocation_DV420;
	public static Foundation.NSString ChromaLocation_Left;
	public static Foundation.NSString ChromaLocation_Top;
	public static Foundation.NSString ChromaLocation_TopLeft;
	public static Foundation.NSString ChromaLocationBottomFieldKey;
	public static Foundation.NSString ChromaLocationTopFieldKey;
	public static Foundation.NSString ChromaSubsampling_411;
	public static Foundation.NSString ChromaSubsampling_420;
	public static Foundation.NSString ChromaSubsampling_422;
	public static Foundation.NSString ChromaSubsamplingKey;
	public static Foundation.NSString CleanApertureHeightKey;
	public static Foundation.NSString CleanApertureHorizontalOffsetKey;
	public static Foundation.NSString CleanApertureKey;
	public static Foundation.NSString CleanApertureVerticalOffsetKey;
	public static Foundation.NSString CleanApertureWidthKey;
	public static Foundation.NSString DisplayDimensionsKey;
	public static Foundation.NSString DisplayHeightKey;
	public static Foundation.NSString DisplayWidthKey;
	public static Foundation.NSString FieldCountKey;
	public static Foundation.NSString FieldDetailKey;
	public static Foundation.NSString FieldDetailSpatialFirstLineEarly;
	public static Foundation.NSString FieldDetailSpatialFirstLineLate;
	public static Foundation.NSString FieldDetailTemporalBottomFirst;
	public static Foundation.NSString FieldDetailTemporalTopFirst;
	public static Foundation.NSString GammaLevelKey;
	public static Foundation.NSString PixelAspectRatioHorizontalSpacingKey;
	public static Foundation.NSString PixelAspectRatioKey;
	public static Foundation.NSString PixelAspectRatioVerticalSpacingKey;
	public static Foundation.NSString PreferredCleanApertureKey;
	public static Foundation.NSString TransferFunction_ITU_R_709_2;
	public static Foundation.NSString TransferFunction_SMPTE_240M_1995;
	public static Foundation.NSString TransferFunction_UseGamma;
	public static Foundation.NSString TransferFunctionKey;
	public static Foundation.NSString YCbCrMatrix_ITU_R_601_4;
	public static Foundation.NSString YCbCrMatrix_ITU_R_709_2;
	public static Foundation.NSString YCbCrMatrix_SMPTE_240M_1995;
	public static Foundation.NSString YCbCrMatrixKey;
```

Added properties:

```
public static Foundation.NSString AlphaChannelIsOpaque { get; }
	public static Foundation.NSString CGColorSpaceKey { get; }
	public static Foundation.NSString ChromaLocation_Bottom { get; }
	public static Foundation.NSString ChromaLocation_BottomLeft { get; }
	public static Foundation.NSString ChromaLocation_Center { get; }
	public static Foundation.NSString ChromaLocation_DV420 { get; }
	public static Foundation.NSString ChromaLocation_Left { get; }
	public static Foundation.NSString ChromaLocation_Top { get; }
	public static Foundation.NSString ChromaLocation_TopLeft { get; }
	public static Foundation.NSString ChromaLocationBottomFieldKey { get; }
	public static Foundation.NSString ChromaLocationTopFieldKey { get; }
	public static Foundation.NSString ChromaSubsampling_411 { get; }
	public static Foundation.NSString ChromaSubsampling_420 { get; }
	public static Foundation.NSString ChromaSubsampling_422 { get; }
	public static Foundation.NSString ChromaSubsamplingKey { get; }
	public static Foundation.NSString CleanApertureHeightKey { get; }
	public static Foundation.NSString CleanApertureHorizontalOffsetKey { get; }
	public static Foundation.NSString CleanApertureKey { get; }
	public static Foundation.NSString CleanApertureVerticalOffsetKey { get; }
	public static Foundation.NSString CleanApertureWidthKey { get; }
	public static Foundation.NSString DisplayDimensionsKey { get; }
	public static Foundation.NSString DisplayHeightKey { get; }
	public static Foundation.NSString DisplayWidthKey { get; }
	public static Foundation.NSString FieldCountKey { get; }
	public static Foundation.NSString FieldDetailKey { get; }
	public static Foundation.NSString FieldDetailSpatialFirstLineEarly { get; }
	public static Foundation.NSString FieldDetailSpatialFirstLineLate { get; }
	public static Foundation.NSString FieldDetailTemporalBottomFirst { get; }
	public static Foundation.NSString FieldDetailTemporalTopFirst { get; }
	public static Foundation.NSString GammaLevelKey { get; }
	public static Foundation.NSString MovieTimeKey { get; }
	public static Foundation.NSString NonPropagatedAttachmentsKey { get; }
	public static Foundation.NSString PixelAspectRatioHorizontalSpacingKey { get; }
	public static Foundation.NSString PixelAspectRatioKey { get; }
	public static Foundation.NSString PixelAspectRatioVerticalSpacingKey { get; }
	public static Foundation.NSString PreferredCleanApertureKey { get; }
	public static Foundation.NSString PropagatedAttachmentsKey { get; }
	public static Foundation.NSString TimeScaleKey { get; }
	public static Foundation.NSString TimeValueKey { get; }
	public static Foundation.NSString TransferFunction_ITU_R_709_2 { get; }
	public static Foundation.NSString TransferFunction_SMPTE_240M_1995 { get; }
	public static Foundation.NSString TransferFunction_UseGamma { get; }
	public static Foundation.NSString TransferFunctionKey { get; }
	public static Foundation.NSString YCbCrMatrix_ITU_R_601_4 { get; }
	public static Foundation.NSString YCbCrMatrix_ITU_R_709_2 { get; }
	public static Foundation.NSString YCbCrMatrix_SMPTE_240M_1995 { get; }
	public static Foundation.NSString YCbCrMatrixKey { get; }
```

### Type Changed: CoreVideo.CVPixelBuffer

Removed constructors:

```
public CVPixelBuffer (System.Drawing.Size size, CVPixelFormatType pixelFormat);
	public CVPixelBuffer (System.Drawing.Size size, CVPixelFormatType pixelFormatType, CVPixelBufferAttributes attributes);

	[Obsolete ("Use constructor with CVPixelBufferAttributes")]
	public CVPixelBuffer (int width, int height, CVPixelFormatType pixelFormatType, Foundation.NSDictionary pixelBufferAttributes);
```

Removed fields:

```
public static Foundation.NSString BytesPerRowAlignmentKey;
	public static Foundation.NSString CGBitmapContextCompatibilityKey;
	public static Foundation.NSString CGImageCompatibilityKey;
	public static int CVImageBufferType;
	public static Foundation.NSString ExtendedPixelsBottomKey;
	public static Foundation.NSString ExtendedPixelsLeftKey;
	public static Foundation.NSString ExtendedPixelsRightKey;
	public static Foundation.NSString ExtendedPixelsTopKey;
	public static Foundation.NSString HeightKey;
	public static Foundation.NSString IOSurfacePropertiesKey;
	public static Foundation.NSString MemoryAllocatorKey;
	public static Foundation.NSString MetalCompatibilityKey;
	public static Foundation.NSString OpenGLCompatibilityKey;
	public static Foundation.NSString OpenGLESCompatibilityKey;
	public static Foundation.NSString PixelFormatTypeKey;
	public static Foundation.NSString PlaneAlignmentKey;
	public static Foundation.NSString WidthKey;
```

Added properties:

```
public static Foundation.NSString BytesPerRowAlignmentKey { get; }
	public static Foundation.NSString CGBitmapContextCompatibilityKey { get; }
	public static Foundation.NSString CGImageCompatibilityKey { get; }
	public static Foundation.NSString ExtendedPixelsBottomKey { get; }
	public static Foundation.NSString ExtendedPixelsLeftKey { get; }
	public static Foundation.NSString ExtendedPixelsRightKey { get; }
	public static Foundation.NSString ExtendedPixelsTopKey { get; }
	public static Foundation.NSString HeightKey { get; }
	public static Foundation.NSString IOSurfacePropertiesKey { get; }
	public static Foundation.NSString MemoryAllocatorKey { get; }
	public static Foundation.NSString MetalCompatibilityKey { get; }
	public static Foundation.NSString OpenGLCompatibilityKey { get; }
	public static Foundation.NSString OpenGLESCompatibilityKey { get; }
	public static Foundation.NSString PixelFormatTypeKey { get; }
	public static Foundation.NSString PlaneAlignmentKey { get; }
	public static Foundation.NSString WidthKey { get; }
```

### Type Changed: CoreVideo.CVPixelBufferAttributes

Removed constructor:

```
public CVPixelBufferAttributes (CVPixelFormatType pixelFormatType, System.Drawing.Size size);
```

### Type Changed: CoreVideo.CVPixelBufferPool

Removed fields:

```
public static Foundation.NSString MaximumBufferAgeKey;
	public static Foundation.NSString MinimumBufferCountKey;
```

Added properties:

```
public static Foundation.NSString AlphaChannelIsOpaque { get; }
	public static Foundation.NSString CGColorSpaceKey { get; }
	public static Foundation.NSString ChromaLocation_Bottom { get; }
	public static Foundation.NSString ChromaLocation_BottomLeft { get; }
	public static Foundation.NSString ChromaLocation_Center { get; }
	public static Foundation.NSString ChromaLocation_DV420 { get; }
	public static Foundation.NSString ChromaLocation_Left { get; }
	public static Foundation.NSString ChromaLocation_Top { get; }
	public static Foundation.NSString ChromaLocation_TopLeft { get; }
	public static Foundation.NSString ChromaLocationBottomFieldKey { get; }
	public static Foundation.NSString ChromaLocationTopFieldKey { get; }
	public static Foundation.NSString ChromaSubsampling_411 { get; }
	public static Foundation.NSString ChromaSubsampling_420 { get; }
	public static Foundation.NSString ChromaSubsampling_422 { get; }
	public static Foundation.NSString ChromaSubsamplingKey { get; }
	public static Foundation.NSString CleanApertureHeightKey { get; }
	public static Foundation.NSString CleanApertureHorizontalOffsetKey { get; }
	public static Foundation.NSString CleanApertureKey { get; }
	public static Foundation.NSString CleanApertureVerticalOffsetKey { get; }
	public static Foundation.NSString CleanApertureWidthKey { get; }
	public static Foundation.NSString DisplayDimensionsKey { get; }
	public static Foundation.NSString DisplayHeightKey { get; }
	public static Foundation.NSString DisplayWidthKey { get; }
	public static Foundation.NSString FieldCountKey { get; }
	public static Foundation.NSString FieldDetailKey { get; }
	public static Foundation.NSString FieldDetailSpatialFirstLineEarly { get; }
	public static Foundation.NSString FieldDetailSpatialFirstLineLate { get; }
	public static Foundation.NSString FieldDetailTemporalBottomFirst { get; }
	public static Foundation.NSString FieldDetailTemporalTopFirst { get; }
	public static Foundation.NSString GammaLevelKey { get; }
	public static Foundation.NSString MaximumBufferAgeKey { get; }
	public static Foundation.NSString MinimumBufferCountKey { get; }
	public static Foundation.NSString MovieTimeKey { get; }
	public static Foundation.NSString NonPropagatedAttachmentsKey { get; }
	public static Foundation.NSString PixelAspectRatioHorizontalSpacingKey { get; }
	public static Foundation.NSString PixelAspectRatioKey { get; }
	public static Foundation.NSString PixelAspectRatioVerticalSpacingKey { get; }
	public static Foundation.NSString PreferredCleanApertureKey { get; }
	public static Foundation.NSString PropagatedAttachmentsKey { get; }
	public static Foundation.NSString TimeScaleKey { get; }
	public static Foundation.NSString TimeValueKey { get; }
	public static Foundation.NSString TransferFunction_ITU_R_709_2 { get; }
	public static Foundation.NSString TransferFunction_SMPTE_240M_1995 { get; }
	public static Foundation.NSString TransferFunction_UseGamma { get; }
	public static Foundation.NSString TransferFunctionKey { get; }
	public static Foundation.NSString YCbCrMatrix_ITU_R_601_4 { get; }
	public static Foundation.NSString YCbCrMatrix_ITU_R_709_2 { get; }
	public static Foundation.NSString YCbCrMatrix_SMPTE_240M_1995 { get; }
	public static Foundation.NSString YCbCrMatrixKey { get; }
```

### Type Changed: CoreVideo.CVTime

Removed methods:

```
public static long GetCurrentHostTime ();
	public static int GetHostClockMinimumTimeDelta ();
```

Added methods:

```
public static ulong GetCurrentHostTime ();
	public static uint GetHostClockMinimumTimeDelta ();
```

## Namespace EventKit

### Type Changed: EventKit.EKAlarm

Modified constructors:

```
public protected EKAlarm (Foundation.NSObjectFlag t)
	public protected EKAlarm (IntPtr handle)
```

### Type Changed: EventKit.EKCalendar

Modified constructors:

```
public protected EKCalendar (Foundation.NSObjectFlag t)
	public protected EKCalendar (IntPtr handle)
```

### Type Changed: EventKit.EKCalendarItem

Modified constructors:

```
public protected EKCalendarItem (Foundation.NSObjectFlag t)
	public protected EKCalendarItem (IntPtr handle)
```

### Type Changed: EventKit.EKEvent

Modified constructors:

```
public protected EKEvent (Foundation.NSObjectFlag t)
	public protected EKEvent (IntPtr handle)
```

Removed property:

```
[Obsolete ("Removed in iOS 6.0")]
	public virtual EKRecurrenceRule RecurrenceRule { get; set; }
```

### Type Changed: EventKit.EKEventStore

Modified constructors:

```
public protected EKEventStore (Foundation.NSObjectFlag t)
	public protected EKEventStore (IntPtr handle)
```

Removed methods:

```
[Obsolete ("Replaced by RemoveCalendar")]
	public bool RemoveCalendarc (EKCalendar calendar, bool commit, out Foundation.NSError error);
	public virtual System.Threading.Tasks.Task<bool> RequestAccessAsync (EKEntityType entityType);
```

Added method:

```
public virtual System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> RequestAccessAsync (EKEntityType entityType);
```

### Type Changed: EventKit.EKObject

Modified constructors:

```
public protected EKObject ()
	public protected EKObject (Foundation.NSObjectFlag t)
	public protected EKObject (IntPtr handle)
```

### Type Changed: EventKit.EKParticipant

Modified constructors:

```
public protected EKParticipant (Foundation.NSObjectFlag t)
	public protected EKParticipant (IntPtr handle)
```

### Type Changed: EventKit.EKRecurrenceDayOfWeek

Modified constructors:

```
public protected EKRecurrenceDayOfWeek (Foundation.NSObjectFlag t)
	public protected EKRecurrenceDayOfWeek (IntPtr handle)
```

### Type Changed: EventKit.EKRecurrenceEnd

Modified constructors:

```
public protected EKRecurrenceEnd (Foundation.NSObjectFlag t)
	public protected EKRecurrenceEnd (IntPtr handle)
```

### Type Changed: EventKit.EKRecurrenceRule

Modified constructors:

```
public protected EKRecurrenceRule (Foundation.NSObjectFlag t)
	public protected EKRecurrenceRule (IntPtr handle)
```

Modified properties:

```
public virtual EKDay FirstDayOfTheWeek { get; }
```

### Type Changed: EventKit.EKReminder

Modified constructors:

```
public protected EKReminder (Foundation.NSObjectFlag t)
	public protected EKReminder (IntPtr handle)
```

### Type Changed: EventKit.EKSource

Modified constructors:

```
public protected EKSource (Foundation.NSObjectFlag t)
	public protected EKSource (IntPtr handle)
```

### Type Changed: EventKit.EKStructuredLocation

Modified constructors:

```
public protected EKStructuredLocation (Foundation.NSObjectFlag t)
	public protected EKStructuredLocation (IntPtr handle)
```

### Removed Type EventKit.EKEventEditViewAction ### Removed Type EventKit.EKEventViewAction 



## Namespace EventKitUI

### Type Changed: EventKitUI.EKCalendarChooser

Modified constructors:

```
public protected EKCalendarChooser (Foundation.NSObjectFlag t)
	public protected EKCalendarChooser (IntPtr handle)
```

Modified properties:

```
public EKCalendarChooserDelegate IEKCalendarChooserDelegate Delegate { get; set; }
```

### Type Changed: EventKitUI.EKCalendarChooserDelegate

Modified constructors:

```
public protected EKCalendarChooserDelegate (Foundation.NSObjectFlag t)
	public protected EKCalendarChooserDelegate (IntPtr handle)
```

### Type Changed: EventKitUI.EKEventEditEventArgs

Removed constructor:

```
public EKEventEditEventArgs (EventKit.EKEventEditViewAction action);
```

Added constructor:

```
public EKEventEditEventArgs (EKEventEditViewAction action);
```

Modified properties:

```
public EventKit.EKEventEditViewAction EKEventEditViewAction Action { get; set; }
```

### Type Changed: EventKitUI.EKEventEditViewController

Modified constructors:

```
public protected EKEventEditViewController (Foundation.NSObjectFlag t)
	public protected EKEventEditViewController (IntPtr handle)
```

Modified properties:

```
public EKEventEditViewDelegate IEKEventEditViewDelegate EditViewDelegate { get; set; }
```

### Type Changed: EventKitUI.EKEventEditViewDelegate

Modified constructors:

```
public protected EKEventEditViewDelegate ()
	public protected EKEventEditViewDelegate (Foundation.NSObjectFlag t)
	public protected EKEventEditViewDelegate (IntPtr handle)
```

Removed method:

```
public virtual void Completed (EKEventEditViewController controller, EventKit.EKEventEditViewAction action);
```

Added method:

```
public virtual void Completed (EKEventEditViewController controller, EKEventEditViewAction action);
```

### Type Changed: EventKitUI.EKEventViewController

Modified constructors:

```
public protected EKEventViewController (Foundation.NSObjectFlag t)
	public protected EKEventViewController (IntPtr handle)
```

Modified properties:

```
public EKEventViewDelegate IEKEventViewDelegate Delegate { get; set; }
```

### Type Changed: EventKitUI.EKEventViewDelegate

Modified constructors:

```
public protected EKEventViewDelegate ()
	public protected EKEventViewDelegate (Foundation.NSObjectFlag t)
	public protected EKEventViewDelegate (IntPtr handle)
```

Removed method:

```
public virtual void Completed (EKEventViewController controller, EventKit.EKEventViewAction action);
```

Added method:

```
public virtual void Completed (EKEventViewController controller, EKEventViewAction action);
```

### Type Changed: EventKitUI.EKEventViewEventArgs

Removed constructor:

```
public EKEventViewEventArgs (EventKit.EKEventViewAction action);
```

Added constructor:

```
public EKEventViewEventArgs (EKEventViewAction action);
```

Modified properties:

```
public EventKit.EKEventViewAction EKEventViewAction Action { get; set; }
```

### Type Changed: EventKitUI.IEKEventEditViewDelegate

Removed method:

```
public virtual void Completed (EKEventEditViewController controller, EventKit.EKEventEditViewAction action);
```

Added method:

```
public virtual void Completed (EKEventEditViewController controller, EKEventEditViewAction action);
```

### Type Changed: EventKitUI.IEKEventViewDelegate

Removed method:

```
public virtual void Completed (EKEventViewController controller, EventKit.EKEventViewAction action);
```

Added method:

```
public virtual void Completed (EKEventViewController controller, EKEventViewAction action);
```

### Removed Type EventKitUI.EKEventViewDelegate_Extensions ### New Type EventKitUI.EKEventEditViewAction

```
[Serializable]
public enum EKEventEditViewAction {
	Canceled = 0,
	Deleted = 2,
	Saved = 1,
}
```

### New Type EventKitUI.EKEventViewAction

```
[Serializable]
public enum EKEventViewAction {
	Deleted = 2,
	Done = 0,
	Responded = 1,
}
```



## Namespace ExternalAccessory

### Type Changed: ExternalAccessory.EAAccessory

Modified constructors:

```
public protected EAAccessory (Foundation.NSObjectFlag t)
	public protected EAAccessory (IntPtr handle)
```

Modified properties:

```
public EAAccessoryDelegate IEAAccessoryDelegate Delegate { get; set; }
```

### Type Changed: ExternalAccessory.EAAccessoryDelegate

Modified constructors:

```
public protected EAAccessoryDelegate (Foundation.NSObjectFlag t)
	public protected EAAccessoryDelegate (IntPtr handle)
```

### Type Changed: ExternalAccessory.EAAccessoryManager

Modified constructors:

```
public protected EAAccessoryManager (Foundation.NSObjectFlag t)
	public protected EAAccessoryManager (IntPtr handle)
```

### Type Changed: ExternalAccessory.EASession

Modified constructors:

```
public protected EASession (Foundation.NSObjectFlag t)
	public protected EASession (IntPtr handle)
```

### Type Changed: ExternalAccessory.EAWiFiUnconfiguredAccessory

Modified constructors:

```
public protected EAWiFiUnconfiguredAccessory (Foundation.NSObjectFlag t)
	public protected EAWiFiUnconfiguredAccessory (IntPtr handle)
```

### Type Changed: ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowser

Modified constructors:

```
public protected EAWiFiUnconfiguredAccessoryBrowser (Foundation.NSObjectFlag t)
	public protected EAWiFiUnconfiguredAccessoryBrowser (IntPtr handle)
```

Modified properties:

```
public EAWiFiUnconfiguredAccessoryBrowserDelegate IEAWiFiUnconfiguredAccessoryBrowserDelegate Delegate { get; set; }
```

### Type Changed: ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserDelegate

Modified constructors:

```
public protected EAWiFiUnconfiguredAccessoryBrowserDelegate ()
	public protected EAWiFiUnconfiguredAccessoryBrowserDelegate (Foundation.NSObjectFlag t)
	public protected EAWiFiUnconfiguredAccessoryBrowserDelegate (IntPtr handle)
```

Modified methods:

```
public abstract void DidFindUnconfiguredAccessories (EAWiFiUnconfiguredAccessoryBrowser browser, Foundation.NSSet accessories)
	public abstract void DidFinishConfiguringAccessory (EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessory accessory, EAWiFiUnconfiguredAccessoryConfigurationStatus status)
	public abstract void DidRemoveUnconfiguredAccessories (EAWiFiUnconfiguredAccessoryBrowser browser, Foundation.NSSet accessories)
	public abstract void DidUpdateState (EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessoryBrowserState state)
```

### Type Changed: ExternalAccessory.IEAWiFiUnconfiguredAccessoryBrowserDelegate

Added methods:

```
public virtual void DidFindUnconfiguredAccessories (EAWiFiUnconfiguredAccessoryBrowser browser, Foundation.NSSet accessories);
	public virtual void DidFinishConfiguringAccessory (EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessory accessory, EAWiFiUnconfiguredAccessoryConfigurationStatus status);
	public virtual void DidRemoveUnconfiguredAccessories (EAWiFiUnconfiguredAccessoryBrowser browser, Foundation.NSSet accessories);
	public virtual void DidUpdateState (EAWiFiUnconfiguredAccessoryBrowser browser, EAWiFiUnconfiguredAccessoryBrowserState state);
```

### Removed Type ExternalAccessory.EAWiFiUnconfiguredAccessoryBrowserDelegate_Extensions 

## Namespace Foundation

### Type Changed: Foundation.DictionaryContainer

Added methods:

```
protected void SetNumberValue (NSString key, uint? value);
	protected void SetNumberValue (NSString key, int? value);
```

### Type Changed: Foundation.ExportAttribute

Modified constructors:

```
public protected ExportAttribute ()
```

### Type Changed: Foundation.INSCopying

Added method:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: Foundation.INSFilePresenter

Added property:

```
public virtual NSOperationQueue PesentedItemOperationQueue { get; }
```

### Type Changed: Foundation.INSMutableCopying

Added method:

```
public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: Foundation.INSObjectProtocol

Modified properties:

```
public abstract int uint RetainCount { get; }
```

### Type Changed: Foundation.INSURLAuthenticationChallengeSender

Removed methods:

```
public virtual void ContinueWithoutCredentialForAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void RejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void UseCredentials (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
```

Added methods:

```
public virtual void ContinueWithoutCredential (NSUrlAuthenticationChallenge challenge);
	public virtual void UseCredential (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
```

### Type Changed: Foundation.INSUrlSessionDownloadDelegate

Added method:

```
public virtual void DidFinishDownloading (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, NSUrl location);
```

### Type Changed: Foundation.NSArray

Modified constructors:

```
public protected NSArray (NSObjectFlag t)
	public protected NSArray (IntPtr handle)
```

Removed method:

```
public T GetItem<T> (int index);
```

Added methods:

```
public T GetItem<T> (uint index);
```

### Type Changed: Foundation.NSAttributedString

Modified constructors:

```
public protected NSAttributedString (IntPtr handle)
	public protected NSAttributedString (NSObjectFlag t)
```

### Type Changed: Foundation.NSAutoreleasePool

Removed method:

```
protected override void Dispose (bool disposing);
```

### Type Changed: Foundation.NSBlockOperation

Modified constructors:

```
public protected NSBlockOperation (NSObjectFlag t)
	public protected NSBlockOperation (IntPtr handle)
```

Removed methods:

```
public virtual void AddExecutionBlock (NSAction method);
	public static NSBlockOperation Create (NSAction method);
```

Added methods:

```
public virtual void AddExecutionBlock (System.Action method);
	public static NSBlockOperation Create (System.Action method);
```

### Type Changed: Foundation.NSBundle

Modified constructors:

```
public protected NSBundle (NSObjectFlag t)
	public protected NSBundle (IntPtr handle)
```

### Type Changed: Foundation.NSByteCountFormatter

Modified constructors:

```
public protected NSByteCountFormatter (NSObjectFlag t)
	public protected NSByteCountFormatter (IntPtr handle)
```

### Type Changed: Foundation.NSCache

Modified constructors:

```
public protected NSCache (NSObjectFlag t)
	public protected NSCache (IntPtr handle)
```

Modified properties:

```
public NSCacheDelegate INSCacheDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSCacheDelegate

Modified constructors:

```
public protected NSCacheDelegate (NSObjectFlag t)
	public protected NSCacheDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSCachedUrlResponse

Modified constructors:

```
public protected NSCachedUrlResponse (NSObjectFlag t)
	public protected NSCachedUrlResponse (IntPtr handle)
```

### Type Changed: Foundation.NSCalendar

Modified constructors:

```
public protected NSCalendar (NSObjectFlag t)
	public protected NSCalendar (IntPtr handle)
```

### Type Changed: Foundation.NSCharacterSet

Modified constructors:

```
public protected NSCharacterSet (NSObjectFlag t)
	public protected NSCharacterSet (IntPtr handle)
```

### Type Changed: Foundation.NSCoder

Modified constructors:

```
public protected NSCoder (NSObjectFlag t)
	public protected NSCoder (IntPtr handle)
```

Added methods:

```
public virtual int DecodeNInt (string key);
	public virtual void Encode (int val, string key);
```

### Type Changed: Foundation.NSCoding

Modified constructors:

```
public protected NSCoding ()
	public NSCoding (NSCoder coder decoder)
	public protected NSCoding (NSObjectFlag t)
	public protected NSCoding (IntPtr handle)
```

### Type Changed: Foundation.NSComparator

Removed methods:

```
public virtual int EndInvoke (System.IAsyncResult result);
	public virtual int Invoke (NSObject obj1, NSObject obj2);
```

Added methods:

```
public virtual NSComparisonResult EndInvoke (System.IAsyncResult result);
	public virtual NSComparisonResult Invoke (NSObject obj1, NSObject obj2);
```

### Type Changed: Foundation.NSComparisonPredicate

Modified constructors:

```
public protected NSComparisonPredicate (NSObjectFlag t)
	public protected NSComparisonPredicate (IntPtr handle)
```

### Type Changed: Foundation.NSCompoundPredicate

Removed constructor:

```
[Obsolete ("This instance of NSCompoundPredicate will be unusable. Symbol kept for binary compatibility")]
	public NSCompoundPredicate ();
```

Modified constructors:

```
public protected NSCompoundPredicate (NSObjectFlag t)
	public protected NSCompoundPredicate (IntPtr handle)
```

### Type Changed: Foundation.NSCopying

Modified constructors:

```
public protected NSCopying ()
	public protected NSCopying (NSObjectFlag t)
	public protected NSCopying (IntPtr handle)
```

Modified methods:

```
public abstract NSObject Copy (NSZone zone)
```

### Type Changed: Foundation.NSData

Modified constructors:

```
public protected NSData (NSObjectFlag t)
	public protected NSData (IntPtr handle)
```

Removed methods:

```
public virtual bool _Save (string file, int options, IntPtr addr);
	public virtual bool _Save (NSUrl url, int options, IntPtr addr);
```

### Type Changed: Foundation.NSDataWritingOptions

Removed value:

```
[Obsolete ("No longer available")]
	Coordinated = 4,
```

### Type Changed: Foundation.NSDate

Modified constructors:

```
public protected NSDate (NSObjectFlag t)
	public protected NSDate (IntPtr handle)
```

Removed methods:

```
public static NSDate op_Implicit (System.DateTime dt);
	public static System.DateTime op_Implicit (NSDate d);
	public override string ToString ();
```

Added methods:

```
public static NSDate op_Explicit (System.DateTime dt);
	public static System.DateTime op_Explicit (NSDate d);
```

### Type Changed: Foundation.NSDateComponents

Modified constructors:

```
public protected NSDateComponents (NSObjectFlag t)
	public protected NSDateComponents (IntPtr handle)
```

### Type Changed: Foundation.NSDateComponentsFormatter

Modified constructors:

```
public protected NSDateComponentsFormatter (NSObjectFlag t)
	public protected NSDateComponentsFormatter (IntPtr handle)
```

### Type Changed: Foundation.NSDateFormatter

Modified constructors:

```
public protected NSDateFormatter (NSObjectFlag t)
	public protected NSDateFormatter (IntPtr handle)
```

### Type Changed: Foundation.NSDateIntervalFormatter

Modified constructors:

```
public protected NSDateIntervalFormatter (NSObjectFlag t)
	public protected NSDateIntervalFormatter (IntPtr handle)
```

### Type Changed: Foundation.NSDecimal

Removed methods:

```
public static NSComparisonResult MultiplyByPowerOf10 (out NSDecimal result, ref NSDecimal number, short power10, NSRoundingMode mode);
	public static NSComparisonResult Power (out NSDecimal result, ref NSDecimal number, int power, NSRoundingMode mode);
```

Added methods:

```
public static NSCalculationError MultiplyByPowerOf10 (out NSDecimal result, ref NSDecimal number, short power10, NSRoundingMode mode);
	public static NSCalculationError Power (out NSDecimal result, ref NSDecimal number, int power, NSRoundingMode mode);
```

### Type Changed: Foundation.NSDecimalNumber

Modified constructors:

```
public protected NSDecimalNumber (IntPtr handle)
	public protected NSDecimalNumber (NSObjectFlag t)
```

### Type Changed: Foundation.NSDictionary

Modified constructors:

```
public protected NSDictionary (IntPtr handle)
	public protected NSDictionary (NSObjectFlag t)
```

### Type Changed: Foundation.NSDirectoryEnumerator

Modified constructors:

```
public protected NSDirectoryEnumerator (NSObjectFlag t)
	public protected NSDirectoryEnumerator (IntPtr handle)
```

### Type Changed: Foundation.NSEnergyFormatter

Modified constructors:

```
public protected NSEnergyFormatter (NSObjectFlag t)
	public protected NSEnergyFormatter (IntPtr handle)
```

### Type Changed: Foundation.NSEnumerator

Modified constructors:

```
public protected NSEnumerator (NSObjectFlag t)
	public protected NSEnumerator (IntPtr handle)
```

### Type Changed: Foundation.NSError

Modified constructors:

```
public protected NSError (NSObjectFlag t)
	public protected NSError (IntPtr handle)
```

### Type Changed: Foundation.NSException

Modified constructors:

```
public protected NSException (NSObjectFlag t)
	public protected NSException (IntPtr handle)
```

### Type Changed: Foundation.NSExpression

Modified constructors:

```
public protected NSExpression (NSObjectFlag t)
	public protected NSExpression (IntPtr handle)
```

### Type Changed: Foundation.NSExtensionContext

Modified constructors:

```
public protected NSExtensionContext (NSObjectFlag t)
	public protected NSExtensionContext (IntPtr handle)
```

### Type Changed: Foundation.NSExtensionItem

Modified constructors:

```
public protected NSExtensionItem (NSObjectFlag t)
	public protected NSExtensionItem (IntPtr handle)
```

### Type Changed: Foundation.NSExtensionRequestHandling

Modified constructors:

```
public protected NSExtensionRequestHandling ()
	public protected NSExtensionRequestHandling (NSObjectFlag t)
	public protected NSExtensionRequestHandling (IntPtr handle)
```

### Type Changed: Foundation.NSFileAccessIntent

Modified constructors:

```
public protected NSFileAccessIntent (NSObjectFlag t)
	public protected NSFileAccessIntent (IntPtr handle)
```

### Type Changed: Foundation.NSFileAttributes

Removed properties:

```
[Obsolete ("Use ExtensionHidden instead")]
	public bool? FileExtensionHidden { get; set; }

	[Obsolete ("Use GroupOwnerAccountID instead")]
	public uint? FileGroupOwnerAccountID { get; set; }

	[Obsolete ("Use GroupOwnerAccountID instead")]
	public uint? FileOwnerAccountID { get; set; }

	[Obsolete ("Use ReferenceCount instead")]
	public uint? FileReferenceCount { get; set; }

	[Obsolete ("Use Size instead")]
	public ulong? FileSize { get; set; }

	[Obsolete ("Use SystemFileNumber instead")]
	public uint? FileSystemFileNumber { get; set; }

	[Obsolete ("Use Type instead")]
	public NSFileType? FileType { get; set; }
```

Modified properties:

```
public uint? short? PosixPermissions { get; set; }
```

Removed method:

```
[Obsolete ("Use FromDictionary instead")]
	public static NSFileAttributes FromDict (NSDictionary dict);
```

### Type Changed: Foundation.NSFileCoordinator

Modified constructors:

```
public protected NSFileCoordinator (NSObjectFlag t)
	public protected NSFileCoordinator (IntPtr handle)
```

Modified properties:

```
public NSFilePresenter[] INSFilePresenter[] FilePresenters { get; }
```

Removed methods:

```
public static void AddFilePresenter (NSFilePresenter filePresenter);
	public virtual void CoordinateBatc (NSUrl[] readingURLs, NSFileCoordinatorReadingOptions readingOptions, NSUrl[] writingURLs, NSFileCoordinatorWritingOptions writingOptions, out NSError error, NSAction batchHandler);
	public virtual void CoordinateRead (NSUrl itemUrl, NSFileCoordinatorReadingOptions options, out NSError error, NSFileCoordinatorWorker worker);
	public virtual void CoordinateWrite (NSUrl url, NSFileCoordinatorWritingOptions options, out NSError error, NSFileCoordinatorWorker worker);
	public static void RemoveFilePresenter (NSFilePresenter filePresenter);
```

Added methods:

```
public static void AddFilePresenter (INSFilePresenter filePresenter);
	public virtual void CoordinateBatc (NSUrl[] readingURLs, NSFileCoordinatorReadingOptions readingOptions, NSUrl[] writingURLs, NSFileCoordinatorWritingOptions writingOptions, out NSError error, System.Action batchHandler);
	public virtual void CoordinateRead (NSUrl itemUrl, NSFileCoordinatorReadingOptions options, out NSError error, System.Action<NSUrl> worker);
	public virtual void CoordinateWrite (NSUrl url, NSFileCoordinatorWritingOptions options, out NSError error, System.Action<NSUrl> worker);
	public static void RemoveFilePresenter (INSFilePresenter filePresenter);
```

### Type Changed: Foundation.NSFileHandle

Modified constructors:

```
public protected NSFileHandle (NSObjectFlag t)
	public protected NSFileHandle (IntPtr handle)
```

Removed methods:

```
public virtual void SetReadabilityHandler (NSFileHandleUpdateHandler readCallback);
	public virtual void SetWriteabilityHandle (NSFileHandleUpdateHandler writeCallback);
```

Added methods:

```
public virtual void SetReadabilityHandler (System.Action<NSFileHandle> readCallback);
	public virtual void SetWriteabilityHandle (System.Action<NSFileHandle> writeCallback);
```

### Type Changed: Foundation.NSFileManager

Modified constructors:

```
public protected NSFileManager (NSObjectFlag t)
	public protected NSFileManager (IntPtr handle)
```

Modified properties:

```
public NSFileManagerDelegate INSFileManagerDelegate Delegate { get; set; }
```

Removed methods:

```
public virtual NSDirectoryEnumerator GetEnumerator (NSUrl url, NSArray properties, NSDirectoryEnumerationOptions options, NSEnumerateErrorHandler handler);
	public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSUrl directoryURL, NSUrl otherURL, out NSError error);
	public virtual bool GetRelationship (out NSURLRelationship outRelationship, NSSearchPathDirectory directory, NSSearchPathDomain domain, NSUrl toItemAtUrl, out NSError error);
```

Added methods:

```
public virtual NSDirectoryEnumerator GetEnumerator (NSUrl url, NSString[] keys, NSDirectoryEnumerationOptions options, NSEnumerateErrorHandler handler);
	public virtual bool GetRelationship (out NSUrlRelationship outRelationship, NSUrl directoryURL, NSUrl otherURL, out NSError error);
	public virtual bool GetRelationship (out NSUrlRelationship outRelationship, NSSearchPathDirectory directory, NSSearchPathDomain domain, NSUrl toItemAtUrl, out NSError error);
```

### Type Changed: Foundation.NSFileManagerDelegate

Modified constructors:

```
public protected NSFileManagerDelegate (NSObjectFlag t)
	public protected NSFileManagerDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSFilePresenter

Modified constructors:

```
public protected NSFilePresenter ()
	public protected NSFilePresenter (NSObjectFlag t)
	public protected NSFilePresenter (IntPtr handle)
```

Modified properties:

```
public abstract NSOperationQueue PesentedItemOperationQueue { get; }
```

Removed methods:

```
public virtual void RelinquishPresentedItemToReader (UIKit.NSFilePresenterReacquirer readerAction);
	public virtual void RelinquishPresentedItemToWriter (UIKit.NSFilePresenterReacquirer writerAction);
```

Added methods:

```
public virtual void RelinquishPresentedItemToReader (NSFilePresenterReacquirer readerAction);
	public virtual void RelinquishPresentedItemToWriter (NSFilePresenterReacquirer writerAction);
```

### Type Changed: Foundation.NSFilePresenter_Extensions

Removed methods:

```
public static NSOperationQueue GetPesentedItemOperationQueue (INSFilePresenter This);
	public static void RelinquishPresentedItemToReader (INSFilePresenter This, UIKit.NSFilePresenterReacquirer readerAction);
	public static void RelinquishPresentedItemToWriter (INSFilePresenter This, UIKit.NSFilePresenterReacquirer writerAction);
```

Added methods:

```
public static void RelinquishPresentedItemToReader (INSFilePresenter This, NSFilePresenterReacquirer readerAction);
	public static void RelinquishPresentedItemToWriter (INSFilePresenter This, NSFilePresenterReacquirer writerAction);
```

### Type Changed: Foundation.NSFileVersion

Modified constructors:

```
public protected NSFileVersion (NSObjectFlag t)
	public protected NSFileVersion (IntPtr handle)
```

### Type Changed: Foundation.NSFileWrapper

Modified constructors:

```
public protected NSFileWrapper (IntPtr handle)
	public protected NSFileWrapper (NSObjectFlag t)
```

### Type Changed: Foundation.NSFormatter

Modified constructors:

```
public protected NSFormatter (NSObjectFlag t)
	public protected NSFormatter (IntPtr handle)
```

### Type Changed: Foundation.NSHttpCookie

Modified constructors:

```
public protected NSHttpCookie (IntPtr handle)
	public protected NSHttpCookie (NSObjectFlag t)
```

Removed fields:

```
public static NSString KeyComment;
	public static NSString KeyCommentURL;
	public static NSString KeyDiscard;
	public static NSString KeyDomain;
	public static NSString KeyExpires;
	public static NSString KeyMaximumAge;
	public static NSString KeyName;
	public static NSString KeyOriginURL;
	public static NSString KeyPath;
	public static NSString KeyPort;
	public static NSString KeySecure;
	public static NSString KeyValue;
	public static NSString KeyVersion;
```

Added properties:

```
public static NSString KeyComment { get; }
	public static NSString KeyCommentUrl { get; }
	public static NSString KeyDiscard { get; }
	public static NSString KeyDomain { get; }
	public static NSString KeyExpires { get; }
	public static NSString KeyMaximumAge { get; }
	public static NSString KeyName { get; }
	public static NSString KeyOriginUrl { get; }
	public static NSString KeyPath { get; }
	public static NSString KeyPort { get; }
	public static NSString KeySecure { get; }
	public static NSString KeyValue { get; }
	public static NSString KeyVersion { get; }
```

### Type Changed: Foundation.NSHttpCookieStorage

Modified constructors:

```
public protected NSHttpCookieStorage (NSObjectFlag t)
	public protected NSHttpCookieStorage (IntPtr handle)
```

Removed fields:

```
public static NSString AcceptPolicyChangedNotification;
	public static NSString CookiesChangedNotification;
```

Added properties:

```
public static NSString AcceptPolicyChangedNotification { get; }
	public static NSString CookiesChangedNotification { get; }
```

### Type Changed: Foundation.NSHttpUrlResponse

Modified constructors:

```
public protected NSHttpUrlResponse (NSObjectFlag t)
	public protected NSHttpUrlResponse (IntPtr handle)
```

### Type Changed: Foundation.NSIndexPath

Modified constructors:

```
public protected NSIndexPath (NSObjectFlag t)
	public protected NSIndexPath (IntPtr handle)
```

Modified properties:

```
public virtual int Row { get; }
	public virtual int Section { get; }
```

Added properties:

```
public virtual int LongRow { get; }
	public virtual int LongSection { get; }
```

Removed methods:

```
public override bool Equals (object obj);

	[Obsolete ("Use NSIndexPath.Create (int[]) instead")]
	public NSIndexPath FromIndexes (uint[] indexes);
	public override int GetHashCode ();
```

Added methods:

```
public static NSIndexPath Create (int[] indexes);
	public static NSIndexPath Create (uint[] indexes);
```

### Type Changed: Foundation.NSIndexSet

Modified constructors:

```
public protected NSIndexSet (NSObjectFlag t)
	public protected NSIndexSet (IntPtr handle)
```

### Type Changed: Foundation.NSInputStream

Modified constructors:

```
public protected NSInputStream (NSObjectFlag t)
	public protected NSInputStream (IntPtr handle)
```

### Type Changed: Foundation.NSInvocation

Modified constructors:

```
public protected NSInvocation (NSObjectFlag t)
	public protected NSInvocation (IntPtr handle)
```

### Type Changed: Foundation.NSItemProvider

Modified constructors:

```
public protected NSItemProvider (NSObjectFlag t)
	public protected NSItemProvider (IntPtr handle)
```

### Type Changed: Foundation.NSJsonSerialization

Modified constructors:

```
public protected NSJsonSerialization (NSObjectFlag t)
	public protected NSJsonSerialization (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use the Deserialize(NSData,NSJsonReadingOptions,out NSError) overload instead")]
	public static NSObject Deserialize (NSData data, NSJsonReadingOptions opt, NSError error);
```

### Type Changed: Foundation.NSKeyedArchiver

Modified constructors:

```
public protected NSKeyedArchiver (NSObjectFlag t)
	public protected NSKeyedArchiver (IntPtr handle)
```

Modified properties:

```
public NSKeyedArchiverDelegate INSKeyedArchiverDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSKeyedArchiverDelegate

Modified constructors:

```
public protected NSKeyedArchiverDelegate (NSObjectFlag t)
	public protected NSKeyedArchiverDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSKeyedUnarchiver

Modified constructors:

```
public protected NSKeyedUnarchiver (NSObjectFlag t)
	public protected NSKeyedUnarchiver (IntPtr handle)
```

Modified properties:

```
public NSKeyedUnarchiverDelegate INSKeyedUnarchiverDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSKeyedUnarchiverDelegate

Modified constructors:

```
public protected NSKeyedUnarchiverDelegate (NSObjectFlag t)
	public protected NSKeyedUnarchiverDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSLengthFormatter

Modified constructors:

```
public protected NSLengthFormatter (NSObjectFlag t)
	public protected NSLengthFormatter (IntPtr handle)
```

### Type Changed: Foundation.NSLinguisticTagger

Modified constructors:

```
public protected NSLinguisticTagger (NSObjectFlag t)
	public protected NSLinguisticTagger (IntPtr handle)
```

### Type Changed: Foundation.NSLocale

Modified constructors:

```
public protected NSLocale (NSObjectFlag t)
	public protected NSLocale (IntPtr handle)
```

### Type Changed: Foundation.NSMachPort

Modified constructors:

```
public protected NSMachPort (NSObjectFlag t)
	public protected NSMachPort (IntPtr handle)
```

Modified properties:

```
public NSMachPortDelegate INSMachPortDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSMachPortDelegate

Modified constructors:

```
public protected NSMachPortDelegate (NSObjectFlag t)
	public protected NSMachPortDelegate (IntPtr handle)
```

Removed method:

```
public override void MessageReceived (NSPortMessage message);
```

### Type Changed: Foundation.NSMassFormatter

Modified constructors:

```
public protected NSMassFormatter (NSObjectFlag t)
	public protected NSMassFormatter (IntPtr handle)
```

### Type Changed: Foundation.NSMetadataItem

Modified constructors:

```
public protected NSMetadataItem (NSObjectFlag t)
	public protected NSMetadataItem (IntPtr handle)
```

### Type Changed: Foundation.NSMetadataQuery

Modified constructors:

```
public protected NSMetadataQuery (NSObjectFlag t)
	public protected NSMetadataQuery (IntPtr handle)
```

Removed properties:

```
public static NSString QueryUbiquitousDataScope { get; }
	public static NSString QueryUbiquitousDocumentsScope { get; }
```

Modified properties:

```
public NSMetadataQueryDelegate INSMetadataQueryDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSMetadataQueryAttributeValueTuple

Modified constructors:

```
public protected NSMetadataQueryAttributeValueTuple (NSObjectFlag t)
	public protected NSMetadataQueryAttributeValueTuple (IntPtr handle)
```

### Type Changed: Foundation.NSMetadataQueryDelegate

Modified constructors:

```
public protected NSMetadataQueryDelegate (NSObjectFlag t)
	public protected NSMetadataQueryDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSMetadataQueryResultGroup

Modified constructors:

```
public protected NSMetadataQueryResultGroup (NSObjectFlag t)
	public protected NSMetadataQueryResultGroup (IntPtr handle)
```

### Type Changed: Foundation.NSMethodSignature

Modified constructors:

```
public protected NSMethodSignature (NSObjectFlag t)
	public protected NSMethodSignature (IntPtr handle)
```

### Type Changed: Foundation.NSMutableArray

Removed constructor:

```
public NSMutableArray (int capacity);
```

Modified constructors:

```
public protected NSMutableArray (NSObjectFlag t)
	public protected NSMutableArray (IntPtr handle)
```

### Type Changed: Foundation.NSMutableAttributedString

Modified constructors:

```
public protected NSMutableAttributedString (IntPtr handle)
	public protected NSMutableAttributedString (NSObjectFlag t)
```

### Type Changed: Foundation.NSMutableCharacterSet

Modified constructors:

```
public protected NSMutableCharacterSet (NSObjectFlag t)
	public protected NSMutableCharacterSet (IntPtr handle)
```

### Type Changed: Foundation.NSMutableCopying

Modified constructors:

```
public protected NSMutableCopying ()
	public protected NSMutableCopying (NSObjectFlag t)
	public protected NSMutableCopying (IntPtr handle)
```

Modified methods:

```
public abstract NSObject MutableCopy (NSZone zone)
```

### Type Changed: Foundation.NSMutableData

Modified constructors:

```
public protected NSMutableData (NSObjectFlag t)
	public protected NSMutableData (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use the Length property setter")]
	public virtual void SetLength (uint len);
```

### Type Changed: Foundation.NSMutableDictionary

Modified constructors:

```
public protected NSMutableDictionary (NSObjectFlag t)
	public protected NSMutableDictionary (IntPtr handle)
```

### Type Changed: Foundation.NSMutableIndexSet

Modified constructors:

```
public protected NSMutableIndexSet (NSObjectFlag t)
	public protected NSMutableIndexSet (IntPtr handle)
```

### Type Changed: Foundation.NSMutableOrderedSet

Modified constructors:

```
public protected NSMutableOrderedSet (IntPtr handle)
	public protected NSMutableOrderedSet (NSObjectFlag t)
```

### Type Changed: Foundation.NSMutableSet

Modified constructors:

```
public protected NSMutableSet (IntPtr handle)
	public protected NSMutableSet (NSObjectFlag t)
```

### Type Changed: Foundation.NSMutableString

Modified constructors:

```
public protected NSMutableString (NSObjectFlag t)
	public protected NSMutableString (IntPtr handle)
```

### Type Changed: Foundation.NSMutableUrlRequest

Modified constructors:

```
public protected NSMutableUrlRequest (NSObjectFlag t)
	public protected NSMutableUrlRequest (IntPtr handle)
```

### Type Changed: Foundation.NSNetService

Modified constructors:

```
public protected NSNetService (NSObjectFlag t)
	public protected NSNetService (IntPtr handle)
```

Modified properties:

```
public NSNetServiceDelegate INSNetServiceDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSNetServiceBrowser

Modified constructors:

```
public protected NSNetServiceBrowser (NSObjectFlag t)
	public protected NSNetServiceBrowser (IntPtr handle)
```

Modified properties:

```
public NSNetServiceBrowserDelegate INSNetServiceBrowserDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSNetServiceBrowserDelegate

Modified constructors:

```
public protected NSNetServiceBrowserDelegate (NSObjectFlag t)
	public protected NSNetServiceBrowserDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSNetServiceDelegate

Modified constructors:

```
public protected NSNetServiceDelegate (NSObjectFlag t)
	public protected NSNetServiceDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSNotification

Modified constructors:

```
public protected NSNotification (NSObjectFlag t)
	public protected NSNotification (IntPtr handle)
```

### Type Changed: Foundation.NSNotificationCenter

Modified constructors:

```
public protected NSNotificationCenter (NSObjectFlag t)
	public protected NSNotificationCenter (IntPtr handle)
```

Removed methods:

```
[Obsolete ("Use AddObserver(NSString, Action, NSObject)")]
	public NSObject AddObserver (string aName, System.Action<NSNotification> notify, NSObject fromObject);
	public virtual NSObject AddObserver (string name, NSObject obj, NSOperationQueue queue, NSNotificationHandler handler);

	[Obsolete ("Use AddObserver(NSObject, Selector, NSString, NSObject) instead")]
	public void AddObserver (NSObject observer, ObjCRuntime.Selector aSelector, string aname, NSObject anObject);

	[Obsolete ("Use AddObserver(NSString, Action) instead")]
	public NSObject AddObserver (string aName, System.Action<NSNotification> notify);
```

Added method:

```
public virtual NSObject AddObserver (string name, NSObject obj, NSOperationQueue queue, System.Action<NSNotification> handler);
```

### Type Changed: Foundation.NSNotificationQueue

Modified constructors:

```
public protected NSNotificationQueue (NSObjectFlag t)
	public protected NSNotificationQueue (IntPtr handle)
```

### Type Changed: Foundation.NSNull

Modified constructors:

```
public protected NSNull (NSObjectFlag t)
	public protected NSNull (IntPtr handle)
```

### Type Changed: Foundation.NSNumber

Modified constructors:

```
public protected NSNumber (NSObjectFlag t)
	public protected NSNumber (IntPtr handle)
```

Added constructors:

```
public NSNumber (float value);
	public NSNumber (int value);
	public NSNumber (uint value);
```

Removed properties:

```
public virtual int IntValue { get; }
	public virtual uint UnsignedIntegerValue { get; }
```

Added properties:

```
public virtual int NIntValue { get; }
	public virtual uint NUIntValue { get; }
```

Removed method:

```
public virtual bool IsEqualToNumber (NSNumber number);
```

Added methods:

```
public static NSNumber FromNFloat (float value);
	public static NSNumber FromNInt (int value);
	public static NSNumber FromNUInt (uint value);
```

### Type Changed: Foundation.NSNumberFormatter

Modified constructors:

```
public protected NSNumberFormatter (NSObjectFlag t)
	public protected NSNumberFormatter (IntPtr handle)
```

### Type Changed: Foundation.NSObject

Removed field:

```
protected bool IsDirectBinding;
```

Modified properties:

```
public virtual int uint RetainCount { get; }
```

Added property:

```
protected bool IsDirectBinding { get; set; }
```

Removed methods:

```
public virtual void AccessibilityDecrement ();
	public virtual void AccessibilityIncrement ();
	public virtual bool AccessibilityScroll (UIKit.UIAccessibilityScrollDirection direction);

	[Obsolete ("Low-level API warning: Use at your own risk: this calls the Retain method on the underlying object; Use DangerousAutorelease to avoid this warning")]
	public NSObject Autorelease ();
	public void BeginInvokeOnMainThread (NSAction action);
	public virtual void Invoke (NSAction action, double delay);
	public virtual void Invoke (NSAction action, System.TimeSpan delay);
	public static void InvokeInBackground (NSAction action);
	public void InvokeOnMainThread (NSAction action);
	public virtual void PerformSelector (ObjCRuntime.Selector sel, NSObject obj, float delay);

	[Obsolete ("Low-level API warning: Use at your own risk: this calls the Release method on the underlying object;  Use DangerousRelease to avoid this warning")]
	public void Release ();

	[Obsolete ("Low-level API warning: Use at your own risk: this calls the Retain method on the underlying object; Use DangerousRetain to avoid this warning")]
	public NSObject Retain ();
```

Added methods:

```
public void BeginInvokeOnMainThread (System.Action action);
	public override bool Equals (object obj);
	public virtual bool Equals (NSObject obj);
	public override int GetHashCode ();
	public virtual void Invoke (System.Action action, System.TimeSpan delay);
	public virtual void Invoke (System.Action action, double delay);
	public static void InvokeInBackground (System.Action action);
	public void InvokeOnMainThread (System.Action action);
```

### Type Changed: Foundation.NSOperation

Modified constructors:

```
public protected NSOperation (NSObjectFlag t)
	public protected NSOperation (IntPtr handle)
```

### Type Changed: Foundation.NSOperationQueue

Modified constructors:

```
public protected NSOperationQueue (NSObjectFlag t)
	public protected NSOperationQueue (IntPtr handle)
```

Removed method:

```
public virtual void AddOperation (NSAction operation);
```

Added method:

```
public virtual void AddOperation (System.Action operation);
```

### Type Changed: Foundation.NSOrderedSet

Modified constructors:

```
public protected NSOrderedSet (IntPtr handle)
	public protected NSOrderedSet (NSObjectFlag t)
```

### Type Changed: Foundation.NSOrthography

Modified constructors:

```
public protected NSOrthography (NSObjectFlag t)
	public protected NSOrthography (IntPtr handle)
```

### Type Changed: Foundation.NSOutputStream

Modified constructors:

```
public protected NSOutputStream (NSObjectFlag t)
	public protected NSOutputStream (IntPtr handle)
```

Removed method:

```
public static NSOutputStream OutputStreamToMemory ();
```

Added method:

```
public static NSObject OutputStreamToMemory ();
```

### Type Changed: Foundation.NSPipe

Modified constructors:

```
public protected NSPipe (NSObjectFlag t)
	public protected NSPipe (IntPtr handle)
```

### Type Changed: Foundation.NSPort

Modified constructors:

```
public protected NSPort (NSObjectFlag t)
	public protected NSPort (IntPtr handle)
```

Modified properties:

```
public NSPortDelegate INSPortDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSPortDelegate

Modified constructors:

```
public protected NSPortDelegate (NSObjectFlag t)
	public protected NSPortDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSPortMessage

Modified constructors:

```
public protected NSPortMessage (NSObjectFlag t)
	public protected NSPortMessage (IntPtr handle)
```

Removed properties:

```
[Obsolete ("Only available on OSX")]
	public virtual uint MsgId { get; set; }

	[Obsolete ("Only available on OSX")]
	public virtual NSPort ReceivePort { get; }

	[Obsolete ("Only available on OSX")]
	public virtual NSPort SendPort { get; }
```

Removed method:

```
[Obsolete ("Only available on OSX")]
	public virtual bool SendBefore (NSDate date);
```

### Type Changed: Foundation.NSPredicate

Modified constructors:

```
public protected NSPredicate (NSObjectFlag t)
	public protected NSPredicate (IntPtr handle)
```

### Type Changed: Foundation.NSProcessInfo

Modified constructors:

```
public protected NSProcessInfo (NSObjectFlag t)
	public protected NSProcessInfo (IntPtr handle)
```

Removed method:

```
public virtual void PerformActivity (NSActivityOptions options, string reason, NSAction runCode);
```

Added method:

```
public virtual void PerformActivity (NSActivityOptions options, string reason, System.Action runCode);
```

### Type Changed: Foundation.NSProgress

Modified constructors:

```
public protected NSProgress (NSObjectFlag t)
	public protected NSProgress (IntPtr handle)
```

Removed methods:

```
public virtual void SetCancellationHandler (NSAction handler);
	public virtual void SetPauseHandler (NSAction handler);
```

Added methods:

```
public virtual void SetCancellationHandler (System.Action handler);
	public virtual void SetPauseHandler (System.Action handler);
```

### Type Changed: Foundation.NSPropertyListSerialization

Modified constructors:

```
public protected NSPropertyListSerialization (NSObjectFlag t)
	public protected NSPropertyListSerialization (IntPtr handle)
```

### Type Changed: Foundation.NSPurgeableData

Modified constructors:

```
public protected NSPurgeableData (NSObjectFlag t)
	public protected NSPurgeableData (IntPtr handle)
```

### Type Changed: Foundation.NSRange

Modified fields:

```
public const readonly int NotFound = 2147483647 null;
```

### Type Changed: Foundation.NSRunLoop

Modified constructors:

```
public protected NSRunLoop (NSObjectFlag t)
	public protected NSRunLoop (IntPtr handle)
```

Removed methods:

```
[Obsolete ("Use AcceptInputForMode (NSRunLoopMode, NSDate)")]
	public void AcceptInputForMode (string mode, NSDate limitDate);

	[Obsolete ("Use AddTimer (NSTimer, NSRunLoopMode)")]
	public void AddTimer (NSTimer timer, string forMode);

	[Obsolete ("Use LimitDateForMode (NSRunLoopMode) instead")]
	public NSDate LimitDateForMode (string mode);
```

### Type Changed: Foundation.NSSet

Modified constructors:

```
public protected NSSet (IntPtr handle)
	public protected NSSet (NSObjectFlag t)
```

### Type Changed: Foundation.NSSortDescriptor

Modified constructors:

```
public protected NSSortDescriptor (NSObjectFlag t)
	public protected NSSortDescriptor (IntPtr handle)
```

### Type Changed: Foundation.NSStream

Modified constructors:

```
public protected NSStream (NSObjectFlag t)
	public protected NSStream (IntPtr handle)
```

Modified properties:

```
public NSStreamDelegate INSStreamDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSStreamDelegate

Modified constructors:

```
public protected NSStreamDelegate (NSObjectFlag t)
	public protected NSStreamDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSString

Modified constructors:

```
public protected NSString (NSObjectFlag t)
	public protected NSString (IntPtr handle)
```

Removed methods:

```
public virtual char _characterAtIndex (int index);

	[Obsolete ("Use Encode instead")]
	public NSData DataUsingEncoding (NSStringEncoding enc);

	[Obsolete ("Use Encode instead")]
	public NSData DataUsingEncoding (NSStringEncoding enc, bool allowLossyConversion);
	public System.Drawing.SizeF DrawString (System.Drawing.PointF point, UIKit.UIFont font);
	public System.Drawing.SizeF DrawString (System.Drawing.RectangleF rect, UIKit.UIFont font, UIKit.UILineBreakMode mode, UIKit.UITextAlignment alignment);
	public System.Drawing.SizeF DrawString (System.Drawing.RectangleF rect, UIKit.UIFont font, UIKit.UILineBreakMode mode);
	public System.Drawing.SizeF DrawString (System.Drawing.RectangleF rect, UIKit.UIFont font);
	public System.Drawing.SizeF DrawString (System.Drawing.PointF point, float width, UIKit.UIFont font, float minFontSize, ref float actualFontSize, UIKit.UILineBreakMode breakMode, UIKit.UIBaselineAdjustment adjustment);
	public System.Drawing.SizeF DrawString (System.Drawing.PointF point, float width, UIKit.UIFont font, float fontSize, UIKit.UILineBreakMode breakMode, UIKit.UIBaselineAdjustment adjustment);
	public System.Drawing.SizeF DrawString (System.Drawing.PointF point, float width, UIKit.UIFont font, UIKit.UILineBreakMode breakMode);

	[Obsolete ("Use the version with a `ref float actualFontSize`")]
	public System.Drawing.SizeF DrawString (System.Drawing.PointF point, float width, UIKit.UIFont font, float minFontSize, float actualFontSize, UIKit.UILineBreakMode breakMode, UIKit.UIBaselineAdjustment adjustment);
	public NSData Encode (NSStringEncoding enc);
	public System.Drawing.SizeF StringSize (UIKit.UIFont font, float minFontSize, ref float actualFontSize, float forWidth, UIKit.UILineBreakMode lineBreakMode);
	public System.Drawing.SizeF StringSize (UIKit.UIFont font, System.Drawing.SizeF constrainedToSize, UIKit.UILineBreakMode lineBreakMode);
	public System.Drawing.SizeF StringSize (UIKit.UIFont font, System.Drawing.SizeF constrainedToSize);
	public System.Drawing.SizeF StringSize (UIKit.UIFont font, float forWidth, UIKit.UILineBreakMode breakMode);
	public System.Drawing.SizeF StringSize (UIKit.UIFont font);
```

Modified methods:

```
public NSData Encode (NSStringEncoding enc, bool allowLossyConversion = false)
```

### Type Changed: Foundation.NSStringDrawingContext

Modified constructors:

```
public protected NSStringDrawingContext (NSObjectFlag t)
	public protected NSStringDrawingContext (IntPtr handle)
```

### Type Changed: Foundation.NSThread

Modified constructors:

```
public protected NSThread (NSObjectFlag t)
	public protected NSThread (IntPtr handle)
```

### Type Changed: Foundation.NSTimer

Removed constructors:

```
public NSTimer (NSDate date, System.TimeSpan when, NSAction action, bool repeats);

	[Obsolete ("This instance of NSTimer would be unusable. Symbol kept for binary compatibility")]
	public NSTimer ();
```

Modified constructors:

```
public protected NSTimer (NSObjectFlag t)
	public protected NSTimer (IntPtr handle)
```

Added constructor:

```
public NSTimer (NSDate date, System.TimeSpan when, System.Action<NSTimer> action, bool repeats);
```

Removed methods:

```
public static NSTimer CreateRepeatingScheduledTimer (System.TimeSpan when, NSAction action);
	public static NSTimer CreateRepeatingScheduledTimer (double seconds, NSAction action);
	public static NSTimer CreateRepeatingTimer (double seconds, NSAction action);
	public static NSTimer CreateRepeatingTimer (System.TimeSpan when, NSAction action);
	public static NSTimer CreateScheduledTimer (double seconds, NSAction action);
	public static NSTimer CreateScheduledTimer (System.TimeSpan when, NSAction action);
	public static NSTimer CreateTimer (double seconds, NSAction action);
	public static NSTimer CreateTimer (System.TimeSpan when, NSAction action);
```

Added methods:

```
public static NSTimer CreateRepeatingScheduledTimer (System.TimeSpan when, System.Action<NSTimer> action);
	public static NSTimer CreateRepeatingScheduledTimer (double seconds, System.Action<NSTimer> action);
	public static NSTimer CreateRepeatingTimer (double seconds, System.Action<NSTimer> action);
	public static NSTimer CreateRepeatingTimer (System.TimeSpan when, System.Action<NSTimer> action);
	public static NSTimer CreateScheduledTimer (double seconds, System.Action<NSTimer> action);
	public static NSTimer CreateScheduledTimer (System.TimeSpan when, System.Action<NSTimer> action);
	public static NSTimer CreateTimer (double seconds, System.Action<NSTimer> action);
	public static NSTimer CreateTimer (System.TimeSpan when, System.Action<NSTimer> action);
```

### Type Changed: Foundation.NSTimeZone

Modified constructors:

```
public protected NSTimeZone (NSObjectFlag t)
	public protected NSTimeZone (IntPtr handle)
```

### Type Changed: Foundation.NSUbiquitousKeyValueStore

Modified constructors:

```
public protected NSUbiquitousKeyValueStore (NSObjectFlag t)
	public protected NSUbiquitousKeyValueStore (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use ToDictionary instead")]
	public virtual NSDictionary DictionaryRepresentation ();
```

Modified methods:

```
public virtual NSDictionary ToDictionary ()
```

### Type Changed: Foundation.NSUndoManager

Modified constructors:

```
public protected NSUndoManager (NSObjectFlag t)
	public protected NSUndoManager (IntPtr handle)
```

### Type Changed: Foundation.NSUrl

Modified constructors:

```
public protected NSUrl (IntPtr handle)
	public protected NSUrl (NSObjectFlag t)
```

Removed methods:

```
public override bool Equals (object t);
	public override int GetHashCode ();
	public virtual bool IsEqual (NSUrl other);

	[Obsolete ("Use the overload with a NSString constant")]
	public bool SetResource (string key, NSObject value);

	[Obsolete ("Use the overload with a NSString constant")]
	public bool SetResource (string key, NSObject value, out NSError error);

	[Obsolete ("Use the overload with a NSString constant")]
	public bool TryGetResource (string key, out NSObject value, out NSError error);

	[Obsolete ("Use the overload with a NSString constant")]
	public bool TryGetResource (string key, out NSObject value);
```

### Type Changed: Foundation.NSUrlAuthenticationChallenge

Modified constructors:

```
public protected NSUrlAuthenticationChallenge (NSObjectFlag t)
	public protected NSUrlAuthenticationChallenge (IntPtr handle)
```

### Type Changed: Foundation.NSURLAuthenticationChallengeSender

Modified constructors:

```
public protected NSURLAuthenticationChallengeSender ()
	public protected NSURLAuthenticationChallengeSender (NSObjectFlag t)
	public protected NSURLAuthenticationChallengeSender (IntPtr handle)
```

Removed methods:

```
public virtual void ContinueWithoutCredentialForAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void RejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void UseCredentials (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
```

Added methods:

```
public virtual void ContinueWithoutCredential (NSUrlAuthenticationChallenge challenge);
	public virtual void PerformDefaultHandling (NSUrlAuthenticationChallenge challenge);
	public virtual void RejectProtectionSpaceAndContinue (NSUrlAuthenticationChallenge challenge);
	public virtual void UseCredential (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
```

### Type Changed: Foundation.NSURLAuthenticationChallengeSender_Extensions

Added methods:

```
public static void PerformDefaultHandling (INSURLAuthenticationChallengeSender This, NSUrlAuthenticationChallenge challenge);
	public static void RejectProtectionSpaceAndContinue (INSURLAuthenticationChallengeSender This, NSUrlAuthenticationChallenge challenge);
```

### Type Changed: Foundation.NSUrlCache

Modified constructors:

```
public protected NSUrlCache (NSObjectFlag t)
	public protected NSUrlCache (IntPtr handle)
```

### Type Changed: Foundation.NSUrlComponents

Modified constructors:

```
public protected NSUrlComponents (NSObjectFlag t)
	public protected NSUrlComponents (IntPtr handle)
```

### Type Changed: Foundation.NSUrlConnection

Removed constructors:

```
public NSUrlConnection (NSUrlRequest request, NSUrlConnectionDelegate connectionDelegate);
	public NSUrlConnection (NSUrlRequest request, NSUrlConnectionDelegate connectionDelegate, bool startImmediately);
```

Modified constructors:

```
public protected NSUrlConnection (NSObjectFlag t)
	public protected NSUrlConnection (IntPtr handle)
```

Added constructors:

```
public NSUrlConnection (NSUrlRequest request, INSUrlConnectionDelegate connectionDelegate);
	public NSUrlConnection (NSUrlRequest request, INSUrlConnectionDelegate connectionDelegate, bool startImmediately);
```

Removed methods:

```
public virtual void ContinueWithoutCredentialForAuthenticationChallenge (NSUrlAuthenticationChallenge challenge);
	public static NSUrlConnection FromRequest (NSUrlRequest request, NSUrlConnectionDelegate connectionDelegate);
	public virtual void PerformDefaultHandlingForChallenge (NSUrlAuthenticationChallenge challenge);
	public virtual void RejectProtectionSpaceAndContinueWithChallenge (NSUrlAuthenticationChallenge challenge);

	[Obsolete ("Use Schedule (NSRunLoop, NSString) instead")]
	public virtual void Schedule (NSRunLoop aRunLoop, string forMode);

	[Obsolete ("Use Unschedule (NSRunLoop, NSString) instead")]
	public virtual void Unschedule (NSRunLoop aRunLoop, string forMode);
	public virtual void UseCredentials (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
```

Added methods:

```
public virtual void ContinueWithoutCredential (NSUrlAuthenticationChallenge challenge);
	public static NSUrlConnection FromRequest (NSUrlRequest request, INSUrlConnectionDelegate connectionDelegate);
	public virtual void PerformDefaultHandling (NSUrlAuthenticationChallenge challenge);
	public virtual void RejectProtectionSpaceAndContinue (NSUrlAuthenticationChallenge challenge);
	public virtual void UseCredential (NSUrlCredential credential, NSUrlAuthenticationChallenge challenge);
```

### Type Changed: Foundation.NSUrlConnectionDelegate

Modified constructors:

```
public protected NSUrlConnectionDelegate (NSObjectFlag t)
	public protected NSUrlConnectionDelegate (IntPtr handle)
```

Removed methods:

```
public virtual void FinishedLoading (NSUrlConnection connection);
	public virtual NSInputStream NeedNewBodyStream (NSUrlConnection connection, NSUrlRequest request);
	public virtual void ReceivedData (NSUrlConnection connection, NSData data);
	public virtual void ReceivedResponse (NSUrlConnection connection, NSUrlResponse response);
	public virtual void SentBodyData (NSUrlConnection connection, int bytesWritten, int totalBytesWritten, int totalBytesExpectedToWrite);
	public virtual NSCachedUrlResponse WillCacheResponse (NSUrlConnection connection, NSCachedUrlResponse cachedResponse);
	public virtual NSUrlRequest WillSendRequest (NSUrlConnection connection, NSUrlRequest request, NSUrlResponse response);
```

### Type Changed: Foundation.NSUrlConnectionDelegate_Extensions

Removed methods:

```
public static void FinishedLoading (INSUrlConnectionDelegate This, NSUrlConnection connection);
	public static NSInputStream NeedNewBodyStream (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlRequest request);
	public static void ReceivedData (INSUrlConnectionDelegate This, NSUrlConnection connection, NSData data);
	public static void ReceivedResponse (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlResponse response);
	public static void SentBodyData (INSUrlConnectionDelegate This, NSUrlConnection connection, int bytesWritten, int totalBytesWritten, int totalBytesExpectedToWrite);
	public static NSCachedUrlResponse WillCacheResponse (INSUrlConnectionDelegate This, NSUrlConnection connection, NSCachedUrlResponse cachedResponse);
	public static NSUrlRequest WillSendRequest (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlRequest request, NSUrlResponse response);
```

### Type Changed: Foundation.NSUrlConnectionDownloadDelegate

Modified constructors:

```
public protected NSUrlConnectionDownloadDelegate ()
	public protected NSUrlConnectionDownloadDelegate (NSObjectFlag t)
	public protected NSUrlConnectionDownloadDelegate (IntPtr handle)
```

Removed methods:

```
public override bool CanAuthenticateAgainstProtectionSpace (NSUrlConnection connection, NSUrlProtectionSpace protectionSpace);
	public override void CanceledAuthenticationChallenge (NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
	public override bool ConnectionShouldUseCredentialStorage (NSUrlConnection connection);
	public override void FailedWithError (NSUrlConnection connection, NSError error);
	public override void FinishedLoading (NSUrlConnection connection);
	public override NSInputStream NeedNewBodyStream (NSUrlConnection connection, NSUrlRequest request);
	public override void ReceivedAuthenticationChallenge (NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
	public override void ReceivedData (NSUrlConnection connection, NSData data);
	public override void ReceivedResponse (NSUrlConnection connection, NSUrlResponse response);
	public override void SentBodyData (NSUrlConnection connection, int bytesWritten, int totalBytesWritten, int totalBytesExpectedToWrite);
	public override NSCachedUrlResponse WillCacheResponse (NSUrlConnection connection, NSCachedUrlResponse cachedResponse);
	public override NSUrlRequest WillSendRequest (NSUrlConnection connection, NSUrlRequest request, NSUrlResponse response);
	public override void WillSendRequestForAuthenticationChallenge (NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
```

### Type Changed: Foundation.NSUrlCredential

Removed constructor:

```
[Obsolete ("Use NSUrlCredential(SecTrust) constructor")]
	public NSUrlCredential (IntPtr trust, bool ignored);
```

Modified constructors:

```
public protected NSUrlCredential (NSObjectFlag t)
	public protected NSUrlCredential (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use SecIdentity property")]
	public virtual IntPtr Identity { get; }
```

Removed method:

```
[Obsolete ("Use NSUrlCredential(SecTrust) constructor")]
	public static NSUrlCredential FromTrust (IntPtr trust);
```

### Type Changed: Foundation.NSUrlCredentialStorage

Modified constructors:

```
public protected NSUrlCredentialStorage (NSObjectFlag t)
	public protected NSUrlCredentialStorage (IntPtr handle)
```

### Type Changed: Foundation.NSUrlProtectionSpace

Modified constructors:

```
public protected NSUrlProtectionSpace (NSObjectFlag t)
	public protected NSUrlProtectionSpace (IntPtr handle)
```

Removed properties:

```
[Obsolete ("Use AuthenticationMethodNegotiate")]
	public static NSString AuthenticationMethodNegotiat { get; }

	[Obsolete ("Use AuthenticationMethodNTLM")]
	public static NSString AuthenticationMethodNTL { get; }

	[Obsolete ("Use AuthenticationMethodServerTrust")]
	public static NSString AuthenticationMethodServerTrus { get; }

	[Obsolete ("Use ServerSecTrust")]
	public virtual IntPtr ServerTrust { get; }
```

### Type Changed: Foundation.NSUrlProtocol

Removed constructors:

```
public NSUrlProtocol (NSUrlRequest request, NSCachedUrlResponse cachedResponse, NSUrlProtocolClient client);
```

Modified constructors:

```
public protected NSUrlProtocol (NSObjectFlag t)
	public protected NSUrlProtocol (IntPtr handle)
```

Added constructor:

```
public NSUrlProtocol (NSUrlRequest request, NSCachedUrlResponse cachedResponse, INSUrlProtocolClient client);
```

Removed property:

```
public virtual NSObject WeakClient { get; }
```

Modified properties:

```
public virtual NSUrlProtocolClient INSUrlProtocolClient Client { get; }
```

### Type Changed: Foundation.NSUrlQueryItem

Modified constructors:

```
public protected NSUrlQueryItem (NSObjectFlag t)
	public protected NSUrlQueryItem (IntPtr handle)
```

### Type Changed: Foundation.NSUrlRequest

Modified constructors:

```
public protected NSUrlRequest (NSObjectFlag t)
	public protected NSUrlRequest (IntPtr handle)
```

### Type Changed: Foundation.NSUrlResponse

Modified constructors:

```
public protected NSUrlResponse (NSObjectFlag t)
	public protected NSUrlResponse (IntPtr handle)
```

### Type Changed: Foundation.NSUrlSession

Removed constructors:

```
public NSUrlSession ();
```

Modified constructors:

```
public protected NSUrlSession (NSObjectFlag t)
	public protected NSUrlSession (IntPtr handle)
```

Modified properties:

```
public NSUrlSessionDelegate INSUrlSessionDelegate Delegate { get; }
```

Removed methods:

```
[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrlRequest request, NSUrlSessionResponse completionHandler);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTask (NSUrl url, NSUrlSessionResponse completionHandler);

	[Obsolete ("Use the override that accept an NSUrlDownloadSessionResponse parameter")]
	public virtual NSUrlSessionDownloadTask CreateDownloadTaskFromResumeData (NSData resumeData, NSUrlSessionResponse completionHandler);
	public virtual void Flush (NSAction completionHandler);
	public virtual void Reset (NSAction completionHandler);
```

Added methods:

```
public virtual void Flush (System.Action completionHandler);
	public virtual void Reset (System.Action completionHandler);
```

### Type Changed: Foundation.NSUrlSessionConfiguration

Removed constructors:

```
public NSUrlSessionConfiguration ();
```

Modified constructors:

```
public protected NSUrlSessionConfiguration (NSObjectFlag t)
	public protected NSUrlSessionConfiguration (IntPtr handle)
```

### Type Changed: Foundation.NSUrlSessionDataDelegate

Modified constructors:

```
public protected NSUrlSessionDataDelegate (NSObjectFlag t)
	public protected NSUrlSessionDataDelegate (IntPtr handle)
```

Removed methods:

```
public override void DidCompleteWithError (NSUrlSession session, NSUrlSessionTask task, NSError error);
	public override void DidReceiveChallenge (NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,Foundation.NSUrlCredential> completionHandler);
	public override void DidSendBodyData (NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public override void NeedNewBodyStream (NSUrlSession session, NSUrlSessionTask task, System.Action<NSInputStream> completionHandler);
	public override void WillPerformHttpRedirection (NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, System.Action<NSUrlRequest> completionHandler);
```

### Type Changed: Foundation.NSUrlSessionDataTask

Modified constructors:

```
public protected NSUrlSessionDataTask (NSObjectFlag t)
	public protected NSUrlSessionDataTask (IntPtr handle)
```

### Type Changed: Foundation.NSUrlSessionDelegate

Modified constructors:

```
public protected NSUrlSessionDelegate (NSObjectFlag t)
	public protected NSUrlSessionDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSUrlSessionDownloadDelegate

Modified constructors:

```
public protected NSUrlSessionDownloadDelegate ()
	public protected NSUrlSessionDownloadDelegate (NSObjectFlag t)
	public protected NSUrlSessionDownloadDelegate (IntPtr handle)
```

Removed methods:

```
public override void DidCompleteWithError (NSUrlSession session, NSUrlSessionTask task, NSError error);
	public override void DidReceiveChallenge (NSUrlSession session, NSUrlSessionTask task, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,Foundation.NSUrlCredential> completionHandler);
	public override void DidSendBodyData (NSUrlSession session, NSUrlSessionTask task, long bytesSent, long totalBytesSent, long totalBytesExpectedToSend);
	public override void NeedNewBodyStream (NSUrlSession session, NSUrlSessionTask task, System.Action<NSInputStream> completionHandler);
	public override void WillPerformHttpRedirection (NSUrlSession session, NSUrlSessionTask task, NSHttpUrlResponse response, NSUrlRequest newRequest, System.Action<NSUrlRequest> completionHandler);
```

Modified methods:

```
public abstract void DidFinishDownloading (NSUrlSession session, NSUrlSessionDownloadTask downloadTask, NSUrl location)
```

### Type Changed: Foundation.NSUrlSessionDownloadDelegate_Extensions

Removed method:

```
public static void DidFinishDownloading (INSUrlSessionDownloadDelegate This, NSUrlSession session, NSUrlSessionDownloadTask downloadTask, NSUrl location);
```

### Type Changed: Foundation.NSUrlSessionDownloadTask

Modified constructors:

```
public protected NSUrlSessionDownloadTask (NSObjectFlag t)
	public protected NSUrlSessionDownloadTask (IntPtr handle)
```

### Type Changed: Foundation.NSUrlSessionDownloadTaskRequest

Removed property:

```
[Obsolete ("Use the Location property")]
	public NSData Data { get; set; }
```

### Type Changed: Foundation.NSUrlSessionTask

Modified constructors:

```
public protected NSUrlSessionTask (NSObjectFlag t)
	public protected NSUrlSessionTask (IntPtr handle)
```

### Type Changed: Foundation.NSUrlSessionTaskDelegate

Modified constructors:

```
public protected NSUrlSessionTaskDelegate (NSObjectFlag t)
	public protected NSUrlSessionTaskDelegate (IntPtr handle)
```

Removed methods:

```
public override void DidBecomeInvalid (NSUrlSession session, NSError error);
	public override void DidFinishEventsForBackgroundSession (NSUrlSession session);
	public override void DidReceiveChallenge (NSUrlSession session, NSUrlAuthenticationChallenge challenge, System.Action<NSUrlSessionAuthChallengeDisposition,Foundation.NSUrlCredential> completionHandler);
```

### Type Changed: Foundation.NSUrlSessionUploadTask

Modified constructors:

```
public protected NSUrlSessionUploadTask (NSObjectFlag t)
	public protected NSUrlSessionUploadTask (IntPtr handle)
```

### Type Changed: Foundation.NSUserActivity

Removed constructors:

```
public NSUserActivity (NSString activityType);
```

Modified constructors:

```
public protected NSUserActivity (NSObjectFlag t)
	public protected NSUserActivity (IntPtr handle)
```

Added constructor:

```
public NSUserActivity (string activityType);
```

Modified properties:

```
public NSUserActivityDelegate INSUserActivityDelegate Delegate { get; set; }
```

### Type Changed: Foundation.NSUserActivityDelegate

Modified constructors:

```
public protected NSUserActivityDelegate (NSObjectFlag t)
	public protected NSUserActivityDelegate (IntPtr handle)
```

### Type Changed: Foundation.NSUserDefaults

Modified constructors:

```
public protected NSUserDefaults (NSObjectFlag t)
	public protected NSUserDefaults (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use ToDictionary instead")]
	public virtual NSDictionary AsDictionary ();
```

Modified methods:

```
public virtual NSDictionary ToDictionary ()
```

### Type Changed: Foundation.NSUuid

Modified constructors:

```
public protected NSUuid (NSObjectFlag t)
	public protected NSUuid (IntPtr handle)
```

### Type Changed: Foundation.NSValue

Modified constructors:

```
public protected NSValue (NSObjectFlag t)
	public protected NSValue (IntPtr handle)
```

### Removed Type Foundation.NSAction ### Removed Type Foundation.NSCoding_Extensions ### Removed Type Foundation.NSCopying_Extensions ### Removed Type Foundation.NSExtension ### Removed Type Foundation.NSExtensionRequestHandling_Extensions ### Removed Type Foundation.NSFileCoordinatorWorker ### Removed Type Foundation.NSFileHandleUpdateHandler ### Removed Type Foundation.NSLocking_Extensions ### Removed Type Foundation.NSMutableCopying_Extensions ### Removed Type Foundation.NSNotificationHandler ### Removed Type Foundation.NSSecureCoding_Extensions ### Removed Type Foundation.NSUrlProtocolClient ### Removed Type Foundation.NSURLRelationship ### Removed Type Foundation.NSURLSessionTaskPriority ### Removed Type Foundation.NSURLUtilities_NSString ### New Type Foundation.INSUrlConnectionDataDelegate

```
public interface INSUrlConnectionDataDelegate : ObjCRuntime.INativeObject, System.IDisposable, INSUrlConnectionDelegate {
}
```

### New Type Foundation.INSUrlProtocolClient

```
public interface INSUrlProtocolClient : ObjCRuntime.INativeObject, System.IDisposable {
	// methods
	public virtual void CachedResponseIsValid (NSUrlProtocol protocol, NSCachedUrlResponse cachedResponse);
	public virtual void CancelledAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
	public virtual void DataLoaded (NSUrlProtocol protocol, NSData data);
	public virtual void FailedWithError (NSUrlProtocol protocol, NSError error);
	public virtual void FinishedLoading (NSUrlProtocol protocol);
	public virtual void ReceivedAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
	public virtual void ReceivedResponse (NSUrlProtocol protocol, NSUrlResponse response, NSUrlCacheStoragePolicy policy);
	public virtual void Redirected (NSUrlProtocol protocol, NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
}
```

### New Type Foundation.NSFilePresenterReacquirer

```
public sealed delegate NSFilePresenterReacquirer : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public NSFilePresenterReacquirer (object object, IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (System.Action reacquirer, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (System.Action reacquirer);
}
```

### New Type Foundation.NSUrlConnectionDataDelegate

```
public class NSUrlConnectionDataDelegate : Foundation.NSUrlConnectionDelegate, INSUrlConnectionDataDelegate, ObjCRuntime.INativeObject, System.IDisposable, INSUrlConnectionDelegate, System.IEquatable<NSObject>, INSObjectProtocol {
	// constructors
	public NSUrlConnectionDataDelegate ();
	protected NSUrlConnectionDataDelegate (NSObjectFlag t);
	protected NSUrlConnectionDataDelegate (IntPtr handle);
	// methods
	public virtual void FinishedLoading (NSUrlConnection connection);
	public virtual NSInputStream NeedNewBodyStream (NSUrlConnection connection, NSUrlRequest request);
	public virtual void ReceivedData (NSUrlConnection connection, NSData data);
	public virtual void ReceivedResponse (NSUrlConnection connection, NSUrlResponse response);
	public virtual void SentBodyData (NSUrlConnection connection, int bytesWritten, int totalBytesWritten, int totalBytesExpectedToWrite);
	public virtual NSCachedUrlResponse WillCacheResponse (NSUrlConnection connection, NSCachedUrlResponse cachedResponse);
	public virtual NSUrlRequest WillSendRequest (NSUrlConnection connection, NSUrlRequest request, NSUrlResponse response);
}
```

### New Type Foundation.NSUrlConnectionDataDelegate_Extensions

```
public static class NSUrlConnectionDataDelegate_Extensions {
	// methods
	public static void FinishedLoading (INSUrlConnectionDataDelegate This, NSUrlConnection connection);
	public static NSInputStream NeedNewBodyStream (INSUrlConnectionDataDelegate This, NSUrlConnection connection, NSUrlRequest request);
	public static void ReceivedData (INSUrlConnectionDataDelegate This, NSUrlConnection connection, NSData data);
	public static void ReceivedResponse (INSUrlConnectionDataDelegate This, NSUrlConnection connection, NSUrlResponse response);
	public static void SentBodyData (INSUrlConnectionDataDelegate This, NSUrlConnection connection, int bytesWritten, int totalBytesWritten, int totalBytesExpectedToWrite);
	public static NSCachedUrlResponse WillCacheResponse (INSUrlConnectionDataDelegate This, NSUrlConnection connection, NSCachedUrlResponse cachedResponse);
	public static NSUrlRequest WillSendRequest (INSUrlConnectionDataDelegate This, NSUrlConnection connection, NSUrlRequest request, NSUrlResponse response);
}
```

### New Type Foundation.NSUrlRelationship

```
[Serializable]
public enum NSUrlRelationship {
	Contains = 0,
	Other = 2,
	Same = 1,
}
```

### New Type Foundation.NSUrlSessionTaskPriority

```
public static class NSUrlSessionTaskPriority {
	// properties
	public static float Default { get; }
	public static float High { get; }
	public static float Low { get; }
}
```

### New Type Foundation.NSUrlUtilities_NSString

```
public static class NSUrlUtilities_NSString {
	// methods
	public static NSString CreateStringByAddingPercentEncoding (NSString This, NSCharacterSet allowedCharacters);
	public static NSString CreateStringByAddingPercentEscapes (NSString This, NSStringEncoding enc);
	public static NSString CreateStringByRemovingPercentEncoding (NSString This);
	public static NSString CreateStringByReplacingPercentEscapes (NSString This, NSStringEncoding enc);
}
```





## Namespace GameController



### Type Changed: GameController.GCController

Modified constructors:

```
public protected GCController (Foundation.NSObjectFlag t)
	public protected GCController (IntPtr handle)
```

Modified properties:

```
public virtual GCControllerPausedHandler System.Action<GCController> ControllerPausedHandler { get; set; }
```

### Type Changed: GameController.GCControllerAxisInput

Removed constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCControllerAxisInput ();
```

Modified constructors:

```
public protected GCControllerAxisInput (Foundation.NSObjectFlag t)
	public protected GCControllerAxisInput (IntPtr handle)
```

### Type Changed: GameController.GCControllerButtonInput

Removed constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCControllerButtonInput ();
```

Modified constructors:

```
public protected GCControllerButtonInput (Foundation.NSObjectFlag t)
	public protected GCControllerButtonInput (IntPtr handle)
```

### Type Changed: GameController.GCControllerDirectionPad

Removed constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCControllerDirectionPad ();
```

Modified constructors:

```
public protected GCControllerDirectionPad (Foundation.NSObjectFlag t)
	public protected GCControllerDirectionPad (IntPtr handle)
```

### Type Changed: GameController.GCControllerElement

Removed constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCControllerElement ();
```

Modified constructors:

```
public protected GCControllerElement (Foundation.NSObjectFlag t)
	public protected GCControllerElement (IntPtr handle)
```

### Type Changed: GameController.GCExtendedGamepad

Removed constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCExtendedGamepad ();
```

Modified constructors:

```
public protected GCExtendedGamepad (Foundation.NSObjectFlag t)
	public protected GCExtendedGamepad (IntPtr handle)
```

### Type Changed: GameController.GCExtendedGamepadSnapshot

Modified constructors:

```
public protected GCExtendedGamepadSnapshot (Foundation.NSObjectFlag t)
	public protected GCExtendedGamepadSnapshot (IntPtr handle)
```

### Type Changed: GameController.GCGamepad

Removed constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCGamepad ();
```

Modified constructors:

```
public protected GCGamepad (Foundation.NSObjectFlag t)
	public protected GCGamepad (IntPtr handle)
```

### Type Changed: GameController.GCGamepadSnapshot

Modified constructors:

```
public protected GCGamepadSnapshot (Foundation.NSObjectFlag t)
	public protected GCGamepadSnapshot (IntPtr handle)
```

### Type Changed: GameController.GCMotion

Modified constructors:

```
public protected GCMotion (Foundation.NSObjectFlag t)
	public protected GCMotion (IntPtr handle)
```

### Removed Type GameController.GCControllerPausedHandler 

## Namespace GameKit



### Type Changed: GameKit.GKAchievement

Modified constructors:

```
public protected GKAchievement (Foundation.NSObjectFlag t)
	public protected GKAchievement (IntPtr handle)
```

Modified properties:

```
public virtual string PlayerID { get; set; }
```

Removed methods:

```
public virtual void ReportAchievement (GKNotificationHandler completionHandler);
	public static void ReportAchievements (GKAchievement[] achievements, GKNotificationHandler completionHandler);
	public static void ResetAchivements (GKNotificationHandler completionHandler);
```

Added methods:

```
public virtual void ReportAchievement (System.Action<Foundation.NSError> completionHandler);
	public static void ReportAchievements (GKAchievement[] achievements, System.Action<Foundation.NSError> completionHandler);
	public static void ResetAchivements (System.Action<Foundation.NSError> completionHandler);
```

### Type Changed: GameKit.GKAchievementChallenge

Modified constructors:

```
public protected GKAchievementChallenge (Foundation.NSObjectFlag t)
	public protected GKAchievementChallenge (IntPtr handle)
```

### Type Changed: GameKit.GKAchievementDescription

Modified constructors:

```
public protected GKAchievementDescription (Foundation.NSObjectFlag t)
	public protected GKAchievementDescription (IntPtr handle)
```

### Type Changed: GameKit.GKAchievementViewController

Modified constructors:

```
public protected GKAchievementViewController (Foundation.NSObjectFlag t)
	public protected GKAchievementViewController (IntPtr handle)
```

Modified properties:

```
public GKAchievementViewControllerDelegate IGKAchievementViewControllerDelegate Delegate { get; set; }
```

### Type Changed: GameKit.GKAchievementViewControllerDelegate

Modified constructors:

```
public protected GKAchievementViewControllerDelegate ()
	public protected GKAchievementViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected GKAchievementViewControllerDelegate (IntPtr handle)
```

Modified methods:

```
public abstract void DidFinish (GKAchievementViewController viewController)
```

### Type Changed: GameKit.GKChallenge

Modified constructors:

```
public protected GKChallenge (Foundation.NSObjectFlag t)
	public protected GKChallenge (IntPtr handle)
```

### Type Changed: GameKit.GKChallengeEventHandler

Modified constructors:

```
public protected GKChallengeEventHandler (Foundation.NSObjectFlag t)
	public protected GKChallengeEventHandler (IntPtr handle)
```

Modified properties:

```
public GKChallengeEventHandlerDelegate IGKChallengeEventHandlerDelegate Delegate { get; set; }
```

### Type Changed: GameKit.GKChallengeEventHandlerDelegate

Modified constructors:

```
public protected GKChallengeEventHandlerDelegate (Foundation.NSObjectFlag t)
	public protected GKChallengeEventHandlerDelegate (IntPtr handle)
```

### Type Changed: GameKit.GKChallengeListener

Modified constructors:

```
public protected GKChallengeListener (Foundation.NSObjectFlag t)
	public protected GKChallengeListener (IntPtr handle)
```

### Type Changed: GameKit.GKFriendRequestComposeViewController

Modified constructors:

```
public protected GKFriendRequestComposeViewController (Foundation.NSObjectFlag t)
	public protected GKFriendRequestComposeViewController (IntPtr handle)
```

Removed property:

```
public virtual string Message { set; }
```

Modified properties:

```
public GKFriendRequestComposeViewControllerDelegate IGKFriendRequestComposeViewControllerDelegate ComposeViewDelegate { get; set; }
```

Added method:

```
public virtual void SetMessage (string message);
```

### Type Changed: GameKit.GKFriendRequestComposeViewControllerDelegate

Modified constructors:

```
public protected GKFriendRequestComposeViewControllerDelegate ()
	public protected GKFriendRequestComposeViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected GKFriendRequestComposeViewControllerDelegate (IntPtr handle)
```

### Type Changed: GameKit.GKGameCenterControllerDelegate

Modified constructors:

```
public protected GKGameCenterControllerDelegate ()
	public protected GKGameCenterControllerDelegate (Foundation.NSObjectFlag t)
	public protected GKGameCenterControllerDelegate (IntPtr handle)
```

Modified methods:

```
public abstract void Finished (GKGameCenterViewController controller)
```

### Type Changed: GameKit.GKGameCenterViewController

Modified constructors:

```
public protected GKGameCenterViewController (Foundation.NSObjectFlag t)
	public protected GKGameCenterViewController (IntPtr handle)
```

Modified properties:

```
public GKGameCenterControllerDelegate IGKGameCenterControllerDelegate Delegate { get; set; }
```

### Type Changed: GameKit.GKInvite

Modified constructors:

```
public protected GKInvite (Foundation.NSObjectFlag t)
	public protected GKInvite (IntPtr handle)
```

### Type Changed: GameKit.GKInviteEventListener

Modified constructors:

```
public protected GKInviteEventListener (Foundation.NSObjectFlag t)
	public protected GKInviteEventListener (IntPtr handle)
```

### Type Changed: GameKit.GKLeaderboard

Modified constructors:

```
public protected GKLeaderboard (Foundation.NSObjectFlag t)
	public protected GKLeaderboard (IntPtr handle)
```

Removed method:

```
public static void SetDefaultLeaderboard (string leaderboardIdentifier, GKNotificationHandler notificationHandler);
```

Added method:

```
public static void SetDefaultLeaderboard (string leaderboardIdentifier, System.Action<Foundation.NSError> notificationHandler);
```

### Type Changed: GameKit.GKLeaderboardSet

Modified constructors:

```
public protected GKLeaderboardSet (Foundation.NSObjectFlag t)
	public protected GKLeaderboardSet (IntPtr handle)
```

### Type Changed: GameKit.GKLeaderboardViewController

Removed constructor:

```
[Obsolete ("Apple never shipped the `initWithTimeScope:playerScope:` selector. Use the default constructor.")]
	public GKLeaderboardViewController (GKLeaderboardTimeScope timeScope, GKLeaderboardPlayerScope playerScope);
```

Modified constructors:

```
public protected GKLeaderboardViewController (Foundation.NSObjectFlag t)
	public protected GKLeaderboardViewController (IntPtr handle)
```

Modified properties:

```
public GKLeaderboardViewControllerDelegate IGKLeaderboardViewControllerDelegate Delegate { get; set; }
```

### Type Changed: GameKit.GKLeaderboardViewControllerDelegate

Modified constructors:

```
public protected GKLeaderboardViewControllerDelegate ()
	public protected GKLeaderboardViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected GKLeaderboardViewControllerDelegate (IntPtr handle)
```

Modified methods:

```
public abstract void DidFinish (GKLeaderboardViewController viewController)
```

### Type Changed: GameKit.GKLocalPlayer

Modified constructors:

```
public protected GKLocalPlayer (Foundation.NSObjectFlag t)
	public protected GKLocalPlayer (IntPtr handle)
```

Removed methods:

```
public virtual void Authenticate (GKNotificationHandler handler);
	public virtual void RegisterListener (GKLocalPlayerListener listener);
	public virtual void UnregisterListener (GKLocalPlayerListener listener);
```

Added methods:

```
public virtual void Authenticate (System.Action<Foundation.NSError> handler);
	public virtual void RegisterListener (IGKLocalPlayerListener listener);
	public virtual void UnregisterListener (IGKLocalPlayerListener listener);
```

### Type Changed: GameKit.GKLocalPlayerListener

Modified constructors:

```
public protected GKLocalPlayerListener (Foundation.NSObjectFlag t)
	public protected GKLocalPlayerListener (IntPtr handle)
```

### Type Changed: GameKit.GKMatch

Modified constructors:

```
public protected GKMatch (Foundation.NSObjectFlag t)
	public protected GKMatch (IntPtr handle)
```

Modified properties:

```
public GKMatchDelegate IGKMatchDelegate Delegate { get; set; }
```

Removed event:

```
[Obsolete ("No longer an iOS API - it will never be called")]
	public event System.EventHandler<GKPlayerErrorEventArgs> ConnectionFailed;
```

Removed method:

```
[Obsolete ("Use SendDataToAllPlayers")]
	public virtual bool SendDataToAllPlayer (Foundation.NSData data, GKMatchSendDataMode mode, out Foundation.NSError error);
```

### Type Changed: GameKit.GKMatchDelegate

Modified constructors:

```
public protected GKMatchDelegate (Foundation.NSObjectFlag t)
	public protected GKMatchDelegate (IntPtr handle)
```

Removed method:

```
[Obsolete ("No longer an iOS API - it will never be called")]
	public virtual void ConnectionFailed (GKMatch match, string playerId, Foundation.NSError error);
```

### Type Changed: GameKit.GKMatchDelegate_Extensions

Removed method:

```
[Obsolete ("No longer an iOS API - it will never be called")]
	public static void ConnectionFailed (IGKMatchDelegate This, GKMatch match, string playerId, Foundation.NSError error);
```

### Type Changed: GameKit.GKMatchmaker

Modified constructors:

```
public protected GKMatchmaker (Foundation.NSObjectFlag t)
	public protected GKMatchmaker (IntPtr handle)
```

Removed method:

```
public virtual void AddPlayers (GKMatch toMatch, GKMatchRequest matchRequest, GKNotificationHandler completionHandler);
```

Added method:

```
public virtual void AddPlayers (GKMatch toMatch, GKMatchRequest matchRequest, System.Action<Foundation.NSError> completionHandler);
```

### Type Changed: GameKit.GKMatchmakerViewController

Modified constructors:

```
public protected GKMatchmakerViewController (Foundation.NSObjectFlag t)
	public protected GKMatchmakerViewController (IntPtr handle)
```

Modified properties:

```
public GKMatchmakerViewControllerDelegate IGKMatchmakerViewControllerDelegate MatchmakerDelegate { get; set; }
```

### Type Changed: GameKit.GKMatchmakerViewControllerDelegate

Modified constructors:

```
public protected GKMatchmakerViewControllerDelegate ()
	public protected GKMatchmakerViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected GKMatchmakerViewControllerDelegate (IntPtr handle)
```

### Type Changed: GameKit.GKMatchRequest

Modified constructors:

```
public protected GKMatchRequest (Foundation.NSObjectFlag t)
	public protected GKMatchRequest (IntPtr handle)
```

### Type Changed: GameKit.GKNotificationBanner

Modified constructors:

```
public protected GKNotificationBanner (Foundation.NSObjectFlag t)
	public protected GKNotificationBanner (IntPtr handle)
```

Removed method:

```
public static void Show (string title, string message, Foundation.NSAction onCompleted);
```

Added method:

```
public static void Show (string title, string message, System.Action onCompleted);
```

### Type Changed: GameKit.GKPeerPickerController

Modified constructors:

```
public protected GKPeerPickerController (Foundation.NSObjectFlag t)
	public protected GKPeerPickerController (IntPtr handle)
```

Modified properties:

```
public GKPeerPickerControllerDelegate IGKPeerPickerControllerDelegate Delegate { get; set; }
```

### Type Changed: GameKit.GKPeerPickerControllerDelegate

Modified constructors:

```
public protected GKPeerPickerControllerDelegate (Foundation.NSObjectFlag t)
	public protected GKPeerPickerControllerDelegate (IntPtr handle)
```

### Type Changed: GameKit.GKPlayer

Modified constructors:

```
public protected GKPlayer (Foundation.NSObjectFlag t)
	public protected GKPlayer (IntPtr handle)
```

Removed property:

```
public Foundation.NSString DidChangeNotificationName { get; }
```

### Type Changed: GameKit.GKSavedGame

Modified constructors:

```
public protected GKSavedGame (Foundation.NSObjectFlag t)
	public protected GKSavedGame (IntPtr handle)
```

### Type Changed: GameKit.GKSavedGameListener

Modified constructors:

```
public protected GKSavedGameListener (Foundation.NSObjectFlag t)
	public protected GKSavedGameListener (IntPtr handle)
```

### Type Changed: GameKit.GKScore

Modified constructors:

```
public protected GKScore (Foundation.NSObjectFlag t)
	public protected GKScore (IntPtr handle)
```

Removed properties:

```
[Obsolete ("Use the Category property instead")]
	public virtual string category { get; set; }
	public virtual GKPlayer GamePlayer { get; }
```

Modified properties:

```
public virtual string Category { get; set; }
	public virtual string GKPlayer Player { get; }
```

Removed method:

```
public virtual void ReportScore (GKNotificationHandler errorHandler);
```

Added methods:

```
public virtual void ReportScore (System.Action<Foundation.NSError> errorHandler);
```

### Type Changed: GameKit.GKScoreChallenge

Modified constructors:

```
public protected GKScoreChallenge (Foundation.NSObjectFlag t)
	public protected GKScoreChallenge (IntPtr handle)
```

### Type Changed: GameKit.GKSession

Modified constructors:

```
public protected GKSession (Foundation.NSObjectFlag t)
	public protected GKSession (IntPtr handle)
```

Modified properties:

```
public GKSessionDelegate IGKSessionDelegate Delegate { get; set; }
```

Removed methods:

```
public virtual bool AcceptConnection (string peerID, IntPtr error_out);
	public virtual bool SendData (Foundation.NSData data, string[] peers, GKSendDataMode mode, IntPtr ns_error_out);
	public virtual bool SendDataToAllPeers (Foundation.NSData data, GKSendDataMode mode, IntPtr ns_error_out);
```

Modified methods:

```
public virtual bool SendData (Foundation.NSData data, string[] peers, GKSendDataMode mode, out Foundation.NSError error)
	public virtual bool SendDataToAllPeers (Foundation.NSData data, GKSendDataMode mode, out Foundation.NSError error)
```

Added method:

```
public virtual bool AcceptConnection (string peerID, out Foundation.NSError error);
```

### Type Changed: GameKit.GKSessionDelegate

Modified constructors:

```
public protected GKSessionDelegate (Foundation.NSObjectFlag t)
	public protected GKSessionDelegate (IntPtr handle)
```

### Type Changed: GameKit.GKTurnBasedEventHandler

Modified constructors:

```
public protected GKTurnBasedEventHandler (Foundation.NSObjectFlag t)
	public protected GKTurnBasedEventHandler (IntPtr handle)
```

Modified properties:

```
public GKTurnBasedEventHandlerDelegate IGKTurnBasedEventHandlerDelegate Delegate { get; set; }
```

### Type Changed: GameKit.GKTurnBasedEventHandlerDelegate

Modified constructors:

```
public protected GKTurnBasedEventHandlerDelegate ()
	public protected GKTurnBasedEventHandlerDelegate (Foundation.NSObjectFlag t)
	public protected GKTurnBasedEventHandlerDelegate (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use HandleInviteFromGameCenter(NSString[])")]
	public virtual void HandleInviteFromGameCenter (GKPlayer[] playersToInvite);
```

Modified methods:

```
public abstract void HandleInviteFromGameCenter (Foundation.NSString[] playersToInvite)
	public abstract void HandleTurnEvent (GKTurnBasedMatch match, bool activated)
```

### Type Changed: GameKit.GKTurnBasedEventHandlerDelegate_Extensions

Removed methods:

```
[Obsolete ("Use HandleInviteFromGameCenter(NSString[])")]
	public static void HandleInviteFromGameCenter (IGKTurnBasedEventHandlerDelegate This, GKPlayer[] playersToInvite);
	public static void HandleInviteFromGameCenter (IGKTurnBasedEventHandlerDelegate This, Foundation.NSString[] playersToInvite);
	public static void HandleTurnEvent (IGKTurnBasedEventHandlerDelegate This, GKTurnBasedMatch match, bool activated);
```

### Type Changed: GameKit.GKTurnBasedEventListener

Modified constructors:

```
public protected GKTurnBasedEventListener (Foundation.NSObjectFlag t)
	public protected GKTurnBasedEventListener (IntPtr handle)
```

### Type Changed: GameKit.GKTurnBasedExchange

Modified constructors:

```
public protected GKTurnBasedExchange (Foundation.NSObjectFlag t)
	public protected GKTurnBasedExchange (IntPtr handle)
```

### Type Changed: GameKit.GKTurnBasedExchangeReply

Modified constructors:

```
public protected GKTurnBasedExchangeReply (Foundation.NSObjectFlag t)
	public protected GKTurnBasedExchangeReply (IntPtr handle)
```

### Type Changed: GameKit.GKTurnBasedMatch

Modified constructors:

```
public protected GKTurnBasedMatch (Foundation.NSObjectFlag t)
	public protected GKTurnBasedMatch (IntPtr handle)
```

Removed methods:

```
public virtual void EndMatchInTurn (Foundation.NSData matchData, GKNotificationHandler onCompletion);
	public virtual void EndTurnWithNextParticipant (GKTurnBasedParticipant nextParticipant, Foundation.NSData matchData, GKNotificationHandler noCompletion);
	public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, Foundation.NSData matchData, GKNotificationHandler onCompletion);
	public virtual void ParticipantQuitOutOfTurn (GKTurnBasedMatchOutcome matchOutcome, GKNotificationHandler onCompletion);
	public virtual void Remove (GKNotificationHandler onCompletion);
```

Added methods:

```
public virtual void EndMatchInTurn (Foundation.NSData matchData, System.Action<Foundation.NSError> onCompletion);
	public virtual void EndTurnWithNextParticipant (GKTurnBasedParticipant nextParticipant, Foundation.NSData matchData, System.Action<Foundation.NSError> noCompletion);
	public virtual void ParticipantQuitInTurn (GKTurnBasedMatchOutcome matchOutcome, GKTurnBasedParticipant nextParticipant, Foundation.NSData matchData, System.Action<Foundation.NSError> onCompletion);
	public virtual void ParticipantQuitOutOfTurn (GKTurnBasedMatchOutcome matchOutcome, System.Action<Foundation.NSError> onCompletion);
	public virtual void Remove (System.Action<Foundation.NSError> onCompletion);
```

### Type Changed: GameKit.GKTurnBasedMatchmakerViewController

Modified constructors:

```
public protected GKTurnBasedMatchmakerViewController (Foundation.NSObjectFlag t)
	public protected GKTurnBasedMatchmakerViewController (IntPtr handle)
```

Modified properties:

```
public GKTurnBasedMatchmakerViewControllerDelegate IGKTurnBasedMatchmakerViewControllerDelegate Delegate { get; set; }
```

### Type Changed: GameKit.GKTurnBasedMatchmakerViewControllerDelegate

Modified constructors:

```
public protected GKTurnBasedMatchmakerViewControllerDelegate ()
	public protected GKTurnBasedMatchmakerViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected GKTurnBasedMatchmakerViewControllerDelegate (IntPtr handle)
```

### Type Changed: GameKit.GKTurnBasedParticipant

Modified constructors:

```
public protected GKTurnBasedParticipant (Foundation.NSObjectFlag t)
	public protected GKTurnBasedParticipant (IntPtr handle)
```

### Type Changed: GameKit.GKVoiceChat

Modified constructors:

```
public protected GKVoiceChat (Foundation.NSObjectFlag t)
	public protected GKVoiceChat (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use PlayerStateUpdateHandler property")]
	public virtual void SetPlayerStateUpdateHandler (GKPlayerStateUpdateHandler handler);
```

### Type Changed: GameKit.GKVoiceChatClient

Modified constructors:

```
public protected GKVoiceChatClient ()
	public protected GKVoiceChatClient (Foundation.NSObjectFlag t)
	public protected GKVoiceChatClient (IntPtr handle)
```

### Type Changed: GameKit.GKVoiceChatService

Modified constructors:

```
public protected GKVoiceChatService (Foundation.NSObjectFlag t)
	public protected GKVoiceChatService (IntPtr handle)
```

Modified properties:

```
public virtual GKVoiceChatClient IGKVoiceChatClient Client { get; set; }
```

Removed methods:

```
public virtual bool AcceptCall (int callID, IntPtr ns_error_out);
	public virtual bool StartVoiceChat (string participantID, IntPtr ns_error_out);
```

Modified methods:

```
public virtual bool AcceptCall (int callId callID, out Foundation.NSError error)
	public virtual bool StartVoiceChat (string participantID, out Foundation.NSError error)
```

### Type Changed: GameKit.IGKAchievementViewControllerDelegate

Added method:

```
public virtual void DidFinish (GKAchievementViewController viewController);
```

### Type Changed: GameKit.IGKGameCenterControllerDelegate

Added method:

```
public virtual void Finished (GKGameCenterViewController controller);
```

### Type Changed: GameKit.IGKLeaderboardViewControllerDelegate

Added method:

```
public virtual void DidFinish (GKLeaderboardViewController viewController);
```

### Type Changed: GameKit.IGKTurnBasedEventHandlerDelegate

Added methods:

```
public virtual void HandleInviteFromGameCenter (Foundation.NSString[] playersToInvite);
	public virtual void HandleTurnEvent (GKTurnBasedMatch match, bool activated);
```

### Removed Type GameKit.GKAchievementViewControllerDelegate_Extensions ### Removed Type GameKit.GKFriendRequestComposeViewControllerDelegate_Extensions ### Removed Type GameKit.GKGameCenterControllerDelegate_Extensions ### Removed Type GameKit.GKLeaderboardViewControllerDelegate_Extensions ### Removed Type GameKit.GKLocalPlayerListener_Extensions ### Removed Type GameKit.GKNotificationHandler ### Removed Type GameKit.GKPlayerErrorEventArgs ### Removed Type GameKit.GKTurnBasedMatchmakerViewControllerDelegate_Extensions 



## Namespace GLKit



### Type Changed: GLKit.GLKBaseEffect

Modified constructors:

```
public protected GLKBaseEffect (Foundation.NSObjectFlag t)
	public protected GLKBaseEffect (IntPtr handle)
```

### Type Changed: GLKit.GLKEffectProperty

Modified constructors:

```
public protected GLKEffectProperty (Foundation.NSObjectFlag t)
	public protected GLKEffectProperty (IntPtr handle)
```

### Type Changed: GLKit.GLKEffectPropertyFog

Modified constructors:

```
public protected GLKEffectPropertyFog (Foundation.NSObjectFlag t)
	public protected GLKEffectPropertyFog (IntPtr handle)
```

### Type Changed: GLKit.GLKEffectPropertyLight

Modified constructors:

```
public protected GLKEffectPropertyLight (Foundation.NSObjectFlag t)
	public protected GLKEffectPropertyLight (IntPtr handle)
```

### Type Changed: GLKit.GLKEffectPropertyMaterial

Modified constructors:

```
public protected GLKEffectPropertyMaterial (Foundation.NSObjectFlag t)
	public protected GLKEffectPropertyMaterial (IntPtr handle)
```

### Type Changed: GLKit.GLKEffectPropertyTexture

Modified constructors:

```
public protected GLKEffectPropertyTexture (Foundation.NSObjectFlag t)
	public protected GLKEffectPropertyTexture (IntPtr handle)
```

### Type Changed: GLKit.GLKEffectPropertyTransform

Modified constructors:

```
public protected GLKEffectPropertyTransform (Foundation.NSObjectFlag t)
	public protected GLKEffectPropertyTransform (IntPtr handle)
```

### Type Changed: GLKit.GLKNamedEffect

Modified constructors:

```
public protected GLKNamedEffect ()
	public protected GLKNamedEffect (Foundation.NSObjectFlag t)
	public protected GLKNamedEffect (IntPtr handle)
```

### Type Changed: GLKit.GLKReflectionMapEffect

Modified constructors:

```
public protected GLKReflectionMapEffect (Foundation.NSObjectFlag t)
	public protected GLKReflectionMapEffect (IntPtr handle)
```

### Type Changed: GLKit.GLKSkyboxEffect

Modified constructors:

```
public protected GLKSkyboxEffect (Foundation.NSObjectFlag t)
	public protected GLKSkyboxEffect (IntPtr handle)
```

### Type Changed: GLKit.GLKTextureInfo

Modified constructors:

```
public protected GLKTextureInfo (Foundation.NSObjectFlag t)
	public protected GLKTextureInfo (IntPtr handle)
```

### Type Changed: GLKit.GLKTextureLoader

Modified constructors:

```
public protected GLKTextureLoader (Foundation.NSObjectFlag t)
	public protected GLKTextureLoader (IntPtr handle)
```

### Type Changed: GLKit.GLKView

Modified constructors:

```
public protected GLKView (Foundation.NSObjectFlag t)
	public protected GLKView (IntPtr handle)
```

Modified properties:

```
public GLKViewDelegate IGLKViewDelegate Delegate { get; set; }
```

### Type Changed: GLKit.GLKViewController

Modified constructors:

```
public protected GLKViewController (Foundation.NSObjectFlag t)
	public protected GLKViewController (IntPtr handle)
```

Modified properties:

```
public GLKViewControllerDelegate IGLKViewControllerDelegate Delegate { get; set; }
```

### Type Changed: GLKit.GLKViewControllerDelegate

Modified constructors:

```
public protected GLKViewControllerDelegate ()
	public protected GLKViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected GLKViewControllerDelegate (IntPtr handle)
```

### Type Changed: GLKit.GLKViewDelegate

Modified constructors:

```
public protected GLKViewDelegate ()
	public protected GLKViewDelegate (Foundation.NSObjectFlag t)
	public protected GLKViewDelegate (IntPtr handle)
```

### Removed Type GLKit.GLKNamedEffect_Extensions ### Removed Type GLKit.GLKViewDelegate_Extensions 



## Namespace HealthKit



### Type Changed: HealthKit.HKAnchoredObjectQuery

Modified constructors:

```
public protected HKAnchoredObjectQuery (Foundation.NSObjectFlag t)
	public protected HKAnchoredObjectQuery (IntPtr handle)
```

### Type Changed: HealthKit.HKAnchoredObjectResultHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (HKAnchoredObjectQuery query, Foundation.NSObject[] results, uint newAnchor, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (HKAnchoredObjectQuery query, Foundation.NSObject[] results, uint newAnchor, Foundation.NSError error);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (HKAnchoredObjectQuery query, HKSampleType[] results, uint newAnchor, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (HKAnchoredObjectQuery query, HKSampleType[] results, uint newAnchor, Foundation.NSError error);
```

### Type Changed: HealthKit.HKBiologicalSexObject

Modified constructors:

```
public protected HKBiologicalSexObject (Foundation.NSObjectFlag t)
	public protected HKBiologicalSexObject (IntPtr handle)
```

### Type Changed: HealthKit.HKBloodTypeObject

Modified constructors:

```
public protected HKBloodTypeObject (Foundation.NSObjectFlag t)
	public protected HKBloodTypeObject (IntPtr handle)
```

### Type Changed: HealthKit.HKCategorySample

Modified constructors:

```
public protected HKCategorySample (Foundation.NSObjectFlag t)
	public protected HKCategorySample (IntPtr handle)
```

### Type Changed: HealthKit.HKCategoryType

Modified constructors:

```
public protected HKCategoryType (Foundation.NSObjectFlag t)
	public protected HKCategoryType (IntPtr handle)
```

### Type Changed: HealthKit.HKCharacteristicType

Modified constructors:

```
public protected HKCharacteristicType (Foundation.NSObjectFlag t)
	public protected HKCharacteristicType (IntPtr handle)
```

### Type Changed: HealthKit.HKCorrelation

Modified constructors:

```
public protected HKCorrelation (Foundation.NSObjectFlag t)
	public protected HKCorrelation (IntPtr handle)
```

### Type Changed: HealthKit.HKCorrelationQuery

Modified constructors:

```
public protected HKCorrelationQuery (Foundation.NSObjectFlag t)
	public protected HKCorrelationQuery (IntPtr handle)
```

### Type Changed: HealthKit.HKCorrelationType

Modified constructors:

```
public protected HKCorrelationType (Foundation.NSObjectFlag t)
	public protected HKCorrelationType (IntPtr handle)
```

### Type Changed: HealthKit.HKHealthStore

Modified constructors:

```
public protected HKHealthStore (Foundation.NSObjectFlag t)
	public protected HKHealthStore (IntPtr handle)
```

Removed methods:

```
public virtual System.Threading.Tasks.Task<bool> DeleteObjectAsync (HKObject obj);
	public virtual System.Threading.Tasks.Task<bool> RequestAuthorizationToShareAsync (Foundation.NSSet typesToShare, Foundation.NSSet typesToRead);
	public virtual System.Threading.Tasks.Task<bool> SaveObjectAsync (HKObject obj);
	public virtual System.Threading.Tasks.Task<bool> SaveObjectsAsync (HKObject[] objects);
```

Added methods:

```
public virtual System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> DeleteObjectAsync (HKObject obj);
	public virtual System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> RequestAuthorizationToShareAsync (Foundation.NSSet typesToShare, Foundation.NSSet typesToRead);
	public virtual System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> SaveObjectAsync (HKObject obj);
	public virtual System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> SaveObjectsAsync (HKObject[] objects);
```

### Type Changed: HealthKit.HKObject

Modified constructors:

```
public protected HKObject (Foundation.NSObjectFlag t)
	public protected HKObject (IntPtr handle)
```

### Type Changed: HealthKit.HKObjectType

Modified constructors:

```
public protected HKObjectType (Foundation.NSObjectFlag t)
	public protected HKObjectType (IntPtr handle)
```

### Type Changed: HealthKit.HKObserverQuery

Modified constructors:

```
public protected HKObserverQuery (Foundation.NSObjectFlag t)
	public protected HKObserverQuery (IntPtr handle)
```

### Type Changed: HealthKit.HKObserverQueryUpdateHandler

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (HKObserverQuery query, HKObserverQueryCompletionHandler completion, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (HKObserverQuery query, HKObserverQueryCompletionHandler completion, Foundation.NSError error);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (HKObserverQuery query, System.Action completion, Foundation.NSError error, System.AsyncCallback callback, object object);
	public virtual void Invoke (HKObserverQuery query, System.Action completion, Foundation.NSError error);
```

### Type Changed: HealthKit.HKQuantity

Modified constructors:

```
public protected HKQuantity (Foundation.NSObjectFlag t)
	public protected HKQuantity (IntPtr handle)
```

### Type Changed: HealthKit.HKQuantitySample

Modified constructors:

```
public protected HKQuantitySample (Foundation.NSObjectFlag t)
	public protected HKQuantitySample (IntPtr handle)
```

### Type Changed: HealthKit.HKQuantityType

Modified constructors:

```
public protected HKQuantityType (Foundation.NSObjectFlag t)
	public protected HKQuantityType (IntPtr handle)
```

### Type Changed: HealthKit.HKQuery

Modified constructors:

```
public protected HKQuery (Foundation.NSObjectFlag t)
	public protected HKQuery (IntPtr handle)
```

### Type Changed: HealthKit.HKSample

Modified constructors:

```
public protected HKSample (Foundation.NSObjectFlag t)
	public protected HKSample (IntPtr handle)
```

### Type Changed: HealthKit.HKSampleQuery

Modified constructors:

```
public protected HKSampleQuery (Foundation.NSObjectFlag t)
	public protected HKSampleQuery (IntPtr handle)
```

### Type Changed: HealthKit.HKSampleType

Modified constructors:

```
public protected HKSampleType (Foundation.NSCoder coder)
	public protected HKSampleType (Foundation.NSObjectFlag t)
	public protected HKSampleType (IntPtr handle)
```

### Type Changed: HealthKit.HKSource

Modified constructors:

```
public protected HKSource (Foundation.NSObjectFlag t)
	public protected HKSource (IntPtr handle)
```

### Type Changed: HealthKit.HKSourceQuery

Modified constructors:

```
public protected HKSourceQuery (Foundation.NSObjectFlag t)
	public protected HKSourceQuery (IntPtr handle)
```

### Type Changed: HealthKit.HKStatistics

Modified constructors:

```
public protected HKStatistics (Foundation.NSObjectFlag t)
	public protected HKStatistics (IntPtr handle)
```

### Type Changed: HealthKit.HKStatisticsCollection

Modified constructors:

```
public protected HKStatisticsCollection (Foundation.NSObjectFlag t)
	public protected HKStatisticsCollection (IntPtr handle)
```

### Type Changed: HealthKit.HKStatisticsCollectionQuery

Modified constructors:

```
public protected HKStatisticsCollectionQuery (Foundation.NSObjectFlag t)
	public protected HKStatisticsCollectionQuery (IntPtr handle)
```

### Type Changed: HealthKit.HKStatisticsQuery

Modified constructors:

```
public protected HKStatisticsQuery (Foundation.NSObjectFlag t)
	public protected HKStatisticsQuery (IntPtr handle)
```

### Type Changed: HealthKit.HKUnit

Modified constructors:

```
public protected HKUnit (Foundation.NSObjectFlag t)
	public protected HKUnit (IntPtr handle)
```

### Type Changed: HealthKit.HKWorkout

Modified constructors:

```
public protected HKWorkout (Foundation.NSObjectFlag t)
	public protected HKWorkout (IntPtr handle)
```

### Type Changed: HealthKit.HKWorkoutEvent

Modified constructors:

```
public protected HKWorkoutEvent (Foundation.NSObjectFlag t)
	public protected HKWorkoutEvent (IntPtr handle)
```

### Type Changed: HealthKit.HKWorkoutType

Modified constructors:

```
public protected HKWorkoutType (Foundation.NSObjectFlag t)
	public protected HKWorkoutType (IntPtr handle)
```

### Removed Type HealthKit.HKObserverQueryCompletionHandler 

## Namespace HomeKit



### Type Changed: HomeKit.HMAccessory

Modified constructors:

```
public protected HMAccessory (Foundation.NSObjectFlag t)
	public protected HMAccessory (IntPtr handle)
```

Modified properties:

```
public HMAccessoryDelegate IHMAccessoryDelegate Delegate { get; set; }
```

### Type Changed: HomeKit.HMAccessoryBrowser

Modified constructors:

```
public protected HMAccessoryBrowser (Foundation.NSObjectFlag t)
	public protected HMAccessoryBrowser (IntPtr handle)
```

Modified properties:

```
public HMAccessoryBrowserDelegate IHMAccessoryBrowserDelegate Delegate { get; set; }
```

### Type Changed: HomeKit.HMAccessoryBrowserDelegate

Modified constructors:

```
public protected HMAccessoryBrowserDelegate (Foundation.NSObjectFlag t)
	public protected HMAccessoryBrowserDelegate (IntPtr handle)
```

### Type Changed: HomeKit.HMAccessoryDelegate

Modified constructors:

```
public protected HMAccessoryDelegate (Foundation.NSObjectFlag t)
	public protected HMAccessoryDelegate (IntPtr handle)
```

### Type Changed: HomeKit.HMAction

Modified constructors:

```
public protected HMAction (Foundation.NSObjectFlag t)
	public protected HMAction (IntPtr handle)
```

### Type Changed: HomeKit.HMActionSet

Modified constructors:

```
public protected HMActionSet (Foundation.NSObjectFlag t)
	public protected HMActionSet (IntPtr handle)
```

### Type Changed: HomeKit.HMCharacteristic

Modified constructors:

```
public protected HMCharacteristic (Foundation.NSObjectFlag t)
	public protected HMCharacteristic (IntPtr handle)
```

### Type Changed: HomeKit.HMCharacteristicMetadata

Modified constructors:

```
public protected HMCharacteristicMetadata (Foundation.NSObjectFlag t)
	public protected HMCharacteristicMetadata (IntPtr handle)
```

### Type Changed: HomeKit.HMCharacteristicWriteAction

Modified constructors:

```
public protected HMCharacteristicWriteAction (Foundation.NSObjectFlag t)
	public protected HMCharacteristicWriteAction (IntPtr handle)
```

### Type Changed: HomeKit.HMHome

Modified constructors:

```
public protected HMHome (Foundation.NSObjectFlag t)
	public protected HMHome (IntPtr handle)
```

Modified properties:

```
public HMHomeDelegate IHMHomeDelegate Delegate { get; set; }
```

### Type Changed: HomeKit.HMHomeDelegate

Modified constructors:

```
public protected HMHomeDelegate (Foundation.NSObjectFlag t)
	public protected HMHomeDelegate (IntPtr handle)
```

### Type Changed: HomeKit.HMHomeManager

Modified constructors:

```
public protected HMHomeManager (Foundation.NSObjectFlag t)
	public protected HMHomeManager (IntPtr handle)
```

Modified properties:

```
public HMHomeManagerDelegate IHMHomeManagerDelegate Delegate { get; set; }
```

### Type Changed: HomeKit.HMHomeManagerDelegate

Modified constructors:

```
public protected HMHomeManagerDelegate (Foundation.NSObjectFlag t)
	public protected HMHomeManagerDelegate (IntPtr handle)
```

### Type Changed: HomeKit.HMRoom

Modified constructors:

```
public protected HMRoom (Foundation.NSObjectFlag t)
	public protected HMRoom (IntPtr handle)
```

### Type Changed: HomeKit.HMService

Modified constructors:

```
public protected HMService (Foundation.NSObjectFlag t)
	public protected HMService (IntPtr handle)
```

### Type Changed: HomeKit.HMServiceGroup

Modified constructors:

```
public protected HMServiceGroup (Foundation.NSObjectFlag t)
	public protected HMServiceGroup (IntPtr handle)
```

### Type Changed: HomeKit.HMTimerTrigger

Modified constructors:

```
public protected HMTimerTrigger (Foundation.NSObjectFlag t)
	public protected HMTimerTrigger (IntPtr handle)
```

### Type Changed: HomeKit.HMTrigger

Modified constructors:

```
public protected HMTrigger (Foundation.NSObjectFlag t)
	public protected HMTrigger (IntPtr handle)
```

### Type Changed: HomeKit.HMUser

Modified constructors:

```
public protected HMUser (Foundation.NSObjectFlag t)
	public protected HMUser (IntPtr handle)
```

### Type Changed: HomeKit.HMZone

Modified constructors:

```
public protected HMZone (Foundation.NSObjectFlag t)
	public protected HMZone (IntPtr handle)
```

## Namespace iAd



### Type Changed: iAd.ADBannerView

Modified constructors:

```
public protected ADBannerView (Foundation.NSObjectFlag t)
	public protected ADBannerView (IntPtr handle)
```

Modified properties:

```
public ADBannerViewDelegate IADBannerViewDelegate Delegate { get; set; }
```

### Type Changed: iAd.ADBannerViewDelegate

Modified constructors:

```
public protected ADBannerViewDelegate (Foundation.NSObjectFlag t)
	public protected ADBannerViewDelegate (IntPtr handle)
```

### Type Changed: iAd.ADClient

Modified constructors:

```
public protected ADClient (Foundation.NSObjectFlag t)
	public protected ADClient (IntPtr handle)
```

### Type Changed: iAd.ADInterstitialAd

Modified constructors:

```
public protected ADInterstitialAd (Foundation.NSObjectFlag t)
	public protected ADInterstitialAd (IntPtr handle)
```

Modified properties:

```
public ADInterstitialAdDelegate IADInterstitialAdDelegate Delegate { get; set; }
```

### Type Changed: iAd.ADInterstitialAdDelegate

Modified constructors:

```
public protected ADInterstitialAdDelegate ()
	public protected ADInterstitialAdDelegate (Foundation.NSObjectFlag t)
	public protected ADInterstitialAdDelegate (IntPtr handle)
```

### Type Changed: iAd.IAdAdditions

Removed method:

```
public static void PrepareInterstitialAds (UIKit.UIViewController This);
```

### Type Changed: iAd.IAdPreroll

Removed methods:

```
public static void PlayPrerollAd (MediaPlayer.MPMoviePlayerController This, PlayPrerollAdCompletionHandler completionHandler);
	public static void PreparePrerollAds (MediaPlayer.MPMoviePlayerController This);
```

Added method:

```
public static void PlayPrerollAd (MediaPlayer.MPMoviePlayerController This, System.Action<Foundation.NSError> completionHandler);
```

### Type Changed: iAd.iAdPreroll_AVPlayerViewController

Removed method:

```
public static void PreparePrerollAds (AVKit.AVPlayerViewController This);
```

### Removed Type iAd.PlayPrerollAdCompletionHandler 

## Namespace ImageIO



### Type Changed: ImageIO.CGImageDestination

Removed methods:

```
public bool CopyImageSource (CGImageSource image, CGImageDestinationOptions options, out Foundation.NSError error);
	public static CGImageDestination FromData (Foundation.NSData data, string typeIdentifier, int imageCount);
	public static CGImageDestination FromData (Foundation.NSData data, string typeIdentifier, int imageCount, CGImageDestinationOptions options);
	public static CGImageDestination FromUrl (Foundation.NSUrl url, string typeIdentifier, int imageCount);
	public static CGImageDestination FromUrl (Foundation.NSUrl url, string typeIdentifier, int imageCount, CGImageDestinationOptions options);
```

Added methods:

```
public bool CopyImageSource (CGImageSource image, CGCopyImageSourceOptions options, out Foundation.NSError error);
	public static CGImageDestination Create (Foundation.NSMutableData data, string typeIdentifier, int imageCount, CGImageDestinationOptions options);
	public static CGImageDestination Create (Foundation.NSUrl url, string typeIdentifier, int imageCount);
```

### Type Changed: ImageIO.CGImageDestinationOptions

Added constructor:

```
public CGImageDestinationOptions (Foundation.NSDictionary dictionary);
```

Removed properties:

```
public System.DateTime? DateTime { get; set; }
	public bool MergeMetadata { get; set; }
	public CGImageMetadata Metadata { get; set; }
	public int? Orientation { get; set; }
	public bool ShouldExcludeGPS { get; set; }
	public bool ShouldExcludeXMP { get; set; }
```

Modified properties:

```
public bool bool? EmbedThumbnail { get; set; }
```

Added properties:

```
public Foundation.NSDictionary CiffDictionary { get; set; }
	public Foundation.NSDictionary DngDictionary { get; set; }
	public Foundation.NSDictionary EightBimDictionary { get; set; }
	public Foundation.NSDictionary ExifAuxDictionary { get; set; }
	public CoreGraphics.CGImagePropertiesExif ExifDictionary { get; set; }
	public Foundation.NSDictionary GifDictionary { get; set; }
	public CoreGraphics.CGImagePropertiesGps GpsDictionary { get; set; }
	public CoreGraphics.CGImagePropertiesIptc IptcDictionary { get; set; }
	public CoreGraphics.CGImagePropertiesJfif JfifDictionary { get; set; }
	public CoreGraphics.CGImagePropertiesPng PngDictionary { get; set; }
	public Foundation.NSDictionary RawDictionary { get; set; }
	public CoreGraphics.CGImagePropertiesTiff TiffDictionary { get; set; }
```

### Type Changed: ImageIO.CGImageSource

Removed method:

```
[Obsolete ("Use UpdateDataProvider(CGDataProvider,bool)")]
	public void UpdateDataProvider (CoreGraphics.CGDataProvider provider);
```

### New Type ImageIO.CGCopyImageSourceOptions

```
public class CGCopyImageSourceOptions {
	// constructors
	public CGCopyImageSourceOptions ();
	// properties
	public System.DateTime? DateTime { get; set; }
	public bool MergeMetadata { get; set; }
	public CGImageMetadata Metadata { get; set; }
	public int? Orientation { get; set; }
	public bool ShouldExcludeGPS { get; set; }
	public bool ShouldExcludeXMP { get; set; }
}
```

### New Type ImageIO.CGImageDestinationOptionsKeys

```
public static class CGImageDestinationOptionsKeys {
	// properties
	public static Foundation.NSString BackgroundColor { get; }
	public static Foundation.NSString CIFFDictionary { get; }
	public static Foundation.NSString DNGDictionary { get; }
	public static Foundation.NSString EightBIMDictionary { get; }
	public static Foundation.NSString EmbedThumbnail { get; }
	public static Foundation.NSString ExifAuxDictionary { get; }
	public static Foundation.NSString ExifDictionary { get; }
	public static Foundation.NSString GIFDictionary { get; }
	public static Foundation.NSString GPSDictionary { get; }
	public static Foundation.NSString ImageMaxPixelSize { get; }
	public static Foundation.NSString IPTCDictionary { get; }
	public static Foundation.NSString JFIFDictionary { get; }
	public static Foundation.NSString LossyCompressionQuality { get; }
	public static Foundation.NSString PNGDictionary { get; }
	public static Foundation.NSString RawDictionary { get; }
	public static Foundation.NSString TIFFDictionary { get; }
}
```

## Namespace JavaScriptCore



### Type Changed: JavaScriptCore.JSContext

Modified constructors:

```
public protected JSContext (Foundation.NSObjectFlag t)
	public protected JSContext (IntPtr handle)
```

### Type Changed: JavaScriptCore.JSExport

Modified constructors:

```
public protected JSExport (Foundation.NSObjectFlag t)
	public protected JSExport (IntPtr handle)
```

### Type Changed: JavaScriptCore.JSManagedValue

Modified constructors:

```
public protected JSManagedValue (Foundation.NSObjectFlag t)
	public protected JSManagedValue (IntPtr handle)
```

### Type Changed: JavaScriptCore.JSValue

Modified constructors:

```
public protected JSValue (Foundation.NSObjectFlag t)
	public protected JSValue (IntPtr handle)
```

### Type Changed: JavaScriptCore.JSVirtualMachine

Modified constructors:

```
public protected JSVirtualMachine (Foundation.NSObjectFlag t)
	public protected JSVirtualMachine (IntPtr handle)
```

### Removed Type JavaScriptCore.JSExport_Extensions 

## Namespace LocalAuthentication



### Type Changed: LocalAuthentication.LAContext

Modified constructors:

```
public protected LAContext (Foundation.NSObjectFlag t)
	public protected LAContext (IntPtr handle)
```

Removed method:

```
public virtual System.Threading.Tasks.Task<bool> EvaluatePolicyAsync (LAPolicy policy, string localizedReason);
```

Added method:

```
public virtual System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> EvaluatePolicyAsync (LAPolicy policy, string localizedReason);
```

## Namespace MapKit



### Type Changed: MapKit.IMKAnnotation

Modified properties:

```
public abstract CoreLocation.CLLocationCoordinate2D Coordinate { get; set; }
```

### Type Changed: MapKit.IMKOverlay

Added property:

```
public virtual MKMapRect BoundingMapRect { get; }
```

### Type Changed: MapKit.MKAnnotation

Modified constructors:

```
public protected MKAnnotation ()
	public protected MKAnnotation (Foundation.NSObjectFlag t)
	public protected MKAnnotation (IntPtr handle)
```

Modified properties:

```
public abstract CoreLocation.CLLocationCoordinate2D Coordinate { get; set; }
```

Added method:

```
public virtual void SetCoordinate (CoreLocation.CLLocationCoordinate2D value);
```

### Type Changed: MapKit.MKAnnotation_Extensions

Added method:

```
public static void SetCoordinate (IMKAnnotation This, CoreLocation.CLLocationCoordinate2D value);
```

### Type Changed: MapKit.MKAnnotationView

Removed constructor:

```
public MKAnnotationView (Foundation.NSObject annotation, string reuseIdentifier);
```

Modified constructors:

```
public protected MKAnnotationView (Foundation.NSObjectFlag t)
	public protected MKAnnotationView (IntPtr handle)
```

Added constructor:

```
public MKAnnotationView (IMKAnnotation annotation, string reuseIdentifier);
```

Modified properties:

```
public virtual Foundation.NSObject IMKAnnotation Annotation { get; set; }
```

### Type Changed: MapKit.MKCircle

Modified constructors:

```
public protected MKCircle (Foundation.NSObjectFlag t)
	public protected MKCircle (IntPtr handle)
```

Removed properties:

```
[Obsolete ("Use BoundingMapRect as it's part of the MKOverlay protocol")]
	public MKMapRect BoundingMap { get; }
	public override string Subtitle { get; }
	public override string Title { get; }
```

Added property:

```
public virtual bool CanReplaceMapContent { get; }
```

### Type Changed: MapKit.MKCircleRenderer

Modified constructors:

```
public protected MKCircleRenderer (Foundation.NSObjectFlag t)
	public protected MKCircleRenderer (IntPtr handle)
```

### Type Changed: MapKit.MKCircleView

Modified constructors:

```
public protected MKCircleView (Foundation.NSObjectFlag t)
	public protected MKCircleView (IntPtr handle)
```

### Type Changed: MapKit.MKDirections

Modified constructors:

```
public protected MKDirections (Foundation.NSObjectFlag t)
	public protected MKDirections (IntPtr handle)
```

### Type Changed: MapKit.MKDirectionsRequest

Modified constructors:

```
public protected MKDirectionsRequest (Foundation.NSObjectFlag t)
	public protected MKDirectionsRequest (IntPtr handle)
```

### Type Changed: MapKit.MKDirectionsResponse

Modified constructors:

```
public protected MKDirectionsResponse (Foundation.NSObjectFlag t)
	public protected MKDirectionsResponse (IntPtr handle)
```

### Type Changed: MapKit.MKDistanceFormatter

Modified constructors:

```
public protected MKDistanceFormatter (Foundation.NSObjectFlag t)
	public protected MKDistanceFormatter (IntPtr handle)
```

### Type Changed: MapKit.MKETAResponse

Modified constructors:

```
public protected MKETAResponse (Foundation.NSObjectFlag t)
	public protected MKETAResponse (IntPtr handle)
```

### Type Changed: MapKit.MKGeodesicPolyline

Modified constructors:

```
public protected MKGeodesicPolyline (Foundation.NSObjectFlag t)
	public protected MKGeodesicPolyline (IntPtr handle)
```

### Type Changed: MapKit.MKLocalSearch

Removed constructors:

```
[Obsolete ("This will not work on iOS8+")]
	public MKLocalSearch ();
```

Modified constructors:

```
public protected MKLocalSearch (Foundation.NSObjectFlag t)
	public protected MKLocalSearch (IntPtr handle)
```

Removed interface:

```
IMKLocalSearch
```

### Type Changed: MapKit.MKLocalSearchRequest

Modified constructors:

```
public protected MKLocalSearchRequest (Foundation.NSObjectFlag t)
	public protected MKLocalSearchRequest (IntPtr handle)
```

Removed interface:

```
IMKLocalSearchRequest
```

### Type Changed: MapKit.MKLocalSearchResponse

Modified constructors:

```
public protected MKLocalSearchResponse (Foundation.NSObjectFlag t)
	public protected MKLocalSearchResponse (IntPtr handle)
```

Removed interface:

```
IMKLocalSearchResponse
```

### Type Changed: MapKit.MKMapCamera

Modified constructors:

```
public protected MKMapCamera (Foundation.NSObjectFlag t)
	public protected MKMapCamera (IntPtr handle)
```

### Type Changed: MapKit.MKMapItem

Modified constructors:

```
public protected MKMapItem (Foundation.NSObjectFlag t)
	public protected MKMapItem (IntPtr handle)
```

### Type Changed: MapKit.MKMapRect

Removed method:

```
public MKMapRect Divide (double amount, CoreGraphics.CGRectEdge edge, out MKMapRect remainder);
```

Added method:

```
public MKMapRect Divide (double amount, System.Drawing.RectangleFEdge edge, out MKMapRect remainder);
```

### Type Changed: MapKit.MKMapSnapshot

Modified constructors:

```
public protected MKMapSnapshot (Foundation.NSObjectFlag t)
	public protected MKMapSnapshot (IntPtr handle)
```

### Type Changed: MapKit.MKMapSnapshotOptions

Modified constructors:

```
public protected MKMapSnapshotOptions (Foundation.NSObjectFlag t)
	public protected MKMapSnapshotOptions (IntPtr handle)
```

### Type Changed: MapKit.MKMapSnapshotter

Modified constructors:

```
public protected MKMapSnapshotter (Foundation.NSObjectFlag t)
	public protected MKMapSnapshotter (IntPtr handle)
```

### Type Changed: MapKit.MKMapView

Modified constructors:

```
public protected MKMapView (Foundation.NSObjectFlag t)
	public protected MKMapView (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use VisibleMapRect")]
	public virtual MKMapRect visibleMapRect { get; set; }
```

Modified properties:

```
public virtual Foundation.NSObject[] IMKAnnotation[] Annotations { get; }
	public MKMapViewDelegate IMKMapViewDelegate Delegate { get; set; }
	public virtual Foundation.NSObject[] IMKOverlay[] Overlays { get; }
	public virtual Foundation.NSObject[] IMKAnnotation[] SelectedAnnotations { get; set; }
```

Removed event:

```
public event System.EventHandler<MMapViewUserTrackingEventArgs> DidChageUserTrackingMode;
```

Added event:

```
public event System.EventHandler<MMapViewUserTrackingEventArgs> DidChangeUserTrackingMode;
```

Removed methods:

```
public void AddAnnotation (MKAnnotation annotation);

	[Obsolete ("Use AddPlacemarks")]
	public void AddAnnotation (MKPlacemark[] placemarks);

	[Obsolete ("Use AddAnnotations")]
	public void AddAnnotation (MKAnnotation[] annotations);
	public virtual void AddAnnotationObject (Foundation.NSObject annotation);
	public virtual void AddAnnotationObjects (Foundation.NSObject[] annotations);
	public void AddAnnotations (MKAnnotation[] annotations);
	public virtual void AddOverlay (Foundation.NSObject overlay);
	public virtual void AddOverlays (Foundation.NSObject[] overlays);
	public void AddPlacemark (MKPlacemark placemark);
	public void AddPlacemarks (MKPlacemark[] placemarks);
	public virtual void DeselectAnnotation (Foundation.NSObject annotation, bool animated);
	public virtual void InsertOverlay (Foundation.NSObject overlay, int index);
	public virtual void InsertOverlayAbove (Foundation.NSObject overlay, Foundation.NSObject sibling);
	public virtual void InsertOverlayBelow (Foundation.NSObject overlay, Foundation.NSObject sibling);
	public virtual void RemoveAnnotation (Foundation.NSObject annotation);
	public virtual void RemoveAnnotations (Foundation.NSObject[] annotations);
	public virtual void RemoveOverlay (Foundation.NSObject overlay);
	public virtual void RemoveOverlays (Foundation.NSObject[] overlays);
	public virtual void SelectAnnotation (Foundation.NSObject annotation, bool animated);
	public virtual MKAnnotationView ViewForAnnotation (Foundation.NSObject annotation);
	public virtual MKOverlayView ViewForOverlay (Foundation.NSObject overlay);
```

Modified methods:

```
public virtual void RemoveOverlays (IMKOverlay[] overlays)
```

Added methods:

```
public virtual void AddAnnotation (IMKAnnotation annotation);
	public virtual void AddAnnotations (IMKAnnotation[] annotations);
	public virtual void AddOverlay (IMKOverlay overlay);
	public virtual void AddOverlays (IMKOverlay[] overlays);
	public virtual void DeselectAnnotation (IMKAnnotation annotation, bool animated);
	public virtual void InsertOverlay (IMKOverlay overlay, int index);
	public virtual void InsertOverlayAbove (IMKOverlay overlay, IMKOverlay sibling);
	public virtual void InsertOverlayBelow (IMKOverlay overlay, IMKOverlay sibling);
	public virtual void RemoveAnnotation (IMKAnnotation annotation);
	public virtual void RemoveAnnotations (IMKAnnotation[] annotations);
	public virtual void RemoveOverlay (IMKOverlay overlay);
	public virtual void SelectAnnotation (IMKAnnotation annotation, bool animated);
	public virtual MKAnnotationView ViewForAnnotation (IMKAnnotation annotation);
	public virtual MKOverlayView ViewForOverlay (IMKOverlay overlay);
```

### Type Changed: MapKit.MKMapViewAnnotation

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (MKMapView mapView, Foundation.NSObject annotation, System.AsyncCallback callback, object object);
	public virtual MKAnnotationView Invoke (MKMapView mapView, Foundation.NSObject annotation);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (MKMapView mapView, IMKAnnotation annotation, System.AsyncCallback callback, object object);
	public virtual MKAnnotationView Invoke (MKMapView mapView, IMKAnnotation annotation);
```

### Type Changed: MapKit.MKMapViewDelegate

Modified constructors:

```
public protected MKMapViewDelegate (Foundation.NSObjectFlag t)
	public protected MKMapViewDelegate (IntPtr handle)
```

Removed methods:

```
public virtual void DidChageUserTrackingMode (MKMapView mapView, MKUserTrackingMode mode, bool animated);
	public virtual MKAnnotationView GetViewForAnnotation (MKMapView mapView, Foundation.NSObject annotation);
	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, Foundation.NSObject overlay);
```

Added methods:

```
public virtual void DidChangeUserTrackingMode (MKMapView mapView, MKUserTrackingMode mode, bool animated);
	public virtual MKAnnotationView GetViewForAnnotation (MKMapView mapView, IMKAnnotation annotation);
	public virtual MKOverlayView GetViewForOverlay (MKMapView mapView, IMKOverlay overlay);
```

### Type Changed: MapKit.MKMapViewDelegate_Extensions

Removed methods:

```
public static void DidChageUserTrackingMode (IMKMapViewDelegate This, MKMapView mapView, MKUserTrackingMode mode, bool animated);
	public static MKAnnotationView GetViewForAnnotation (IMKMapViewDelegate This, MKMapView mapView, Foundation.NSObject annotation);
	public static MKOverlayView GetViewForOverlay (IMKMapViewDelegate This, MKMapView mapView, Foundation.NSObject overlay);
```

Added methods:

```
public static void DidChangeUserTrackingMode (IMKMapViewDelegate This, MKMapView mapView, MKUserTrackingMode mode, bool animated);
	public static MKAnnotationView GetViewForAnnotation (IMKMapViewDelegate This, MKMapView mapView, IMKAnnotation annotation);
	public static MKOverlayView GetViewForOverlay (IMKMapViewDelegate This, MKMapView mapView, IMKOverlay overlay);
```

### Type Changed: MapKit.MKMapViewOverlay

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (MKMapView mapView, Foundation.NSObject overlay, System.AsyncCallback callback, object object);
	public virtual MKOverlayView Invoke (MKMapView mapView, Foundation.NSObject overlay);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (MKMapView mapView, IMKOverlay overlay, System.AsyncCallback callback, object object);
	public virtual MKOverlayView Invoke (MKMapView mapView, IMKOverlay overlay);
```

### Type Changed: MapKit.MKMultiPoint

Modified constructors:

```
public protected MKMultiPoint (Foundation.NSObjectFlag t)
	public protected MKMultiPoint (IntPtr handle)
```

### Type Changed: MapKit.MKOverlay

Modified constructors:

```
public protected MKOverlay ()
	public protected MKOverlay (Foundation.NSObjectFlag t)
	public protected MKOverlay (IntPtr handle)
```

Removed properties:

```
public override CoreLocation.CLLocationCoordinate2D Coordinate { get; set; }
	public override string Subtitle { get; }
	public override string Title { get; }
```

Modified properties:

```
public abstract MKMapRect BoundingMapRect { get; }
```

Added property:

```
public virtual bool CanReplaceMapContent { get; }
```

### Type Changed: MapKit.MKOverlay_Extensions

Removed method:

```
public static MKMapRect GetBoundingMapRect (IMKOverlay This);
```

Added method:

```
public static bool GetCanReplaceMapContent (IMKOverlay This);
```

### Type Changed: MapKit.MKOverlayPathRenderer

Modified constructors:

```
public protected MKOverlayPathRenderer (Foundation.NSObjectFlag t)
	public protected MKOverlayPathRenderer (IntPtr handle)
```

### Type Changed: MapKit.MKOverlayPathView

Modified constructors:

```
public protected MKOverlayPathView (Foundation.NSObjectFlag t)
	public protected MKOverlayPathView (IntPtr handle)
```

### Type Changed: MapKit.MKOverlayRenderer

Modified constructors:

```
public protected MKOverlayRenderer (Foundation.NSObjectFlag t)
	public protected MKOverlayRenderer (IntPtr handle)
```

### Type Changed: MapKit.MKOverlayView

Removed constructor:

```
public MKOverlayView (Foundation.NSObject overlay);
```

Modified constructors:

```
public protected MKOverlayView (Foundation.NSObjectFlag t)
	public protected MKOverlayView (IntPtr handle)
```

Added constructor:

```
public MKOverlayView (IMKOverlay overlay);
```

Modified properties:

```
public virtual Foundation.NSObject IMKOverlay Overlay { get; }
```

### Type Changed: MapKit.MKPinAnnotationView

Removed constructor:

```
public MKPinAnnotationView (Foundation.NSObject annotation, string reuseIdentifier);
```

Modified constructors:

```
public protected MKPinAnnotationView (Foundation.NSObjectFlag t)
	public protected MKPinAnnotationView (IntPtr handle)
```

Added constructor:

```
public MKPinAnnotationView (IMKAnnotation annotation, string reuseIdentifier);
```

### Type Changed: MapKit.MKPlacemark

Modified constructors:

```
public protected MKPlacemark (Foundation.NSObjectFlag t)
	public protected MKPlacemark (IntPtr handle)
```

Modified properties:

```
public virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; set; }
```

Added method:

```
public virtual void SetCoordinate (CoreLocation.CLLocationCoordinate2D value);
```

### Type Changed: MapKit.MKPointAnnotation

Modified constructors:

```
public protected MKPointAnnotation (Foundation.NSObjectFlag t)
	public protected MKPointAnnotation (IntPtr handle)
```

### Type Changed: MapKit.MKPolygon

Modified constructors:

```
public protected MKPolygon (Foundation.NSObjectFlag t)
	public protected MKPolygon (IntPtr handle)
```

Removed properties:

```
public override string Subtitle { get; }
	public override string Title { get; }
```

Added property:

```
public virtual bool CanReplaceMapContent { get; }
```

Removed method:

```
public static MKPolygon _FromPoints (IntPtr points, int count, MKPolygon[] interiorPolygons);
```

### Type Changed: MapKit.MKPolygonRenderer

Modified constructors:

```
public protected MKPolygonRenderer (Foundation.NSObjectFlag t)
	public protected MKPolygonRenderer (IntPtr handle)
```

### Type Changed: MapKit.MKPolygonView

Modified constructors:

```
public protected MKPolygonView (Foundation.NSObjectFlag t)
	public protected MKPolygonView (IntPtr handle)
```

### Type Changed: MapKit.MKPolyline

Modified constructors:

```
public protected MKPolyline (Foundation.NSObjectFlag t)
	public protected MKPolyline (IntPtr handle)
```

Removed properties:

```
public override string Subtitle { get; }
	public override string Title { get; }
```

Added property:

```
public virtual bool CanReplaceMapContent { get; }
```

### Type Changed: MapKit.MKPolylineRenderer

Modified constructors:

```
public protected MKPolylineRenderer (Foundation.NSObjectFlag t)
	public protected MKPolylineRenderer (IntPtr handle)
```

### Type Changed: MapKit.MKPolylineView

Modified constructors:

```
public protected MKPolylineView (Foundation.NSObjectFlag t)
	public protected MKPolylineView (IntPtr handle)
```

### Type Changed: MapKit.MKReverseGeocoder

Modified constructors:

```
public protected MKReverseGeocoder (Foundation.NSObjectFlag t)
	public protected MKReverseGeocoder (IntPtr handle)
```

Modified properties:

```
public MKReverseGeocoderDelegate IMKReverseGeocoderDelegate Delegate { get; set; }
```

### Type Changed: MapKit.MKReverseGeocoderDelegate

Modified constructors:

```
public protected MKReverseGeocoderDelegate ()
	public protected MKReverseGeocoderDelegate (Foundation.NSObjectFlag t)
	public protected MKReverseGeocoderDelegate (IntPtr handle)
```

### Type Changed: MapKit.MKRoute

Modified constructors:

```
public protected MKRoute (Foundation.NSObjectFlag t)
	public protected MKRoute (IntPtr handle)
```

### Type Changed: MapKit.MKRouteStep

Modified constructors:

```
public protected MKRouteStep (Foundation.NSObjectFlag t)
	public protected MKRouteStep (IntPtr handle)
```

### Type Changed: MapKit.MKShape

Modified constructors:

```
public protected MKShape ()
	public protected MKShape (Foundation.NSObjectFlag t)
	public protected MKShape (IntPtr handle)
```

Modified properties:

```
public override virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; set; }
```

Added method:

```
public virtual void SetCoordinate (CoreLocation.CLLocationCoordinate2D value);
```

### Type Changed: MapKit.MKTileOverlay

Modified constructors:

```
public protected MKTileOverlay (Foundation.NSObjectFlag t)
	public protected MKTileOverlay (IntPtr handle)
```

Modified properties:

```
public override virtual MKMapRect BoundingMapRect { get; }
```

Added property:

```
public virtual CoreLocation.CLLocationCoordinate2D Coordinate { get; }
```

Modified methods:

```
public override virtual bool Intersects (MKMapRect rect)
```

### Type Changed: MapKit.MKTileOverlayRenderer

Removed constructors:

```
[Obsolete ("This will not work on iOS8+")]
	public MKTileOverlayRenderer ();
```

Modified constructors:

```
public protected MKTileOverlayRenderer (Foundation.NSObjectFlag t)
	public protected MKTileOverlayRenderer (IntPtr handle)
```

### Type Changed: MapKit.MKUserLocation

Modified constructors:

```
public protected MKUserLocation (Foundation.NSObjectFlag t)
	public protected MKUserLocation (IntPtr handle)
```

### Type Changed: MapKit.MKUserTrackingBarButtonItem

Modified constructors:

```
public protected MKUserTrackingBarButtonItem (Foundation.NSObjectFlag t)
	public protected MKUserTrackingBarButtonItem (IntPtr handle)
```

### Removed Type MapKit.IMKLocalSearch ### Removed Type MapKit.IMKLocalSearchRequest ### Removed Type MapKit.IMKLocalSearchResponse ### Removed Type MapKit.MKLocalSearch_Extensions ### Removed Type MapKit.MKLocalSearchRequest_Extensions ### Removed Type MapKit.MKLocalSearchResponse_Extensions ### Removed Type MapKit.MKReverseGeocoderDelegate_Extensions 



## Namespace MediaPlayer



### Type Changed: MediaPlayer.IMPPlayableContentDataSource

Added methods:

```
public virtual MPContentItem ContentItem (Foundation.NSIndexPath indexPath);
	public virtual int NumberOfChildItems (Foundation.NSIndexPath indexPath);
```

### Type Changed: MediaPlayer.MPChangePlaybackRateCommand

Modified constructors:

```
public protected MPChangePlaybackRateCommand (Foundation.NSObjectFlag t)
	public protected MPChangePlaybackRateCommand (IntPtr handle)
```

### Type Changed: MediaPlayer.MPChangePlaybackRateCommandEvent

Modified constructors:

```
public protected MPChangePlaybackRateCommandEvent (Foundation.NSObjectFlag t)
	public protected MPChangePlaybackRateCommandEvent (IntPtr handle)
```

### Type Changed: MediaPlayer.MPContentItem

Modified constructors:

```
public protected MPContentItem (Foundation.NSObjectFlag t)
	public protected MPContentItem (IntPtr handle)
```

### Type Changed: MediaPlayer.MPFeedbackCommand

Modified constructors:

```
public protected MPFeedbackCommand (Foundation.NSObjectFlag t)
	public protected MPFeedbackCommand (IntPtr handle)
```

### Type Changed: MediaPlayer.MPFeedbackCommandEvent

Modified constructors:

```
public protected MPFeedbackCommandEvent (Foundation.NSObjectFlag t)
	public protected MPFeedbackCommandEvent (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMediaItem

Modified constructors:

```
public protected MPMediaItem (Foundation.NSObjectFlag t)
	public protected MPMediaItem (IntPtr handle)
```

Removed methods:

```
[Obsolete ("Use CanFilterByProperty (NSString) instead")]
	public static bool CanFilterByProperty (string property);
	public static bool CanFilterByProperty (Foundation.NSString property);
	public virtual void EnumerateValues (Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);

	[Obsolete ("Use ValueForProperty (NSString) instead")]
	public virtual Foundation.NSObject ValueForProperty (string property);
	public virtual Foundation.NSObject ValueForProperty (Foundation.NSString property);
```

### Type Changed: MediaPlayer.MPMediaItemArtwork

Modified constructors:

```
public protected MPMediaItemArtwork (Foundation.NSObjectFlag t)
	public protected MPMediaItemArtwork (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMediaItemCollection

Modified constructors:

```
public protected MPMediaItemCollection (Foundation.NSObjectFlag t)
	public protected MPMediaItemCollection (IntPtr handle)
```

Added methods:

```
public static bool CanFilterByProperty (Foundation.NSString property);
	public virtual void EnumerateValues (Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);
	public virtual Foundation.NSObject ValueForProperty (Foundation.NSString property);
```

### Type Changed: MediaPlayer.MPMediaLibrary

Modified constructors:

```
public protected MPMediaLibrary (Foundation.NSObjectFlag t)
	public protected MPMediaLibrary (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMediaPickerController

Modified constructors:

```
public protected MPMediaPickerController (Foundation.NSObjectFlag t)
	public protected MPMediaPickerController (IntPtr handle)
```

Modified properties:

```
public MPMediaPickerControllerDelegate IMPMediaPickerControllerDelegate Delegate { get; set; }
```

### Type Changed: MediaPlayer.MPMediaPickerControllerDelegate

Modified constructors:

```
public protected MPMediaPickerControllerDelegate (Foundation.NSObjectFlag t)
	public protected MPMediaPickerControllerDelegate (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMediaPlaylist

Modified constructors:

```
public protected MPMediaPlaylist (Foundation.NSObjectFlag t)
	public protected MPMediaPlaylist (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMediaPredicate

Modified constructors:

```
public protected MPMediaPredicate (Foundation.NSObjectFlag t)
	public protected MPMediaPredicate (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMediaPropertyPredicate

Modified constructors:

```
public protected MPMediaPropertyPredicate (Foundation.NSObjectFlag t)
	public protected MPMediaPropertyPredicate (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMediaQuery

Modified constructors:

```
public protected MPMediaQuery (Foundation.NSObjectFlag t)
	public protected MPMediaQuery (IntPtr handle)
```

Removed properties:

```
public static MPMediaQuery albumsQuery { get; }
	public static MPMediaQuery artistsQuery { get; }
	public static MPMediaQuery audiobooksQuery { get; }
	public static MPMediaQuery compilationsQuery { get; }
	public static MPMediaQuery composersQuery { get; }
	public static MPMediaQuery genresQuery { get; }
	public static MPMediaQuery playlistsQuery { get; }
	public static MPMediaQuery podcastsQuery { get; }
	public static MPMediaQuery songsQuery { get; }
```

Added properties:

```
public static MPMediaQuery AlbumsQuery { get; }
	public static MPMediaQuery ArtistsQuery { get; }
	public static MPMediaQuery AudiobooksQuery { get; }
	public static MPMediaQuery CompilationsQuery { get; }
	public static MPMediaQuery ComposersQuery { get; }
	public static MPMediaQuery GenresQuery { get; }
	public static MPMediaQuery PlaylistsQuery { get; }
	public static MPMediaQuery PodcastsQuery { get; }
	public static MPMediaQuery SongsQuery { get; }
```

Removed methods:

```
public MPMediaItemCollection GetCollection (int index);
	public MPMediaItem GetItem (int index);
	public MPMediaQuerySection GetSection (int index);
```

Added methods:

```
public MPMediaItemCollection GetCollection (uint index);
	public MPMediaItem GetItem (uint index);
	public MPMediaQuerySection GetSection (uint index);
```

### Type Changed: MediaPlayer.MPMediaQuerySection

Modified constructors:

```
public protected MPMediaQuerySection (Foundation.NSObjectFlag t)
	public protected MPMediaQuerySection (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMediaType

Removed values:

```
[Obsolete ("Use Shorter name AnyAudio")]
	MPMediaTypeAnyAudio = 255,

	[Obsolete ("Use Shorter name AudioBook")]
	MPMediaTypeAudioBook = 4,

	[Obsolete ("Use Shorter name Music")]
	MPMediaTypeMusic = 1,

	[Obsolete ("Use Shorter name Podcast")]
	MPMediaTypePodcast = 2,
```

Modified fields:

```
Any = -1 18446744073709551615
```

### Type Changed: MediaPlayer.MPMovieAccessLog

Modified constructors:

```
public protected MPMovieAccessLog (Foundation.NSObjectFlag t)
	public protected MPMovieAccessLog (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMovieAccessLogEvent

Modified constructors:

```
public protected MPMovieAccessLogEvent (Foundation.NSObjectFlag t)
	public protected MPMovieAccessLogEvent (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMovieErrorLog

Modified constructors:

```
public protected MPMovieErrorLog (Foundation.NSObjectFlag t)
	public protected MPMovieErrorLog (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMovieErrorLogEvent

Modified constructors:

```
public protected MPMovieErrorLogEvent (Foundation.NSObjectFlag t)
	public protected MPMovieErrorLogEvent (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMoviePlayerController

Modified constructors:

```
public protected MPMoviePlayerController (Foundation.NSObjectFlag t)
	public protected MPMoviePlayerController (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMoviePlayerViewController

Modified constructors:

```
public protected MPMoviePlayerViewController (Foundation.NSObjectFlag t)
	public protected MPMoviePlayerViewController (IntPtr handle)
```

### Type Changed: MediaPlayer.MPMusicPlayerController

Modified constructors:

```
public protected MPMusicPlayerController (Foundation.NSObjectFlag t)
	public protected MPMusicPlayerController (IntPtr handle)
```

### Type Changed: MediaPlayer.MPNowPlayingInfoCenter

Modified constructors:

```
public protected MPNowPlayingInfoCenter (Foundation.NSObjectFlag t)
	public protected MPNowPlayingInfoCenter (IntPtr handle)
```

### Type Changed: MediaPlayer.MPPlayableContentDataSource

Modified constructors:

```
public protected MPPlayableContentDataSource ()
	public protected MPPlayableContentDataSource (Foundation.NSObjectFlag t)
	public protected MPPlayableContentDataSource (IntPtr handle)
```

Modified methods:

```
public abstract MPContentItem ContentItem (Foundation.NSIndexPath indexPath)
	public abstract int NumberOfChildItems (Foundation.NSIndexPath indexPath)
```

### Type Changed: MediaPlayer.MPPlayableContentDataSource_Extensions

Removed methods:

```
public static MPContentItem ContentItem (IMPPlayableContentDataSource This, Foundation.NSIndexPath indexPath);
	public static int NumberOfChildItems (IMPPlayableContentDataSource This, Foundation.NSIndexPath indexPath);
```

### Type Changed: MediaPlayer.MPPlayableContentDelegate

Modified constructors:

```
public protected MPPlayableContentDelegate (Foundation.NSObjectFlag t)
	public protected MPPlayableContentDelegate (IntPtr handle)
```

### Type Changed: MediaPlayer.MPPlayableContentManager

Modified constructors:

```
public protected MPPlayableContentManager (Foundation.NSObjectFlag t)
	public protected MPPlayableContentManager (IntPtr handle)
```

Modified properties:

```
public MPPlayableContentDataSource IMPPlayableContentDataSource DataSource { get; set; }
	public MPPlayableContentDelegate IMPPlayableContentDelegate Delegate { get; set; }
```

### Type Changed: MediaPlayer.MPRatingCommand

Modified constructors:

```
public protected MPRatingCommand (Foundation.NSObjectFlag t)
	public protected MPRatingCommand (IntPtr handle)
```

### Type Changed: MediaPlayer.MPRatingCommandEvent

Modified constructors:

```
public protected MPRatingCommandEvent (Foundation.NSObjectFlag t)
	public protected MPRatingCommandEvent (IntPtr handle)
```

### Type Changed: MediaPlayer.MPRemoteCommand

Modified constructors:

```
public protected MPRemoteCommand (Foundation.NSObjectFlag t)
	public protected MPRemoteCommand (IntPtr handle)
```

### Type Changed: MediaPlayer.MPRemoteCommandCenter

Modified constructors:

```
public protected MPRemoteCommandCenter (Foundation.NSObjectFlag t)
	public protected MPRemoteCommandCenter (IntPtr handle)
```

### Type Changed: MediaPlayer.MPRemoteCommandEvent

Modified constructors:

```
public protected MPRemoteCommandEvent (Foundation.NSObjectFlag t)
	public protected MPRemoteCommandEvent (IntPtr handle)
```

### Type Changed: MediaPlayer.MPSeekCommandEvent

Modified constructors:

```
public protected MPSeekCommandEvent (Foundation.NSObjectFlag t)
	public protected MPSeekCommandEvent (IntPtr handle)
```

### Type Changed: MediaPlayer.MPSkipIntervalCommand

Modified constructors:

```
public protected MPSkipIntervalCommand (Foundation.NSObjectFlag t)
	public protected MPSkipIntervalCommand (IntPtr handle)
```

Removed property:

```
public virtual Foundation.NSArray _PreferredIntervals { get; set; }
```

### Type Changed: MediaPlayer.MPSkipIntervalCommandEvent

Modified constructors:

```
public protected MPSkipIntervalCommandEvent (Foundation.NSObjectFlag t)
	public protected MPSkipIntervalCommandEvent (IntPtr handle)
```

### Type Changed: MediaPlayer.MPTimedMetadata

Modified constructors:

```
public protected MPTimedMetadata (Foundation.NSObjectFlag t)
	public protected MPTimedMetadata (IntPtr handle)
```

### Type Changed: MediaPlayer.MPVolumeView

Modified constructors:

```
public protected MPVolumeView (Foundation.NSObjectFlag t)
	public protected MPVolumeView (IntPtr handle)
```

### Removed Type MediaPlayer.MPMediaItemProperty ### Removed Type MediaPlayer.MPMediaPlayback_Extensions ### New Type MediaPlayer.MPMediaEntity

```
public class MPMediaEntity : Foundation.NSObject, Foundation.INSCoding, Foundation.INSSecureCoding, ObjCRuntime.INativeObject, System.IDisposable, System.IEquatable<Foundation.NSObject>, Foundation.INSObjectProtocol {
	// constructors
	public MPMediaEntity ();
	public MPMediaEntity (Foundation.NSCoder coder);
	protected MPMediaEntity (Foundation.NSObjectFlag t);
	protected MPMediaEntity (IntPtr handle);
	// properties
	public override IntPtr ClassHandle { get; }
	// methods
	public static bool CanFilterByProperty (Foundation.NSString property);
	public virtual void EncodeTo (Foundation.NSCoder encoder);
	public virtual void EnumerateValues (Foundation.NSSet propertiesToEnumerate, MPMediaItemEnumerator enumerator);
	public virtual Foundation.NSObject ValueForProperty (Foundation.NSString property);
}
```





## Namespace MediaToolbox



### Type Changed: MediaToolbox.MTAudioProcessingTap

Removed methods:

```
[Obsolete ("Use overload with AudioBuffers")]
	public MTAudioProcessingTapError GetSourceAudio (long frames, ref AudioToolbox.AudioBufferList bufferList, out MTAudioProcessingTapFlags flags, out CoreMedia.CMTimeRange timeRange, long framesProvided);

	[Obsolete ("Use GetSourceAudio(int,AudioBuffers,out MTAudioProcessingTapFlags, out CMTimeRange, out int) instead")]
	public MTAudioProcessingTapError GetSourceAudio (long frames, AudioToolbox.AudioBuffers bufferList, out MTAudioProcessingTapFlags flags, out CoreMedia.CMTimeRange timeRange, long framesProvided);
```

### Type Changed: MediaToolbox.MTAudioProcessingTapCallbacks

Removed constructor:

```
[Obsolete ("Use constructor with MTAudioProcessingTapProcessDelegate")]
	public MTAudioProcessingTapCallbacks (MTAudioProcessingTapProcessCallback process);
```

Removed property:

```
[Obsolete ("Use Processing property instead")]
	public MTAudioProcessingTapProcessCallback Process { get; }
```

### Type Changed: MediaToolbox.MTAudioProcessingTapPrepareCallback

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (MTAudioProcessingTap tap, long maxFrames, ref AudioToolbox.AudioStreamBasicDescription processingFormat, System.AsyncCallback callback, object object);
	public virtual void Invoke (MTAudioProcessingTap tap, long maxFrames, ref AudioToolbox.AudioStreamBasicDescription processingFormat);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (MTAudioProcessingTap tap, int maxFrames, ref AudioToolbox.AudioStreamBasicDescription processingFormat, System.AsyncCallback callback, object object);
	public virtual void Invoke (MTAudioProcessingTap tap, int maxFrames, ref AudioToolbox.AudioStreamBasicDescription processingFormat);
```

### Type Changed: MediaToolbox.MTAudioProcessingTapProcessDelegate

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (MTAudioProcessingTap tap, long numberFrames, MTAudioProcessingTapFlags flags, AudioToolbox.AudioBuffers bufferList, out long numberFramesOut, out MTAudioProcessingTapFlags flagsOut, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out long numberFramesOut, out MTAudioProcessingTapFlags flagsOut, System.IAsyncResult result);
	public virtual void Invoke (MTAudioProcessingTap tap, long numberFrames, MTAudioProcessingTapFlags flags, AudioToolbox.AudioBuffers bufferList, out long numberFramesOut, out MTAudioProcessingTapFlags flagsOut);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (MTAudioProcessingTap tap, int numberFrames, MTAudioProcessingTapFlags flags, AudioToolbox.AudioBuffers bufferList, out int numberFramesOut, out MTAudioProcessingTapFlags flagsOut, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (out int numberFramesOut, out MTAudioProcessingTapFlags flagsOut, System.IAsyncResult result);
	public virtual void Invoke (MTAudioProcessingTap tap, int numberFrames, MTAudioProcessingTapFlags flags, AudioToolbox.AudioBuffers bufferList, out int numberFramesOut, out MTAudioProcessingTapFlags flagsOut);
```

### Removed Type MediaToolbox.MTAudioProcessingTapProcessCallback 

## Namespace MessageUI



### Type Changed: MessageUI.MFMailComposeViewController

Modified constructors:

```
public protected MFMailComposeViewController (Foundation.NSObjectFlag t)
	public protected MFMailComposeViewController (IntPtr handle)
```

Modified properties:

```
public MFMailComposeViewControllerDelegate IMFMailComposeViewControllerDelegate MailComposeDelegate { get; set; }
```

### Type Changed: MessageUI.MFMailComposeViewControllerDelegate

Modified constructors:

```
public protected MFMailComposeViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected MFMailComposeViewControllerDelegate (IntPtr handle)
```

Removed methods:

```
public override void DidShowViewController (UIKit.UINavigationController navigationController, UIKit.UIViewController viewController, bool animated);
	public override UIKit.IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UIKit.UINavigationController navigationController, UIKit.UINavigationControllerOperation operation, UIKit.UIViewController fromViewController, UIKit.UIViewController toViewController);
	public override UIKit.IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UIKit.UINavigationController navigationController, UIKit.IUIViewControllerAnimatedTransitioning animationController);
	public override UIKit.UIInterfaceOrientation GetPreferredInterfaceOrientation (UIKit.UINavigationController navigationController);
	public override UIKit.UIInterfaceOrientationMask SupportedInterfaceOrientations (UIKit.UINavigationController navigationController);
	public override void WillShowViewController (UIKit.UINavigationController navigationController, UIKit.UIViewController viewController, bool animated);
```

### Type Changed: MessageUI.MFMessageComposeViewController

Modified constructors:

```
public protected MFMessageComposeViewController (Foundation.NSObjectFlag t)
	public protected MFMessageComposeViewController (IntPtr handle)
```

Modified properties:

```
public MFMessageComposeViewControllerDelegate IMFMessageComposeViewControllerDelegate MessageComposeDelegate { get; set; }
```

### Type Changed: MessageUI.MFMessageComposeViewControllerDelegate

Modified constructors:

```
public protected MFMessageComposeViewControllerDelegate ()
	public protected MFMessageComposeViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected MFMessageComposeViewControllerDelegate (IntPtr handle)
```

### Removed Type MessageUI.MFMessageComposeViewControllerDelegate_Extensions 

## Namespace Metal



### Type Changed: Metal.IMTLCommandBuffer

Added methods:

```
public virtual IMTLParallelRenderCommandEncoder CreateParallelRenderCommandEncoder (MTLRenderPassDescriptor renderPassDescriptor);
	public virtual IMTLRenderCommandEncoder CreateRenderCommandEncoder (MTLRenderPassDescriptor renderPassDescriptor);
	public virtual void PresentDrawable (IMTLDrawable drawable);
	public virtual void PresentDrawable (IMTLDrawable drawable, double presentationTime);
```

### Type Changed: Metal.IMTLComputeCommandEncoder

Removed method:

```
public virtual void SispatchThreadgroups (MTLSize threadgroupsPerGrid, MTLSize threadsPerThreadgroup);
```

Added methods:

```
public virtual void DispatchThreadgroups (MTLSize threadgroupsPerGrid, MTLSize threadsPerThreadgroup);
	public virtual void SetBuffers (IMTLBuffer[] buffers, IntPtr offsets, Foundation.NSRange range);
	public virtual void SetSamplerStates (IMTLSamplerState[] samplers, Foundation.NSRange range);
	public virtual void SetSamplerStates (IMTLSamplerState[] samplers, IntPtr floatArrayPtrLodMinClamps, IntPtr floatArrayPtrLodMaxClamps, Foundation.NSRange range);
	public virtual void SetTextures (IMTLTexture[] textures, Foundation.NSRange range);
```

### Type Changed: Metal.IMTLDepthStencilState

Added properties:

```
public virtual IMTLDevice Device { get; }
	public virtual string Label { get; }
```

### Type Changed: Metal.IMTLDevice

Added methods:

```
public virtual IMTLComputePipelineState CreateComputePipelineState (IMTLFunction computeFunction, MTLPipelineOption options, out MTLComputePipelineReflection reflection, out Foundation.NSError error);
	public virtual void CreateComputePipelineState (IMTLFunction computeFunction, System.Action<IMTLComputePipelineState,Foundation.NSError> completionHandler);
	public virtual void CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, System.Action<IMTLRenderPipelineState,Metal.MTLRenderPipelineReflection,Foundation.NSError> completionHandler);
	public virtual IMTLRenderPipelineState CreateRenderPipelineState (MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, out MTLRenderPipelineReflection reflection, out Foundation.NSError error);
```

### Type Changed: Metal.IMTLRenderCommandEncoder

Added method:

```
public virtual void SetVertexTextures (IMTLTexture[] textures, Foundation.NSRange range);
```

### Type Changed: Metal.IMTLTexture

Added methods:

```
public virtual void GetBytes (IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage, MTLRegion region, uint level, uint slice);
	public virtual void GetBytes (IntPtr pixelBytes, uint bytesPerRow, MTLRegion region, uint level);
	public virtual void ReplaceRegion (MTLRegion region, uint level, uint slice, IntPtr pixelBytes, uint bytesPerRow, uint bytesPerImage);
	public virtual void ReplaceRegion (MTLRegion region, uint level, IntPtr pixelBytes, uint bytesPerRow);
```

### Type Changed: Metal.MTLArgument

Modified constructors:

```
public protected MTLArgument (Foundation.NSObjectFlag t)
	public protected MTLArgument (IntPtr handle)
```

### Type Changed: Metal.MTLArrayType

Modified constructors:

```
public protected MTLArrayType (Foundation.NSObjectFlag t)
	public protected MTLArrayType (IntPtr handle)
```

### Type Changed: Metal.MTLCompileOptions

Modified constructors:

```
public protected MTLCompileOptions (Foundation.NSObjectFlag t)
	public protected MTLCompileOptions (IntPtr handle)
```

### Type Changed: Metal.MTLComputePipelineReflection

Modified constructors:

```
public protected MTLComputePipelineReflection (Foundation.NSObjectFlag t)
	public protected MTLComputePipelineReflection (IntPtr handle)
```

### Type Changed: Metal.MTLDepthStencilDescriptor

Modified constructors:

```
public protected MTLDepthStencilDescriptor (Foundation.NSObjectFlag t)
	public protected MTLDepthStencilDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLDevice_Extensions

Removed methods:

```
public static IMTLComputePipelineState CreateComputePipelineState (IMTLDevice This, IMTLFunction computeFunction, MTLPipelineOption options, out MTLComputePipelineReflection reflection, out Foundation.NSError error);
	public static void CreateComputePipelineState (IMTLDevice This, IMTLFunction computeFunction, System.Action<IMTLComputePipelineState,Foundation.NSError> completionHandler);
	public static IMTLRenderPipelineState CreateRenderPipelineState (IMTLDevice This, MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, out MTLRenderPipelineReflection reflection, out Foundation.NSError error);
	public static void CreateRenderPipelineState (IMTLDevice This, MTLRenderPipelineDescriptor descriptor, MTLPipelineOption options, System.Action<IMTLRenderPipelineState,Metal.MTLRenderPipelineReflection,Foundation.NSError> completionHandler);
```

### Type Changed: Metal.MTLDrawable

Modified constructors:

```
public protected MTLDrawable ()
	public protected MTLDrawable (Foundation.NSObjectFlag t)
	public protected MTLDrawable (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPassAttachmentDescriptor

Modified constructors:

```
public protected MTLRenderPassAttachmentDescriptor (Foundation.NSObjectFlag t)
	public protected MTLRenderPassAttachmentDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPassColorAttachmentDescriptor

Modified constructors:

```
public protected MTLRenderPassColorAttachmentDescriptor (Foundation.NSObjectFlag t)
	public protected MTLRenderPassColorAttachmentDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPassColorAttachmentDescriptorArray

Modified constructors:

```
public protected MTLRenderPassColorAttachmentDescriptorArray (Foundation.NSObjectFlag t)
	public protected MTLRenderPassColorAttachmentDescriptorArray (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPassDepthAttachmentDescriptor

Modified constructors:

```
public protected MTLRenderPassDepthAttachmentDescriptor (Foundation.NSObjectFlag t)
	public protected MTLRenderPassDepthAttachmentDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPassDescriptor

Modified constructors:

```
public protected MTLRenderPassDescriptor (Foundation.NSObjectFlag t)
	public protected MTLRenderPassDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPassStencilAttachmentDescriptor

Modified constructors:

```
public protected MTLRenderPassStencilAttachmentDescriptor (Foundation.NSObjectFlag t)
	public protected MTLRenderPassStencilAttachmentDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPipelineColorAttachmentDescriptor

Modified constructors:

```
public protected MTLRenderPipelineColorAttachmentDescriptor (Foundation.NSObjectFlag t)
	public protected MTLRenderPipelineColorAttachmentDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPipelineColorAttachmentDescriptorArray

Modified constructors:

```
public protected MTLRenderPipelineColorAttachmentDescriptorArray (Foundation.NSObjectFlag t)
	public protected MTLRenderPipelineColorAttachmentDescriptorArray (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPipelineDescriptor

Modified constructors:

```
public protected MTLRenderPipelineDescriptor (Foundation.NSObjectFlag t)
	public protected MTLRenderPipelineDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLRenderPipelineReflection

Modified constructors:

```
public protected MTLRenderPipelineReflection (Foundation.NSObjectFlag t)
	public protected MTLRenderPipelineReflection (IntPtr handle)
```

### Type Changed: Metal.MTLSamplerDescriptor

Modified constructors:

```
public protected MTLSamplerDescriptor (Foundation.NSObjectFlag t)
	public protected MTLSamplerDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLStencilDescriptor

Modified constructors:

```
public protected MTLStencilDescriptor (Foundation.NSObjectFlag t)
	public protected MTLStencilDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLStructMember

Modified constructors:

```
public protected MTLStructMember (Foundation.NSObjectFlag t)
	public protected MTLStructMember (IntPtr handle)
```

### Type Changed: Metal.MTLStructType

Modified constructors:

```
public protected MTLStructType (Foundation.NSObjectFlag t)
	public protected MTLStructType (IntPtr handle)
```

### Type Changed: Metal.MTLTextureDescriptor

Modified constructors:

```
public protected MTLTextureDescriptor (Foundation.NSObjectFlag t)
	public protected MTLTextureDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLVertexAttribute

Modified constructors:

```
public protected MTLVertexAttribute (Foundation.NSObjectFlag t)
	public protected MTLVertexAttribute (IntPtr handle)
```

### Type Changed: Metal.MTLVertexAttributeDescriptor

Modified constructors:

```
public protected MTLVertexAttributeDescriptor (Foundation.NSObjectFlag t)
	public protected MTLVertexAttributeDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLVertexAttributeDescriptorArray

Modified constructors:

```
public protected MTLVertexAttributeDescriptorArray (Foundation.NSObjectFlag t)
	public protected MTLVertexAttributeDescriptorArray (IntPtr handle)
```

### Type Changed: Metal.MTLVertexBufferLayoutDescriptor

Modified constructors:

```
public protected MTLVertexBufferLayoutDescriptor (Foundation.NSObjectFlag t)
	public protected MTLVertexBufferLayoutDescriptor (IntPtr handle)
```

### Type Changed: Metal.MTLVertexBufferLayoutDescriptorArray

Modified constructors:

```
public protected MTLVertexBufferLayoutDescriptorArray (Foundation.NSObjectFlag t)
	public protected MTLVertexBufferLayoutDescriptorArray (IntPtr handle)
```

### Type Changed: Metal.MTLVertexDescriptor

Modified constructors:

```
public protected MTLVertexDescriptor (Foundation.NSObjectFlag t)
	public protected MTLVertexDescriptor (IntPtr handle)
```

### Removed Type Metal.MTLBlitCommandEncoder_Extensions ### Removed Type Metal.MTLBuffer_Extensions ### Removed Type Metal.MTLCommandBuffer_Extensions ### Removed Type Metal.MTLCommandEncoder_Extensions ### Removed Type Metal.MTLCommandQueue_Extensions ### Removed Type Metal.MTLComputeCommandEncoder_Extensions ### Removed Type Metal.MTLComputePipelineState_Extensions ### Removed Type Metal.MTLDepthStencilState_Extensions ### Removed Type Metal.MTLDrawable_Extensions ### Removed Type Metal.MTLFunction_Extensions ### Removed Type Metal.MTLLibrary_Extensions ### Removed Type Metal.MTLParallelRenderCommandEncoder_Extensions ### Removed Type Metal.MTLRenderCommandEncoder_Extensions ### Removed Type Metal.MTLRenderPipelineState_Extensions ### Removed Type Metal.MTLResource_Extensions ### Removed Type Metal.MTLSamplerState_Extensions ### Removed Type Metal.MTLTexture_Extensions 



## Namespace MobileCoreServices



### Type Changed: MobileCoreServices.UTType

Removed constructor:

```
public UTType ();
```

Modified methods:

```
static public bool ConformsTo (string uti, string conformsToUti)
	static public string[] CopyAllTags (string uti, string tagClass)
	static public string[] CreateAllIdentifiers (string tagClass, string tag, string conformingToUti)
	static public string GetDescription (string uti)
```

## Namespace MultipeerConnectivity



### Type Changed: MultipeerConnectivity.IMCBrowserViewControllerDelegate

Added methods:

```
public virtual void DidFinish (MCBrowserViewController browserViewController);
	public virtual void WasCancelled (MCBrowserViewController browserViewController);
```

### Type Changed: MultipeerConnectivity.IMCNearbyServiceAdvertiserDelegate

Added method:

```
public virtual void DidReceiveInvitationFromPeer (MCNearbyServiceAdvertiser advertiser, MCPeerID peerID, Foundation.NSData context, MCNearbyServiceAdvertiserInvitationHandler invitationHandler);
```

### Type Changed: MultipeerConnectivity.IMCNearbyServiceBrowserDelegate

Added methods:

```
public virtual void FoundPeer (MCNearbyServiceBrowser browser, MCPeerID peerID, Foundation.NSDictionary info);
	public virtual void LostPeer (MCNearbyServiceBrowser browser, MCPeerID peerID);
```

### Type Changed: MultipeerConnectivity.MCAdvertiserAssistant

Modified constructors:

```
public protected MCAdvertiserAssistant (Foundation.NSObjectFlag t)
	public protected MCAdvertiserAssistant (IntPtr handle)
```

Modified properties:

```
public MCAdvertiserAssistantDelegate IMCAdvertiserAssistantDelegate Delegate { get; set; }
```

### Type Changed: MultipeerConnectivity.MCAdvertiserAssistantDelegate

Modified constructors:

```
public protected MCAdvertiserAssistantDelegate (Foundation.NSObjectFlag t)
	public protected MCAdvertiserAssistantDelegate (IntPtr handle)
```

### Type Changed: MultipeerConnectivity.MCBrowserViewController

Modified constructors:

```
public protected MCBrowserViewController (Foundation.NSObjectFlag t)
	public protected MCBrowserViewController (IntPtr handle)
```

Modified properties:

```
public MCBrowserViewControllerDelegate IMCBrowserViewControllerDelegate Delegate { get; set; }
```

### Type Changed: MultipeerConnectivity.MCBrowserViewControllerDelegate

Modified constructors:

```
public protected MCBrowserViewControllerDelegate ()
	public protected MCBrowserViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected MCBrowserViewControllerDelegate (IntPtr handle)
```

Modified methods:

```
public abstract void DidFinish (MCBrowserViewController browserViewController)
	public abstract void WasCancelled (MCBrowserViewController browserViewController)
```

### Type Changed: MultipeerConnectivity.MCBrowserViewControllerDelegate_Extensions

Removed methods:

```
public static void DidFinish (IMCBrowserViewControllerDelegate This, MCBrowserViewController browserViewController);
	public static void WasCancelled (IMCBrowserViewControllerDelegate This, MCBrowserViewController browserViewController);
```

### Type Changed: MultipeerConnectivity.MCNearbyServiceAdvertiser

Modified constructors:

```
public protected MCNearbyServiceAdvertiser (Foundation.NSObjectFlag t)
	public protected MCNearbyServiceAdvertiser (IntPtr handle)
```

Modified properties:

```
public MCNearbyServiceAdvertiserDelegate IMCNearbyServiceAdvertiserDelegate Delegate { get; set; }
```

### Type Changed: MultipeerConnectivity.MCNearbyServiceAdvertiserDelegate

Modified constructors:

```
public protected MCNearbyServiceAdvertiserDelegate ()
	public protected MCNearbyServiceAdvertiserDelegate (Foundation.NSObjectFlag t)
	public protected MCNearbyServiceAdvertiserDelegate (IntPtr handle)
```

Modified methods:

```
public abstract void DidReceiveInvitationFromPeer (MCNearbyServiceAdvertiser advertiser, MCPeerID peerID, Foundation.NSData context, MCNearbyServiceAdvertiserInvitationHandler invitationHandler)
```

### Type Changed: MultipeerConnectivity.MCNearbyServiceAdvertiserDelegate_Extensions

Removed method:

```
public static void DidReceiveInvitationFromPeer (IMCNearbyServiceAdvertiserDelegate This, MCNearbyServiceAdvertiser advertiser, MCPeerID peerID, Foundation.NSData context, MCNearbyServiceAdvertiserInvitationHandler invitationHandler);
```

### Type Changed: MultipeerConnectivity.MCNearbyServiceBrowser

Modified constructors:

```
public protected MCNearbyServiceBrowser (Foundation.NSObjectFlag t)
	public protected MCNearbyServiceBrowser (IntPtr handle)
```

Modified properties:

```
public MCNearbyServiceBrowserDelegate IMCNearbyServiceBrowserDelegate Delegate { get; set; }
```

### Type Changed: MultipeerConnectivity.MCNearbyServiceBrowserDelegate

Modified constructors:

```
public protected MCNearbyServiceBrowserDelegate ()
	public protected MCNearbyServiceBrowserDelegate (Foundation.NSObjectFlag t)
	public protected MCNearbyServiceBrowserDelegate (IntPtr handle)
```

Modified methods:

```
public abstract void FoundPeer (MCNearbyServiceBrowser browser, MCPeerID peerID, Foundation.NSDictionary info)
	public abstract void LostPeer (MCNearbyServiceBrowser browser, MCPeerID peerID)
```

### Type Changed: MultipeerConnectivity.MCNearbyServiceBrowserDelegate_Extensions

Removed methods:

```
public static void FoundPeer (IMCNearbyServiceBrowserDelegate This, MCNearbyServiceBrowser browser, MCPeerID peerID, Foundation.NSDictionary info);
	public static void LostPeer (IMCNearbyServiceBrowserDelegate This, MCNearbyServiceBrowser browser, MCPeerID peerID);
```

### Type Changed: MultipeerConnectivity.MCPeerID

Modified constructors:

```
public protected MCPeerID (Foundation.NSObjectFlag t)
	public protected MCPeerID (IntPtr handle)
```

### Type Changed: MultipeerConnectivity.MCSession

Modified constructors:

```
public protected MCSession (Foundation.NSObjectFlag t)
	public protected MCSession (IntPtr handle)
```

Modified properties:

```
public MCSessionDelegate IMCSessionDelegate Delegate { get; set; }
```

### Type Changed: MultipeerConnectivity.MCSessionDelegate

Modified constructors:

```
public protected MCSessionDelegate ()
	public protected MCSessionDelegate (Foundation.NSObjectFlag t)
	public protected MCSessionDelegate (IntPtr handle)
```

## Namespace NetworkExtension



### Type Changed: NetworkExtension.NEEvaluateConnectionRule

Modified constructors:

```
public protected NEEvaluateConnectionRule (Foundation.NSObjectFlag t)
	public protected NEEvaluateConnectionRule (IntPtr handle)
```

### Type Changed: NetworkExtension.NEOnDemandRule

Modified constructors:

```
public protected NEOnDemandRule ()
	public protected NEOnDemandRule (Foundation.NSCoder coder)
	public protected NEOnDemandRule (Foundation.NSObjectFlag t)
	public protected NEOnDemandRule (IntPtr handle)
```

### Type Changed: NetworkExtension.NEOnDemandRuleConnect

Modified constructors:

```
public protected NEOnDemandRuleConnect (Foundation.NSObjectFlag t)
	public protected NEOnDemandRuleConnect (IntPtr handle)
```

### Type Changed: NetworkExtension.NEOnDemandRuleDisconnect

Modified constructors:

```
public protected NEOnDemandRuleDisconnect (Foundation.NSObjectFlag t)
	public protected NEOnDemandRuleDisconnect (IntPtr handle)
```

### Type Changed: NetworkExtension.NEOnDemandRuleEvaluateConnection

Modified constructors:

```
public protected NEOnDemandRuleEvaluateConnection (Foundation.NSObjectFlag t)
	public protected NEOnDemandRuleEvaluateConnection (IntPtr handle)
```

### Type Changed: NetworkExtension.NEOnDemandRuleIgnore

Modified constructors:

```
public protected NEOnDemandRuleIgnore (Foundation.NSObjectFlag t)
	public protected NEOnDemandRuleIgnore (IntPtr handle)
```

### Type Changed: NetworkExtension.NEVpnConnection

Modified constructors:

```
public protected NEVpnConnection (Foundation.NSObjectFlag t)
	public protected NEVpnConnection (IntPtr handle)
```

### Type Changed: NetworkExtension.NEVpnIke2SecurityAssociationParameters

Modified constructors:

```
public protected NEVpnIke2SecurityAssociationParameters (Foundation.NSObjectFlag t)
	public protected NEVpnIke2SecurityAssociationParameters (IntPtr handle)
```

### Type Changed: NetworkExtension.NEVpnManager

Modified constructors:

```
public protected NEVpnManager (Foundation.NSObjectFlag t)
	public protected NEVpnManager (IntPtr handle)
```

### Type Changed: NetworkExtension.NEVpnProtocol

Modified constructors:

```
public protected NEVpnProtocol ()
	public protected NEVpnProtocol (Foundation.NSCoder coder)
	public protected NEVpnProtocol (Foundation.NSObjectFlag t)
	public protected NEVpnProtocol (IntPtr handle)
```

### Type Changed: NetworkExtension.NEVpnProtocolIke2

Modified constructors:

```
public protected NEVpnProtocolIke2 (Foundation.NSObjectFlag t)
	public protected NEVpnProtocolIke2 (IntPtr handle)
```

### Type Changed: NetworkExtension.NEVpnProtocolIpSec

Modified constructors:

```
public protected NEVpnProtocolIpSec (Foundation.NSObjectFlag t)
	public protected NEVpnProtocolIpSec (IntPtr handle)
```

## Namespace NewsstandKit



### Type Changed: NewsstandKit.NKAssetDownload

Modified constructors:

```
public protected NKAssetDownload (Foundation.NSObjectFlag t)
	public protected NKAssetDownload (IntPtr handle)
```

Removed method:

```
public virtual Foundation.NSUrlConnection DownloadWithDelegate (Foundation.NSUrlConnectionDownloadDelegate downloadDelegate);
```

Added method:

```
public virtual Foundation.NSUrlConnection DownloadWithDelegate (Foundation.INSUrlConnectionDownloadDelegate downloadDelegate);
```

### Type Changed: NewsstandKit.NKIssue

Modified constructors:

```
public protected NKIssue (Foundation.NSObjectFlag t)
	public protected NKIssue (IntPtr handle)
```

### Type Changed: NewsstandKit.NKLibrary

Modified constructors:

```
public protected NKLibrary (Foundation.NSObjectFlag t)
	public protected NKLibrary (IntPtr handle)
```

## Namespace NotificationCenter



### Type Changed: NotificationCenter.NCWidgetController

Modified constructors:

```
public protected NCWidgetController (Foundation.NSObjectFlag t)
	public protected NCWidgetController (IntPtr handle)
```

### Type Changed: NotificationCenter.NCWidgetProviding

Modified constructors:

```
public protected NCWidgetProviding (Foundation.NSObjectFlag t)
	public protected NCWidgetProviding (IntPtr handle)
```

### Type Changed: NotificationCenter.UIVibrancyEffect_NotificationCenter

Removed method:

```
public static UIKit.UIVibrancyEffect NotificationCenterVibrancyEffect (UIKit.UIVibrancyEffect This);
```

## Namespace ObjCRuntime



### Type Changed: ObjCRuntime.BlockLiteral

Removed fields:

```
public IntPtr block_descriptor;
	public BlockFlags flags;
	public IntPtr global_handle;
	public IntPtr invoke;
	public IntPtr isa;
	public IntPtr local_handle;
	public int reserved;
```

### Type Changed: ObjCRuntime.Class

Removed method:

```
public static void RegisterMethods (System.Type type, System.Collections.Generic.Dictionary<System.IntPtr,ObjCRuntime.MethodDescription> methods);
```

### Type Changed: ObjCRuntime.Dlfcn

Removed methods:

```
public static System.Drawing.SizeF GetSizeF (IntPtr handle, string symbol);
	public static void SetSizeF (IntPtr handle, string symbol, System.Drawing.SizeF value);
```

Added methods:

```
public static float GetNFloat (IntPtr handle, string symbol);
	public static int GetNInt (IntPtr handle, string symbol);
	public static uint GetNUInt (IntPtr handle, string symbol);
```

### Type Changed: ObjCRuntime.Platform

Removed values:

```
[Obsolete ("Use iOS_Version")]
	iOS = 4294967295,

	[Obsolete ("Use Mac_Version")]
	Mac = 18446744069414584320,
```

### Type Changed: ObjCRuntime.PlatformHelper

Removed methods:

```
[Obsolete ("UseCompareIosVersion")]
	public static int CompareIos (Platform a, Platform b);

	[Obsolete ("Use CompareMacVersion")]
	public static int CompareMac (Platform a, Platform b);

	[Obsolete ("Use ToIosVersion")]
	public static Platform ToIos (Platform platform);

	[Obsolete ("Use ToMacVersion")]
	public static Platform ToMac (Platform platform);
```

### Type Changed: ObjCRuntime.Runtime

Removed methods:

```
public static System.Delegate CreateBlockProxy (System.Reflection.MethodInfo method, IntPtr block);
	public static System.Reflection.MethodInfo GetBlockWrapperCreator (System.Reflection.MethodInfo method, int parameter);
	public static System.Delegate GetDelegateForBlock (IntPtr methodPtr, System.Type type);
```

### Type Changed: ObjCRuntime.Selector

Removed constructor:

```
[Obsolete ("Use the (string) constructor.")]
	public Selector (string name, bool alloc);
```

Removed fields:

```
public static IntPtr Init;
	public static IntPtr InitWithCoder;
```

### Removed Type ObjCRuntime.AlphaAttribute ### Removed Type ObjCRuntime.BlockDescriptor ### Removed Type ObjCRuntime.LionAttribute ### Removed Type ObjCRuntime.MavericksAttribute ### Removed Type ObjCRuntime.Messaging ### Removed Type ObjCRuntime.MethodDescription ### Removed Type ObjCRuntime.MountainLionAttribute ### Removed Type ObjCRuntime.NSStringStruct ### Removed Type ObjCRuntime.SinceAttribute ### New Type ObjCRuntime.Constants

```
public static class Constants {
	// fields
	public static const string AccelerateImageLibrary = "/System/Library/Frameworks/Accelerate.framework/Frameworks/vImage.framework/vImage";
	public static const string AccountsLibrary = "/System/Library/Frameworks/Accounts.framework/Accounts";
	public static const string AddressBookLibrary = "/System/Library/Frameworks/AddressBook.framework/AddressBook";
	public static const string AddressBookUILibrary = "/System/Library/Frameworks/AddressBookUI.framework/AddressBookUI";
	public static const string AssetsLibraryLibrary = "/System/Library/Frameworks/AssetsLibrary.framework/AssetsLibrary";
	public static const string AudioToolboxLibrary = "/System/Library/Frameworks/AudioToolbox.framework/AudioToolbox";
	public static const string AudioUnitLibrary = "/System/Library/Frameworks/AudioToolbox.framework/AudioToolbox";
	public static const string AVFoundationLibrary = "/System/Library/Frameworks/AVFoundation.framework/AVFoundation";
	public static const string AVKitLibrary = "/System/Library/Frameworks/AVKit.framework/AVKit";
	public static const string CFNetworkLibrary = "/System/Library/Frameworks/CFNetwork.framework/CFNetwork";
	public static const string CloudKitLibrary = "/System/Library/Frameworks/CloudKit.framework/CloudKit";
	public static const string CoreAnimationLibrary = "/System/Library/Frameworks/QuartzCore.framework/QuartzCore";
	public static const string CoreAudioKitLibrary = "/System/Library/Frameworks/CoreAudioKit.framework/CoreAudioKit";
	public static const string CoreBluetoothLibrary = "/System/Library/Frameworks/CoreBluetooth.framework/CoreBluetooth";
	public static const string CoreDataLibrary = "/System/Library/Frameworks/CoreData.framework/CoreData";
	public static const string CoreFoundationLibrary = "/System/Library/Frameworks/CoreFoundation.framework/CoreFoundation";
	public static const string CoreGraphicsLibrary = "/System/Library/Frameworks/CoreGraphics.framework/CoreGraphics";
	public static const string CoreImageLibrary = "/System/Library/Frameworks/CoreImage.framework/CoreImage";
	public static const string CoreLocationLibrary = "/System/Library/Frameworks/CoreLocation.framework/CoreLocation";
	public static const string CoreMediaLibrary = "/System/Library/Frameworks/CoreMedia.framework/CoreMedia";
	public static const string CoreMidiLibrary = "/System/Library/Frameworks/CoreMIDI.framework/CoreMIDI";
	public static const string CoreMotionLibrary = "System/Library/Frameworks/CoreMotion.framework/CoreMotion";
	public static const string CoreServicesLibrary = "/System/Library/Frameworks/MobileCoreServices.framework/MobileCoreServices";
	public static const string CoreTelephonyLibrary = "/System/Library/Frameworks/CoreTelephony.framework/CoreTelephony";
	public static const string CoreTextLibrary = "/System/Library/Frameworks/CoreText.framework/CoreText";
	public static const string CoreVideoLibrary = "/System/Library/Frameworks/CoreVideo.framework/CoreVideo";
	public static const string EventKitLibrary = "/System/Library/Frameworks/EventKit.framework/EventKit";
	public static const string ExternalAccessoryLibrary = "/System/Library/Frameworks/ExternalAccessory.framework/ExternalAccessory";
	public static const string FoundationLibrary = "/System/Library/Frameworks/Foundation.framework/Foundation";
	public static const string GameControllerLibrary = "/System/Library/Frameworks/GameController.framework/GameController";
	public static const string GameKitLibrary = "/System/Library/Frameworks/GameKit.framework/GameKit";
	public static const string GLKitLibrary = "/System/Library/Frameworks/GLKit.framework/GLKit";
	public static const string HealthKitLibrary = "/System/Library/Frameworks/HealthKit.framework/HealthKit";
	public static const string HomeKitLibrary = "/System/Library/Frameworks/HomeKit.framework/HomeKit";
	public static const string iAdLibrary = "/System/Library/Frameworks/iAd.framework/iAd";
	public static const string ImageIOLibrary = "/System/Library/Frameworks/ImageIO.framework/ImageIO";
	public static const string JavaScriptCoreLibrary = "/System/Library/Frameworks/JavaScriptCore.framework/JavaScriptCore";
	public static const string LocalAuthenticationLibrary = "/System/Library/Frameworks/LocalAuthentication.framework/LocalAuthentication";
	public static const string MapKitLibrary = "/System/Library/Frameworks/MapKit.framework/MapKit";
	public static const string MediaAccessibilityLibrary = "/System/Library/Frameworks/MediaAccessibility.framework/MediaAccessibility";
	public static const string MediaPlayerLibrary = "/System/Library/Frameworks/MediaPlayer.framework/MediaPlayer";
	public static const string MediaToolboxLibrary = "/System/Library/Frameworks/MediaToolbox.framework/MediaToolbox";
	public static const string MessageUILibrary = "/System/Library/Frameworks/MessageUI.framework/MessageUI";
	public static const string MetalLibrary = "/System/Library/Frameworks/Metal.framework/Metal";
	public static const string MobileCoreServicesLibrary = "/System/Library/Frameworks/MobileCoreServices.framework/MobileCoreServices";
	public static const string MultipeerConnectivityLibrary = "/System/Library/Frameworks/MultipeerConnectivity.framework/MultipeerConnectivity";
	public static const string NetworkExtensionLibrary = "/System/Library/Frameworks/NetworkExtension.framework/NetworkExtension";
	public static const string NewsstandKitLibrary = "/System/Library/Frameworks/NewsstandKit.framework/NewsstandKit";
	public static const string ObjectiveCLibrary = "/usr/lib/libobjc.dylib";
	public static const string OpenGLESLibrary = "/System/Library/Frameworks/OpenGLES.framework/OpenGLES";
	public static const string PassKitLibrary = "/System/Library/Frameworks/PassKit.framework/PassKit";
	public static const string PhotosLibrary = "/System/Library/Frameworks/Photos.framework/Photos";
	public static const string PhotosUILibrary = "/System/Library/Frameworks/PhotosUI.framework/PhotosUI";
	public static const string PushKitLibrary = "/System/Library/Frameworks/PushKit.framework/PushKit";
	public static const string QuartzLibrary = "/System/Library/Frameworks/QuartzCore.framework/QuartzCore";
	public static const string QuickLookLibrary = "/System/Library/Frameworks/QuickLook.framework/QuickLook";
	public static const string SafariServicesLibrary = "/System/Library/Frameworks/SafariServices.framework/SafariServices";
	public static const string SceneKitLibrary = "/System/Library/Frameworks/SceneKit.framework/SceneKit";
	public static const string SecurityLibrary = "/System/Library/Frameworks/Security.framework/Security";
	public static const string SocialLibrary = "/System/Library/Frameworks/Social.framework/Social";
	public static const string SpriteKitLibrary = "/System/Library/Frameworks/SpriteKit.framework/SpriteKit";
	public static const string StoreKitLibrary = "/System/Library/Frameworks/StoreKit.framework/StoreKit";
	public static const string SystemConfigurationLibrary = "/System/Library/Frameworks/SystemConfiguration.framework/SystemConfiguration";
	public static const string SystemLibrary = "/usr/lib/libSystem.dylib";
	public static const string UIKitLibrary = "/System/Library/Frameworks/UIKit.framework/UIKit";
	public static const string Version = "8.6.0";
	public static const string VideoToolboxLibrary = "/System/Library/Frameworks/VideoToolbox.framework/VideoToolbox";
}
```

### New Type ObjCRuntime.MonoNativeFunctionWrapperAttribute

```
public sealed class MonoNativeFunctionWrapperAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public MonoNativeFunctionWrapperAttribute ();
}
```

### New Type ObjCRuntime.MonoPInvokeCallbackAttribute

```
public sealed class MonoPInvokeCallbackAttribute : System.Attribute, System.Runtime.InteropServices._Attribute {
	// constructors
	public MonoPInvokeCallbackAttribute (System.Type t);
}
```

### New Type ObjCRuntime.RuntimeException

```
public class RuntimeException : System.Exception, System.Runtime.Serialization.ISerializable, System.Runtime.InteropServices._Exception {
	// constructors
	public RuntimeException (string message, object[] args);
	public RuntimeException (int code, string message, object[] args);
	public RuntimeException (int code, bool error, string message, object[] args);
	public RuntimeException (int code, bool error, System.Exception innerException, string message, object[] args);
	// properties
	public int Code { get; }
	public bool Error { get; }
}
```





## Namespace OpenGLES



### Type Changed: OpenGLES.EAGLContext

Modified constructors:

```
public protected EAGLContext (Foundation.NSObjectFlag t)
	public protected EAGLContext (IntPtr handle)
```

### Type Changed: OpenGLES.EAGLSharegroup

Modified constructors:

```
public protected EAGLSharegroup (Foundation.NSObjectFlag t)
	public protected EAGLSharegroup (IntPtr handle)
```

### Removed Type OpenGLES.EAGLDrawable_Extensions 

## Namespace PassKit



### Type Changed: PassKit.IPKPaymentAuthorizationViewControllerDelegate

Removed method:

```
public virtual void DidAuthorizePayment (PKPaymentAuthorizationViewController controller, PKPayment payment, PKPaymentAuthorizationHandler completion);
```

Added method:

```
public virtual void DidAuthorizePayment (PKPaymentAuthorizationViewController controller, PKPayment payment, System.Action<PKPaymentAuthorizationStatus> completion);
```

### Type Changed: PassKit.PKAddPassesViewController

Modified constructors:

```
public protected PKAddPassesViewController (Foundation.NSObjectFlag t)
	public protected PKAddPassesViewController (IntPtr handle)
```

Modified properties:

```
public PKAddPassesViewControllerDelegate IPKAddPassesViewControllerDelegate Delegate { get; set; }
```

### Type Changed: PassKit.PKAddPassesViewControllerDelegate

Modified constructors:

```
public protected PKAddPassesViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected PKAddPassesViewControllerDelegate (IntPtr handle)
```

### Type Changed: PassKit.PKObject

Modified constructors:

```
public protected PKObject (Foundation.NSObjectFlag t)
	public protected PKObject (IntPtr handle)
```

### Type Changed: PassKit.PKPass

Modified constructors:

```
public protected PKPass (Foundation.NSObjectFlag t)
	public protected PKPass (IntPtr handle)
```

### Type Changed: PassKit.PKPassKitErrorCode

Removed value:

```
[Obsolete ("renamed to InvalidSignature")]
	CertificateRevoked = 3,
```

### Type Changed: PassKit.PKPassLibrary

Modified constructors:

```
public protected PKPassLibrary (Foundation.NSObjectFlag t)
	public protected PKPassLibrary (IntPtr handle)
```

### Type Changed: PassKit.PKPayment

Modified constructors:

```
public protected PKPayment (Foundation.NSObjectFlag t)
	public protected PKPayment (IntPtr handle)
```

### Type Changed: PassKit.PKPaymentAuthorizationEventArgs

Removed constructor:

```
public PKPaymentAuthorizationEventArgs (PKPayment payment, PKPaymentAuthorizationHandler completion);
```

Added constructor:

```
public PKPaymentAuthorizationEventArgs (PKPayment payment, System.Action<PKPaymentAuthorizationStatus> completion);
```

Modified properties:

```
public PKPaymentAuthorizationHandler System.Action<PKPaymentAuthorizationStatus> Completion { get; set; }
```

### Type Changed: PassKit.PKPaymentAuthorizationViewController

Modified constructors:

```
public protected PKPaymentAuthorizationViewController (Foundation.NSObjectFlag t)
	public protected PKPaymentAuthorizationViewController (IntPtr handle)
```

Modified properties:

```
public PKPaymentAuthorizationViewControllerDelegate IPKPaymentAuthorizationViewControllerDelegate Delegate { get; set; }
```

### Type Changed: PassKit.PKPaymentAuthorizationViewControllerDelegate

Modified constructors:

```
public protected PKPaymentAuthorizationViewControllerDelegate ()
	public protected PKPaymentAuthorizationViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected PKPaymentAuthorizationViewControllerDelegate (IntPtr handle)
```

Removed method:

```
public virtual void DidAuthorizePayment (PKPaymentAuthorizationViewController controller, PKPayment payment, PKPaymentAuthorizationHandler completion);
```

Added method:

```
public virtual void DidAuthorizePayment (PKPaymentAuthorizationViewController controller, PKPayment payment, System.Action<PKPaymentAuthorizationStatus> completion);
```

### Type Changed: PassKit.PKPaymentPass

Modified constructors:

```
public protected PKPaymentPass (Foundation.NSObjectFlag t)
	public protected PKPaymentPass (IntPtr handle)
```

### Type Changed: PassKit.PKPaymentRequest

Modified constructors:

```
public protected PKPaymentRequest (Foundation.NSObjectFlag t)
	public protected PKPaymentRequest (IntPtr handle)
```

### Type Changed: PassKit.PKPaymentSummaryItem

Modified constructors:

```
public protected PKPaymentSummaryItem (Foundation.NSObjectFlag t)
	public protected PKPaymentSummaryItem (IntPtr handle)
```

### Type Changed: PassKit.PKPaymentToken

Modified constructors:

```
public protected PKPaymentToken (Foundation.NSObjectFlag t)
	public protected PKPaymentToken (IntPtr handle)
```

### Type Changed: PassKit.PKShippingMethod

Modified constructors:

```
public protected PKShippingMethod (Foundation.NSObjectFlag t)
	public protected PKShippingMethod (IntPtr handle)
```

### Removed Type PassKit.PKPaymentAuthorizationHandler 

## Namespace Photos



### Type Changed: Photos.IPHPhotoLibraryChangeObserver

Added method:

```
public virtual void PhotoLibraryDidChange (PHChange changeInstance);
```

### Type Changed: Photos.PHAdjustmentData

Modified constructors:

```
public protected PHAdjustmentData (Foundation.NSObjectFlag t)
	public protected PHAdjustmentData (IntPtr handle)
```

### Type Changed: Photos.PHAsset

Modified constructors:

```
public protected PHAsset (Foundation.NSObjectFlag t)
	public protected PHAsset (IntPtr handle)
```

### Type Changed: Photos.PHAssetChangeRequest

Modified constructors:

```
public protected PHAssetChangeRequest (Foundation.NSObjectFlag t)
	public protected PHAssetChangeRequest (IntPtr handle)
```

### Type Changed: Photos.PHAssetCollection

Modified constructors:

```
public protected PHAssetCollection (Foundation.NSObjectFlag t)
	public protected PHAssetCollection (IntPtr handle)
```

### Type Changed: Photos.PHAssetCollectionChangeRequest

Modified constructors:

```
public protected PHAssetCollectionChangeRequest (Foundation.NSObjectFlag t)
	public protected PHAssetCollectionChangeRequest (IntPtr handle)
```

### Type Changed: Photos.PHAssetCollectionSubtype

Modified fields:

```
Any = 2147483647 9223372036854775807
```

### Type Changed: Photos.PHCachingImageManager

Modified constructors:

```
public protected PHCachingImageManager (Foundation.NSObjectFlag t)
	public protected PHCachingImageManager (IntPtr handle)
```

### Type Changed: Photos.PHChange

Modified constructors:

```
public protected PHChange (Foundation.NSObjectFlag t)
	public protected PHChange (IntPtr handle)
```

### Type Changed: Photos.PHCollection

Modified constructors:

```
public protected PHCollection (Foundation.NSObjectFlag t)
	public protected PHCollection (IntPtr handle)
```

### Type Changed: Photos.PHCollectionList

Modified constructors:

```
public protected PHCollectionList (Foundation.NSObjectFlag t)
	public protected PHCollectionList (IntPtr handle)
```

### Type Changed: Photos.PHCollectionListChangeRequest

Modified constructors:

```
public protected PHCollectionListChangeRequest (Foundation.NSObjectFlag t)
	public protected PHCollectionListChangeRequest (IntPtr handle)
```

### Type Changed: Photos.PHCollectionListSubtype

Modified fields:

```
Any = 2147483647 9223372036854775807
```

### Type Changed: Photos.PHContentEditingInput

Modified constructors:

```
public protected PHContentEditingInput (Foundation.NSObjectFlag t)
	public protected PHContentEditingInput (IntPtr handle)
```

### Type Changed: Photos.PHContentEditingInputRequestOptions

Modified constructors:

```
public protected PHContentEditingInputRequestOptions (Foundation.NSObjectFlag t)
	public protected PHContentEditingInputRequestOptions (IntPtr handle)
```

### Type Changed: Photos.PHContentEditingOutput

Modified constructors:

```
public protected PHContentEditingOutput (Foundation.NSObjectFlag t)
	public protected PHContentEditingOutput (IntPtr handle)
```

### Type Changed: Photos.PHFetchOptions

Modified constructors:

```
public protected PHFetchOptions (Foundation.NSObjectFlag t)
	public protected PHFetchOptions (IntPtr handle)
```

### Type Changed: Photos.PHFetchResult

Modified constructors:

```
public protected PHFetchResult (Foundation.NSObjectFlag t)
	public protected PHFetchResult (IntPtr handle)
```

### Type Changed: Photos.PHFetchResultChangeDetails

Modified constructors:

```
public protected PHFetchResultChangeDetails (Foundation.NSObjectFlag t)
	public protected PHFetchResultChangeDetails (IntPtr handle)
```

### Type Changed: Photos.PHImageManager

Modified constructors:

```
public protected PHImageManager (Foundation.NSObjectFlag t)
	public protected PHImageManager (IntPtr handle)
```

### Type Changed: Photos.PHImageRequestOptions

Modified constructors:

```
public protected PHImageRequestOptions (Foundation.NSObjectFlag t)
	public protected PHImageRequestOptions (IntPtr handle)
```

### Type Changed: Photos.PHObject

Modified constructors:

```
public protected PHObject (Foundation.NSObjectFlag t)
	public protected PHObject (IntPtr handle)
```

### Type Changed: Photos.PHObjectChangeDetails

Modified constructors:

```
public protected PHObjectChangeDetails (Foundation.NSObjectFlag t)
	public protected PHObjectChangeDetails (IntPtr handle)
```

### Type Changed: Photos.PHObjectPlaceholder

Modified constructors:

```
public protected PHObjectPlaceholder (Foundation.NSObjectFlag t)
	public protected PHObjectPlaceholder (IntPtr handle)
```

### Type Changed: Photos.PHPhotoLibrary

Modified constructors:

```
public protected PHPhotoLibrary (Foundation.NSObjectFlag t)
	public protected PHPhotoLibrary (IntPtr handle)
```

Removed methods:

```
public virtual void RegisterChangeObserver (PHPhotoLibraryChangeObserver observer);
	public virtual void UnregisterChangeObserver (PHPhotoLibraryChangeObserver observer);
```

Added methods:

```
public virtual void RegisterChangeObserver (IPHPhotoLibraryChangeObserver observer);
	public virtual void UnregisterChangeObserver (IPHPhotoLibraryChangeObserver observer);
```

### Type Changed: Photos.PHPhotoLibraryChangeObserver

Modified constructors:

```
public protected PHPhotoLibraryChangeObserver ()
	public protected PHPhotoLibraryChangeObserver (Foundation.NSObjectFlag t)
	public protected PHPhotoLibraryChangeObserver (IntPtr handle)
```

Modified methods:

```
public abstract void PhotoLibraryDidChange (PHChange changeInstance)
```

### Type Changed: Photos.PHVideoRequestOptions

Modified constructors:

```
public protected PHVideoRequestOptions (Foundation.NSObjectFlag t)
	public protected PHVideoRequestOptions (IntPtr handle)
```

### Removed Type Photos.PHPhotoLibraryChangeObserver_Extensions 

## Namespace PhotosUI



### Type Changed: PhotosUI.PHContentEditingController

Modified constructors:

```
public protected PHContentEditingController ()
	public protected PHContentEditingController (Foundation.NSObjectFlag t)
	public protected PHContentEditingController (IntPtr handle)
```

### Removed Type PhotosUI.PHContentEditingController_Extensions 

## Namespace PushKit



### Type Changed: PushKit.PKPushCredentials

Modified constructors:

```
public protected PKPushCredentials (Foundation.NSObjectFlag t)
	public protected PKPushCredentials (IntPtr handle)
```

### Type Changed: PushKit.PKPushPayload

Modified constructors:

```
public protected PKPushPayload (Foundation.NSObjectFlag t)
	public protected PKPushPayload (IntPtr handle)
```

### Type Changed: PushKit.PKPushRegistry

Modified constructors:

```
public protected PKPushRegistry (Foundation.NSObjectFlag t)
	public protected PKPushRegistry (IntPtr handle)
```

Modified properties:

```
public PKPushRegistryDelegate IPKPushRegistryDelegate Delegate { get; set; }
```

### Type Changed: PushKit.PKPushRegistryDelegate

Modified constructors:

```
public protected PKPushRegistryDelegate ()
	public protected PKPushRegistryDelegate (Foundation.NSObjectFlag t)
	public protected PKPushRegistryDelegate (IntPtr handle)
```

## Namespace QuickLook



### Type Changed: QuickLook.IQLPreviewControllerDataSource

Removed method:

```
public virtual QLPreviewItem GetPreviewItem (QLPreviewController controller, int index);
```

Added method:

```
public virtual IQLPreviewItem GetPreviewItem (QLPreviewController controller, int index);
```

### Type Changed: QuickLook.QLFrame

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (QLPreviewController controller, QLPreviewItem item, ref UIKit.UIView view, System.AsyncCallback callback, object object);
	public virtual System.Drawing.RectangleF Invoke (QLPreviewController controller, QLPreviewItem item, ref UIKit.UIView view);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (QLPreviewController controller, IQLPreviewItem item, ref UIKit.UIView view, System.AsyncCallback callback, object object);
	public virtual System.Drawing.RectangleF Invoke (QLPreviewController controller, IQLPreviewItem item, ref UIKit.UIView view);
```

### Type Changed: QuickLook.QLOpenUrl

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (QLPreviewController controller, Foundation.NSUrl url, QLPreviewItem item, System.AsyncCallback callback, object object);
	public virtual bool Invoke (QLPreviewController controller, Foundation.NSUrl url, QLPreviewItem item);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (QLPreviewController controller, Foundation.NSUrl url, IQLPreviewItem item, System.AsyncCallback callback, object object);
	public virtual bool Invoke (QLPreviewController controller, Foundation.NSUrl url, IQLPreviewItem item);
```

### Type Changed: QuickLook.QLPreviewController

Modified constructors:

```
public protected QLPreviewController (Foundation.NSObjectFlag t)
	public protected QLPreviewController (IntPtr handle)
```

Modified properties:

```
public virtual QLPreviewItem IQLPreviewItem CurrentPreviewItem { get; }
	public QLPreviewControllerDataSource IQLPreviewControllerDataSource DataSource { get; set; }
	public QLPreviewControllerDelegate IQLPreviewControllerDelegate Delegate { get; set; }
```

Removed method:

```
public static bool CanPreviewItem (QLPreviewItem item);
```

Added method:

```
public static bool CanPreviewItem (IQLPreviewItem item);
```

### Type Changed: QuickLook.QLPreviewControllerDataSource

Modified constructors:

```
public protected QLPreviewControllerDataSource ()
	public protected QLPreviewControllerDataSource (Foundation.NSObjectFlag t)
	public protected QLPreviewControllerDataSource (IntPtr handle)
```

Removed method:

```
public virtual QLPreviewItem GetPreviewItem (QLPreviewController controller, int index);
```

Added method:

```
public virtual IQLPreviewItem GetPreviewItem (QLPreviewController controller, int index);
```

### Type Changed: QuickLook.QLPreviewControllerDelegate

Modified constructors:

```
public protected QLPreviewControllerDelegate (Foundation.NSObjectFlag t)
	public protected QLPreviewControllerDelegate (IntPtr handle)
```

Removed methods:

```
public virtual System.Drawing.RectangleF FrameForPreviewItem (QLPreviewController controller, QLPreviewItem item, ref UIKit.UIView view);
	public virtual bool ShouldOpenUrl (QLPreviewController controller, Foundation.NSUrl url, QLPreviewItem item);
	public virtual UIKit.UIImage TransitionImageForPreviewItem (QLPreviewController controller, QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

Added methods:

```
public virtual System.Drawing.RectangleF FrameForPreviewItem (QLPreviewController controller, IQLPreviewItem item, ref UIKit.UIView view);
	public virtual bool ShouldOpenUrl (QLPreviewController controller, Foundation.NSUrl url, IQLPreviewItem item);
	public virtual UIKit.UIImage TransitionImageForPreviewItem (QLPreviewController controller, IQLPreviewItem item, System.Drawing.RectangleF contentRect);
```

### Type Changed: QuickLook.QLPreviewControllerDelegate_Extensions

Removed methods:

```
public static System.Drawing.RectangleF FrameForPreviewItem (IQLPreviewControllerDelegate This, QLPreviewController controller, QLPreviewItem item, ref UIKit.UIView view);
	public static bool ShouldOpenUrl (IQLPreviewControllerDelegate This, QLPreviewController controller, Foundation.NSUrl url, QLPreviewItem item);
	public static UIKit.UIImage TransitionImageForPreviewItem (IQLPreviewControllerDelegate This, QLPreviewController controller, QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

Added methods:

```
public static System.Drawing.RectangleF FrameForPreviewItem (IQLPreviewControllerDelegate This, QLPreviewController controller, IQLPreviewItem item, ref UIKit.UIView view);
	public static bool ShouldOpenUrl (IQLPreviewControllerDelegate This, QLPreviewController controller, Foundation.NSUrl url, IQLPreviewItem item);
	public static UIKit.UIImage TransitionImageForPreviewItem (IQLPreviewControllerDelegate This, QLPreviewController controller, IQLPreviewItem item, System.Drawing.RectangleF contentRect);
```

### Type Changed: QuickLook.QLPreviewItem

Modified constructors:

```
public protected QLPreviewItem ()
	public protected QLPreviewItem (Foundation.NSObjectFlag t)
	public protected QLPreviewItem (IntPtr handle)
```

### Type Changed: QuickLook.QLTransition

Removed methods:

```
public virtual System.IAsyncResult BeginInvoke (QLPreviewController controller, QLPreviewItem item, System.Drawing.RectangleF contentRect, System.AsyncCallback callback, object object);
	public virtual UIKit.UIImage Invoke (QLPreviewController controller, QLPreviewItem item, System.Drawing.RectangleF contentRect);
```

Added methods:

```
public virtual System.IAsyncResult BeginInvoke (QLPreviewController controller, IQLPreviewItem item, System.Drawing.RectangleF contentRect, System.AsyncCallback callback, object object);
	public virtual UIKit.UIImage Invoke (QLPreviewController controller, IQLPreviewItem item, System.Drawing.RectangleF contentRect);
```

### Removed Type QuickLook.QLPreviewControllerDataSource_Extensions ### Removed Type QuickLook.QLPreviewItem_Extensions 



## Namespace SafariServices



### Type Changed: SafariServices.SSReadingList

Modified constructors:

```
public protected SSReadingList (Foundation.NSObjectFlag t)
	public protected SSReadingList (IntPtr handle)
```

## Namespace SceneKit



### Type Changed: SceneKit.ISCNActionable

Added methods:

```
public virtual SCNAction GetAction (string key);
	public virtual bool HasActions ();
	public virtual void RemoveAction (string key);
	public virtual void RemoveAllActions ();
	public virtual void RunAction (SCNAction action);
	public virtual void RunAction (SCNAction action, string key);
	public virtual void RunAction (SCNAction action, System.Action block);
	public virtual void RunAction (SCNAction action, string key, System.Action block);
```

### Type Changed: SceneKit.ISCNAnimatable

Added methods:

```
public virtual void AddAnimation (CoreAnimation.CAAnimation animation, Foundation.NSString key);
	public virtual CoreAnimation.CAAnimation GetAnimation (Foundation.NSString key);
	public virtual Foundation.NSString[] GetAnimationKeys ();
	public virtual bool IsAnimationPaused (Foundation.NSString key);
	public virtual void PauseAnimation (Foundation.NSString key);
	public virtual void RemoveAllAnimations ();
	public virtual void RemoveAnimation (Foundation.NSString key);
	public virtual void RemoveAnimation (Foundation.NSString key, float duration);
	public virtual void ResumeAnimation (Foundation.NSString key);
```

### Type Changed: SceneKit.ISCNBoundingVolume

Added methods:

```
public virtual bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max);
	public virtual bool GetBoundingSphere (ref SCNVector3 center, ref float radius);
```

### Type Changed: SceneKit.ISCNSceneRenderer

Added properties:

```
public virtual bool AutoenablesDefaultLighting { get; set; }
	public virtual IntPtr Context { get; }
	public virtual bool JitteringEnabled { get; set; }
	public virtual bool Loops { get; set; }
	public virtual SpriteKit.SKScene OverlayScene { get; set; }
	public virtual bool Playing { get; set; }
	public virtual SCNNode PointOfView { get; set; }
	public virtual SCNScene Scene { get; set; }
	public virtual double SceneTimeInSeconds { get; set; }
	public virtual bool ShowsStatistics { get; set; }
	public virtual Foundation.NSObject WeakSceneRendererDelegate { get; set; }
```

Added methods:

```
public virtual bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView);
	public virtual bool Prepare (Foundation.NSObject obj, System.Func<bool> abortHandler);
	public virtual void Prepare (Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public virtual SCNVector3 ProjectPoint (SCNVector3 point);
	public virtual SCNVector3 UnprojectPoint (SCNVector3 point);
```

### Type Changed: SceneKit.SCNAction

Modified constructors:

```
public protected SCNAction (Foundation.NSObjectFlag t)
	public protected SCNAction (IntPtr handle)
```

### Type Changed: SceneKit.SCNActionable

Modified constructors:

```
public protected SCNActionable ()
	public protected SCNActionable (Foundation.NSObjectFlag t)
	public protected SCNActionable (IntPtr handle)
```

Modified methods:

```
public abstract SCNAction GetAction (string key)
	public abstract bool HasActions ()
	public abstract void RemoveAction (string key)
	public abstract void RemoveAllActions ()
	public abstract void RunAction (SCNAction action)
	public abstract void RunAction (SCNAction action, System.Action block)
	public abstract void RunAction (SCNAction action, string key)
	public abstract void RunAction (SCNAction action, string key, System.Action block)
```

### Type Changed: SceneKit.SCNAnimatable

Modified constructors:

```
public protected SCNAnimatable ()
	public protected SCNAnimatable (Foundation.NSObjectFlag t)
	public protected SCNAnimatable (IntPtr handle)
```

Modified methods:

```
public abstract void AddAnimation (CoreAnimation.CAAnimation animation, Foundation.NSString key)
	public abstract CoreAnimation.CAAnimation GetAnimation (Foundation.NSString key)
	public abstract Foundation.NSString[] GetAnimationKeys ()
	public abstract bool IsAnimationPaused (Foundation.NSString key)
	public abstract void PauseAnimation (Foundation.NSString key)
	public abstract void RemoveAllAnimations ()
	public abstract void RemoveAnimation (Foundation.NSString key)
	public abstract void RemoveAnimation (Foundation.NSString key, float duration)
	public abstract void ResumeAnimation (Foundation.NSString key)
```

### Type Changed: SceneKit.SCNAnimationEvent

Modified constructors:

```
public protected SCNAnimationEvent (Foundation.NSObjectFlag t)
	public protected SCNAnimationEvent (IntPtr handle)
```

### Type Changed: SceneKit.SCNBoundingVolume

Modified constructors:

```
public protected SCNBoundingVolume ()
	public protected SCNBoundingVolume (Foundation.NSObjectFlag t)
	public protected SCNBoundingVolume (IntPtr handle)
```

Modified methods:

```
public abstract bool GetBoundingBox (ref SCNVector3 min, ref SCNVector3 max)
	public abstract bool GetBoundingSphere (ref SCNVector3 center, ref float radius)
```

### Type Changed: SceneKit.SCNBox

Modified constructors:

```
public protected SCNBox (Foundation.NSObjectFlag t)
	public protected SCNBox (IntPtr handle)
```

### Type Changed: SceneKit.SCNCamera

Modified constructors:

```
public protected SCNCamera (Foundation.NSObjectFlag t)
	public protected SCNCamera (IntPtr handle)
```

### Type Changed: SceneKit.SCNCapsule

Modified constructors:

```
public protected SCNCapsule (Foundation.NSObjectFlag t)
	public protected SCNCapsule (IntPtr handle)
```

### Type Changed: SceneKit.SCNCone

Modified constructors:

```
public protected SCNCone (Foundation.NSObjectFlag t)
	public protected SCNCone (IntPtr handle)
```

### Type Changed: SceneKit.SCNConstraint

Modified constructors:

```
public protected SCNConstraint (Foundation.NSCoder coder)
	public protected SCNConstraint (Foundation.NSObjectFlag t)
	public protected SCNConstraint (IntPtr handle)
```

### Type Changed: SceneKit.SCNCylinder

Modified constructors:

```
public protected SCNCylinder (Foundation.NSObjectFlag t)
	public protected SCNCylinder (IntPtr handle)
```

### Type Changed: SceneKit.SCNFloor

Modified constructors:

```
public protected SCNFloor (Foundation.NSObjectFlag t)
	public protected SCNFloor (IntPtr handle)
```

### Type Changed: SceneKit.SCNGeometry

Modified constructors:

```
public protected SCNGeometry (Foundation.NSObjectFlag t)
	public protected SCNGeometry (IntPtr handle)
```

### Type Changed: SceneKit.SCNGeometryElement

Modified constructors:

```
public protected SCNGeometryElement (Foundation.NSObjectFlag t)
	public protected SCNGeometryElement (IntPtr handle)
```

### Type Changed: SceneKit.SCNGeometrySource

Modified constructors:

```
public protected SCNGeometrySource (Foundation.NSObjectFlag t)
	public protected SCNGeometrySource (IntPtr handle)
```

### Type Changed: SceneKit.SCNHitTest

Removed property:

```
public static Foundation.NSString IgnoreHiddenNodes { get; }
```

### Type Changed: SceneKit.SCNHitTestResult

Modified constructors:

```
public protected SCNHitTestResult (Foundation.NSObjectFlag t)
	public protected SCNHitTestResult (IntPtr handle)
```

### Type Changed: SceneKit.SCNIKConstraint

Modified constructors:

```
public protected SCNIKConstraint (Foundation.NSObjectFlag t)
	public protected SCNIKConstraint (IntPtr handle)
```

### Type Changed: SceneKit.SCNLevelOfDetail

Modified constructors:

```
public protected SCNLevelOfDetail (Foundation.NSObjectFlag t)
	public protected SCNLevelOfDetail (IntPtr handle)
```

### Type Changed: SceneKit.SCNLight

Modified constructors:

```
public protected SCNLight (Foundation.NSObjectFlag t)
	public protected SCNLight (IntPtr handle)
```

### Type Changed: SceneKit.SCNLookAtConstraint

Modified constructors:

```
public protected SCNLookAtConstraint (Foundation.NSObjectFlag t)
	public protected SCNLookAtConstraint (IntPtr handle)
```

### Type Changed: SceneKit.SCNMaterial

Modified constructors:

```
public protected SCNMaterial (Foundation.NSObjectFlag t)
	public protected SCNMaterial (IntPtr handle)
```

### Type Changed: SceneKit.SCNMaterialProperty

Modified constructors:

```
public protected SCNMaterialProperty (Foundation.NSObjectFlag t)
	public protected SCNMaterialProperty (IntPtr handle)
```

### Type Changed: SceneKit.SCNMatrix4

Modified fields:

```
public readonly SCNMatrix4 Identity;
```

Removed methods:

```
[Obsolete ("Use CreatePerspectiveOffCenter instead.")]
	public static SCNMatrix4 Frustum (float left, float right, float bottom, float top, float near, float far);

	[Obsolete ("Use CreatePerspectiveFieldOfView instead.")]
	public static SCNMatrix4 Perspective (float fovy, float aspect, float near, float far);

	[Obsolete ("Use CreateFromAxisAngle instead.")]
	public static SCNMatrix4 Rotate (SCNVector3 axis, float angle);

	[Obsolete ("Use CreateRotationX instead.")]
	public static SCNMatrix4 RotateX (float angle);

	[Obsolete ("Use CreateRotationY instead.")]
	public static SCNMatrix4 RotateY (float angle);

	[Obsolete ("Use CreateRotationZ instead.")]
	public static SCNMatrix4 RotateZ (float angle);

	[Obsolete ("Use CreateTranslation instead.")]
	public static SCNMatrix4 Translation (SCNVector3 trans);

	[Obsolete ("Use CreateTranslation instead.")]
	public static SCNMatrix4 Translation (float x, float y, float z);
```

### Type Changed: SceneKit.SCNMorpher

Modified constructors:

```
public protected SCNMorpher (Foundation.NSObjectFlag t)
	public protected SCNMorpher (IntPtr handle)
```

### Type Changed: SceneKit.SCNNode

Modified constructors:

```
public protected SCNNode (Foundation.NSObjectFlag t)
	public protected SCNNode (IntPtr handle)
```

Modified properties:

```
public SCNNodeRendererDelegate ISCNNodeRendererDelegate RendererDelegate { get; set; }
```

### Type Changed: SceneKit.SCNNodeRendererDelegate

Modified constructors:

```
public protected SCNNodeRendererDelegate (Foundation.NSObjectFlag t)
	public protected SCNNodeRendererDelegate (IntPtr handle)
```

### Type Changed: SceneKit.SCNParticlePropertyController

Modified constructors:

```
public protected SCNParticlePropertyController (Foundation.NSObjectFlag t)
	public protected SCNParticlePropertyController (IntPtr handle)
```

### Type Changed: SceneKit.SCNParticleSystem

Modified constructors:

```
public protected SCNParticleSystem (Foundation.NSObjectFlag t)
	public protected SCNParticleSystem (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsBallSocketJoint

Modified constructors:

```
public protected SCNPhysicsBallSocketJoint (Foundation.NSObjectFlag t)
	public protected SCNPhysicsBallSocketJoint (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsBehavior

Modified constructors:

```
public protected SCNPhysicsBehavior (Foundation.NSCoder coder)
	public protected SCNPhysicsBehavior (Foundation.NSObjectFlag t)
	public protected SCNPhysicsBehavior (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsBody

Modified constructors:

```
public protected SCNPhysicsBody (Foundation.NSObjectFlag t)
	public protected SCNPhysicsBody (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsContact

Modified constructors:

```
public protected SCNPhysicsContact (Foundation.NSObjectFlag t)
	public protected SCNPhysicsContact (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsContactDelegate

Modified constructors:

```
public protected SCNPhysicsContactDelegate (Foundation.NSObjectFlag t)
	public protected SCNPhysicsContactDelegate (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsField

Modified constructors:

```
public protected SCNPhysicsField (Foundation.NSObjectFlag t)
	public protected SCNPhysicsField (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsHingeJoint

Modified constructors:

```
public protected SCNPhysicsHingeJoint (Foundation.NSObjectFlag t)
	public protected SCNPhysicsHingeJoint (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsShape

Modified constructors:

```
public protected SCNPhysicsShape (Foundation.NSObjectFlag t)
	public protected SCNPhysicsShape (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsSliderJoint

Modified constructors:

```
public protected SCNPhysicsSliderJoint (Foundation.NSObjectFlag t)
	public protected SCNPhysicsSliderJoint (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsVehicle

Modified constructors:

```
public protected SCNPhysicsVehicle (Foundation.NSObjectFlag t)
	public protected SCNPhysicsVehicle (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsVehicleWheel

Modified constructors:

```
public protected SCNPhysicsVehicleWheel (Foundation.NSObjectFlag t)
	public protected SCNPhysicsVehicleWheel (IntPtr handle)
```

### Type Changed: SceneKit.SCNPhysicsWorld

Modified constructors:

```
public protected SCNPhysicsWorld (Foundation.NSObjectFlag t)
	public protected SCNPhysicsWorld (IntPtr handle)
```

Modified properties:

```
public SCNPhysicsContactDelegate ISCNPhysicsContactDelegate ContactDelegate { get; set; }
```

### Type Changed: SceneKit.SCNPlane

Modified constructors:

```
public protected SCNPlane (Foundation.NSObjectFlag t)
	public protected SCNPlane (IntPtr handle)
```

### Type Changed: SceneKit.SCNProgram

Modified constructors:

```
public protected SCNProgram (Foundation.NSObjectFlag t)
	public protected SCNProgram (IntPtr handle)
```

Modified properties:

```
public SCNProgramDelegate ISCNProgramDelegate Delegate { get; set; }
```

### Type Changed: SceneKit.SCNProgramDelegate

Modified constructors:

```
public protected SCNProgramDelegate (Foundation.NSObjectFlag t)
	public protected SCNProgramDelegate (IntPtr handle)
```

Removed methods:

```
[Obsolete ("Do not use; this method only exist in OSX, not in iOS")]
	public virtual bool BindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);

	[Obsolete ("Do not use; this method only exist in OSX, not in iOS")]
	public virtual bool IsProgramOpaque (SCNProgram program);

	[Obsolete ("Do not use; this method only exist in OSX, not in iOS")]
	public virtual void UnbindValue (SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
```

### Type Changed: SceneKit.SCNProgramDelegate_Extensions

Removed methods:

```
[Obsolete ("Do not use; this method only exist in OSX, not in iOS")]
	public static bool BindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);

	[Obsolete ("Do not use; this method only exist in OSX, not in iOS")]
	public static bool IsProgramOpaque (ISCNProgramDelegate This, SCNProgram program);

	[Obsolete ("Do not use; this method only exist in OSX, not in iOS")]
	public static void UnbindValue (ISCNProgramDelegate This, SCNProgram program, string symbol, uint location, uint programID, SCNRenderer renderer);
```

### Type Changed: SceneKit.SCNPyramid

Modified constructors:

```
public protected SCNPyramid (Foundation.NSObjectFlag t)
	public protected SCNPyramid (IntPtr handle)
```

### Type Changed: SceneKit.SCNQuaternion

Modified fields:

```
public readonly SCNQuaternion Identity;
```

Removed property:

```
[Obsolete ("Use Xyz property instead.")]
	public SCNVector3 XYZ { get; set; }
```

Removed methods:

```
[Obsolete ("Use Multiply instead.")]
	public static SCNQuaternion Mult (SCNQuaternion left, SCNQuaternion right);

	[Obsolete ("Use Multiply instead.")]
	public static void Mult (ref SCNQuaternion left, ref SCNQuaternion right, out SCNQuaternion result);

	[Obsolete ("Use the overload without the ref float scale")]
	public static void Multiply (ref SCNQuaternion quaternion, ref float scale, out SCNQuaternion result);
```

### Type Changed: SceneKit.SCNRenderer

Modified constructors:

```
public protected SCNRenderer (Foundation.NSObjectFlag t)
	public protected SCNRenderer (IntPtr handle)
```

Modified properties:

```
public SCNSceneRendererDelegate ISCNSceneRendererDelegate SceneRendererDelegate { get; set; }
```

### Type Changed: SceneKit.SCNScene

Modified constructors:

```
public protected SCNScene (Foundation.NSObjectFlag t)
	public protected SCNScene (IntPtr handle)
```

### Type Changed: SceneKit.SCNSceneExportDelegate

Modified constructors:

```
public protected SCNSceneExportDelegate (Foundation.NSObjectFlag t)
	public protected SCNSceneExportDelegate (IntPtr handle)
```

### Type Changed: SceneKit.SCNSceneRenderer

Modified constructors:

```
public protected SCNSceneRenderer ()
	public protected SCNSceneRenderer (Foundation.NSObjectFlag t)
	public protected SCNSceneRenderer (IntPtr handle)
```

Modified properties:

```
public abstract bool AutoenablesDefaultLighting { get; set; }
	public abstract IntPtr Context { get; }
	public abstract bool JitteringEnabled { get; set; }
	public abstract bool Loops { get; set; }
	public abstract SpriteKit.SKScene OverlayScene { get; set; }
	public abstract bool Playing { get; set; }
	public abstract SCNNode PointOfView { get; set; }
	public abstract SCNScene Scene { get; set; }
	public SCNSceneRendererDelegate ISCNSceneRendererDelegate SceneRendererDelegate { get; set; }
	public abstract double SceneTimeInSeconds { get; set; }
	public abstract bool ShowsStatistics { get; set; }
	public abstract Foundation.NSObject WeakSceneRendererDelegate { get; set; }
```

Modified methods:

```
public abstract bool IsNodeInsideFrustum (SCNNode node, SCNNode pointOfView)
	public abstract bool Prepare (Foundation.NSObject obj, System.Func<bool> abortHandler)
	public abstract void Prepare (Foundation.NSObject[] objects, System.Action<bool> completionHandler)
	public abstract SCNVector3 ProjectPoint (SCNVector3 point)
	public abstract SCNVector3 UnprojectPoint (SCNVector3 point)
```

### Type Changed: SceneKit.SCNSceneRenderer_Extensions

Removed methods:

```
public static bool GetAutoenablesDefaultLighting (ISCNSceneRenderer This);
	public static IntPtr GetContext (ISCNSceneRenderer This);
	public static bool GetJitteringEnabled (ISCNSceneRenderer This);
	public static bool GetLoops (ISCNSceneRenderer This);
	public static SpriteKit.SKScene GetOverlayScene (ISCNSceneRenderer This);
	public static bool GetPlaying (ISCNSceneRenderer This);
	public static SCNNode GetPointOfView (ISCNSceneRenderer This);
	public static SCNScene GetScene (ISCNSceneRenderer This);
	public static double GetSceneTimeInSeconds (ISCNSceneRenderer This);
	public static bool GetShowsStatistics (ISCNSceneRenderer This);
	public static Foundation.NSObject GetWeakSceneRendererDelegate (ISCNSceneRenderer This);
	public static bool IsNodeInsideFrustum (ISCNSceneRenderer This, SCNNode node, SCNNode pointOfView);
	public static void Prepare (ISCNSceneRenderer This, Foundation.NSObject[] objects, System.Action<bool> completionHandler);
	public static bool Prepare (ISCNSceneRenderer This, Foundation.NSObject obj, System.Func<bool> abortHandler);
	public static SCNVector3 ProjectPoint (ISCNSceneRenderer This, SCNVector3 point);
	public static void SetAutoenablesDefaultLighting (ISCNSceneRenderer This, bool value);
	public static void SetJitteringEnabled (ISCNSceneRenderer This, bool value);
	public static void SetLoops (ISCNSceneRenderer This, bool value);
	public static void SetOverlayScene (ISCNSceneRenderer This, SpriteKit.SKScene value);
	public static void SetPlaying (ISCNSceneRenderer This, bool value);
	public static void SetPointOfView (ISCNSceneRenderer This, SCNNode value);
	public static void SetScene (ISCNSceneRenderer This, SCNScene value);
	public static void SetSceneTimeInSeconds (ISCNSceneRenderer This, double value);
	public static void SetShowsStatistics (ISCNSceneRenderer This, bool value);
	public static void SetWeakSceneRendererDelegate (ISCNSceneRenderer This, Foundation.NSObject value);
	public static SCNVector3 UnprojectPoint (ISCNSceneRenderer This, SCNVector3 point);
```

### Type Changed: SceneKit.SCNSceneRendererDelegate

Modified constructors:

```
public protected SCNSceneRendererDelegate (Foundation.NSObjectFlag t)
	public protected SCNSceneRendererDelegate (IntPtr handle)
```

Removed methods:

```
public virtual void DidApplyAnimations (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void DidRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public virtual void DidSimulatePhysics (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void Update (SCNSceneRenderer renderer, double timeInSeconds);
	public virtual void WillRenderScene (SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
```

Added methods:

```
public virtual void DidApplyAnimations (ISCNSceneRenderer renderer, double timeInSeconds);
	public virtual void DidRenderScene (ISCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public virtual void DidSimulatePhysics (ISCNSceneRenderer renderer, double timeInSeconds);
	public virtual void Update (ISCNSceneRenderer renderer, double timeInSeconds);
	public virtual void WillRenderScene (ISCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
```

### Type Changed: SceneKit.SCNSceneRendererDelegate_Extensions

Removed methods:

```
public static void DidApplyAnimations (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, double timeInSeconds);
	public static void DidRenderScene (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public static void DidSimulatePhysics (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, double timeInSeconds);
	public static void Update (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, double timeInSeconds);
	public static void WillRenderScene (ISCNSceneRendererDelegate This, SCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
```

Added methods:

```
public static void DidApplyAnimations (ISCNSceneRendererDelegate This, ISCNSceneRenderer renderer, double timeInSeconds);
	public static void DidRenderScene (ISCNSceneRendererDelegate This, ISCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
	public static void DidSimulatePhysics (ISCNSceneRendererDelegate This, ISCNSceneRenderer renderer, double timeInSeconds);
	public static void Update (ISCNSceneRendererDelegate This, ISCNSceneRenderer renderer, double timeInSeconds);
	public static void WillRenderScene (ISCNSceneRendererDelegate This, ISCNSceneRenderer renderer, SCNScene scene, double timeInSeconds);
```

### Type Changed: SceneKit.SCNSceneSource

Modified constructors:

```
public protected SCNSceneSource (Foundation.NSObjectFlag t)
	public protected SCNSceneSource (IntPtr handle)
```

Removed method:

```
public virtual Foundation.NSObject[] IdentifiersOfEntriesWithClass (ObjCRuntime.Class entryClass);
```

Added method:

```
public virtual string[] GetIdentifiersOfEntries (ObjCRuntime.Class entryClass);
```

### Type Changed: SceneKit.SCNShadable

Modified constructors:

```
public protected SCNShadable (Foundation.NSObjectFlag t)
	public protected SCNShadable (IntPtr handle)
```

### Type Changed: SceneKit.SCNShape

Modified constructors:

```
public protected SCNShape (Foundation.NSObjectFlag t)
	public protected SCNShape (IntPtr handle)
```

### Type Changed: SceneKit.SCNSkinner

Modified constructors:

```
public protected SCNSkinner (Foundation.NSObjectFlag t)
	public protected SCNSkinner (IntPtr handle)
```

### Type Changed: SceneKit.SCNSphere

Modified constructors:

```
public protected SCNSphere (Foundation.NSObjectFlag t)
	public protected SCNSphere (IntPtr handle)
```

### Type Changed: SceneKit.SCNTechnique

Modified constructors:

```
public protected SCNTechnique (Foundation.NSObjectFlag t)
	public protected SCNTechnique (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use ToDictionary () instead")]
	public virtual Foundation.NSDictionary DictionaryRepresentation { get; }
```

Removed method:

```
protected override void Dispose (bool disposing);
```

Modified methods:

```
public virtual Foundation.NSDictionary ToDictionary ()
```

### Type Changed: SceneKit.SCNTechniqueSupport

Modified constructors:

```
public protected SCNTechniqueSupport ()
	public protected SCNTechniqueSupport (Foundation.NSObjectFlag t)
	public protected SCNTechniqueSupport (IntPtr handle)
```

### Type Changed: SceneKit.SCNText

Modified constructors:

```
public protected SCNText (Foundation.NSObjectFlag t)
	public protected SCNText (IntPtr handle)
```

### Type Changed: SceneKit.SCNTorus

Modified constructors:

```
public protected SCNTorus (Foundation.NSObjectFlag t)
	public protected SCNTorus (IntPtr handle)
```

### Type Changed: SceneKit.SCNTransaction

Modified constructors:

```
public protected SCNTransaction (Foundation.NSObjectFlag t)
	public protected SCNTransaction (IntPtr handle)
```

Removed method:

```
public static void SetCompletionBlock (Foundation.NSAction completion);
```

Added method:

```
public static void SetCompletionBlock (System.Action completion);
```

### Type Changed: SceneKit.SCNTransformConstraint

Modified constructors:

```
public protected SCNTransformConstraint (Foundation.NSObjectFlag t)
	public protected SCNTransformConstraint (IntPtr handle)
```

### Type Changed: SceneKit.SCNTube

Modified constructors:

```
public protected SCNTube (Foundation.NSObjectFlag t)
	public protected SCNTube (IntPtr handle)
```

### Type Changed: SceneKit.SCNVector3

Removed methods:

```
[Obsolete ("Use static Add() method instead.")]
	public void Add (SCNVector3 right);

	[Obsolete ("Use static Add() method instead.")]
	public void Add (ref SCNVector3 right);

	[Obsolete ("Use static Divide() method instead.")]
	public static void Div (ref SCNVector3 a, float f, out SCNVector3 result);

	[Obsolete ("Use static Divide() method instead.")]
	public static SCNVector3 Div (SCNVector3 a, float f);

	[Obsolete ("Use static Divide() method instead.")]
	public void Div (float f);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Mult (float f);

	[Obsolete ("Use static Multiply() method instead.")]
	public static void Mult (ref SCNVector3 a, float f, out SCNVector3 result);

	[Obsolete ("Use static Multiply() method instead.")]
	public static SCNVector3 Mult (SCNVector3 a, float f);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (float sx, float sy, float sz);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (SCNVector3 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (ref SCNVector3 scale);

	[Obsolete ("Use static Subtract() method instead.")]
	public static void Sub (ref SCNVector3 a, ref SCNVector3 b, out SCNVector3 result);

	[Obsolete ("Use static Subtract() method instead.")]
	public static SCNVector3 Sub (SCNVector3 a, SCNVector3 b);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (SCNVector3 right);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (ref SCNVector3 right);
```

### Type Changed: SceneKit.SCNVector4

Modified fields:

```
public readonly SCNVector4 UnitW;
	public readonly SCNVector4 UnitX;
	public readonly SCNVector4 UnitY;
	public readonly SCNVector4 UnitZ;
	public readonly SCNVector4 Zero;
```

Removed methods:

```
[Obsolete ("Use static Add() method instead.")]
	public void Add (SCNVector4 right);

	[Obsolete ("Use static Add() method instead.")]
	public void Add (ref SCNVector4 right);

	[Obsolete ("Use static Divide() method instead.")]
	public void Div (float f);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Mult (float f);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (ref SCNVector4 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (SCNVector4 scale);

	[Obsolete ("Use static Multiply() method instead.")]
	public void Scale (float sx, float sy, float sz, float sw);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (SCNVector4 right);

	[Obsolete ("Use static Subtract() method instead.")]
	public void Sub (ref SCNVector4 right);
```

### Type Changed: SceneKit.SCNView

Modified constructors:

```
public protected SCNView (Foundation.NSObjectFlag t)
	public protected SCNView (IntPtr handle)
```

Modified properties:

```
public virtual OpenGLES.EAGLContext IntPtr Context { get; set; }
	public SCNSceneRendererDelegate ISCNSceneRendererDelegate SceneRendererDelegate { get; set; }
```

Added property:

```
public virtual OpenGLES.EAGLContext EAGLContext { get; set; }
```

### Removed Type SceneKit.SCNActionable_Extensions ### Removed Type SceneKit.SCNAnimatable_Extensions ### Removed Type SceneKit.SCNBoundingVolume_Extensions ### Removed Type SceneKit.SCNTechniqueSupport_Extensions 



## Namespace Security



### Type Changed: Security.SecCertificate

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: Security.SecIdentity

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: Security.SecKey

Removed methods:

```
[Obsolete ("Use the Decrypt overload which returns (out) the plainText array so you can adjust it if needed")]
	public SecStatusCode Decrypt (SecPadding padding, byte[] cipherText, byte[] plainText);

	[Obsolete ("Use the Decrypt overload which returns (ref) the plainTextLen value so you can adjust it if needed")]
	public SecStatusCode Decrypt (SecPadding padding, IntPtr cipherText, int cipherTextLen, IntPtr plainText, int plainTextLen);

	[Obsolete ("Use the Encrypt overload which returns (out) the cipherTextLen value so you can adjust it if needed")]
	public SecStatusCode Encrypt (SecPadding padding, IntPtr plainText, int plainTextLen, IntPtr cipherText, int cipherTextLen);
```

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: Security.SecKeyChain

Added interface:

```
ObjCRuntime.INativeObject
```

Added property:

```
public virtual IntPtr Handle { get; }
```

### Type Changed: Security.SecRecord

Removed property:

```
[Obsolete ("Use GetValueRef and SetValueRef instead")]
	public Foundation.NSObject ValueRef { get; set; }
```

Modified properties:

```
public Foundation.NSArray SecKeyChain[] MatchItemList { get; set; }
```

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

### Type Changed: Security.SslProtocol

Removed value:

```
[Obsolete ("Use Ssl_3_0")]
	Ssl3_0 = 2,
```

## Namespace Social



### Type Changed: Social.SLComposeServiceViewController

Modified constructors:

```
public protected SLComposeServiceViewController (Foundation.NSObjectFlag t)
	public protected SLComposeServiceViewController (IntPtr handle)
```

### Type Changed: Social.SLComposeSheetConfigurationItem

Modified constructors:

```
public protected SLComposeSheetConfigurationItem (Foundation.NSObjectFlag t)
	public protected SLComposeSheetConfigurationItem (IntPtr handle)
```

### Type Changed: Social.SLComposeViewController

Modified constructors:

```
public protected SLComposeViewController (Foundation.NSObjectFlag t)
	public protected SLComposeViewController (IntPtr handle)
```

### Type Changed: Social.SLRequest

Modified constructors:

```
public protected SLRequest (Foundation.NSObjectFlag t)
	public protected SLRequest (IntPtr handle)
```

## Namespace SpriteKit



### Type Changed: SpriteKit.SK3DNode

Modified constructors:

```
public protected SK3DNode (Foundation.NSObjectFlag t)
	public protected SK3DNode (IntPtr handle)
```

### Type Changed: SpriteKit.SKAction

Modified constructors:

```
public protected SKAction (Foundation.NSObjectFlag t)
	public protected SKAction (IntPtr handle)
```

Removed methods:

```
[Obsolete ("Use Run(Action) instead")]
	public static SKAction RunBlock (System.Action block);

	[Obsolete ("Use Run(Action,DispatchQueue) instead")]
	public static SKAction RunBlock (System.Action block, CoreFoundation.DispatchQueue queue);
```

### Type Changed: SpriteKit.SKConstraint

Modified constructors:

```
public protected SKConstraint (Foundation.NSObjectFlag t)
	public protected SKConstraint (IntPtr handle)
```

### Type Changed: SpriteKit.SKCropNode

Modified constructors:

```
public protected SKCropNode (Foundation.NSObjectFlag t)
	public protected SKCropNode (IntPtr handle)
```

### Type Changed: SpriteKit.SKEffectNode

Modified constructors:

```
public protected SKEffectNode (Foundation.NSObjectFlag t)
	public protected SKEffectNode (IntPtr handle)
```

### Type Changed: SpriteKit.SKEmitterNode

Modified constructors:

```
public protected SKEmitterNode (Foundation.NSObjectFlag t)
	public protected SKEmitterNode (IntPtr handle)
```

### Type Changed: SpriteKit.SKFieldNode

Modified constructors:

```
public protected SKFieldNode (Foundation.NSObjectFlag t)
	public protected SKFieldNode (IntPtr handle)
```

### Type Changed: SpriteKit.SKKeyframeSequence

Modified constructors:

```
public protected SKKeyframeSequence (IntPtr handle)
	public protected SKKeyframeSequence (Foundation.NSObjectFlag t)
```

### Type Changed: SpriteKit.SKLabelNode

Modified constructors:

```
public protected SKLabelNode (Foundation.NSObjectFlag t)
	public protected SKLabelNode (IntPtr handle)
```

### Type Changed: SpriteKit.SKLightNode

Modified constructors:

```
public protected SKLightNode (Foundation.NSObjectFlag t)
	public protected SKLightNode (IntPtr handle)
```

### Type Changed: SpriteKit.SKMutableTexture

Modified constructors:

```
public protected SKMutableTexture (Foundation.NSObjectFlag t)
	public protected SKMutableTexture (IntPtr handle)
```

### Type Changed: SpriteKit.SKNode

Modified constructors:

```
public protected SKNode (Foundation.NSObjectFlag t)
	public protected SKNode (IntPtr handle)
```

Removed property:

```
public virtual float Scale { set; }
```

Added methods:

```
public virtual void SetScale (float scale);
```

### Type Changed: SpriteKit.SKPhysicsBody

Modified constructors:

```
public protected SKPhysicsBody (Foundation.NSObjectFlag t)
	public protected SKPhysicsBody (IntPtr handle)
```

Removed methods:

```
[Obsolete ("Use the method FromBodies instead")]
	public static SKPhysicsBody BodyWithBodies (SKPhysicsBody[] bodies);

	[Obsolete ("Use the CreateCircularBody method instead")]
	public static SKPhysicsBody BodyWithCircleOfRadius (float radius);

	[Obsolete ("Use the CreateCircularBody method instead")]
	public static SKPhysicsBody BodyWithCircleOfRadius (float radius, System.Drawing.PointF center);

	[Obsolete ("Use the CreateEdgeChain method instead")]
	public static SKPhysicsBody BodyWithEdgeChainFromPath (CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateEdge method instead")]
	public static SKPhysicsBody BodyWithEdgeFromPoint (System.Drawing.PointF fromPoint, System.Drawing.PointF toPoint);

	[Obsolete ("Use the CreateEdgeLoop method instead")]
	public static SKPhysicsBody BodyWithEdgeLoopFromPath (CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateEdgeLoop method instead")]
	public static SKPhysicsBody BodyWithEdgeLoopFromRect (System.Drawing.RectangleF rect);

	[Obsolete ("Use the CreateBodyFromPath method instead")]
	public static SKPhysicsBody BodyWithPolygonFromPath (CoreGraphics.CGPath path);

	[Obsolete ("Use the CreateRectangularBody method instead")]
	public static SKPhysicsBody BodyWithRectangleOfSize (System.Drawing.SizeF size);

	[Obsolete ("Use the CreateRectangularBody method instead")]
	public static SKPhysicsBody BodyWithRectangleOfSize (System.Drawing.SizeF size, System.Drawing.PointF center);
```

### Type Changed: SpriteKit.SKPhysicsContact

Modified constructors:

```
public protected SKPhysicsContact (Foundation.NSObjectFlag t)
	public protected SKPhysicsContact (IntPtr handle)
```

### Type Changed: SpriteKit.SKPhysicsContactDelegate

Modified constructors:

```
public protected SKPhysicsContactDelegate (Foundation.NSObjectFlag t)
	public protected SKPhysicsContactDelegate (IntPtr handle)
```

### Type Changed: SpriteKit.SKPhysicsJoint

Modified constructors:

```
public protected SKPhysicsJoint ()
	public protected SKPhysicsJoint (Foundation.NSCoder coder)
	public protected SKPhysicsJoint (Foundation.NSObjectFlag t)
	public protected SKPhysicsJoint (IntPtr handle)
```

### Type Changed: SpriteKit.SKPhysicsJointFixed

Modified constructors:

```
public protected SKPhysicsJointFixed (Foundation.NSObjectFlag t)
	public protected SKPhysicsJointFixed (IntPtr handle)
```

### Type Changed: SpriteKit.SKPhysicsJointLimit

Modified constructors:

```
public protected SKPhysicsJointLimit (Foundation.NSObjectFlag t)
	public protected SKPhysicsJointLimit (IntPtr handle)
```

### Type Changed: SpriteKit.SKPhysicsJointPin

Modified constructors:

```
public protected SKPhysicsJointPin (Foundation.NSObjectFlag t)
	public protected SKPhysicsJointPin (IntPtr handle)
```

### Type Changed: SpriteKit.SKPhysicsJointSliding

Modified constructors:

```
public protected SKPhysicsJointSliding (Foundation.NSObjectFlag t)
	public protected SKPhysicsJointSliding (IntPtr handle)
```

### Type Changed: SpriteKit.SKPhysicsJointSpring

Modified constructors:

```
public protected SKPhysicsJointSpring (Foundation.NSObjectFlag t)
	public protected SKPhysicsJointSpring (IntPtr handle)
```

### Type Changed: SpriteKit.SKPhysicsWorld

Modified constructors:

```
public protected SKPhysicsWorld (Foundation.NSObjectFlag t)
	public protected SKPhysicsWorld (IntPtr handle)
```

Modified properties:

```
public SKPhysicsContactDelegate ISKPhysicsContactDelegate ContactDelegate { get; set; }
```

### Type Changed: SpriteKit.SKRange

Modified constructors:

```
public protected SKRange (Foundation.NSObjectFlag t)
	public protected SKRange (IntPtr handle)
```

### Type Changed: SpriteKit.SKReachConstraints

Modified constructors:

```
public protected SKReachConstraints (Foundation.NSObjectFlag t)
	public protected SKReachConstraints (IntPtr handle)
```

### Type Changed: SpriteKit.SKRegion

Modified constructors:

```
public protected SKRegion (Foundation.NSObjectFlag t)
	public protected SKRegion (IntPtr handle)
```

### Type Changed: SpriteKit.SKScene

Modified constructors:

```
public protected SKScene (Foundation.NSObjectFlag t)
	public protected SKScene (IntPtr handle)
```

Modified properties:

```
public SKSceneDelegate ISKSceneDelegate Delegate { get; set; }
```

### Type Changed: SpriteKit.SKSceneDelegate

Modified constructors:

```
public protected SKSceneDelegate (Foundation.NSObjectFlag t)
	public protected SKSceneDelegate (IntPtr handle)
```

### Type Changed: SpriteKit.SKShader

Modified constructors:

```
public protected SKShader (Foundation.NSObjectFlag t)
	public protected SKShader (IntPtr handle)
```

### Type Changed: SpriteKit.SKShapeNode

Modified constructors:

```
public protected SKShapeNode (Foundation.NSObjectFlag t)
	public protected SKShapeNode (IntPtr handle)
```

### Type Changed: SpriteKit.SKSpriteNode

Modified constructors:

```
public protected SKSpriteNode (IntPtr handle)
	public protected SKSpriteNode (Foundation.NSObjectFlag t)
```

### Type Changed: SpriteKit.SKTexture

Modified constructors:

```
public protected SKTexture (Foundation.NSObjectFlag t)
	public protected SKTexture (IntPtr handle)
```

Removed methods:

```
public virtual void Preload (Foundation.NSAction completion);
	public static void PreloadTextures (SKTexture[] textures, Foundation.NSAction completion);
```

Added methods:

```
public virtual void Preload (System.Action completion);
	public static void PreloadTextures (SKTexture[] textures, System.Action completion);
```

### Type Changed: SpriteKit.SKTextureAtlas

Modified constructors:

```
public protected SKTextureAtlas (Foundation.NSObjectFlag t)
	public protected SKTextureAtlas (IntPtr handle)
```

Removed methods:

```
public virtual void Preload (Foundation.NSAction completion);
	public static void PreloadTextures (SKTextureAtlas[] textures, Foundation.NSAction completion);
```

Added methods:

```
public virtual void Preload (System.Action completion);
	public static void PreloadTextures (SKTextureAtlas[] textures, System.Action completion);
```

### Type Changed: SpriteKit.SKTransition

Modified constructors:

```
public protected SKTransition (Foundation.NSObjectFlag t)
	public protected SKTransition (IntPtr handle)
```

### Type Changed: SpriteKit.SKUniform

Modified constructors:

```
public protected SKUniform (IntPtr handle)
	public protected SKUniform (Foundation.NSObjectFlag t)
```

### Type Changed: SpriteKit.SKVideoNode

Modified constructors:

```
public protected SKVideoNode (Foundation.NSObjectFlag t)
	public protected SKVideoNode (IntPtr handle)
```

### Type Changed: SpriteKit.SKView

Modified constructors:

```
public protected SKView (Foundation.NSObjectFlag t)
	public protected SKView (IntPtr handle)
```

## Namespace StoreKit



### Type Changed: StoreKit.SKDownload

Modified constructors:

```
public protected SKDownload (Foundation.NSObjectFlag t)
	public protected SKDownload (IntPtr handle)
```

### Type Changed: StoreKit.SKMutablePayment

Modified constructors:

```
public protected SKMutablePayment (Foundation.NSObjectFlag t)
	public protected SKMutablePayment (IntPtr handle)
```

### Type Changed: StoreKit.SKPayment

Modified constructors:

```
public protected SKPayment (Foundation.NSObjectFlag t)
	public protected SKPayment (IntPtr handle)
```

### Type Changed: StoreKit.SKPaymentQueue

Modified constructors:

```
public protected SKPaymentQueue (Foundation.NSObjectFlag t)
	public protected SKPaymentQueue (IntPtr handle)
```

Removed methods:

```
public virtual void AddTransactionObserver (SKPaymentTransactionObserver observer);
	public virtual void RemoveTransactionObserver (SKPaymentTransactionObserver observer);
```

Added methods:

```
public virtual void AddTransactionObserver (ISKPaymentTransactionObserver observer);
	public virtual void RemoveTransactionObserver (ISKPaymentTransactionObserver observer);
```

### Type Changed: StoreKit.SKPaymentTransaction

Modified constructors:

```
public protected SKPaymentTransaction (Foundation.NSObjectFlag t)
	public protected SKPaymentTransaction (IntPtr handle)
```

### Type Changed: StoreKit.SKPaymentTransactionObserver

Modified constructors:

```
public protected SKPaymentTransactionObserver ()
	public protected SKPaymentTransactionObserver (Foundation.NSObjectFlag t)
	public protected SKPaymentTransactionObserver (IntPtr handle)
```

### Type Changed: StoreKit.SKProduct

Modified constructors:

```
public protected SKProduct (Foundation.NSObjectFlag t)
	public protected SKProduct (IntPtr handle)
```

### Type Changed: StoreKit.SKProductsRequest

Modified constructors:

```
public protected SKProductsRequest (Foundation.NSObjectFlag t)
	public protected SKProductsRequest (IntPtr handle)
```

Modified properties:

```
public SKProductsRequestDelegate ISKProductsRequestDelegate Delegate { get; set; }
```

Removed events:

```
public event System.EventHandler<SKRequestErrorEventArgs> RequestFailed;
	public event System.EventHandler RequestFinished;
```

### Type Changed: StoreKit.SKProductsRequestDelegate

Modified constructors:

```
public protected SKProductsRequestDelegate ()
	public protected SKProductsRequestDelegate (Foundation.NSObjectFlag t)
	public protected SKProductsRequestDelegate (IntPtr handle)
```

Removed methods:

```
public override void RequestFailed (SKRequest request, Foundation.NSError error);
	public override void RequestFinished (SKRequest request);
```

### Type Changed: StoreKit.SKProductsResponse

Modified constructors:

```
public protected SKProductsResponse (Foundation.NSObjectFlag t)
	public protected SKProductsResponse (IntPtr handle)
```

### Type Changed: StoreKit.SKReceiptRefreshRequest

Modified constructors:

```
public protected SKReceiptRefreshRequest (Foundation.NSObjectFlag t)
	public protected SKReceiptRefreshRequest (IntPtr handle)
```

### Type Changed: StoreKit.SKRequest

Modified constructors:

```
public protected SKRequest (Foundation.NSObjectFlag t)
	public protected SKRequest (IntPtr handle)
```

Modified properties:

```
public SKRequestDelegate ISKRequestDelegate Delegate { get; set; }
```

### Type Changed: StoreKit.SKRequestDelegate

Modified constructors:

```
public protected SKRequestDelegate (Foundation.NSObjectFlag t)
	public protected SKRequestDelegate (IntPtr handle)
```

### Type Changed: StoreKit.SKStoreProductViewController

Modified constructors:

```
public protected SKStoreProductViewController (Foundation.NSObjectFlag t)
	public protected SKStoreProductViewController (IntPtr handle)
```

Modified properties:

```
public SKStoreProductViewControllerDelegate ISKStoreProductViewControllerDelegate Delegate { get; set; }
```

Removed method:

```
public System.Threading.Tasks.Task<bool> LoadProductAsync (StoreProductParameters parameters);
```

Added method:

```
public System.Threading.Tasks.Task<System.Tuple<System.Boolean,Foundation.NSError>> LoadProductAsync (StoreProductParameters parameters);
```

### Type Changed: StoreKit.SKStoreProductViewControllerDelegate

Modified constructors:

```
public protected SKStoreProductViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected SKStoreProductViewControllerDelegate (IntPtr handle)
```

### Removed Type StoreKit.SKProductsRequestDelegate_Extensions 

## Namespace SystemConfiguration



### Type Changed: SystemConfiguration.CaptiveNetwork

Removed methods:

```
[Obsolete ("Replaced by TryCopyCurrentNetworkInfo")]
	public static Foundation.NSDictionary CopyCurrentNetworkInfo (string interfaceName);

	[Obsolete ("Replaced by TryGetSupportedInterfaces")]
	public static string[] GetSupportedInterfaces ();
```

### Type Changed: SystemConfiguration.NetworkReachability

Removed method:

```
[Obsolete ("Use SetNotification instead")]
	public bool SetCallback (NetworkReachability.Notification callback);
```

Modified methods:

```
public protected virtual void Dispose (bool disposing)
```

## Namespace Twitter



### Type Changed: Twitter.TWRequest

Modified constructors:

```
public protected TWRequest (Foundation.NSObjectFlag t)
	public protected TWRequest (IntPtr handle)
```

### Type Changed: Twitter.TWTweetComposeViewController

Modified constructors:

```
public protected TWTweetComposeViewController (Foundation.NSObjectFlag t)
	public protected TWTweetComposeViewController (IntPtr handle)
```

Removed method:

```
public virtual void SetCompletionHandler (TWTweetComposeHandler handler);
```

Added method:

```
public virtual void SetCompletionHandler (System.Action<TWTweetComposeViewControllerResult> handler);
```

### Removed Type Twitter.TWTweetComposeHandler 

## Namespace UIKit



### Type Changed: UIKit.INSTextAttachmentContainer

Added methods:

```
public virtual System.Drawing.RectangleF GetAttachmentBounds (NSTextContainer textContainer, System.Drawing.RectangleF proposedLineFragment, System.Drawing.PointF glyphPosition, uint characterIndex);
	public virtual UIImage GetImageForBounds (System.Drawing.RectangleF bounds, NSTextContainer textContainer, uint characterIndex);
```

### Type Changed: UIKit.IUIBarPositioning

Added property:

```
public virtual UIBarPosition BarPosition { get; }
```

### Type Changed: UIKit.IUISearchResultsUpdating

Added method:

```
public virtual void UpdateSearchResultsForSearchController (UISearchController searchController);
```

### Type Changed: UIKit.IUITextInputDelegate

Removed methods:

```
public virtual void SelectionDidChange (Foundation.NSObject uiTextInput);
	public virtual void SelectionWillChange (Foundation.NSObject uiTextInput);
	public virtual void TextDidChange (Foundation.NSObject textInput);
	public virtual void TextWillChange (Foundation.NSObject textInput);
```

Added methods:

```
public virtual void SelectionDidChange (IUITextInput uiTextInput);
	public virtual void SelectionWillChange (IUITextInput uiTextInput);
	public virtual void TextDidChange (IUITextInput textInput);
	public virtual void TextWillChange (IUITextInput textInput);
```

### Type Changed: UIKit.IUITraitEnvironment

Added property:

```
public virtual UITraitCollection TraitCollection { get; }
```

Added method:

```
public virtual void TraitCollectionDidChange (UITraitCollection previousTraitCollection);
```

### Type Changed: UIKit.IUIViewControllerContextTransitioning

Added property:

```
public virtual CoreGraphics.CGAffineTransform TargetTransform { get; }
```

Added method:

```
public virtual UIView GetViewFor (Foundation.NSString uiTransitionContextToOrFromKey);
```

### Type Changed: UIKit.IUIViewControllerTransitionCoordinatorContext

Added methods:

```
public virtual UIView GetTransitionViewControllerForKey (Foundation.NSString key);
	public virtual CoreGraphics.CGAffineTransform TargetTransform ();
```

### Type Changed: UIKit.NSAttributedStringAttachmentConveniences

Removed method:

```
public static Foundation.NSAttributedString FromTextAttachment (Foundation.NSAttributedString This, NSTextAttachment attachment);
```

### Type Changed: UIKit.NSFileProviderExtension

Modified constructors:

```
public protected NSFileProviderExtension (Foundation.NSObjectFlag t)
	public protected NSFileProviderExtension (IntPtr handle)
```

### Type Changed: UIKit.NSLayoutConstraint

Modified constructors:

```
public protected NSLayoutConstraint (Foundation.NSObjectFlag t)
	public protected NSLayoutConstraint (IntPtr handle)
```

### Type Changed: UIKit.NSLayoutManager

Modified constructors:

```
public protected NSLayoutManager (Foundation.NSObjectFlag t)
	public protected NSLayoutManager (IntPtr handle)
```

Modified properties:

```
public NSLayoutManagerDelegate INSLayoutManagerDelegate Delegate { get; set; }
```

Removed methods:

```
public virtual Foundation.NSRange CharacterRangeForGlyphRangeInternal (Foundation.NSRange glyphRange, IntPtr actualGlyphRange);
	public virtual uint GetLineFragmentInsertionPoints (uint charIndex, bool alternatePosition, bool inDisplayOrder, IntPtr positions, IntPtr charIndexes);
```

### Type Changed: UIKit.NSLayoutManagerDelegate

Modified constructors:

```
public protected NSLayoutManagerDelegate (Foundation.NSObjectFlag t)
	public protected NSLayoutManagerDelegate (IntPtr handle)
```

### Type Changed: UIKit.NSMutableParagraphStyle

Modified constructors:

```
public protected NSMutableParagraphStyle (Foundation.NSObjectFlag t)
	public protected NSMutableParagraphStyle (IntPtr handle)
```

### Type Changed: UIKit.NSParagraphStyle

Modified constructors:

```
public protected NSParagraphStyle (Foundation.NSObjectFlag t)
	public protected NSParagraphStyle (IntPtr handle)
```

### Type Changed: UIKit.NSShadow

Modified constructors:

```
public protected NSShadow (Foundation.NSObjectFlag t)
	public protected NSShadow (IntPtr handle)
```

### Type Changed: UIKit.NSTextAttachment

Modified constructors:

```
public protected NSTextAttachment (Foundation.NSObjectFlag t)
	public protected NSTextAttachment (IntPtr handle)
```

### Type Changed: UIKit.NSTextAttachmentContainer

Modified constructors:

```
public protected NSTextAttachmentContainer ()
	public protected NSTextAttachmentContainer (Foundation.NSObjectFlag t)
	public protected NSTextAttachmentContainer (IntPtr handle)
```

Modified methods:

```
public abstract System.Drawing.RectangleF GetAttachmentBounds (NSTextContainer textContainer, System.Drawing.RectangleF proposedLineFragment, System.Drawing.PointF glyphPosition, uint characterIndex)
	public abstract UIImage GetImageForBounds (System.Drawing.RectangleF bounds, NSTextContainer textContainer, uint characterIndex)
```

### Type Changed: UIKit.NSTextContainer

Modified constructors:

```
public protected NSTextContainer (Foundation.NSObjectFlag t)
	public protected NSTextContainer (IntPtr handle)
```

### Type Changed: UIKit.NSTextStorage

Modified constructors:

```
public protected NSTextStorage (Foundation.NSObjectFlag t)
	public protected NSTextStorage (IntPtr handle)
```

Modified properties:

```
public NSTextStorageDelegate INSTextStorageDelegate Delegate { get; set; }
```

### Type Changed: UIKit.NSTextStorageDelegate

Modified constructors:

```
public protected NSTextStorageDelegate (Foundation.NSObjectFlag t)
	public protected NSTextStorageDelegate (IntPtr handle)
```

### Type Changed: UIKit.NSTextTab

Modified constructors:

```
public protected NSTextTab (Foundation.NSObjectFlag t)
	public protected NSTextTab (IntPtr handle)
```

### Type Changed: UIKit.UIAcceleration

Modified constructors:

```
public protected UIAcceleration (Foundation.NSObjectFlag t)
	public protected UIAcceleration (IntPtr handle)
```

### Type Changed: UIKit.UIAccelerometer

Modified constructors:

```
public protected UIAccelerometer (Foundation.NSObjectFlag t)
	public protected UIAccelerometer (IntPtr handle)
```

Modified properties:

```
public UIAccelerometerDelegate IUIAccelerometerDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIAccelerometerDelegate

Modified constructors:

```
public protected UIAccelerometerDelegate (Foundation.NSObjectFlag t)
	public protected UIAccelerometerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIAccessibilityCustomAction

Modified constructors:

```
public protected UIAccessibilityCustomAction (Foundation.NSObjectFlag t)
	public protected UIAccessibilityCustomAction (IntPtr handle)
```

### Type Changed: UIKit.UIAccessibilityElement

Removed constructors:

```
public UIAccessibilityElement ();
```

Modified constructors:

```
public protected UIAccessibilityElement (Foundation.NSObjectFlag t)
	public protected UIAccessibilityElement (IntPtr handle)
```

### Type Changed: UIKit.UIActionSheet

Modified constructors:

```
public protected UIActionSheet (IntPtr handle)
	public protected UIActionSheet (Foundation.NSObjectFlag t)
```

Modified properties:

```
public UIActionSheetDelegate IUIActionSheetDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIActionSheetDelegate

Modified constructors:

```
public protected UIActionSheetDelegate (Foundation.NSObjectFlag t)
	public protected UIActionSheetDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIActivity

Modified constructors:

```
public protected UIActivity (Foundation.NSObjectFlag t)
	public protected UIActivity (IntPtr handle)
```

### Type Changed: UIKit.UIActivityIndicatorView

Modified constructors:

```
public protected UIActivityIndicatorView (Foundation.NSObjectFlag t)
	public protected UIActivityIndicatorView (IntPtr handle)
```

### Type Changed: UIKit.UIActivityItemProvider

Modified constructors:

```
public protected UIActivityItemProvider (Foundation.NSObjectFlag t)
	public protected UIActivityItemProvider (IntPtr handle)
```

### Type Changed: UIKit.UIActivityItemSource

Modified constructors:

```
public protected UIActivityItemSource ()
	public protected UIActivityItemSource (Foundation.NSObjectFlag t)
	public protected UIActivityItemSource (IntPtr handle)
```

### Type Changed: UIKit.UIActivityViewController

Modified constructors:

```
public protected UIActivityViewController (Foundation.NSObjectFlag t)
	public protected UIActivityViewController (IntPtr handle)
```

### Type Changed: UIKit.UIAdaptivePresentationControllerDelegate

Modified constructors:

```
public protected UIAdaptivePresentationControllerDelegate (Foundation.NSObjectFlag t)
	public protected UIAdaptivePresentationControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIAlertAction

Modified constructors:

```
public protected UIAlertAction (Foundation.NSObjectFlag t)
	public protected UIAlertAction (IntPtr handle)
```

### Type Changed: UIKit.UIAlertController

Modified constructors:

```
public protected UIAlertController (Foundation.NSObjectFlag t)
	public protected UIAlertController (IntPtr handle)
```

### Type Changed: UIKit.UIAlertView

Modified constructors:

```
public protected UIAlertView (Foundation.NSObjectFlag t)
	public protected UIAlertView (IntPtr handle)
```

Modified properties:

```
public UIAlertViewDelegate IUIAlertViewDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIAlertViewDelegate

Modified constructors:

```
public protected UIAlertViewDelegate (Foundation.NSObjectFlag t)
	public protected UIAlertViewDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIAppearance

Modified constructors:

```
public protected UIAppearance (Foundation.NSObjectFlag t)
	public protected UIAppearance (IntPtr handle)
```

Removed field:

```
public static IntPtr SelectorAppearance;
```

### Type Changed: UIKit.UIAppearanceContainer

Modified constructors:

```
public protected UIAppearanceContainer (Foundation.NSObjectFlag t)
	public protected UIAppearanceContainer (IntPtr handle)
```

### Type Changed: UIKit.UIApplication

Modified constructors:

```
public protected UIApplication (Foundation.NSObjectFlag t)
	public protected UIApplication (IntPtr handle)
```

Modified properties:

```
public UIApplicationDelegate IUIApplicationDelegate Delegate { get; set; }
```

Removed methods:

```
public virtual int BeginBackgroundTask (Foundation.NSAction backgroundTimeExpired);
	public virtual int BeginBackgroundTask (string taskName, Foundation.NSAction expirationHandler);
	public virtual void PresentLocationNotificationNow (UILocalNotification notification);
	public virtual bool SetKeepAliveTimeout (double timeout, Foundation.NSAction handler);
```

Added methods:

```
public virtual int BeginBackgroundTask (System.Action backgroundTimeExpired);
	public virtual int BeginBackgroundTask (string taskName, System.Action expirationHandler);
	public virtual void PresentLocalNotificationNow (UILocalNotification notification);
	public virtual bool SetKeepAliveTimeout (double timeout, System.Action handler);
```

### Type Changed: UIKit.UIApplicationDelegate

Modified constructors:

```
public protected UIApplicationDelegate (Foundation.NSObjectFlag t)
	public protected UIApplicationDelegate (IntPtr handle)
```

Removed methods:

```
public virtual void HandleEventsForBackgroundUrl (UIApplication application, string sessionIdentifier, Foundation.NSAction completionHandler);

	[Obsolete ("Override the overload accepting an UIApplication argument")]
	public virtual void UserActivityUpdated (Foundation.NSUserActivity userActivity);
```

Added method:

```
public virtual void HandleEventsForBackgroundUrl (UIApplication application, string sessionIdentifier, System.Action completionHandler);
```

### Type Changed: UIKit.UIApplicationDelegate_Extensions

Removed methods:

```
public static void HandleEventsForBackgroundUrl (IUIApplicationDelegate This, UIApplication application, string sessionIdentifier, Foundation.NSAction completionHandler);

	[Obsolete ("Override the overload accepting an UIApplication argument")]
	public static void UserActivityUpdated (IUIApplicationDelegate This, Foundation.NSUserActivity userActivity);
```

Added method:

```
public static void HandleEventsForBackgroundUrl (IUIApplicationDelegate This, UIApplication application, string sessionIdentifier, System.Action completionHandler);
```

### Type Changed: UIKit.UIAttachmentBehavior

Modified constructors:

```
public protected UIAttachmentBehavior (Foundation.NSObjectFlag t)
	public protected UIAttachmentBehavior (IntPtr handle)
```

### Type Changed: UIKit.UIBarButtonItem

Modified constructors:

```
public protected UIBarButtonItem (IntPtr handle)
	public protected UIBarButtonItem (Foundation.NSObjectFlag t)
```

### Type Changed: UIKit.UIBarItem

Modified constructors:

```
public protected UIBarItem ()
	public protected UIBarItem (Foundation.NSObjectFlag t)
	public protected UIBarItem (IntPtr handle)
```

### Type Changed: UIKit.UIBarPositioning

Modified constructors:

```
public protected UIBarPositioning ()
	public protected UIBarPositioning (Foundation.NSObjectFlag t)
	public protected UIBarPositioning (IntPtr handle)
```

Modified properties:

```
public abstract UIBarPosition BarPosition { get; }
```

### Type Changed: UIKit.UIBarPositioningDelegate

Modified constructors:

```
public protected UIBarPositioningDelegate (Foundation.NSObjectFlag t)
	public protected UIBarPositioningDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIBezierPath

Modified constructors:

```
public protected UIBezierPath (Foundation.NSObjectFlag t)
	public protected UIBezierPath (IntPtr handle)
```

### Type Changed: UIKit.UIBlurEffect

Modified constructors:

```
public protected UIBlurEffect (Foundation.NSObjectFlag t)
	public protected UIBlurEffect (IntPtr handle)
```

### Type Changed: UIKit.UIButton

Modified constructors:

```
public protected UIButton (Foundation.NSObjectFlag t)
	public protected UIButton (IntPtr handle)
```

### Type Changed: UIKit.UICollectionReusableView

Modified constructors:

```
public protected UICollectionReusableView (Foundation.NSObjectFlag t)
	public protected UICollectionReusableView (IntPtr handle)
```

### Type Changed: UIKit.UICollectionView

Modified constructors:

```
public protected UICollectionView (Foundation.NSObjectFlag t)
	public protected UICollectionView (IntPtr handle)
```

Modified properties:

```
public UICollectionViewDataSource IUICollectionViewDataSource DataSource { get; set; }
	public UICollectionViewDelegate IUICollectionViewDelegate Delegate { get; set; }
```

Removed methods:

```
public virtual Foundation.NSObject DequeueReusableCell (Foundation.NSString reuseIdentifier, Foundation.NSIndexPath indexPath);
	public virtual Foundation.NSObject DequeueReusableSupplementaryView (Foundation.NSString kind, Foundation.NSString identifier, Foundation.NSIndexPath indexPath);
	public virtual void PerformBatchUpdates (Foundation.NSAction updates, UICompletionHandler completed);
	public virtual System.Threading.Tasks.Task<bool> PerformBatchUpdatesAsync (Foundation.NSAction updates);
```

Added methods:

```
public virtual UICollectionReusableView DequeueReusableCell (Foundation.NSString reuseIdentifier, Foundation.NSIndexPath indexPath);
	public virtual UICollectionReusableView DequeueReusableSupplementaryView (Foundation.NSString kind, Foundation.NSString identifier, Foundation.NSIndexPath indexPath);
	public virtual void PerformBatchUpdates (System.Action updates, UICompletionHandler completed);
	public virtual System.Threading.Tasks.Task<bool> PerformBatchUpdatesAsync (System.Action updates);
```

### Type Changed: UIKit.UICollectionViewCell

Modified constructors:

```
public protected UICollectionViewCell (Foundation.NSObjectFlag t)
	public protected UICollectionViewCell (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewController

Modified constructors:

```
public protected UICollectionViewController (Foundation.NSObjectFlag t)
	public protected UICollectionViewController (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewDataSource

Modified constructors:

```
public protected UICollectionViewDataSource ()
	public protected UICollectionViewDataSource (Foundation.NSObjectFlag t)
	public protected UICollectionViewDataSource (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewDelegate

Modified constructors:

```
public protected UICollectionViewDelegate (Foundation.NSObjectFlag t)
	public protected UICollectionViewDelegate (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewDelegateFlowLayout

Modified constructors:

```
public protected UICollectionViewDelegateFlowLayout (Foundation.NSObjectFlag t)
	public protected UICollectionViewDelegateFlowLayout (IntPtr handle)
```

Removed methods:

```
public override bool CanPerformAction (UICollectionView collectionView, ObjCRuntime.Selector action, Foundation.NSIndexPath indexPath, Foundation.NSObject sender);
	public override void CellDisplayingEnded (UICollectionView collectionView, UICollectionViewCell cell, Foundation.NSIndexPath indexPath);
	public override void ItemDeselected (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public override void ItemHighlighted (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public override void ItemSelected (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public override void ItemUnhighlighted (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public override void PerformAction (UICollectionView collectionView, ObjCRuntime.Selector action, Foundation.NSIndexPath indexPath, Foundation.NSObject sender);
	public override bool ShouldDeselectItem (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public override bool ShouldHighlightItem (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public override bool ShouldSelectItem (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public override bool ShouldShowMenu (UICollectionView collectionView, Foundation.NSIndexPath indexPath);
	public override void SupplementaryViewDisplayingEnded (UICollectionView collectionView, UICollectionReusableView view, Foundation.NSString elementKind, Foundation.NSIndexPath indexPath);
	public override UICollectionViewTransitionLayout TransitionLayout (UICollectionView collectionView, UICollectionViewLayout fromLayout, UICollectionViewLayout toLayout);
	public override void WillDisplayCell (UICollectionView collectionView, UICollectionViewCell cell, Foundation.NSIndexPath indexPath);
	public override void WillDisplaySupplementaryView (UICollectionView collectionView, UICollectionReusableView view, string elementKind, Foundation.NSIndexPath indexPath);
```

### Type Changed: UIKit.UICollectionViewFlowLayout

Modified constructors:

```
public protected UICollectionViewFlowLayout (Foundation.NSObjectFlag t)
	public protected UICollectionViewFlowLayout (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewFlowLayoutInvalidationContext

Modified constructors:

```
public protected UICollectionViewFlowLayoutInvalidationContext (Foundation.NSObjectFlag t)
	public protected UICollectionViewFlowLayoutInvalidationContext (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewLayout

Modified constructors:

```
public protected UICollectionViewLayout (Foundation.NSObjectFlag t)
	public protected UICollectionViewLayout (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewLayoutAttributes

Modified constructors:

```
public protected UICollectionViewLayoutAttributes (Foundation.NSObjectFlag t)
	public protected UICollectionViewLayoutAttributes (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewLayoutInvalidationContext

Modified constructors:

```
public protected UICollectionViewLayoutInvalidationContext (Foundation.NSObjectFlag t)
	public protected UICollectionViewLayoutInvalidationContext (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewSource

Modified constructors:

```
public protected UICollectionViewSource (Foundation.NSObjectFlag t)
	public protected UICollectionViewSource (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewTransitionLayout

Modified constructors:

```
public protected UICollectionViewTransitionLayout (Foundation.NSObjectFlag t)
	public protected UICollectionViewTransitionLayout (IntPtr handle)
```

### Type Changed: UIKit.UICollectionViewUpdateItem

Modified constructors:

```
public protected UICollectionViewUpdateItem (Foundation.NSObjectFlag t)
	public protected UICollectionViewUpdateItem (IntPtr handle)
```

### Type Changed: UIKit.UICollisionBehavior

Modified constructors:

```
public protected UICollisionBehavior (Foundation.NSObjectFlag t)
	public protected UICollisionBehavior (IntPtr handle)
```

Modified properties:

```
public UICollisionBehaviorDelegate IUICollisionBehaviorDelegate CollisionDelegate { get; set; }
```

### Type Changed: UIKit.UICollisionBehaviorDelegate

Modified constructors:

```
public protected UICollisionBehaviorDelegate (Foundation.NSObjectFlag t)
	public protected UICollisionBehaviorDelegate (IntPtr handle)
```

### Type Changed: UIKit.UICollisionBehaviorMode

Modified fields:

```
Everything = 4294967295 18446744073709551615
```

### Type Changed: UIKit.UIColor

Modified constructors:

```
public protected UIColor (Foundation.NSObjectFlag t)
	public protected UIColor (IntPtr handle)
```

### Type Changed: UIKit.UIContentContainer

Modified constructors:

```
public protected UIContentContainer ()
	public protected UIContentContainer (Foundation.NSObjectFlag t)
	public protected UIContentContainer (IntPtr handle)
```

### Type Changed: UIKit.UIControl

Modified constructors:

```
public protected UIControl (Foundation.NSObjectFlag t)
	public protected UIControl (IntPtr handle)
```

### Type Changed: UIKit.UICoordinateSpace

Modified constructors:

```
public protected UICoordinateSpace ()
	public protected UICoordinateSpace (Foundation.NSObjectFlag t)
	public protected UICoordinateSpace (IntPtr handle)
```

### Type Changed: UIKit.UIDataDetectorType

Modified fields:

```
All = 4294967295 18446744073709551615
```

### Type Changed: UIKit.UIDatePicker

Modified constructors:

```
public protected UIDatePicker (Foundation.NSObjectFlag t)
	public protected UIDatePicker (IntPtr handle)
```

### Type Changed: UIKit.UIDevice

Modified constructors:

```
public protected UIDevice (Foundation.NSObjectFlag t)
	public protected UIDevice (IntPtr handle)
```

Removed property:

```
[Obsolete ("Deprecated in iOS 5.0. Apple now reject application using it the selector is removed and an empty string is returned")]
	public virtual string UniqueIdentifier { get; }
```

### Type Changed: UIKit.UIDictationPhrase

Modified constructors:

```
public protected UIDictationPhrase (Foundation.NSObjectFlag t)
	public protected UIDictationPhrase (IntPtr handle)
```

### Type Changed: UIKit.UIDocument

Modified constructors:

```
public protected UIDocument (Foundation.NSObjectFlag t)
	public protected UIDocument (IntPtr handle)
```

Removed methods:

```
public virtual void PerformAsynchronousFileAccess (Foundation.NSAction action);
	public virtual void RelinquishPresentedItemToReader (NSFilePresenterReacquirer readerAction);
	public virtual void RelinquishPresentedItemToWriter (NSFilePresenterReacquirer writerAction);
```

Added methods:

```
public virtual void PerformAsynchronousFileAccess (System.Action action);
	public virtual void RelinquishPresentedItemToReader (Foundation.NSFilePresenterReacquirer readerAction);
	public virtual void RelinquishPresentedItemToWriter (Foundation.NSFilePresenterReacquirer writerAction);
```

### Type Changed: UIKit.UIDocumentInteractionController

Modified constructors:

```
public protected UIDocumentInteractionController (Foundation.NSObjectFlag t)
	public protected UIDocumentInteractionController (IntPtr handle)
```

Modified properties:

```
public UIDocumentInteractionControllerDelegate IUIDocumentInteractionControllerDelegate Delegate { get; set; }
```

Removed method:

```
[Obsolete ("Use DismissPreview (typo) method instead")]
	public virtual void DimissPreview (bool animated);
```

### Type Changed: UIKit.UIDocumentInteractionControllerDelegate

Modified constructors:

```
public protected UIDocumentInteractionControllerDelegate (Foundation.NSObjectFlag t)
	public protected UIDocumentInteractionControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIDocumentMenuDelegate

Modified constructors:

```
public protected UIDocumentMenuDelegate ()
	public protected UIDocumentMenuDelegate (Foundation.NSObjectFlag t)
	public protected UIDocumentMenuDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIDocumentMenuViewController

Modified constructors:

```
public protected UIDocumentMenuViewController (Foundation.NSObjectFlag t)
	public protected UIDocumentMenuViewController (IntPtr handle)
```

Modified properties:

```
public UIDocumentMenuDelegate IUIDocumentMenuDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIDocumentPickerDelegate

Modified constructors:

```
public protected UIDocumentPickerDelegate ()
	public protected UIDocumentPickerDelegate (Foundation.NSObjectFlag t)
	public protected UIDocumentPickerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIDocumentPickerExtensionViewController

Modified constructors:

```
public protected UIDocumentPickerExtensionViewController (Foundation.NSObjectFlag t)
	public protected UIDocumentPickerExtensionViewController (IntPtr handle)
```

### Type Changed: UIKit.UIDocumentPickerViewController

Modified constructors:

```
public protected UIDocumentPickerViewController (Foundation.NSObjectFlag t)
	public protected UIDocumentPickerViewController (IntPtr handle)
```

Modified properties:

```
public UIDocumentPickerDelegate IUIDocumentPickerDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIDynamicAnimator

Modified constructors:

```
public protected UIDynamicAnimator (Foundation.NSObjectFlag t)
	public protected UIDynamicAnimator (IntPtr handle)
```

Modified properties:

```
public UIDynamicAnimatorDelegate IUIDynamicAnimatorDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIDynamicAnimatorDelegate

Modified constructors:

```
public protected UIDynamicAnimatorDelegate ()
	public protected UIDynamicAnimatorDelegate (Foundation.NSObjectFlag t)
	public protected UIDynamicAnimatorDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIDynamicBehavior

Modified constructors:

```
public protected UIDynamicBehavior (Foundation.NSObjectFlag t)
	public protected UIDynamicBehavior (IntPtr handle)
```

Modified properties:

```
public virtual Foundation.NSAction System.Action Action { get; set; }
```

### Type Changed: UIKit.UIDynamicItem

Modified constructors:

```
public protected UIDynamicItem ()
	public protected UIDynamicItem (Foundation.NSObjectFlag t)
	public protected UIDynamicItem (IntPtr handle)
```

### Type Changed: UIKit.UIDynamicItemBehavior

Modified constructors:

```
public protected UIDynamicItemBehavior (Foundation.NSObjectFlag t)
	public protected UIDynamicItemBehavior (IntPtr handle)
```

### Type Changed: UIKit.UIEvent

Modified constructors:

```
public protected UIEvent (Foundation.NSObjectFlag t)
	public protected UIEvent (IntPtr handle)
```

### Type Changed: UIKit.UIFont

Removed constructors:

```
[Obsolete ("This constructor does not return a valid, default, instance")]
	public UIFont ();
```

Modified constructors:

```
public protected UIFont (Foundation.NSObjectFlag t)
	public protected UIFont (IntPtr handle)
```

### Type Changed: UIKit.UIFontAttributes

Removed property:

```
public Foundation.NSDictionary Variation { get; set; }
```

### Type Changed: UIKit.UIFontDescriptor

Modified constructors:

```
public protected UIFontDescriptor (Foundation.NSObjectFlag t)
	public protected UIFontDescriptor (IntPtr handle)
```

Removed property:

```
public Foundation.NSDictionary Variation { get; }
```

### Type Changed: UIKit.UIGestureRecognizer

Removed constructors:

```
public UIGestureRecognizer (Foundation.NSAction action);
```

Modified constructors:

```
public protected UIGestureRecognizer (Foundation.NSObjectFlag t)
	public protected UIGestureRecognizer (IntPtr handle)
```

Added constructor:

```
public UIGestureRecognizer (System.Action action);
```

Removed field:

```
[Obsolete ("Don't use, this field has been removed the Unified API. Use 'Selector.GetHandle ()' instead.")]
	public static ObjCRuntime.Selector ParametrizedSelector;
```

Modified properties:

```
public UIGestureRecognizerDelegate IUIGestureRecognizerDelegate Delegate { get; set; }
```

Removed method:

```
public UIGestureRecognizer.Token AddTarget (Foundation.NSAction action);
```

Added method:

```
public UIGestureRecognizer.Token AddTarget (System.Action action);
```

### Type Changed: UIKit.UIGestureRecognizerDelegate

Modified constructors:

```
public protected UIGestureRecognizerDelegate (Foundation.NSObjectFlag t)
	public protected UIGestureRecognizerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIGravityBehavior

Modified constructors:

```
public protected UIGravityBehavior (Foundation.NSObjectFlag t)
	public protected UIGravityBehavior (IntPtr handle)
```

### Type Changed: UIKit.UIImage

Modified constructors:

```
public protected UIImage (IntPtr handle)
	public protected UIImage (Foundation.NSObjectFlag t)
```

Removed methods:

```
[Obsolete ("This always returns null. Use the overload that accept a System.String 'name' instead.")]
	public static UIImage CreateAnimatedImage (UIImage[] images, UIEdgeInsets capInsets, double duration);

	[Obsolete ("This is identical to FromFile. Caching is done when using FromBundle")]
	public static UIImage FromFileUncached (string filename);
```

### Type Changed: UIKit.UIImageAsset

Modified constructors:

```
public protected UIImageAsset (Foundation.NSObjectFlag t)
	public protected UIImageAsset (IntPtr handle)
```

### Type Changed: UIKit.UIImagePickerController

Modified constructors:

```
public protected UIImagePickerController (Foundation.NSObjectFlag t)
	public protected UIImagePickerController (IntPtr handle)
```

Removed fields:

```
public static Foundation.NSString CropRect;
	public static Foundation.NSString EditedImage;
	public static Foundation.NSString MediaType;
	public static Foundation.NSString MediaURL;
	public static Foundation.NSString OriginalImage;
```

Removed properties:

```
public System.Func<UINavigationController,UIKit.UINavigationControllerOperation,UIKit.UIViewController,UIKit.UIViewController,UIKit.IUIViewControllerAnimatedTransitioning> GetAnimationControllerForOperation { get; set; }
	public System.Func<UINavigationController,UIKit.IUIViewControllerAnimatedTransitioning,UIKit.IUIViewControllerInteractiveTransitioning> GetInteractionControllerForAnimationController { get; set; }
	public System.Func<UINavigationController,UIKit.UIInterfaceOrientation> GetPreferredInterfaceOrientation { get; set; }
	public System.Func<UINavigationController,UIKit.UIInterfaceOrientationMask> SupportedInterfaceOrientations { get; set; }
```

Added properties:

```
public static Foundation.NSString CropRect { get; }
	public static Foundation.NSString EditedImage { get; }
	public static Foundation.NSString MediaType { get; }
	public static Foundation.NSString MediaURL { get; }
	public static Foundation.NSString OriginalImage { get; }
```

Removed events:

```
public event System.EventHandler<UINavigationControllerEventArgs> DidShowViewController;
	public event System.EventHandler<UINavigationControllerEventArgs> WillShowViewController;
```

### Type Changed: UIKit.UIImagePickerControllerDelegate

Modified constructors:

```
public protected UIImagePickerControllerDelegate (Foundation.NSObjectFlag t)
	public protected UIImagePickerControllerDelegate (IntPtr handle)
```

Removed methods:

```
public override void DidShowViewController (UINavigationController navigationController, UIViewController viewController, bool animated);
	public override IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
	public override IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, IUIViewControllerAnimatedTransitioning animationController);
	public override UIInterfaceOrientation GetPreferredInterfaceOrientation (UINavigationController navigationController);
	public override UIInterfaceOrientationMask SupportedInterfaceOrientations (UINavigationController navigationController);
	public override void WillShowViewController (UINavigationController navigationController, UIViewController viewController, bool animated);
```

### Type Changed: UIKit.UIImageView

Modified constructors:

```
public protected UIImageView (Foundation.NSObjectFlag t)
	public protected UIImageView (IntPtr handle)
```

### Type Changed: UIKit.UIInputView

Modified constructors:

```
public protected UIInputView (Foundation.NSObjectFlag t)
	public protected UIInputView (IntPtr handle)
```

### Type Changed: UIKit.UIInputViewController

Modified constructors:

```
public protected UIInputViewController (Foundation.NSObjectFlag t)
	public protected UIInputViewController (IntPtr handle)
```

Removed methods:

```
public virtual void SelectionDidChange (Foundation.NSObject uiTextInput);
	public virtual void SelectionWillChange (Foundation.NSObject uiTextInput);
	public virtual void TextDidChange (Foundation.NSObject textInput);
	public virtual void TextWillChange (Foundation.NSObject textInput);
```

Added methods:

```
public virtual void SelectionDidChange (IUITextInput uiTextInput);
	public virtual void SelectionWillChange (IUITextInput uiTextInput);
	public virtual void TextDidChange (IUITextInput textInput);
	public virtual void TextWillChange (IUITextInput textInput);
```

### Type Changed: UIKit.UIInterpolatingMotionEffect

Modified constructors:

```
public protected UIInterpolatingMotionEffect (Foundation.NSObjectFlag t)
	public protected UIInterpolatingMotionEffect (IntPtr handle)
```

### Type Changed: UIKit.UIKeyCommand

Modified constructors:

```
public protected UIKeyCommand (Foundation.NSObjectFlag t)
	public protected UIKeyCommand (IntPtr handle)
```

### Type Changed: UIKit.UILabel

Modified constructors:

```
public protected UILabel (Foundation.NSObjectFlag t)
	public protected UILabel (IntPtr handle)
```

### Type Changed: UIKit.UILayoutSupport

Modified constructors:

```
public protected UILayoutSupport ()
	public protected UILayoutSupport (Foundation.NSObjectFlag t)
	public protected UILayoutSupport (IntPtr handle)
```

### Type Changed: UIKit.UILexicon

Modified constructors:

```
public protected UILexicon (Foundation.NSObjectFlag t)
	public protected UILexicon (IntPtr handle)
```

### Type Changed: UIKit.UILexiconEntry

Modified constructors:

```
public protected UILexiconEntry (Foundation.NSObjectFlag t)
	public protected UILexiconEntry (IntPtr handle)
```

### Type Changed: UIKit.UILocalizedIndexedCollation

Modified constructors:

```
public protected UILocalizedIndexedCollation (Foundation.NSObjectFlag t)
	public protected UILocalizedIndexedCollation (IntPtr handle)
```

### Type Changed: UIKit.UILocalNotification

Modified constructors:

```
public protected UILocalNotification (Foundation.NSObjectFlag t)
	public protected UILocalNotification (IntPtr handle)
```

### Type Changed: UIKit.UILongPressGestureRecognizer

Removed constructors:

```
public UILongPressGestureRecognizer (Foundation.NSAction action);
```

Modified constructors:

```
public protected UILongPressGestureRecognizer (Foundation.NSObjectFlag t)
	public protected UILongPressGestureRecognizer (IntPtr handle)
```

Added constructor:

```
public UILongPressGestureRecognizer (System.Action action);
```

### Type Changed: UIKit.UIManagedDocument

Modified constructors:

```
public protected UIManagedDocument (Foundation.NSObjectFlag t)
	public protected UIManagedDocument (IntPtr handle)
```

### Type Changed: UIKit.UIMarkupTextPrintFormatter

Modified constructors:

```
public protected UIMarkupTextPrintFormatter (Foundation.NSObjectFlag t)
	public protected UIMarkupTextPrintFormatter (IntPtr handle)
```

### Type Changed: UIKit.UIMenuController

Modified constructors:

```
public protected UIMenuController (Foundation.NSObjectFlag t)
	public protected UIMenuController (IntPtr handle)
```

### Type Changed: UIKit.UIMenuItem

Modified constructors:

```
public protected UIMenuItem (Foundation.NSObjectFlag t)
	public protected UIMenuItem (IntPtr handle)
```

### Type Changed: UIKit.UIMotionEffect

Modified constructors:

```
public protected UIMotionEffect (Foundation.NSObjectFlag t)
	public protected UIMotionEffect (IntPtr handle)
```

### Type Changed: UIKit.UIMotionEffectGroup

Modified constructors:

```
public protected UIMotionEffectGroup (Foundation.NSObjectFlag t)
	public protected UIMotionEffectGroup (IntPtr handle)
```

### Type Changed: UIKit.UIMutableUserNotificationAction

Modified constructors:

```
public protected UIMutableUserNotificationAction (Foundation.NSObjectFlag t)
	public protected UIMutableUserNotificationAction (IntPtr handle)
```

### Type Changed: UIKit.UIMutableUserNotificationCategory

Modified constructors:

```
public protected UIMutableUserNotificationCategory (Foundation.NSObjectFlag t)
	public protected UIMutableUserNotificationCategory (IntPtr handle)
```

### Type Changed: UIKit.UINavigationBar

Modified constructors:

```
public protected UINavigationBar (Foundation.NSObjectFlag t)
	public protected UINavigationBar (IntPtr handle)
```

Modified properties:

```
public UINavigationBarDelegate IUINavigationBarDelegate Delegate { get; set; }
```

Removed methods:

```
[Obsolete ("Use TitleTextAttributes property with UIStringAttributes")]
	public UITextAttributes GetTitleTextAttributes ();
	public virtual UINavigationItem PopNavigationItemAnimated (bool animated);

	[Obsolete ("Use TitleTextAttributes with UIStringAttributes")]
	public void SetTitleTextAttributes (UITextAttributes attributes);
```

Added method:

```
public virtual UINavigationItem PopNavigationItem (bool animated);
```

### Type Changed: UIKit.UINavigationBarDelegate

Modified constructors:

```
public protected UINavigationBarDelegate (Foundation.NSObjectFlag t)
	public protected UINavigationBarDelegate (IntPtr handle)
```

Removed method:

```
public override UIBarPosition GetPositionForBar (IUIBarPositioning barPositioning);
```

### Type Changed: UIKit.UINavigationController

Modified constructors:

```
public protected UINavigationController (Foundation.NSObjectFlag t)
	public protected UINavigationController (IntPtr handle)
```

Modified properties:

```
public UINavigationControllerDelegate IUINavigationControllerDelegate Delegate { get; set; }
```

Removed method:

```
public virtual UIViewController PopViewControllerAnimated (bool animated);
```

Added method:

```
public virtual UIViewController PopViewController (bool animated);
```

### Type Changed: UIKit.UINavigationControllerDelegate

Modified constructors:

```
public protected UINavigationControllerDelegate (Foundation.NSObjectFlag t)
	public protected UINavigationControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UINavigationItem

Modified constructors:

```
public protected UINavigationItem (Foundation.NSObjectFlag t)
	public protected UINavigationItem (IntPtr handle)
```

### Type Changed: UIKit.UINib

Modified constructors:

```
public protected UINib (Foundation.NSObjectFlag t)
	public protected UINib (IntPtr handle)
```

Removed method:

```
[Obsolete ("Use Instantiate method")]
	public Foundation.NSObject[] InstantiateWithOwneroptions (Foundation.NSObject ownerOrNil, Foundation.NSDictionary optionsOrNil);
```

### Type Changed: UIKit.UIObjectRestoration

Modified constructors:

```
public protected UIObjectRestoration (Foundation.NSObjectFlag t)
	public protected UIObjectRestoration (IntPtr handle)
```

### Type Changed: UIKit.UIPageControl

Modified constructors:

```
public protected UIPageControl (Foundation.NSObjectFlag t)
	public protected UIPageControl (IntPtr handle)
```

### Type Changed: UIKit.UIPageViewController

Modified constructors:

```
public protected UIPageViewController (IntPtr handle)
	public protected UIPageViewController (Foundation.NSObjectFlag t)
```

Modified properties:

```
public UIPageViewControllerDataSource IUIPageViewControllerDataSource DataSource { get; set; }
	public UIPageViewControllerDelegate IUIPageViewControllerDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIPageViewControllerDataSource

Modified constructors:

```
public protected UIPageViewControllerDataSource ()
	public protected UIPageViewControllerDataSource (Foundation.NSObjectFlag t)
	public protected UIPageViewControllerDataSource (IntPtr handle)
```

### Type Changed: UIKit.UIPageViewControllerDelegate

Modified constructors:

```
public protected UIPageViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected UIPageViewControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIPanGestureRecognizer

Removed constructors:

```
public UIPanGestureRecognizer (Foundation.NSAction action);
```

Modified constructors:

```
public protected UIPanGestureRecognizer (Foundation.NSObjectFlag t)
	public protected UIPanGestureRecognizer (IntPtr handle)
```

Added constructor:

```
public UIPanGestureRecognizer (System.Action action);
```

### Type Changed: UIKit.UIPasteboard

Modified constructors:

```
public protected UIPasteboard (Foundation.NSObjectFlag t)
	public protected UIPasteboard (IntPtr handle)
```

### Type Changed: UIKit.UIPercentDrivenInteractiveTransition

Modified constructors:

```
public protected UIPercentDrivenInteractiveTransition (Foundation.NSObjectFlag t)
	public protected UIPercentDrivenInteractiveTransition (IntPtr handle)
```

### Type Changed: UIKit.UIPickerView

Modified constructors:

```
public protected UIPickerView (Foundation.NSObjectFlag t)
	public protected UIPickerView (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use Model instead")]
	public UIPickerViewModel Source { get; set; }
```

Modified properties:

```
public UIPickerViewDelegate IUIPickerViewDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIPickerViewAccessibilityDelegate

Modified constructors:

```
public protected UIPickerViewAccessibilityDelegate (Foundation.NSObjectFlag t)
	public protected UIPickerViewAccessibilityDelegate (IntPtr handle)
```

Removed methods:

```
public override Foundation.NSAttributedString GetAttributedTitle (UIPickerView pickerView, int row, int component);
	public override float GetComponentWidth (UIPickerView pickerView, int component);
	public override float GetRowHeight (UIPickerView pickerView, int component);
	public override string GetTitle (UIPickerView pickerView, int row, int component);
	public override UIView GetView (UIPickerView pickerView, int row, int component, UIView view);
	public override void Selected (UIPickerView pickerView, int row, int component);
```

### Type Changed: UIKit.UIPickerViewDataSource

Modified constructors:

```
public protected UIPickerViewDataSource ()
	public protected UIPickerViewDataSource (Foundation.NSObjectFlag t)
	public protected UIPickerViewDataSource (IntPtr handle)
```

### Type Changed: UIKit.UIPickerViewDelegate

Modified constructors:

```
public protected UIPickerViewDelegate (Foundation.NSObjectFlag t)
	public protected UIPickerViewDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIPickerViewModel

Modified constructors:

```
public protected UIPickerViewModel (Foundation.NSObjectFlag t)
	public protected UIPickerViewModel (IntPtr handle)
```

### Type Changed: UIKit.UIPinchGestureRecognizer

Removed constructors:

```
public UIPinchGestureRecognizer (Foundation.NSAction action);
```

Modified constructors:

```
public protected UIPinchGestureRecognizer (Foundation.NSObjectFlag t)
	public protected UIPinchGestureRecognizer (IntPtr handle)
```

Added constructor:

```
public UIPinchGestureRecognizer (System.Action action);
```

### Type Changed: UIKit.UIPopoverArrowDirection

Modified fields:

```
Unknown = 4294967295 18446744073709551615
```

### Type Changed: UIKit.UIPopoverBackgroundView

Modified constructors:

```
public protected UIPopoverBackgroundView (Foundation.NSObjectFlag t)
	public protected UIPopoverBackgroundView (IntPtr handle)
```

### Type Changed: UIKit.UIPopoverController

Modified constructors:

```
public protected UIPopoverController (Foundation.NSObjectFlag t)
	public protected UIPopoverController (IntPtr handle)
```

Modified properties:

```
public UIPopoverControllerDelegate IUIPopoverControllerDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIPopoverControllerDelegate

Modified constructors:

```
public protected UIPopoverControllerDelegate (Foundation.NSObjectFlag t)
	public protected UIPopoverControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIPopoverPresentationController

Modified constructors:

```
public protected UIPopoverPresentationController (Foundation.NSObjectFlag t)
	public protected UIPopoverPresentationController (IntPtr handle)
```

Removed property:

```
[Obsolete ("Use the Delegate property")]
	public UIPopoverPresentationControllerDelegate Delegat { get; set; }
```

Modified properties:

```
public UIPopoverPresentationControllerDelegate IUIPopoverPresentationControllerDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIPopoverPresentationControllerDelegate

Modified constructors:

```
public protected UIPopoverPresentationControllerDelegate (Foundation.NSObjectFlag t)
	public protected UIPopoverPresentationControllerDelegate (IntPtr handle)
```

Removed methods:

```
public override UIModalPresentationStyle GetAdaptivePresentationStyle (UIPresentationController forPresentationController);
	public override UIViewController GetViewControllerForAdaptivePresentation (UIPresentationController controller, UIModalPresentationStyle style);
```

### Type Changed: UIKit.UIPresentationController

Modified constructors:

```
public protected UIPresentationController (Foundation.NSObjectFlag t)
	public protected UIPresentationController (IntPtr handle)
```

Modified properties:

```
public UIAdaptivePresentationControllerDelegate IUIAdaptivePresentationControllerDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIPrinter

Modified constructors:

```
public protected UIPrinter (Foundation.NSObjectFlag t)
	public protected UIPrinter (IntPtr handle)
```

### Type Changed: UIKit.UIPrinterPickerController

Modified constructors:

```
public protected UIPrinterPickerController (Foundation.NSObjectFlag t)
	public protected UIPrinterPickerController (IntPtr handle)
```

Modified properties:

```
public UIPrinterPickerControllerDelegate IUIPrinterPickerControllerDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIPrinterPickerControllerDelegate

Modified constructors:

```
public protected UIPrinterPickerControllerDelegate (Foundation.NSObjectFlag t)
	public protected UIPrinterPickerControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIPrintFormatter

Removed constructors:

```
[Obsolete ("This cannot be directly created. Use UISimpleTextPrintFormatter instead.")]
	public UIPrintFormatter (string text);

	[Obsolete ("This cannot be directly created. Use UISimpleTextPrintFormatter instead.")]
	public UIPrintFormatter (Foundation.NSAttributedString attributedText);
```

Modified constructors:

```
public protected UIPrintFormatter (Foundation.NSObjectFlag t)
	public protected UIPrintFormatter (IntPtr handle)
```

Removed property:

```
[Obsolete ("This cannot be used directly. Use UISimpleTextPrintFormatter instead.")]
	public virtual Foundation.NSAttributedString AttributedText { get; set; }
```

### Type Changed: UIKit.UIPrintInfo

Modified constructors:

```
public protected UIPrintInfo (Foundation.NSObjectFlag t)
	public protected UIPrintInfo (IntPtr handle)
```

### Type Changed: UIKit.UIPrintInteractionController

Modified constructors:

```
public protected UIPrintInteractionController (Foundation.NSObjectFlag t)
	public protected UIPrintInteractionController (IntPtr handle)
```

Modified properties:

```
public UIPrintInteractionControllerDelegate IUIPrintInteractionControllerDelegate Delegate { get; set; }
```

Removed methods:

```
public virtual void Present (bool animated, UIPrintInteractionCompletionHandler completion);
	public virtual void PresentFromBarButtonItem (UIBarButtonItem item, bool animated, UIPrintInteractionCompletionHandler completion);
	public virtual void PresentFromRectInView (System.Drawing.RectangleF rect, UIView view, bool animated, UIPrintInteractionCompletionHandler completion);
```

Added methods:

```
public virtual bool Present (bool animated, UIPrintInteractionCompletionHandler completion);
	public virtual System.Threading.Tasks.Task<UIPrintInteractionResult> PresentAsync (bool animated, out bool result);
	public virtual bool PresentFromBarButtonItem (UIBarButtonItem item, bool animated, UIPrintInteractionCompletionHandler completion);
	public virtual System.Threading.Tasks.Task<UIPrintInteractionResult> PresentFromBarButtonItemAsync (UIBarButtonItem item, bool animated, out bool result);
	public virtual bool PresentFromRectInView (System.Drawing.RectangleF rect, UIView view, bool animated, UIPrintInteractionCompletionHandler completion);
	public virtual System.Threading.Tasks.Task<UIPrintInteractionResult> PresentFromRectInViewAsync (System.Drawing.RectangleF rect, UIView view, bool animated, out bool result);
```

### Type Changed: UIKit.UIPrintInteractionControllerDelegate

Modified constructors:

```
public protected UIPrintInteractionControllerDelegate (Foundation.NSObjectFlag t)
	public protected UIPrintInteractionControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIPrintPageRenderer

Modified constructors:

```
public protected UIPrintPageRenderer (Foundation.NSObjectFlag t)
	public protected UIPrintPageRenderer (IntPtr handle)
```

### Type Changed: UIKit.UIPrintPaper

Modified constructors:

```
public protected UIPrintPaper (Foundation.NSObjectFlag t)
	public protected UIPrintPaper (IntPtr handle)
```

### Type Changed: UIKit.UIProgressView

Modified constructors:

```
public protected UIProgressView (Foundation.NSObjectFlag t)
	public protected UIProgressView (IntPtr handle)
```

### Type Changed: UIKit.UIPushBehavior

Modified constructors:

```
public protected UIPushBehavior (Foundation.NSObjectFlag t)
	public protected UIPushBehavior (IntPtr handle)
```

### Type Changed: UIKit.UIReferenceLibraryViewController

Modified constructors:

```
public protected UIReferenceLibraryViewController (Foundation.NSObjectFlag t)
	public protected UIReferenceLibraryViewController (IntPtr handle)
```

### Type Changed: UIKit.UIRefreshControl

Modified constructors:

```
public protected UIRefreshControl (Foundation.NSObjectFlag t)
	public protected UIRefreshControl (IntPtr handle)
```

### Type Changed: UIKit.UIResponder

Modified constructors:

```
public protected UIResponder (Foundation.NSObjectFlag t)
	public protected UIResponder (IntPtr handle)
```

Removed methods:

```
[Obsolete ("Override Copy(NSObject)")]
	public virtual void Copy ();

	[Obsolete ("Override Cut(NSObject)")]
	public virtual void Cut ();

	[Obsolete ("Override Delete(NSObject)")]
	public virtual void Delete ();

	[Obsolete ("Override Paste(NSObject)")]
	public virtual void Paste ();

	[Obsolete ("Override Select(NSObject)")]
	public virtual void Select ();

	[Obsolete ("Override SelectAll(NSObject)")]
	public virtual void SelectAll ();
```

### Type Changed: UIKit.UIRotationGestureRecognizer

Removed constructors:

```
public UIRotationGestureRecognizer (Foundation.NSAction action);
```

Modified constructors:

```
public protected UIRotationGestureRecognizer (Foundation.NSObjectFlag t)
	public protected UIRotationGestureRecognizer (IntPtr handle)
```

Added constructor:

```
public UIRotationGestureRecognizer (System.Action action);
```

### Type Changed: UIKit.UIScreen

Modified constructors:

```
public protected UIScreen (Foundation.NSObjectFlag t)
	public protected UIScreen (IntPtr handle)
```

Removed method:

```
public CoreAnimation.CADisplayLink CreateDisplayLink (Foundation.NSAction action);
```

Added method:

```
public CoreAnimation.CADisplayLink CreateDisplayLink (System.Action action);
```

### Type Changed: UIKit.UIScreenEdgePanGestureRecognizer

Removed constructors:

```
public UIScreenEdgePanGestureRecognizer (Foundation.NSAction action);
```

Modified constructors:

```
public protected UIScreenEdgePanGestureRecognizer (Foundation.NSObjectFlag t)
	public protected UIScreenEdgePanGestureRecognizer (IntPtr handle)
```

Added constructor:

```
public UIScreenEdgePanGestureRecognizer (System.Action action);
```

### Type Changed: UIKit.UIScreenMode

Modified constructors:

```
public protected UIScreenMode (Foundation.NSObjectFlag t)
	public protected UIScreenMode (IntPtr handle)
```

### Type Changed: UIKit.UIScrollView

Modified constructors:

```
public protected UIScrollView (Foundation.NSObjectFlag t)
	public protected UIScrollView (IntPtr handle)
```

Modified properties:

```
public UIScrollViewDelegate IUIScrollViewDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIScrollViewAccessibilityDelegate

Modified constructors:

```
public protected UIScrollViewAccessibilityDelegate (Foundation.NSObjectFlag t)
	public protected UIScrollViewAccessibilityDelegate (IntPtr handle)
```

Removed methods:

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
	public override void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
	public override void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
	public override void ZoomingStarted (UIScrollView scrollView, UIView view);
```

### Type Changed: UIKit.UIScrollViewDelegate

Modified constructors:

```
public protected UIScrollViewDelegate (Foundation.NSObjectFlag t)
	public protected UIScrollViewDelegate (IntPtr handle)
```

### Type Changed: UIKit.UISearchBar

Modified constructors:

```
public protected UISearchBar (Foundation.NSObjectFlag t)
	public protected UISearchBar (IntPtr handle)
```

Removed property:

```
public System.Func<IUIBarPositioning,UIKit.UIBarPosition> GetPositionForBar { get; set; }
```

Modified properties:

```
public UISearchBarDelegate IUISearchBarDelegate Delegate { get; set; }
```

Removed methods:

```
public virtual UIImage BackgroundImageForBarMetrics (UIBarMetrics barMetrics);
	public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarMetrics barMetrics);
```

### Type Changed: UIKit.UISearchBar.UISearchBarAppearance

Removed methods:

```
public virtual UIImage BackgroundImageForBarMetrics (UIBarMetrics barMetrics);
	public virtual void SetBackgroundImage (UIImage backgroundImage, UIBarMetrics barMetrics);
```

### Type Changed: UIKit.UISearchBarDelegate

Modified constructors:

```
public protected UISearchBarDelegate (Foundation.NSObjectFlag t)
	public protected UISearchBarDelegate (IntPtr handle)
```

Removed method:

```
public override UIBarPosition GetPositionForBar (IUIBarPositioning barPositioning);
```

### Type Changed: UIKit.UISearchController

Modified constructors:

```
public protected UISearchController (Foundation.NSObjectFlag t)
	public protected UISearchController (IntPtr handle)
```

Modified properties:

```
public UISearchControllerDelegate IUISearchControllerDelegate Delegate { get; set; }
	public UISearchResultsUpdating IUISearchResultsUpdating SearchResultsUpdater { get; set; }
```

Removed method:

```
public virtual IUIViewControllerAnimatedTransitioning PresentingController (UIViewController presented, UIViewController presenting, UIViewController source);
```

Added method:

```
public virtual IUIViewControllerAnimatedTransitioning GetAnimationControllerForPresentedController (UIViewController presented, UIViewController presenting, UIViewController source);
```

### Type Changed: UIKit.UISearchControllerDelegate

Modified constructors:

```
public protected UISearchControllerDelegate (Foundation.NSObjectFlag t)
	public protected UISearchControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UISearchDisplayController

Modified constructors:

```
public protected UISearchDisplayController (Foundation.NSObjectFlag t)
	public protected UISearchDisplayController (IntPtr handle)
```

Modified properties:

```
public UISearchDisplayDelegate IUISearchDisplayDelegate Delegate { get; set; }
	public UITableViewDataSource IUITableViewDataSource SearchResultsDataSource { get; set; }
	public UITableViewDelegate IUITableViewDelegate SearchResultsDelegate { get; set; }
```

### Type Changed: UIKit.UISearchDisplayDelegate

Modified constructors:

```
public protected UISearchDisplayDelegate (Foundation.NSObjectFlag t)
	public protected UISearchDisplayDelegate (IntPtr handle)
```

### Type Changed: UIKit.UISearchResultsUpdating

Modified constructors:

```
public protected UISearchResultsUpdating ()
	public protected UISearchResultsUpdating (Foundation.NSObjectFlag t)
	public protected UISearchResultsUpdating (IntPtr handle)
```

Modified methods:

```
public abstract void UpdateSearchResultsForSearchController (UISearchController searchController)
```

### Type Changed: UIKit.UISegmentedControl

Modified constructors:

```
public protected UISegmentedControl (Foundation.NSObjectFlag t)
	public protected UISegmentedControl (IntPtr handle)
```

### Type Changed: UIKit.UISimpleTextPrintFormatter

Modified constructors:

```
public protected UISimpleTextPrintFormatter (Foundation.NSObjectFlag t)
	public protected UISimpleTextPrintFormatter (IntPtr handle)
```

### Type Changed: UIKit.UISlider

Modified constructors:

```
public protected UISlider (Foundation.NSObjectFlag t)
	public protected UISlider (IntPtr handle)
```

### Type Changed: UIKit.UISnapBehavior

Modified constructors:

```
public protected UISnapBehavior (Foundation.NSObjectFlag t)
	public protected UISnapBehavior (IntPtr handle)
```

### Type Changed: UIKit.UISplitViewController

Modified constructors:

```
public protected UISplitViewController (Foundation.NSObjectFlag t)
	public protected UISplitViewController (IntPtr handle)
```

Modified properties:

```
public UISplitViewControllerDelegate IUISplitViewControllerDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UISplitViewControllerDelegate

Modified constructors:

```
public protected UISplitViewControllerDelegate (Foundation.NSObjectFlag t)
	public protected UISplitViewControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIStateRestoring

Modified constructors:

```
public protected UIStateRestoring (Foundation.NSObjectFlag t)
	public protected UIStateRestoring (IntPtr handle)
```

### Type Changed: UIKit.UIStepper

Modified constructors:

```
public protected UIStepper (Foundation.NSObjectFlag t)
	public protected UIStepper (IntPtr handle)
```

### Type Changed: UIKit.UIStoryboard

Modified constructors:

```
public protected UIStoryboard (Foundation.NSObjectFlag t)
	public protected UIStoryboard (IntPtr handle)
```

Removed methods:

```
public virtual Foundation.NSObject InstantiateInitialViewController ();
	public virtual Foundation.NSObject InstantiateViewController (string identifier);
```

Added methods:

```
public virtual UIViewController InstantiateInitialViewController ();
	public virtual UIViewController InstantiateViewController (string identifier);
```

### Type Changed: UIKit.UIStoryboardPopoverSegue

Modified constructors:

```
public protected UIStoryboardPopoverSegue (Foundation.NSObjectFlag t)
	public protected UIStoryboardPopoverSegue (IntPtr handle)
```

### Type Changed: UIKit.UIStoryboardSegue

Modified constructors:

```
public protected UIStoryboardSegue (Foundation.NSObjectFlag t)
	public protected UIStoryboardSegue (IntPtr handle)
```

Removed method:

```
public static UIStoryboardSegue Create (string identifier, UIViewController source, UIViewController destination, Foundation.NSAction performHandler);
```

Added method:

```
public static UIStoryboardSegue Create (string identifier, UIViewController source, UIViewController destination, System.Action performHandler);
```

### Type Changed: UIKit.UISwipeGestureRecognizer

Removed constructors:

```
public UISwipeGestureRecognizer (Foundation.NSAction action);
```

Modified constructors:

```
public protected UISwipeGestureRecognizer (Foundation.NSObjectFlag t)
	public protected UISwipeGestureRecognizer (IntPtr handle)
```

Added constructor:

```
public UISwipeGestureRecognizer (System.Action action);
```

### Type Changed: UIKit.UISwitch

Modified constructors:

```
public protected UISwitch (Foundation.NSObjectFlag t)
	public protected UISwitch (IntPtr handle)
```

### Type Changed: UIKit.UITabBar

Modified constructors:

```
public protected UITabBar (Foundation.NSObjectFlag t)
	public protected UITabBar (IntPtr handle)
```

Modified properties:

```
public UITabBarDelegate IUITabBarDelegate Delegate { get; set; }
```

Removed method:

```
public virtual bool EndCustomizingAnimated (bool animated);
```

Added method:

```
public virtual bool EndCustomizing (bool animated);
```

### Type Changed: UIKit.UITabBarController

Modified constructors:

```
public protected UITabBarController (Foundation.NSObjectFlag t)
	public protected UITabBarController (IntPtr handle)
```

Modified properties:

```
public UITabBarControllerDelegate IUITabBarControllerDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UITabBarControllerDelegate

Modified constructors:

```
public protected UITabBarControllerDelegate (Foundation.NSObjectFlag t)
	public protected UITabBarControllerDelegate (IntPtr handle)
```

### Type Changed: UIKit.UITabBarDelegate

Modified constructors:

```
public protected UITabBarDelegate (Foundation.NSObjectFlag t)
	public protected UITabBarDelegate (IntPtr handle)
```

### Type Changed: UIKit.UITabBarItem

Modified constructors:

```
public protected UITabBarItem (Foundation.NSObjectFlag t)
	public protected UITabBarItem (IntPtr handle)
```

### Type Changed: UIKit.UITableView

Modified constructors:

```
public protected UITableView (Foundation.NSObjectFlag t)
	public protected UITableView (IntPtr handle)
```

Modified properties:

```
public UITableViewDataSource IUITableViewDataSource DataSource { get; set; }
	public UITableViewDelegate IUITableViewDelegate Delegate { get; set; }
```

Removed method:

```
[Obsolete ("Use RegisterNibForCellReuse")]
	public void RegisterNibforCellReuse (UINib nib, string reuseIdentifier);
```

Modified methods:

```
public virtual void RegisterNibForCellReuse (UINib nib, string reuseIdentifier)
	public virtual void RegisterNibForCellReuse (UINib nib, Foundation.NSString reuseIdentifier)
	public virtual void RegisterNibForHeaderFooterViewReuse (UINib nib, string reuseIdentifier)
```

### Type Changed: UIKit.UITableViewCell

Modified constructors:

```
public protected UITableViewCell (Foundation.NSObjectFlag t)
	public protected UITableViewCell (IntPtr handle)
```

Modified properties:

```
public virtual string Foundation.NSString ReuseIdentifier { get; }
```

### Type Changed: UIKit.UITableViewController

Modified constructors:

```
public protected UITableViewController (Foundation.NSObjectFlag t)
	public protected UITableViewController (IntPtr handle)
```

### Type Changed: UIKit.UITableViewDataSource

Modified constructors:

```
public protected UITableViewDataSource ()
	public protected UITableViewDataSource (Foundation.NSObjectFlag t)
	public protected UITableViewDataSource (IntPtr handle)
```

### Type Changed: UIKit.UITableViewDelegate

Modified constructors:

```
public protected UITableViewDelegate (Foundation.NSObjectFlag t)
	public protected UITableViewDelegate (IntPtr handle)
```

Removed methods:

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
	public override void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
	public override void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
	public override void ZoomingStarted (UIScrollView scrollView, UIView view);
```

### Type Changed: UIKit.UITableViewHeaderFooterView

Modified constructors:

```
public protected UITableViewHeaderFooterView (Foundation.NSObjectFlag t)
	public protected UITableViewHeaderFooterView (IntPtr handle)
```

### Type Changed: UIKit.UITableViewRowAction

Modified constructors:

```
public protected UITableViewRowAction (Foundation.NSObjectFlag t)
	public protected UITableViewRowAction (IntPtr handle)
```

### Type Changed: UIKit.UITableViewSource

Modified constructors:

```
public protected UITableViewSource ()
	public protected UITableViewSource (Foundation.NSObjectFlag t)
	public protected UITableViewSource (IntPtr handle)
```

Removed methods:

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
	public override void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
	public override void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
	public override void ZoomingStarted (UIScrollView scrollView, UIView view);
```

### Type Changed: UIKit.UITapGestureRecognizer

Removed constructors:

```
public UITapGestureRecognizer (Foundation.NSAction action);
```

Modified constructors:

```
public protected UITapGestureRecognizer (Foundation.NSObjectFlag t)
	public protected UITapGestureRecognizer (IntPtr handle)
```

Added constructor:

```
public UITapGestureRecognizer (System.Action action);
```

### Type Changed: UIKit.UITextChecker

Modified constructors:

```
public protected UITextChecker (Foundation.NSObjectFlag t)
	public protected UITextChecker (IntPtr handle)
```

### Type Changed: UIKit.UITextDocumentProxy

Modified constructors:

```
public protected UITextDocumentProxy ()
	public protected UITextDocumentProxy (Foundation.NSObjectFlag t)
	public protected UITextDocumentProxy (IntPtr handle)
```

### Type Changed: UIKit.UITextField

Modified constructors:

```
public protected UITextField (Foundation.NSObjectFlag t)
	public protected UITextField (IntPtr handle)
```

Modified properties:

```
public UITextFieldDelegate IUITextFieldDelegate Delegate { get; set; }
	public UITextInputDelegate IUITextInputDelegate InputDelegate { get; set; }
	public UITextInputTokenizer IUITextInputTokenizer Tokenizer { get; }
```

### Type Changed: UIKit.UITextFieldDelegate

Modified constructors:

```
public protected UITextFieldDelegate (Foundation.NSObjectFlag t)
	public protected UITextFieldDelegate (IntPtr handle)
```

### Type Changed: UIKit.UITextInputDelegate

Modified constructors:

```
public protected UITextInputDelegate ()
	public protected UITextInputDelegate (Foundation.NSObjectFlag t)
	public protected UITextInputDelegate (IntPtr handle)
```

Removed methods:

```
public virtual void SelectionDidChange (Foundation.NSObject uiTextInput);
	public virtual void SelectionWillChange (Foundation.NSObject uiTextInput);
	public virtual void TextDidChange (Foundation.NSObject textInput);
	public virtual void TextWillChange (Foundation.NSObject textInput);
```

Added methods:

```
public virtual void SelectionDidChange (IUITextInput uiTextInput);
	public virtual void SelectionWillChange (IUITextInput uiTextInput);
	public virtual void TextDidChange (IUITextInput textInput);
	public virtual void TextWillChange (IUITextInput textInput);
```

### Type Changed: UIKit.UITextInputMode

Modified constructors:

```
public protected UITextInputMode (Foundation.NSObjectFlag t)
	public protected UITextInputMode (IntPtr handle)
```

### Type Changed: UIKit.UITextInputStringTokenizer

Removed constructors:

```
public UITextInputStringTokenizer (Foundation.NSObject textInput);
```

Modified constructors:

```
public protected UITextInputStringTokenizer (Foundation.NSObjectFlag t)
	public protected UITextInputStringTokenizer (IntPtr handle)
```

Added constructor:

```
public UITextInputStringTokenizer (IUITextInput textInput);
```

Modified methods:

```
public override virtual UITextPosition GetPosition (UITextPosition fromPosition, UITextGranularity toBoundary, UITextDirection inDirection)
	public override virtual UITextRange GetRangeEnclosingPosition (UITextPosition position, UITextGranularity granularity, UITextDirection direction)
	public override virtual bool ProbeDirection (UITextPosition probePosition, UITextGranularity atBoundary, UITextDirection inDirection)
	public override virtual bool ProbeDirectionWithinTextUnit (UITextPosition probePosition, UITextGranularity withinTextUnit, UITextDirection inDirection)
```

### Type Changed: UIKit.UITextInputTokenizer

Modified constructors:

```
public protected UITextInputTokenizer ()
	public protected UITextInputTokenizer (Foundation.NSObjectFlag t)
	public protected UITextInputTokenizer (IntPtr handle)
```

### Type Changed: UIKit.UITextPosition

Modified constructors:

```
public protected UITextPosition (Foundation.NSObjectFlag t)
	public protected UITextPosition (IntPtr handle)
```

### Type Changed: UIKit.UITextRange

Modified constructors:

```
public protected UITextRange (Foundation.NSObjectFlag t)
	public protected UITextRange (IntPtr handle)
```

Removed properties:

```
[Obsolete ("Use End instead")]
	public virtual UITextPosition end { get; }

	[Obsolete ("Use Start instead")]
	public virtual UITextPosition start { get; }
```

Modified properties:

```
public virtual UITextPosition End { get; }
	public virtual UITextPosition Start { get; }
```

### Type Changed: UIKit.UITextSelectionRect

Modified constructors:

```
public protected UITextSelectionRect (Foundation.NSObjectFlag t)
	public protected UITextSelectionRect (IntPtr handle)
```

### Type Changed: UIKit.UITextView

Modified constructors:

```
public protected UITextView (Foundation.NSObjectFlag t)
	public protected UITextView (IntPtr handle)
```

Removed properties:

```
public UIScrollViewCondition ShouldScrollToTop { get; set; }
	public UIScrollViewGetZoomView ViewForZoomingInScrollView { get; set; }
```

Modified properties:

```
public UITextViewDelegate IUITextViewDelegate Delegate { get; set; }
	public UITextInputDelegate IUITextInputDelegate InputDelegate { get; set; }
	public UITextInputTokenizer IUITextInputTokenizer Tokenizer { get; }
```

Removed events:

```
public event System.EventHandler DecelerationEnded;
	public event System.EventHandler DecelerationStarted;
	public event System.EventHandler DidZoom;
	public event System.EventHandler<DraggingEventArgs> DraggingEnded;
	public event System.EventHandler DraggingStarted;
	public event System.EventHandler ScrollAnimationEnded;
	public event System.EventHandler Scrolled;
	public event System.EventHandler ScrolledToTop;
	public event System.EventHandler<WillEndDraggingEventArgs> WillEndDragging;
	public event System.EventHandler<ZoomingEndedEventArgs> ZoomingEnded;
	public event System.EventHandler<UIScrollViewZoomingEventArgs> ZoomingStarted;
```

### Type Changed: UIKit.UITextViewDelegate

Modified constructors:

```
public protected UITextViewDelegate (Foundation.NSObjectFlag t)
	public protected UITextViewDelegate (IntPtr handle)
```

Removed methods:

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
	public override void WillEndDragging (UIScrollView scrollView, System.Drawing.PointF velocity, ref System.Drawing.PointF targetContentOffset);
	public override void ZoomingEnded (UIScrollView scrollView, UIView withView, float atScale);
	public override void ZoomingStarted (UIScrollView scrollView, UIView view);
```

### Type Changed: UIKit.UIToolbar

Modified constructors:

```
public protected UIToolbar (Foundation.NSObjectFlag t)
	public protected UIToolbar (IntPtr handle)
```

Modified properties:

```
public UIToolbarDelegate IUIToolbarDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIToolbarDelegate

Modified constructors:

```
public protected UIToolbarDelegate (Foundation.NSObjectFlag t)
	public protected UIToolbarDelegate (IntPtr handle)
```

Removed method:

```
public override UIBarPosition GetPositionForBar (IUIBarPositioning barPositioning);
```

### Type Changed: UIKit.UITouch

Modified constructors:

```
public protected UITouch (Foundation.NSObjectFlag t)
	public protected UITouch (IntPtr handle)
```

### Type Changed: UIKit.UITraitCollection

Modified constructors:

```
public protected UITraitCollection (Foundation.NSObjectFlag t)
	public protected UITraitCollection (IntPtr handle)
```

### Type Changed: UIKit.UITraitEnvironment

Modified constructors:

```
public protected UITraitEnvironment ()
	public protected UITraitEnvironment (Foundation.NSObjectFlag t)
	public protected UITraitEnvironment (IntPtr handle)
```

Modified properties:

```
public abstract UITraitCollection TraitCollection { get; }
```

Modified methods:

```
public abstract void TraitCollectionDidChange (UITraitCollection previousTraitCollection)
```

### Type Changed: UIKit.UIUserNotificationAction

Modified constructors:

```
public protected UIUserNotificationAction (Foundation.NSObjectFlag t)
	public protected UIUserNotificationAction (IntPtr handle)
```

### Type Changed: UIKit.UIUserNotificationCategory

Modified constructors:

```
public protected UIUserNotificationCategory (Foundation.NSObjectFlag t)
	public protected UIUserNotificationCategory (IntPtr handle)
```

### Type Changed: UIKit.UIUserNotificationSettings

Modified constructors:

```
public protected UIUserNotificationSettings (Foundation.NSObjectFlag t)
	public protected UIUserNotificationSettings (IntPtr handle)
```

### Type Changed: UIKit.UIVibrancyEffect

Modified constructors:

```
public protected UIVibrancyEffect (Foundation.NSObjectFlag t)
	public protected UIVibrancyEffect (IntPtr handle)
```

### Type Changed: UIKit.UIVideoEditorController

Modified constructors:

```
public protected UIVideoEditorController (Foundation.NSObjectFlag t)
	public protected UIVideoEditorController (IntPtr handle)
```

Removed properties:

```
public System.Func<UINavigationController,UIKit.UINavigationControllerOperation,UIKit.UIViewController,UIKit.UIViewController,UIKit.IUIViewControllerAnimatedTransitioning> GetAnimationControllerForOperation { get; set; }
	public System.Func<UINavigationController,UIKit.IUIViewControllerAnimatedTransitioning,UIKit.IUIViewControllerInteractiveTransitioning> GetInteractionControllerForAnimationController { get; set; }
	public System.Func<UINavigationController,UIKit.UIInterfaceOrientation> GetPreferredInterfaceOrientation { get; set; }
	public System.Func<UINavigationController,UIKit.UIInterfaceOrientationMask> SupportedInterfaceOrientations { get; set; }
```

Modified properties:

```
public UIVideoEditorControllerDelegate IUIVideoEditorControllerDelegate Delegate { get; set; }
```

Removed events:

```
public event System.EventHandler<UINavigationControllerEventArgs> DidShowViewController;
	public event System.EventHandler<UINavigationControllerEventArgs> WillShowViewController;
```

### Type Changed: UIKit.UIVideoEditorControllerDelegate

Modified constructors:

```
public protected UIVideoEditorControllerDelegate (Foundation.NSObjectFlag t)
	public protected UIVideoEditorControllerDelegate (IntPtr handle)
```

Removed methods:

```
public override void DidShowViewController (UINavigationController navigationController, UIViewController viewController, bool animated);
	public override IUIViewControllerAnimatedTransitioning GetAnimationControllerForOperation (UINavigationController navigationController, UINavigationControllerOperation operation, UIViewController fromViewController, UIViewController toViewController);
	public override IUIViewControllerInteractiveTransitioning GetInteractionControllerForAnimationController (UINavigationController navigationController, IUIViewControllerAnimatedTransitioning animationController);
	public override UIInterfaceOrientation GetPreferredInterfaceOrientation (UINavigationController navigationController);
	public override UIInterfaceOrientationMask SupportedInterfaceOrientations (UINavigationController navigationController);
	public override void WillShowViewController (UINavigationController navigationController, UIViewController viewController, bool animated);
```

### Type Changed: UIKit.UIView

Modified constructors:

```
public protected UIView (Foundation.NSObjectFlag t)
	public protected UIView (IntPtr handle)
```

Removed property:

```
public virtual bool EnableInputClicksWhenVisible { get; }
```

Removed methods:

```
public static void AddKeyframeWithRelativeStartTime (double frameStartTime, double frameDuration, Foundation.NSAction animations);
	public static void Animate (double duration, double delay, UIViewAnimationOptions options, Foundation.NSAction animation, Foundation.NSAction completion);
	public static void Animate (double duration, Foundation.NSAction animation);
	public static void Animate (double duration, Foundation.NSAction animation, Foundation.NSAction completion);
	public static System.Threading.Tasks.Task<bool> AnimateAsync (double duration, Foundation.NSAction animation);
	public static void AnimateKeyframes (double duration, double delay, UIViewKeyframeAnimationOptions options, Foundation.NSAction animations, UICompletionHandler completion);
	public static System.Threading.Tasks.Task<bool> AnimateKeyframesAsync (double duration, double delay, UIViewKeyframeAnimationOptions options, Foundation.NSAction animations);
	public static void AnimateNotify (double duration, double delay, float springWithDampingRatio, float initialSpringVelocity, UIViewAnimationOptions options, Foundation.NSAction animations, UICompletionHandler completion);
	public static void AnimateNotify (double duration, double delay, UIViewAnimationOptions options, Foundation.NSAction animation, UICompletionHandler completion);
	public static void AnimateNotify (double duration, Foundation.NSAction animation, UICompletionHandler completion);
	public static System.Threading.Tasks.Task<bool> AnimateNotifyAsync (double duration, Foundation.NSAction animation);
	public static System.Threading.Tasks.Task<bool> AnimateNotifyAsync (double duration, double delay, UIViewAnimationOptions options, Foundation.NSAction animation);
	public static System.Threading.Tasks.Task<bool> AnimateNotifyAsync (double duration, double delay, float springWithDampingRatio, float initialSpringVelocity, UIViewAnimationOptions options, Foundation.NSAction animations);

	[Obsolete ("Use the version with a `ref float actualFontSize`")]
	public System.Drawing.SizeF DrawString (string str, System.Drawing.PointF point, float width, UIFont font, float minFontSize, float actualFontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
	public System.Drawing.SizeF DrawString (string str, System.Drawing.RectangleF rect, UIFont font, UILineBreakMode mode, UITextAlignment alignment);
	public System.Drawing.SizeF DrawString (string str, System.Drawing.RectangleF rect, UIFont font, UILineBreakMode mode);
	public System.Drawing.SizeF DrawString (string str, System.Drawing.RectangleF rect, UIFont font);
	public System.Drawing.SizeF DrawString (string str, System.Drawing.PointF point, float width, UIFont font, float minFontSize, ref float actualFontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
	public System.Drawing.SizeF DrawString (string str, System.Drawing.PointF point, float width, UIFont font, float fontSize, UILineBreakMode breakMode, UIBaselineAdjustment adjustment);
	public System.Drawing.SizeF DrawString (string str, System.Drawing.PointF point, float width, UIFont font, UILineBreakMode breakMode);
	public System.Drawing.SizeF DrawString (string str, System.Drawing.PointF point, UIFont font);
	public bool EndEditing (bool force);
	public static void PerformSystemAnimation (UISystemAnimation animation, UIView[] views, UIViewAnimationOptions options, Foundation.NSAction parallelAnimations, UICompletionHandler completion);
	public static System.Threading.Tasks.Task<bool> PerformSystemAnimationAsync (UISystemAnimation animation, UIView[] views, UIViewAnimationOptions options, Foundation.NSAction parallelAnimations);
	public static void PerformWithoutAnimation (Foundation.NSAction actionsWithoutAnimation);
	public System.Drawing.SizeF StringSize (string str, UIFont font, float minFontSize, ref float actualFontSize, float forWidth, UILineBreakMode lineBreakMode);
	public System.Drawing.SizeF StringSize (string str, UIFont font, System.Drawing.SizeF constrainedToSize, UILineBreakMode lineBreakMode);
	public System.Drawing.SizeF StringSize (string str, UIFont font);
	public System.Drawing.SizeF StringSize (string str, UIFont font, float forWidth, UILineBreakMode breakMode);
	public System.Drawing.SizeF StringSize (string str, UIFont font, System.Drawing.SizeF constrainedToSize);
	public static void Transition (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options, Foundation.NSAction completion);
	public static void Transition (UIView withView, double duration, UIViewAnimationOptions options, Foundation.NSAction animation, Foundation.NSAction completion);
	public static void TransitionNotify (UIView withView, double duration, UIViewAnimationOptions options, Foundation.NSAction animation, UICompletionHandler completion);
	public static System.Threading.Tasks.Task<bool> TransitionNotifyAsync (UIView withView, double duration, UIViewAnimationOptions options, Foundation.NSAction animation);
```

Added methods:

```
public static void AddKeyframeWithRelativeStartTime (double frameStartTime, double frameDuration, System.Action animations);
	public static void Animate (double duration, System.Action animation, System.Action completion);
	public static void Animate (double duration, double delay, UIViewAnimationOptions options, System.Action animation, System.Action completion);
	public static void Animate (double duration, System.Action animation);
	public static System.Threading.Tasks.Task<bool> AnimateAsync (double duration, System.Action animation);
	public static void AnimateKeyframes (double duration, double delay, UIViewKeyframeAnimationOptions options, System.Action animations, UICompletionHandler completion);
	public static System.Threading.Tasks.Task<bool> AnimateKeyframesAsync (double duration, double delay, UIViewKeyframeAnimationOptions options, System.Action animations);
	public static void AnimateNotify (double duration, System.Action animation, UICompletionHandler completion);
	public static void AnimateNotify (double duration, double delay, float springWithDampingRatio, float initialSpringVelocity, UIViewAnimationOptions options, System.Action animations, UICompletionHandler completion);
	public static void AnimateNotify (double duration, double delay, UIViewAnimationOptions options, System.Action animation, UICompletionHandler completion);
	public static System.Threading.Tasks.Task<bool> AnimateNotifyAsync (double duration, double delay, float springWithDampingRatio, float initialSpringVelocity, UIViewAnimationOptions options, System.Action animations);
	public static System.Threading.Tasks.Task<bool> AnimateNotifyAsync (double duration, double delay, UIViewAnimationOptions options, System.Action animation);
	public static System.Threading.Tasks.Task<bool> AnimateNotifyAsync (double duration, System.Action animation);
	public static void PerformSystemAnimation (UISystemAnimation animation, UIView[] views, UIViewAnimationOptions options, System.Action parallelAnimations, UICompletionHandler completion);
	public static System.Threading.Tasks.Task<bool> PerformSystemAnimationAsync (UISystemAnimation animation, UIView[] views, UIViewAnimationOptions options, System.Action parallelAnimations);
	public static void PerformWithoutAnimation (System.Action actionsWithoutAnimation);
	public static void Transition (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options, System.Action completion);
	public static void Transition (UIView withView, double duration, UIViewAnimationOptions options, System.Action animation, System.Action completion);
	public static void TransitionNotify (UIView withView, double duration, UIViewAnimationOptions options, System.Action animation, UICompletionHandler completion);
	public static System.Threading.Tasks.Task<bool> TransitionNotifyAsync (UIView withView, double duration, UIViewAnimationOptions options, System.Action animation);
```

### Type Changed: UIKit.UIViewController

Modified constructors:

```
public protected UIViewController (Foundation.NSObjectFlag t)
	public protected UIViewController (IntPtr handle)
```

Modified properties:

```
public UIViewControllerTransitioningDelegate IUIViewControllerTransitioningDelegate TransitioningDelegate { get; set; }
```

Removed methods:

```
public virtual void DismissModalViewControllerAnimated (bool animated);
	public virtual void DismissViewController (bool animated, Foundation.NSAction completionHandler);
	public virtual void PresentViewController (UIViewController viewControllerToPresent, bool animated, Foundation.NSAction completionHandler);
	public virtual void Transition (UIViewController fromViewController, UIViewController toViewController, double duration, UIViewAnimationOptions options, Foundation.NSAction animations, UICompletionHandler completionHandler);
	public virtual System.Threading.Tasks.Task<bool> TransitionAsync (UIViewController fromViewController, UIViewController toViewController, double duration, UIViewAnimationOptions options, Foundation.NSAction animations);
```

Added methods:

```
public virtual void DismissModalViewController (bool animated);
	public virtual void DismissViewController (bool animated, System.Action completionHandler);
	public virtual void PresentViewController (UIViewController viewControllerToPresent, bool animated, System.Action completionHandler);
	public virtual void Transition (UIViewController fromViewController, UIViewController toViewController, double duration, UIViewAnimationOptions options, System.Action animations, UICompletionHandler completionHandler);
	public virtual System.Threading.Tasks.Task<bool> TransitionAsync (UIViewController fromViewController, UIViewController toViewController, double duration, UIViewAnimationOptions options, System.Action animations);
```

### Type Changed: UIKit.UIViewControllerAnimatedTransitioning

Modified constructors:

```
public protected UIViewControllerAnimatedTransitioning ()
	public protected UIViewControllerAnimatedTransitioning (Foundation.NSObjectFlag t)
	public protected UIViewControllerAnimatedTransitioning (IntPtr handle)
```

### Type Changed: UIKit.UIViewControllerContextTransitioning

Modified constructors:

```
public protected UIViewControllerContextTransitioning ()
	public protected UIViewControllerContextTransitioning (Foundation.NSObjectFlag t)
	public protected UIViewControllerContextTransitioning (IntPtr handle)
```

Modified properties:

```
public abstract CoreGraphics.CGAffineTransform TargetTransform { get; }
```

Modified methods:

```
public abstract UIView GetViewFor (Foundation.NSString uiTransitionContextToOrFromKey)
```

### Type Changed: UIKit.UIViewControllerInteractiveTransitioning

Modified constructors:

```
public protected UIViewControllerInteractiveTransitioning ()
	public protected UIViewControllerInteractiveTransitioning (Foundation.NSObjectFlag t)
	public protected UIViewControllerInteractiveTransitioning (IntPtr handle)
```

### Type Changed: UIKit.UIViewControllerTransitionCoordinatorContext_Extensions

Removed methods:

```
public static UIView GetTransitionViewControllerForKey (IUIViewControllerTransitionCoordinatorContext This, Foundation.NSString key);
	public static CoreGraphics.CGAffineTransform TargetTransform (IUIViewControllerTransitionCoordinatorContext This);
```

### Type Changed: UIKit.UIViewControllerTransitioningDelegate

Modified constructors:

```
public protected UIViewControllerTransitioningDelegate (Foundation.NSObjectFlag t)
	public protected UIViewControllerTransitioningDelegate (IntPtr handle)
```

Removed method:

```
public virtual IUIViewControllerAnimatedTransitioning PresentingController (UIViewController presented, UIViewController presenting, UIViewController source);
```

Added method:

```
public virtual IUIViewControllerAnimatedTransitioning GetAnimationControllerForPresentedController (UIViewController presented, UIViewController presenting, UIViewController source);
```

### Type Changed: UIKit.UIViewControllerTransitioningDelegate_Extensions

Removed method:

```
public static IUIViewControllerAnimatedTransitioning PresentingController (IUIViewControllerTransitioningDelegate This, UIViewController presented, UIViewController presenting, UIViewController source);
```

Added method:

```
public static IUIViewControllerAnimatedTransitioning GetAnimationControllerForPresentedController (IUIViewControllerTransitioningDelegate This, UIViewController presented, UIViewController presenting, UIViewController source);
```

### Type Changed: UIKit.UIViewPrintFormatter

Modified constructors:

```
public protected UIViewPrintFormatter (Foundation.NSObjectFlag t)
	public protected UIViewPrintFormatter (IntPtr handle)
```

### Type Changed: UIKit.UIVisualEffect

Modified constructors:

```
public protected UIVisualEffect (Foundation.NSObjectFlag t)
	public protected UIVisualEffect (IntPtr handle)
```

### Type Changed: UIKit.UIVisualEffectView

Modified constructors:

```
public protected UIVisualEffectView (Foundation.NSObjectFlag t)
	public protected UIVisualEffectView (IntPtr handle)
```

### Type Changed: UIKit.UIWebView

Modified constructors:

```
public protected UIWebView (Foundation.NSObjectFlag t)
	public protected UIWebView (IntPtr handle)
```

Modified properties:

```
public UIWebViewDelegate IUIWebViewDelegate Delegate { get; set; }
```

### Type Changed: UIKit.UIWebViewDelegate

Modified constructors:

```
public protected UIWebViewDelegate (Foundation.NSObjectFlag t)
	public protected UIWebViewDelegate (IntPtr handle)
```

### Type Changed: UIKit.UIWindow

Modified constructors:

```
public protected UIWindow (Foundation.NSObjectFlag t)
	public protected UIWindow (IntPtr handle)
```

Removed fields:

```
[Obsolete ("Use UIWindowLevel.Alert")]
	public static const float LevelAlert;

	[Obsolete ("Use UIWindowLevel.Normal")]
	public static const float LevelNormal;

	[Obsolete ("Use UIWindowLevel.StatusBar")]
	public static const float LevelStatusBar;
```

### Removed Type UIKit.IUIGuidedAccessRestriction ### Removed Type UIKit.NSFilePresenterReacquirer ### Removed Type UIKit.NSTextAttachmentContainer_Extensions ### Removed Type UIKit.NSTextLayoutOrientationProvider_Extensions ### Removed Type UIKit.UIAccessibilityIdentification_Extensions ### Removed Type UIKit.UIAccessibilityReadingContent_Extensions ### Removed Type UIKit.UIAppearance_Extensions ### Removed Type UIKit.UIAppearanceContainer_Extensions ### Removed Type UIKit.UIBarPositioning_Extensions ### Removed Type UIKit.UICollectionViewSource_Extensions ### Removed Type UIKit.UIContentContainer_Extensions ### Removed Type UIKit.UICoordinateSpace_Extensions ### Removed Type UIKit.UIDataSourceModelAssociation_Extensions ### Removed Type UIKit.UIDocumentMenuDelegate_Extensions ### Removed Type UIKit.UIDynamicAnimatorDelegate_Extensions ### Removed Type UIKit.UIDynamicItem_Extensions ### Removed Type UIKit.UIInputViewAudioFeedback_Extensions ### Removed Type UIKit.UIKeyInput_Extensions ### Removed Type UIKit.UILayoutSupport_Extensions ### Removed Type UIKit.UINavigationControllerEventArgs ### Removed Type UIKit.UIObjectRestoration_Extensions ### Removed Type UIKit.UIPickerViewDataSource_Extensions ### Removed Type UIKit.UIPickerViewModel_Extensions ### Removed Type UIKit.UIPopoverBackgroundViewMethods_Extensions ### Removed Type UIKit.UISearchResultsUpdating_Extensions ### Removed Type UIKit.UITextDocumentProxy_Extensions ### Removed Type UIKit.UITextInputDelegate_Extensions ### Removed Type UIKit.UITextInputTokenizer_Extensions ### Removed Type UIKit.UITextInputTraits_Extensions ### Removed Type UIKit.UIToolbarDelegate_Extensions ### Removed Type UIKit.UITraitEnvironment_Extensions ### Removed Type UIKit.UIViewControllerContextTransitioning_Extensions ### Removed Type UIKit.UIViewControllerTransitionCoordinator_Extensions 



## Namespace WebKit



### Type Changed: WebKit.WKBackForwardList

Modified constructors:

```
public protected WKBackForwardList (Foundation.NSObjectFlag t)
	public protected WKBackForwardList (IntPtr handle)
```

### Type Changed: WebKit.WKBackForwardListItem

Modified constructors:

```
public protected WKBackForwardListItem (Foundation.NSObjectFlag t)
	public protected WKBackForwardListItem (IntPtr handle)
```

### Type Changed: WebKit.WKFrameInfo

Modified constructors:

```
public protected WKFrameInfo (Foundation.NSObjectFlag t)
	public protected WKFrameInfo (IntPtr handle)
```

### Type Changed: WebKit.WKNavigation

Modified constructors:

```
public protected WKNavigation (Foundation.NSObjectFlag t)
	public protected WKNavigation (IntPtr handle)
```

### Type Changed: WebKit.WKNavigationAction

Modified constructors:

```
public protected WKNavigationAction (Foundation.NSObjectFlag t)
	public protected WKNavigationAction (IntPtr handle)
```

### Type Changed: WebKit.WKNavigationDelegate

Modified constructors:

```
public protected WKNavigationDelegate (Foundation.NSObjectFlag t)
	public protected WKNavigationDelegate (IntPtr handle)
```

### Type Changed: WebKit.WKNavigationResponse

Modified constructors:

```
public protected WKNavigationResponse (Foundation.NSObjectFlag t)
	public protected WKNavigationResponse (IntPtr handle)
```

### Type Changed: WebKit.WKPreferences

Modified constructors:

```
public protected WKPreferences (Foundation.NSObjectFlag t)
	public protected WKPreferences (IntPtr handle)
```

### Type Changed: WebKit.WKProcessPool

Modified constructors:

```
public protected WKProcessPool (Foundation.NSObjectFlag t)
	public protected WKProcessPool (IntPtr handle)
```

### Type Changed: WebKit.WKScriptMessage

Modified constructors:

```
public protected WKScriptMessage (Foundation.NSObjectFlag t)
	public protected WKScriptMessage (IntPtr handle)
```

### Type Changed: WebKit.WKScriptMessageHandler

Modified constructors:

```
public protected WKScriptMessageHandler ()
	public protected WKScriptMessageHandler (Foundation.NSObjectFlag t)
	public protected WKScriptMessageHandler (IntPtr handle)
```

### Type Changed: WebKit.WKUIDelegate

Modified constructors:

```
public protected WKUIDelegate (Foundation.NSObjectFlag t)
	public protected WKUIDelegate (IntPtr handle)
```

### Type Changed: WebKit.WKUserContentController

Modified constructors:

```
public protected WKUserContentController (Foundation.NSObjectFlag t)
	public protected WKUserContentController (IntPtr handle)
```

Removed method:

```
public virtual void AddScriptMessageHandler (WKScriptMessageHandler scriptMessageHandler, string name);
```

Added method:

```
public virtual void AddScriptMessageHandler (IWKScriptMessageHandler scriptMessageHandler, string name);
```

### Type Changed: WebKit.WKUserScript

Modified constructors:

```
public protected WKUserScript (Foundation.NSObjectFlag t)
	public protected WKUserScript (IntPtr handle)
```

### Type Changed: WebKit.WKWebView

Modified constructors:

```
public protected WKWebView (Foundation.NSObjectFlag t)
	public protected WKWebView (IntPtr handle)
```

Modified properties:

```
public WKNavigationDelegate IWKNavigationDelegate NavigationDelegate { get; set; }
	public WKUIDelegate IWKUIDelegate UIDelegate { get; set; }
```

### Type Changed: WebKit.WKWebViewConfiguration

Modified constructors:

```
public protected WKWebViewConfiguration (Foundation.NSObjectFlag t)
	public protected WKWebViewConfiguration (IntPtr handle)
```

### Type Changed: WebKit.WKWindowFeatures

Modified constructors:

```
public protected WKWindowFeatures (Foundation.NSObjectFlag t)
	public protected WKWindowFeatures (IntPtr handle)
```

### Removed Type WebKit.WKScriptMessageHandler_Extensions 

## Removed Namespace MonoTouch



### Removed Type MonoTouch.Constants ### Removed Type MonoTouch.MonoNativeFunctionWrapperAttribute ### Removed Type MonoTouch.MonoPInvokeCallbackAttribute ### Removed Type MonoTouch.RuntimeException 



## Removed Namespace AudioUnitWrapper



### Removed Type AudioUnitWrapper._AudioConverter ### Removed Type AudioUnitWrapper._AudioConverterEventArgs 



## New Namespace System



### New Type System.nfloat

```
[Serializable]
public struct nfloat, IFormattable, IConvertible, IComparable, System.IComparable<float>, System.IEquatable<float> {
	// fields
	public static float Epsilon;
	public static float MaxValue;
	public static float MinValue;
	public static float NaN;
	public static float NegativeInfinity;
	public static float PositiveInfinity;
	public static int Size;
	// methods
	public virtual int CompareTo (object value);
	public virtual int CompareTo (float value);
	public static void CopyArray (float[] source, int startIndex, IntPtr destination, int length);
	public static void CopyArray (IntPtr source, float[] destination, int startIndex, int length);
	public virtual bool Equals (float obj);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public virtual TypeCode GetTypeCode ();
	public static bool IsInfinity (float f);
	public static bool IsNaN (float f);
	public static bool IsNegativeInfinity (float f);
	public static bool IsPositiveInfinity (float f);
	public static float op_Addition (float l, float r);
	public static float op_Decrement (float v);
	public static float op_Division (float l, float r);
	public static bool op_Equality (float l, float r);
	public static float op_Explicit (IntPtr v);
	public static Decimal op_Explicit (float v);
	public static float op_Explicit (Decimal v);
	public static float op_Explicit (double v);
	public static float op_Explicit (float v);
	public static uint op_Explicit (float v);
	public static int op_Explicit (float v);
	public static ushort op_Explicit (float v);
	public static short op_Explicit (float v);
	public static char op_Explicit (float v);
	public static byte op_Explicit (float v);
	public static sbyte op_Explicit (float v);
	public static IntPtr op_Explicit (float v);
	public static long op_Explicit (float v);
	public static ulong op_Explicit (float v);
	public static bool op_GreaterThan (float l, float r);
	public static bool op_GreaterThanOrEqual (float l, float r);
	public static float op_Implicit (long v);
	public static float op_Implicit (short v);
	public static float op_Implicit (ulong v);
	public static float op_Implicit (char v);
	public static double op_Implicit (float v);
	public static float op_Implicit (byte v);
	public static float op_Implicit (sbyte v);
	public static float op_Implicit (float v);
	public static float op_Implicit (ushort v);
	public static float op_Implicit (uint v);
	public static float op_Implicit (int v);
	public static float op_Increment (float v);
	public static bool op_Inequality (float l, float r);
	public static bool op_LessThan (float l, float r);
	public static bool op_LessThanOrEqual (float l, float r);
	public static float op_Modulus (float l, float r);
	public static float op_Multiply (float l, float r);
	public static float op_Subtraction (float l, float r);
	public static float op_UnaryNegation (float v);
	public static float op_UnaryPlus (float v);
	public static float Parse (string s, Globalization.NumberStyles style);
	public static float Parse (string s, IFormatProvider provider);
	public static float Parse (string s, Globalization.NumberStyles style, IFormatProvider provider);
	public static float Parse (string s);
	public string ToString (string format);
	public virtual string ToString (string format, IFormatProvider provider);
	public override string ToString ();
	public virtual string ToString (IFormatProvider provider);
	public static bool TryParse (string s, Globalization.NumberStyles style, IFormatProvider provider, out float result);
	public static bool TryParse (string s, out float result);
}
```

### New Type System.nint

```
[Serializable]
public struct nint, IFormattable, IConvertible, IComparable, System.IComparable<int>, System.IEquatable<int> {
	// fields
	public static int MaxValue;
	public static int MinValue;
	public static int Size;
	// methods
	public virtual int CompareTo (object value);
	public virtual int CompareTo (int value);
	public static void CopyArray (int[] source, int startIndex, IntPtr destination, int length);
	public static void CopyArray (IntPtr source, int[] destination, int startIndex, int length);
	public override bool Equals (object obj);
	public virtual bool Equals (int obj);
	public override int GetHashCode ();
	public virtual TypeCode GetTypeCode ();
	public static int op_Addition (int l, int r);
	public static int op_BitwiseAnd (int l, int r);
	public static int op_BitwiseOr (int l, int r);
	public static int op_Decrement (int v);
	public static int op_Division (int l, int r);
	public static bool op_Equality (int l, int r);
	public static int op_ExclusiveOr (int l, int r);
	public static int op_Explicit (double v);
	public static int op_Explicit (Decimal v);
	public static char op_Explicit (int v);
	public static int op_Explicit (uint v);
	public static uint op_Explicit (int v);
	public static int op_Explicit (float v);
	public static int op_Explicit (IntPtr v);
	public static IntPtr op_Explicit (int v);
	public static sbyte op_Explicit (int v);
	public static byte op_Explicit (int v);
	public static uint op_Explicit (int v);
	public static int op_Explicit (int v);
	public static int op_Explicit (ulong v);
	public static int op_Explicit (uint v);
	public static ushort op_Explicit (int v);
	public static int op_Explicit (long v);
	public static int op_Explicit (ushort v);
	public static ulong op_Explicit (int v);
	public static int op_Explicit (float v);
	public static short op_Explicit (int v);
	public static bool op_GreaterThan (int l, int r);
	public static bool op_GreaterThanOrEqual (int l, int r);
	public static int op_Implicit (short v);
	public static float op_Implicit (int v);
	public static int op_Implicit (int v);
	public static float op_Implicit (int v);
	public static int op_Implicit (sbyte v);
	public static int op_Implicit (byte v);
	public static double op_Implicit (int v);
	public static Decimal op_Implicit (int v);
	public static int op_Implicit (char v);
	public static long op_Implicit (int v);
	public static int op_Increment (int v);
	public static bool op_Inequality (int l, int r);
	public static int op_LeftShift (int l, int r);
	public static bool op_LessThan (int l, int r);
	public static bool op_LessThanOrEqual (int l, int r);
	public static int op_Modulus (int l, int r);
	public static int op_Multiply (int l, int r);
	public static int op_OnesComplement (int v);
	public static int op_RightShift (int l, int r);
	public static int op_Subtraction (int l, int r);
	public static int op_UnaryNegation (int v);
	public static int op_UnaryPlus (int v);
	public static int Parse (string s, IFormatProvider provider);
	public static int Parse (string s);
	public static int Parse (string s, Globalization.NumberStyles style);
	public static int Parse (string s, Globalization.NumberStyles style, IFormatProvider provider);
	public string ToString (string format);
	public virtual string ToString (string format, IFormatProvider provider);
	public override string ToString ();
	public virtual string ToString (IFormatProvider provider);
	public static bool TryParse (string s, out int result);
	public static bool TryParse (string s, Globalization.NumberStyles style, IFormatProvider provider, out int result);
}
```

### New Type System.NMath

```
public static class NMath {
	// fields
	public static float E;
	public static float PI;
	// methods
	public static float Abs (float value);
	public static int Abs (int value);
	public static float Acos (float d);
	public static float Asin (float d);
	public static float Atan (float d);
	public static float Atan2 (float y, float x);
	public static long BigMul (int a, int b);
	public static float Ceiling (float value);
	public static float Cos (float d);
	public static float Cosh (float value);
	public static int DivRem (int a, int b, out int result);
	public static float Exp (float d);
	public static float Floor (float d);
	public static float IEEERemainder (float x, float y);
	public static float Log (float a, float newBase);
	public static float Log (float d);
	public static float Log10 (float d);
	public static float Max (float val1, float val2);
	public static uint Max (uint val1, uint val2);
	public static int Max (int val1, int val2);
	public static uint Min (uint val1, uint val2);
	public static int Min (int val1, int val2);
	public static float Min (float val1, float val2);
	public static float Pow (float x, float y);
	public static float Round (float a);
	public static float Round (float value, int digits);
	public static float Round (float value, MidpointRounding mode);
	public static float Round (float value, int digits, MidpointRounding mode);
	public static int Sign (float value);
	public static int Sign (int value);
	public static float Sin (float a);
	public static float Sinh (float value);
	public static float Sqrt (float d);
	public static float Tan (float a);
	public static float Tanh (float value);
	public static float Truncate (float d);
}
```

### New Type System.nuint

```
[Serializable]
public struct nuint, IFormattable, IConvertible, IComparable, System.IComparable<uint>, System.IEquatable<uint> {
	// fields
	public static uint MaxValue;
	public static uint MinValue;
	public static int Size;
	// methods
	public virtual int CompareTo (uint value);
	public virtual int CompareTo (object value);
	public static void CopyArray (uint[] source, int startIndex, IntPtr destination, int length);
	public static void CopyArray (IntPtr source, uint[] destination, int startIndex, int length);
	public virtual bool Equals (uint obj);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public virtual TypeCode GetTypeCode ();
	public static uint op_Addition (uint l, uint r);
	public static uint op_BitwiseAnd (uint l, uint r);
	public static uint op_BitwiseOr (uint l, uint r);
	public static uint op_Decrement (uint v);
	public static uint op_Division (uint l, uint r);
	public static bool op_Equality (uint l, uint r);
	public static uint op_ExclusiveOr (uint l, uint r);
	public static uint op_Explicit (double v);
	public static uint op_Explicit (Decimal v);
	public static uint op_Explicit (IntPtr v);
	public static IntPtr op_Explicit (uint v);
	public static char op_Explicit (uint v);
	public static uint op_Explicit (sbyte v);
	public static sbyte op_Explicit (uint v);
	public static byte op_Explicit (uint v);
	public static uint op_Explicit (float v);
	public static uint op_Explicit (ulong v);
	public static uint op_Explicit (int v);
	public static long op_Explicit (uint v);
	public static uint op_Explicit (long v);
	public static uint op_Explicit (uint v);
	public static int op_Explicit (uint v);
	public static short op_Explicit (uint v);
	public static ushort op_Explicit (uint v);
	public static uint op_Explicit (float v);
	public static uint op_Explicit (short v);
	public static bool op_GreaterThan (uint l, uint r);
	public static bool op_GreaterThanOrEqual (uint l, uint r);
	public static float op_Implicit (uint v);
	public static float op_Implicit (uint v);
	public static uint op_Implicit (byte v);
	public static uint op_Implicit (ushort v);
	public static Decimal op_Implicit (uint v);
	public static ulong op_Implicit (uint v);
	public static uint op_Implicit (char v);
	public static uint op_Implicit (uint v);
	public static double op_Implicit (uint v);
	public static uint op_Increment (uint v);
	public static bool op_Inequality (uint l, uint r);
	public static uint op_LeftShift (uint l, int r);
	public static bool op_LessThan (uint l, uint r);
	public static bool op_LessThanOrEqual (uint l, uint r);
	public static uint op_Modulus (uint l, uint r);
	public static uint op_Multiply (uint l, uint r);
	public static uint op_OnesComplement (uint v);
	public static uint op_RightShift (uint l, int r);
	public static uint op_Subtraction (uint l, uint r);
	public static uint op_UnaryPlus (uint v);
	public static uint Parse (string s, Globalization.NumberStyles style, IFormatProvider provider);
	public static uint Parse (string s);
	public static uint Parse (string s, IFormatProvider provider);
	public static uint Parse (string s, Globalization.NumberStyles style);
	public virtual string ToString (string format, IFormatProvider provider);
	public string ToString (string format);
	public virtual string ToString (IFormatProvider provider);
	public override string ToString ();
	public static bool TryParse (string s, Globalization.NumberStyles style, IFormatProvider provider, out uint result);
	public static bool TryParse (string s, out uint result);
}
```
