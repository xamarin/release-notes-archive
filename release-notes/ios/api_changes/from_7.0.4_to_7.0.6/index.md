---
id: 640998DB-847B-4EB7-BD5F-D4F966FBB8E4
title: "From 7.0.4 to 7.0.6"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed fields:

```
public static const string Version = "7.0.4";
```

Added fields:

```
public static const string Version = "7.0.6";
```

## Namespace MonoTouch.Accounts

### Type Changed: MonoTouch.Accounts.ACAccount

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.Accounts.ACAccountCredential

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.Accounts.ACAccountType

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.AddressBookUI

### Type Changed: MonoTouch.AddressBookUI.ABNewPersonViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.AddressBookUI.ABPersonViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.AddressBookUI.ABUnknownPersonViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.AudioUnit

### Type Changed: MonoTouch.AudioUnit.AudioUnit

Added methods:

```
public ClassInfoDictionary GetClassInfo (AudioUnitScopeType scope, uint audioUnitElement);
	public uint GetMaximumFramesPerSlice (AudioUnitScopeType scope, uint audioUnitElement);
	public AudioUnitStatus LoadInstrument (SamplerInstrumentData instrumentData, AudioUnitScopeType scope, uint audioUnitElement);
	public AudioUnitStatus SetClassInfo (ClassInfoDictionary preset, AudioUnitScopeType scope, uint audioUnitElement);
```

### Type Changed: MonoTouch.AudioUnit.AudioUnitPropertyIDType

Added values:

```
LoadAudioFiles = 4101,
	LoadInstrument = 4102,
```

### Type Changed: MonoTouch.AudioUnit.AudioUnitStatus

Added values:

```
FileNotFound = -43,
```

### New Type MonoTouch.AudioUnit.ClassInfoDictionary

```
public class ClassInfoDictionary : MonoTouch.Foundation.DictionaryContainer {
	// constructors
	public ClassInfoDictionary ();
	public ClassInfoDictionary (MonoTouch.Foundation.NSDictionary dictionary);
	// properties
	public MonoTouch.AudioUnit.AudioComponentManufacturerType? Manufacturer { get; }
	public string Name { get; }
	public MonoTouch.AudioUnit.AudioComponentType? Type { get; }
}
```

### New Type MonoTouch.AudioUnit.InstrumentType

```
[Serializable]
public enum InstrumentType {
	Audiofile = 3,
	AUPreset = 2,
	DLSPreset = 1,
	EXS24 = 4,
	SF2Preset = 1,
}
```

### New Type MonoTouch.AudioUnit.SamplerInstrumentData

```
public class SamplerInstrumentData {
	// constructors
	public SamplerInstrumentData (MonoTouch.CoreFoundation.CFUrl fileUrl, InstrumentType instrumentType);
	// fields
	public static const byte DefaultBankLSB;
	public static const byte DefaultMelodicBankMSB;
	public static const byte DefaultPercussionBankMSB;
	// properties
	public byte BankLSB { get; set; }
	public byte BankMSB { get; set; }
	public MonoTouch.CoreFoundation.CFUrl FileUrl { get; }
	public InstrumentType InstrumentType { get; }
	public byte PresetID { get; set; }
}
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAsset

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetTrack

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetTrackGroup

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVAssetWriterInputGroup

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVAsynchronousVideoCompositionRequest

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVAudioMix

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVAudioMixInputParameters

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVCaptureVideoPreviewLayer

Added interfaces:

```
MonoTouch.CoreAnimation.ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.AVFoundation.AVComposition

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVCompositionTrack

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVMediaSelectionGroup

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVMediaSelectionOption

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVMetadataItem

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVMutableAudioMix

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVMutableAudioMixInputParameters

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVMutableComposition

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVMutableCompositionTrack

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVMutableMetadataItem

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVMutableTimedMetadataGroup

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVMutableVideoComposition

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVMutableVideoCompositionInstruction

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.AVFoundation.AVMutableVideoCompositionLayerInstruction

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.AVFoundation.AVPlayerItem

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVPlayerItemAccessLog

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVPlayerItemAccessLogEvent

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVPlayerItemErrorLog

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVPlayerItemErrorLogEvent

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVPlayerLayer

Added interfaces:

```
MonoTouch.CoreAnimation.ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.AVFoundation.AVSpeechSynthesisVoice

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.AVFoundation.AVSpeechUtterance

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVSynchronizedLayer

Added interfaces:

```
MonoTouch.CoreAnimation.ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.AVFoundation.AVTextStyleRule

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVTimedMetadataGroup

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVUrlAsset

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.AVFoundation.AVVideoComposition

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVVideoCompositionInstruction

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.AVFoundation.AVVideoCompositionLayerInstruction

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

## Namespace MonoTouch.CoreAnimation

### Type Changed: MonoTouch.CoreAnimation.CAAnimation

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	ICAMediaTiming
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreAnimation.CAAnimationGroup

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	ICAMediaTiming
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CABasicAnimation

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	ICAMediaTiming
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAEAGLLayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAEmitterBehavior

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAEmitterCell

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

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

### Type Changed: MonoTouch.CoreAnimation.CAEmitterLayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAGradientLayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	ICAMediaTiming
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CALayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAMediaTimingFunction

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAPropertyAnimation

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	ICAMediaTiming
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAReplicatorLayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAScrollLayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAShapeLayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CATextLayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CATiledLayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CATransformLayer

Added interfaces:

```
ICAMediaTiming
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CATransition

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	ICAMediaTiming
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreAnimation.CAValueFunction

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### New Type MonoTouch.CoreAnimation.CAMediaTiming

```
public class CAMediaTiming : MonoTouch.Foundation.NSObject, ICAMediaTiming, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public CAMediaTiming ();
	public CAMediaTiming (MonoTouch.Foundation.NSCoder coder);
	public CAMediaTiming (MonoTouch.Foundation.NSObjectFlag t);
	public CAMediaTiming (System.IntPtr handle);
	// properties
	public virtual bool AutoReverses { get; set; }
	public virtual double BeginTime { get; set; }
	public virtual double Duration { get; set; }
	public virtual string FillMode { get; set; }
	public virtual float RepeatCount { get; set; }
	public virtual double RepeatDuration { get; set; }
	public virtual float Speed { get; set; }
	public virtual double TimeOffset { get; set; }
}
```

### New Type MonoTouch.CoreAnimation.CAMediaTiming_Extensions

```
public static class CAMediaTiming_Extensions {
}
```

### New Type MonoTouch.CoreAnimation.ICAMediaTiming

```
public interface ICAMediaTiming : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

## Namespace MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.CBCentral

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreBluetooth.CBPeripheral

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreBluetooth.CBUUID

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

## Namespace MonoTouch.CoreData

### Type Changed: MonoTouch.CoreData.NSAttributeDescription

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreData.NSEntityDescription

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreData.NSFetchedPropertyDescription

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreData.NSFetchRequest

Added interfaces:

```
MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.CoreData.NSManagedObjectContext

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreData.NSManagedObjectID

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreData.NSManagedObjectModel

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreData.NSPersistentStoreRequest

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreData.NSPropertyDescription

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreData.NSRelationshipDescription

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreData.NSSaveChangesRequest

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

## Namespace MonoTouch.CoreImage

### Type Changed: MonoTouch.CoreImage.CIAdditionCompositing

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIAffineClamp

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIAffineFilter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIAffineTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIAffineTransform

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIBarsSwipeTransition

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIBlendFilter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIBlendWithAlphaMask

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIBlendWithMask

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIBloom

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIBumpDistortion

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIBumpDistortionLinear

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CICheckerboardGenerator

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CICircleSplashDistortion

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CICircularScreen

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColor

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreImage.CIColorBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorBurnBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorClamp

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorControls

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorCrossPolynomial

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorCube

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorCubeWithColorSpace

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorDodgeBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorInvert

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorMap

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorMatrix

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorMonochrome

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorPolynomial

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIColorPosterize

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CICompositingFilter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIConstantColorGenerator

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIContext

Removed methods:

```
[Obsolete ("Deprecated in iOS 6.0. Use DrawImage (CIImage, RectangleF, RectangleF) instead")]
	public virtual void DrawImage (CIImage image, System.Drawing.PointF atPoint, System.Drawing.RectangleF fromRect);
```

Added methods:

```
[Obsolete ("Deprecated in iOS 6.0. Use DrawImage (CIImage, CGRect, CGRect) instead")]
	public virtual void DrawImage (CIImage image, System.Drawing.PointF atPoint, System.Drawing.RectangleF fromRect);
```

### Type Changed: MonoTouch.CoreImage.CIConvolution3X3

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIConvolution5X5

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIConvolution9Horizontal

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIConvolution9Vertical

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIConvolutionCore

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CICopyMachineTransition

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CICrop

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIDarkenBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIDifferenceBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIDisintegrateWithMaskTransition

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIDissolveTransition

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIDistortionFilter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIDotScreen

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIEightfoldReflectedTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIExclusionBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIExposureAdjust

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIFaceBalance

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIFalseColor

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIFilter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreImage.CIFlashTransition

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIFourfoldReflectedTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIFourfoldRotatedTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIFourfoldTranslatedTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIGammaAdjust

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIGaussianBlur

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIGaussianGradient

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIGlideReflectedTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIGloom

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIHardLightBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIHatchedScreen

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIHighlightShadowAdjust

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIHoleDistortion

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIHueAdjust

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIHueBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIImage

Removed constructors:

```
public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer);
	public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, MonoTouch.Foundation.NSDictionary dict);
	public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, CIImageInitializationOptions options);
	public CIImage (MonoTouch.CoreGraphics.CGLayer layer);
	public CIImage (MonoTouch.CoreGraphics.CGLayer layer, MonoTouch.Foundation.NSDictionary d);
	public CIImage (MonoTouch.CoreGraphics.CGLayer layer, CIImageInitializationOptions options);
```

Added constructors:

```
[Obsolete ("CVImageBuffer is used on OS X, for iOS use CVPixelBuffer")]
	public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer);

	public CIImage (MonoTouch.CoreVideo.CVPixelBuffer buffer, CIImageInitializationOptions options);
	public CIImage (MonoTouch.CoreVideo.CVPixelBuffer buffer, MonoTouch.Foundation.NSDictionary dict);
	public CIImage (MonoTouch.CoreVideo.CVPixelBuffer buffer);
	[Obsolete ("CVImageBuffer is used on OS X, for iOS use CVPixelBuffer")]
	public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, MonoTouch.Foundation.NSDictionary dict);

	[Obsolete ("CVImageBuffer is used on OS X, for iOS use CVPixelBuffer")]
	public CIImage (MonoTouch.CoreVideo.CVImageBuffer imageBuffer, CIImageInitializationOptions options);

	[Obsolete ("A CIImage cannot be created from a CGLayer on iOS (only OS X)")]
	public CIImage (MonoTouch.CoreGraphics.CGLayer layer);

	[Obsolete ("A CIImage cannot be created from a CGLayer on iOS (only OS X)")]
	public CIImage (MonoTouch.CoreGraphics.CGLayer layer, MonoTouch.Foundation.NSDictionary d);

	[Obsolete ("A CIImage cannot be created from a CGLayer on iOS (only OS X)")]
	public CIImage (MonoTouch.CoreGraphics.CGLayer layer, CIImageInitializationOptions options);
```

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreImage.CILanczosScaleTransform

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CILightenBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CILightTunnel

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CILinearGradient

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CILinearToSRGBToneCurve

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CILineScreen

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CILuminosityBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIMaskToAlpha

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIMaximumComponent

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIMaximumCompositing

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIMinimumComponent

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIMinimumCompositing

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIModTransition

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIMultiplyBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIMultiplyCompositing

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIOverlayBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPerspectiveTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPerspectiveTransform

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPerspectiveTransformWithExtent

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffect

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectChrome

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectFade

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectInstant

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectMono

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectNoir

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectProcess

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectTonal

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPhotoEffectTransfer

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPinchDistortion

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIPixellate

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIQRCodeGenerator

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIRadialGradient

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIRandomGenerator

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISaturationBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIScreenBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIScreenFilter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISepiaTone

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISharpenLuminance

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISixfoldReflectedTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISixfoldRotatedTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISmoothLinearGradient

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISoftLightBlendMode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISourceAtopCompositing

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISourceInCompositing

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISourceOutCompositing

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISourceOverCompositing

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISRGBToneCurveToLinear

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIStarShineGenerator

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIStraightenFilter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIStripesGenerator

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CISwipeTransition

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CITemperatureAndTint

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CITileFilter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIToneCurve

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CITransitionFilter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CITriangleKaleidoscope

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CITwelvefoldReflectedTile

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CITwirlDistortion

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIUnsharpMask

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIVector

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreImage.CIVibrance

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIVignette

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIVignetteEffect

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIVortexDistortion

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreImage.CIWhitePointAdjust

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Removed Type MonoTouch.CoreImage.CIDetectorKeys 

## Namespace MonoTouch.CoreLocation

### Type Changed: MonoTouch.CoreLocation.CLBeacon

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreLocation.CLBeaconRegion

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreLocation.CLCircularRegion

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.CoreLocation.CLHeading

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreLocation.CLLocation

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreLocation.CLPlacemark

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreLocation.CLRegion

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

## Namespace MonoTouch.CoreMotion

### Type Changed: MonoTouch.CoreMotion.CMAccelerometerData

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.CoreMotion.CMAttitude

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreMotion.CMDeviceMotion

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.CoreMotion.CMGyroData

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.CoreMotion.CMLogItem

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.CoreMotion.CMMagnetometerData

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
	MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.CoreMotion.CMMotionActivity

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

## Namespace MonoTouch.EventKit

### Type Changed: MonoTouch.EventKit.EKAlarm

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.EventKit.EKParticipant

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.EventKit.EKRecurrenceDayOfWeek

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.EventKit.EKRecurrenceEnd

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.EventKit.EKRecurrenceRule

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.EventKit.EKStructuredLocation

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

## Namespace MonoTouch.EventKitUI

### Type Changed: MonoTouch.EventKitUI.EKCalendarChooser

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.EventKitUI.EKEventViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.Foundation

### Type Changed: MonoTouch.Foundation.NSAlignmentOptions

Removed values:

```
RectFlipped = -2147483648,
```

Added values:

```
RectFlipped = -9223372036854775808,
```

### Type Changed: MonoTouch.Foundation.NSArray

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSAttributedString

Added interfaces:

```
INSMutableCopying
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSByteCountFormatter

Added interfaces:

```
INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSCachedUrlResponse

Added interfaces:

```
INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSCalendar

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSCharacterSet

Added interfaces:

```
INSMutableCopying
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSComparisonPredicate

Added interfaces:

```
INSSecureCoding
	INSCoding
	INSCopying
```

### Type Changed: MonoTouch.Foundation.NSCompoundPredicate

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSData

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSDate

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual string DescriptionWithLocale (NSLocale locale);
```

### Type Changed: MonoTouch.Foundation.NSDateComponents

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSDateFormatter

Added interfaces:

```
INSCopying
	INSCoding
```

Added methods:

```
public static string GetDateFormatFromTemplate (string template, uint options, NSLocale locale);
	public static string ToLocalizedString (NSDate date, NSDateFormatterStyle dateStyle, NSDateFormatterStyle timeStyle);
```

### Type Changed: MonoTouch.Foundation.NSDecimal

Added interfaces:

```
System.IEquatable<NSDecimal>
```

Added methods:

```
public virtual bool Equals (NSDecimal other);
```

### Type Changed: MonoTouch.Foundation.NSDecimalNumber

Added interfaces:

```
INSSecureCoding
	INSCoding
	INSCopying
```

### Type Changed: MonoTouch.Foundation.NSDictionary

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSError

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSException

Added interfaces:

```
INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSExpression

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSFileHandle

Added interfaces:

```
INSSecureCoding
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSFileWrapper

Added interfaces:

```
INSCoding
```

### Type Changed: MonoTouch.Foundation.NSFormatter

Added interfaces:

```
INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSHttpUrlResponse

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSIndexPath

Added interfaces:

```
INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSIndexSet

Added interfaces:

```
INSMutableCopying
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSLocale

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSMachPort

Added interfaces:

```
INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableArray

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableAttributedString

Added interfaces:

```
INSMutableCopying
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableCharacterSet

Added interfaces:

```
INSMutableCopying
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableData

Removed constructors:

```
public NSMutableData (uint len);
```

Added constructors:

```
public NSMutableData (uint capacity);
```

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableDictionary

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableIndexSet

Added interfaces:

```
INSMutableCopying
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableOrderedSet

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableSet

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableString

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSMutableUrlRequest

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSNetService

Removed properties:

```
public virtual NSData[] Addresses { get; }
	public virtual string Domain { get; }
	public virtual string HostName { get; }
	public virtual string Name { get; }
	public virtual int Port { get; }
	public virtual string Type { get; }
	public virtual NSObject WeakDelegate { get; set; }
```

Added properties:

```
[Obsolete ("Deprecated in iOS 6.1 and OS X 10.8")]
	public virtual NSData[] Addresses { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OS X 10.8")]
	public virtual string Domain { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OS X 10.8")]
	public virtual string HostName { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OS X 10.8")]
	public virtual string Name { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OS X 10.8")]
	public virtual int Port { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OS X 10.8")]
	public virtual string Type { get; }

	[Obsolete ("Deprecated in iOS 6.1 and OS X 10.8")]
	public virtual NSObject WeakDelegate { get; set; }
```

### Type Changed: MonoTouch.Foundation.NSNotification

Added interfaces:

```
INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSNull

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSNumber

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSNumberFormatter

Added interfaces:

```
INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSObject

Added methods:

```
protected void InitializeHandle (System.IntPtr handle, string initSelector);
	protected void InitializeHandle (System.IntPtr handle);
```

### Type Changed: MonoTouch.Foundation.NSOrderedSet

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSOrthography

Added interfaces:

```
INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSPort

Added interfaces:

```
INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSPredicate

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSPurgeableData

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSSet

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSSortDescriptor

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSString

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSTimeZone

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSUrl

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSUrlAuthenticationChallenge

Added interfaces:

```
INSSecureCoding
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSUrlComponents

Added interfaces:

```
INSCopying
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSUrlConnectionDelegate

Added methods:

```
public virtual void WillSendRequestForAuthenticationChallenge (NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
```

### Type Changed: MonoTouch.Foundation.NSUrlConnectionDelegate_Extensions

Added methods:

```
public static void WillSendRequestForAuthenticationChallenge (INSUrlConnectionDelegate This, NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
```

### Type Changed: MonoTouch.Foundation.NSUrlConnectionDownloadDelegate

Added methods:

```
public override void WillSendRequestForAuthenticationChallenge (NSUrlConnection connection, NSUrlAuthenticationChallenge challenge);
```

### Type Changed: MonoTouch.Foundation.NSUrlCredential

Removed constructors:

```
public NSUrlCredential (System.IntPtr trust, bool ignored);
```

Added constructors:

```
[Obsolete ("Use NSUrlCredential(SecTrust) constructor")]
	public NSUrlCredential (System.IntPtr trust, bool ignored);

	public NSUrlCredential (MonoTouch.Security.SecTrust trust);
	public NSUrlCredential (MonoTouch.Security.SecIdentity identity, MonoTouch.Security.SecCertificate[] certificates, NSUrlCredentialPersistence persistence);
```

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Removed properties:

```
public virtual System.IntPtr Identity { get; }
```

Added properties:

```
public virtual MonoTouch.Security.SecCertificate[] Certificates { get; }
	[Obsolete ("Use SecIdentity property")]
	public virtual System.IntPtr Identity { get; }

	public MonoTouch.Security.SecIdentity SecIdentity { get; }
```

Removed methods:

```
public static NSUrlCredential FromTrust (System.IntPtr SecTrustRef_trust);
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public static NSUrlCredential FromIdentityCertificatesPersistance (MonoTouch.Security.SecIdentity identity, MonoTouch.Security.SecCertificate[] certificates, NSUrlCredentialPersistence persistence);
	public static NSUrlCredential FromTrust (MonoTouch.Security.SecTrust trust);
	[Obsolete ("Use NSUrlCredential(SecTrust) constructor")]
	public static NSUrlCredential FromTrust (System.IntPtr trust);
```

### Type Changed: MonoTouch.Foundation.NSUrlProtectionSpace

Added constructors:

```
public NSUrlProtectionSpace (string host, int port, string protocol, string realm, string authenticationMethod, bool useProxy);
```

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Removed properties:

```
public static NSString AuthenticationMethodNegotiat { get; }
	public static NSString AuthenticationMethodNTL { get; }
	public static NSString AuthenticationMethodServerTrus { get; }
	public virtual System.IntPtr ServerTrust { get; }
```

Added properties:

```
[Obsolete ("Use AuthenticationMethodNegotiate")]
	public static NSString AuthenticationMethodNegotiat { get; }

	public static NSString AuthenticationMethodNegotiate { get; }
	[Obsolete ("Use AuthenticationMethodNTLM")]
	public static NSString AuthenticationMethodNTL { get; }

	public static NSString AuthenticationMethodNTLM { get; }
	[Obsolete ("Use AuthenticationMethodServerTrust")]
	public static NSString AuthenticationMethodServerTrus { get; }

	public static NSString AuthenticationMethodServerTrust { get; }
	public MonoTouch.Security.SecTrust ServerSecTrust { get; }
	[Obsolete ("Use ServerSecTrust")]
	public virtual System.IntPtr ServerTrust { get; }
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSUrlRequest

Added interfaces:

```
INSMutableCopying
	INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSUrlResponse

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionConfiguration

Added interfaces:

```
INSCopying
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionDataTask

Added interfaces:

```
INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionDownloadTask

Added interfaces:

```
INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionTask

Added interfaces:

```
INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSUrlSessionUploadTask

Added interfaces:

```
INSCopying
	INSCoding
```

### Type Changed: MonoTouch.Foundation.NSUuid

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
```

### Type Changed: MonoTouch.Foundation.NSValue

Added interfaces:

```
INSSecureCoding
	INSCopying
	INSCoding
```

Removed properties:

```
public virtual System.Drawing.PointF PointFValue { get; }
	public virtual System.Drawing.RectangleF RectangleFValue { get; }
	public virtual System.Drawing.SizeF SizeFValue { get; }
```

Added properties:

```
public virtual System.Drawing.PointF CGPointValue { get; }
	public virtual System.Drawing.RectangleF CGRectValue { get; }
	public virtual System.Drawing.SizeF CGSizeValue { get; }
	public System.Drawing.PointF PointFValue { get; }
	public System.Drawing.RectangleF RectangleFValue { get; }
	public System.Drawing.SizeF SizeFValue { get; }
```

Added methods:

```
public virtual NSObject Copy (NSZone zone);
	public static NSValue FromCGPoint (System.Drawing.PointF point);
	public static NSValue FromCGRect (System.Drawing.RectangleF rect);
	public static NSValue FromCGSize (System.Drawing.SizeF size);
```

### New Type MonoTouch.Foundation.INSCoding

```
public interface INSCoding : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.Foundation.INSCopying

```
public interface INSCopying : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.Foundation.INSMutableCopying

```
public interface INSMutableCopying : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSCopying {
}
```

### New Type MonoTouch.Foundation.INSSecureCoding

```
public interface INSSecureCoding : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable, INSCoding {
}
```

### New Type MonoTouch.Foundation.NSCoding

```
public class NSCoding : MonoTouch.Foundation.NSObject, INSCoding, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCoding ();
	public NSCoding (NSCoder coder);
	public NSCoding (NSObjectFlag t);
	public NSCoding (System.IntPtr handle);
}
```

### New Type MonoTouch.Foundation.NSCoding_Extensions

```
public static class NSCoding_Extensions {
}
```

### New Type MonoTouch.Foundation.NSCopying

```
public class NSCopying : MonoTouch.Foundation.NSObject, INSCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSCopying ();
	public NSCopying (NSCoder coder);
	public NSCopying (NSObjectFlag t);
	public NSCopying (System.IntPtr handle);
	// methods
	public virtual NSObject Copy (NSZone zone);
}
```

### New Type MonoTouch.Foundation.NSCopying_Extensions

```
public static class NSCopying_Extensions {
	// methods
	public static NSObject Copy (INSCopying This, NSZone zone);
}
```

### New Type MonoTouch.Foundation.NSMutableCopying

```
public class NSMutableCopying : MonoTouch.Foundation.NSObject, INSCopying, INSMutableCopying, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public NSMutableCopying ();
	public NSMutableCopying (NSCoder coder);
	public NSMutableCopying (NSObjectFlag t);
	public NSMutableCopying (System.IntPtr handle);
	// methods
	public virtual NSObject Copy (NSZone zone);
	public virtual NSObject MutableCopy (NSZone zone);
}
```

### New Type MonoTouch.Foundation.NSMutableCopying_Extensions

```
public static class NSMutableCopying_Extensions {
	// methods
	public static NSObject MutableCopy (INSMutableCopying This, NSZone zone);
}
```

### New Type MonoTouch.Foundation.NSSecureCoding

```
public class NSSecureCoding {
	// constructors
	public NSSecureCoding ();
	// methods
	public static bool SupportsSecureCoding (System.Type type);
	public static bool SupportsSecureCoding (MonoTouch.ObjCRuntime.Class klass);
}
```

### New Type MonoTouch.Foundation.NSSecureCoding_Extensions

```
public static class NSSecureCoding_Extensions {
}
```

### New Type MonoTouch.Foundation.NSZone

```
public class NSZone : MonoTouch.ObjCRuntime.INativeObject {
	// constructors
	public NSZone (System.IntPtr handle);
	// fields
	public static NSZone Default;
	// properties
	public virtual System.IntPtr Handle { get; }
	public string Name { get; set; }
}
```

## Namespace MonoTouch.GameController

### Type Changed: MonoTouch.GameController.GCControllerAxisInput

Removed constructors:

```
public GCControllerAxisInput ();
```

Added constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCControllerAxisInput ();
```

### Type Changed: MonoTouch.GameController.GCControllerButtonInput

Removed constructors:

```
public GCControllerButtonInput ();
```

Added constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCControllerButtonInput ();
```

### Type Changed: MonoTouch.GameController.GCControllerDirectionPad

Removed constructors:

```
public GCControllerDirectionPad ();
```

Added constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCControllerDirectionPad ();
```

### Type Changed: MonoTouch.GameController.GCControllerElement

Removed constructors:

```
public GCControllerElement ();
```

Added constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCControllerElement ();
```

### Type Changed: MonoTouch.GameController.GCExtendedGamepad

Removed constructors:

```
public GCExtendedGamepad ();
```

Added constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCExtendedGamepad ();
```

### Type Changed: MonoTouch.GameController.GCGamepad

Removed constructors:

```
public GCGamepad ();
```

Added constructors:

```
[Obsolete ("Cannot create a default instance")]
	public GCGamepad ();
```

## Namespace MonoTouch.GameKit

### Type Changed: MonoTouch.GameKit.GKAchievement

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKAchievementChallenge

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKAchievementDescription

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKAchievementViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKChallenge

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKGameCenterViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKLeaderboardSet

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Removed constructors:

```
public GKLeaderboardViewController (GKLeaderboardTimeScope timeScope, GKLeaderboardPlayerScope playerScope);
```

Added constructors:

```
[Obsolete ("Apple never shipped the `initWithTimeScope:playerScope:` selector. Use the default constructor.")]
	public GKLeaderboardViewController (GKLeaderboardTimeScope timeScope, GKLeaderboardPlayerScope playerScope);
```

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKLocalPlayer

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKMatchmakerViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKPlayer

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKScore

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKScoreChallenge

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.GLKit

### Type Changed: MonoTouch.GLKit.GLKTextureInfo

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.GLKit.GLKView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.GLKit.GLKViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.iAd

### Type Changed: MonoTouch.iAd.ADBannerView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.MapKit

### Type Changed: MonoTouch.MapKit.IMKLocalSearchRequest

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.MapKit.MKAnnotationView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MapKit.MKCircleView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MapKit.MKDistanceFormatter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MapKit.MKLocalSearchRequest

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MapKit.MKMapCamera

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MapKit.MKMapSnapshotOptions

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MapKit.MKMapView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MapKit.MKOverlayPathRenderer

Added constructors:

```
public MKOverlayPathRenderer (IMKOverlay overlay);
```

### Type Changed: MonoTouch.MapKit.MKOverlayPathView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MapKit.MKOverlayView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MapKit.MKPlacemark

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MapKit.MKPolygonView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MapKit.MKPolylineView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MapKit.MKUserTrackingBarButtonItem

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.MediaPlayer

### Type Changed: MonoTouch.MediaPlayer.MPMediaItem

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaItemCollection

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaLibrary

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaPickerController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaPlaylist

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaPredicate

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaPropertyPredicate

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaQuery

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MediaPlayer.MPMediaQuerySection

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MediaPlayer.MPMovieAccessLog

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MediaPlayer.MPMovieAccessLogEvent

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MediaPlayer.MPMovieErrorLog

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MediaPlayer.MPMovieErrorLogEvent

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MediaPlayer.MPVolumeView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.MessageUI

### Type Changed: MonoTouch.MessageUI.MFMailComposeViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.MultipeerConnectivity

### Type Changed: MonoTouch.MultipeerConnectivity.IMCSessionDelegate

Removed methods:

```
public virtual void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID formPeer, MonoTouch.Foundation.NSUrl localUrl, MonoTouch.Foundation.NSError& error);
```

Added methods:

```
public virtual void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, MonoTouch.Foundation.NSUrl localUrl, MonoTouch.Foundation.NSError error);
```

### Type Changed: MonoTouch.MultipeerConnectivity.MCBrowserViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.MultipeerConnectivity.MCPeerID

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.MultipeerConnectivity.MCSessionDelegate

Removed methods:

```
public virtual void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID formPeer, MonoTouch.Foundation.NSUrl localUrl, MonoTouch.Foundation.NSError& error);
```

Added methods:

```
public virtual void DidFinishReceivingResource (MCSession session, string resourceName, MCPeerID fromPeer, MonoTouch.Foundation.NSUrl localUrl, MonoTouch.Foundation.NSError error);
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Dlfcn

Added methods:

```
public static System.Drawing.SizeF GetCGSize (System.IntPtr handle, string symbol);
	public static void SetCGSize (System.IntPtr handle, string symbol, System.Drawing.SizeF value);
```

### Type Changed: MonoTouch.ObjCRuntime.LinkTarget

Added values:

```
Arm64 = 32,
	Simulator64 = 64,
```

### Type Changed: MonoTouch.ObjCRuntime.LionAttribute

Added methods:

```
public override string ToString ();
```

### Type Changed: MonoTouch.ObjCRuntime.MountainLionAttribute

Added methods:

```
public override string ToString ();
```

### Type Changed: MonoTouch.ObjCRuntime.SinceAttribute

Added methods:

```
public override string ToString ();
```

### New Type MonoTouch.ObjCRuntime.AvailabilityAttribute

```
public class AvailabilityAttribute : System.Attribute {
	// constructors
	public AvailabilityAttribute ();
	public AvailabilityAttribute (Platform introduced, Platform deprecated, Platform obsoleted, Platform unavailable);
	// properties
	public bool AlwaysAvailable { get; }
	public Platform Deprecated { get; set; }
	public Platform Introduced { get; set; }
	public string Message { get; set; }
	public Platform Obsoleted { get; set; }
	public Platform Unavailable { get; set; }
	// methods
	public static AvailabilityAttribute Get (System.Reflection.MemberInfo member);
	public static AvailabilityAttribute Merge (System.Collections.Generic.IEnumerable<object> attrs);
	public override string ToString ();
}
```

### New Type MonoTouch.ObjCRuntime.MavericksAttribute

```
public sealed class MavericksAttribute : MonoTouch.ObjCRuntime.AvailabilityAttribute {
	// constructors
	public MavericksAttribute ();
	// methods
	public override string ToString ();
}
```

### New Type MonoTouch.ObjCRuntime.NativeAttribute

```
public sealed class NativeAttribute : System.Attribute {
	// constructors
	public NativeAttribute ();
}
```

### New Type MonoTouch.ObjCRuntime.Platform

```
[Serializable]
[Flags]
public enum Platform {
	iOS = 4294967295,
	iOS_2_0 = 131072,
	iOS_3_0 = 196608,
	iOS_3_2 = 197120,
	iOS_4_0 = 262144,
	iOS_4_1 = 262400,
	iOS_4_2 = 262656,
	iOS_4_3 = 262912,
	iOS_5_0 = 327680,
	iOS_5_1 = 327936,
	iOS_6_0 = 393216,
	iOS_6_1 = 393472,
	iOS_7_0 = 458752,
	Mac = 18446744069414584320,
	Mac_10_6 = 2821346836873216,
	Mac_10_7 = 2822446348500992,
	Mac_10_8 = 2823545860128768,
	Mac_10_9 = 2824645371756544,
	None = 0,
}
```

### New Type MonoTouch.ObjCRuntime.PlatformHelper

```
public static class PlatformHelper {
	// methods
	public static int CompareIos (Platform a, Platform b);
	public static int CompareMac (Platform a, Platform b);
	public static Platform GetHostApiPlatform ();
	public static bool IsIos (Platform platform);
	public static bool IsMac (Platform platform);
	public static bool IsValid (Platform platform);
	public static Platform ParseApiPlatform (string productName, string productVersion);
	public static Platform ToIos (Platform platform);
	public static Platform ToMac (Platform platform);
}
```

## Namespace MonoTouch.PassKit

### Type Changed: MonoTouch.PassKit.PKAddPassesViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.PassKit.PKPass

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

## Namespace MonoTouch.QuickLook

### Type Changed: MonoTouch.QuickLook.QLPreviewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.Security

### Type Changed: MonoTouch.Security.SecCertificate

Added constructors:

```
public SecCertificate (System.IntPtr handle);
```

Added methods:

```
public System.Security.Cryptography.X509Certificates.X509Certificate ToX509Certificate ();
	public System.Security.Cryptography.X509Certificates.X509Certificate2 ToX509Certificate2 ();
```

### Type Changed: MonoTouch.Security.SecPolicy

Added constructors:

```
public SecPolicy (System.IntPtr handle);
```

### Type Changed: MonoTouch.Security.SecTrust

Added constructors:

```
public SecTrust (System.IntPtr handle);
```

## Namespace MonoTouch.Social

### Type Changed: MonoTouch.Social.SLComposeViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKAction

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.SpriteKit.SKCropNode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKEffectNode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKEmitterNode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKKeyframeSequence

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.SpriteKit.SKLabelNode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKNode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsBody

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsJoint

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsJointFixed

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsJointLimit

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsJointPin

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsJointSliding

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsJointSpring

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsWorld

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKScene

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKShapeNode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKSpriteNode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKTexture

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.SpriteKit.SKTextureAtlas

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKVideoNode

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.SpriteKit.SKView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.StoreKit

### Type Changed: MonoTouch.StoreKit.SKMutablePayment

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

Removed methods:

```
public static SKMutablePayment PaymentWithProduct (string identifier);
```

Added methods:

```
[Obsolete ("Deprecated in iOS 5.0. Use PaymentWithProduct(SKProduct) after fetching the list of available products from SKProductRequest")]
	public static SKMutablePayment PaymentWithProduct (string identifier);
```

### Type Changed: MonoTouch.StoreKit.SKPayment

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.StoreKit.SKStoreProductViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.Twitter

### Type Changed: MonoTouch.Twitter.TWTweetComposeViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

## Namespace MonoTouch.UIKit

### Type Changed: MonoTouch.UIKit.NSLayoutConstraint

Added methods:

```
public static NSLayoutConstraint Create (MonoTouch.ObjCRuntime.INativeObject view1, NSLayoutAttribute attribute1, NSLayoutRelation relation, MonoTouch.ObjCRuntime.INativeObject view2, NSLayoutAttribute attribute2, float multiplier, float constant);
```

### Type Changed: MonoTouch.UIKit.NSLayoutManager

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.NSMutableParagraphStyle

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.NSParagraphStyle

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
	public virtual MonoTouch.Foundation.NSObject MutableCopy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.NSShadow

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.NSTextAttachment

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.NSTextContainer

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.NSTextStorage

Added interfaces:

```
MonoTouch.Foundation.INSMutableCopying
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.NSTextTab

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UIActionSheet

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIActivityIndicatorView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIActivityViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIAlertView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate

Removed methods:

```
public virtual bool HandleOpenURL (UIApplication application, MonoTouch.Foundation.NSUrl url);
```

Added methods:

```
[Obsolete ("Override 'OpenUrl' instead on iOS 4.2+. The later will be called if both are implemented.")]
	public virtual bool HandleOpenURL (UIApplication application, MonoTouch.Foundation.NSUrl url);
```

### Type Changed: MonoTouch.UIKit.UIApplicationDelegate_Extensions

Removed methods:

```
public static bool HandleOpenURL (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSUrl url);
```

Added methods:

```
[Obsolete ("Override 'OpenUrl' instead on iOS 4.2+. The later will be called if both are implemented.")]
	public static bool HandleOpenURL (IUIApplicationDelegate This, UIApplication application, MonoTouch.Foundation.NSUrl url);
```

### Type Changed: MonoTouch.UIKit.UIBarButtonItem

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIBezierPath

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UIButton

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UICollectionReusableView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UICollectionView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UICollectionViewCell

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UICollectionViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UICollectionViewFlowLayout

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UICollectionViewLayout

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UICollectionViewLayoutAttributes

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UICollectionViewTransitionLayout

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIColor

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UIControl

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIDatePicker

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIFont

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UIFontDescriptor

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UIImage

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIImagePickerController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIImageView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIInputView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIInterpolatingMotionEffect

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIKeyCommand

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UILabel

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UILocalNotification

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UIMarkupTextPrintFormatter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.UIKit.UIMotionEffect

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UIMotionEffectGroup

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UINavigationBar

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UINavigationController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UINavigationItem

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIPageControl

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIPageViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIPickerView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIPopoverBackgroundView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIPrintFormatter

Removed constructors:

```
public UIPrintFormatter (string text);
	public UIPrintFormatter (MonoTouch.Foundation.NSAttributedString attributedText);
```

Added constructors:

```
[Obsolete ("This cannot be directly created. Use UISimpleTextPrintFormatter instead.")]
	public UIPrintFormatter (string text);

	[Obsolete ("This cannot be directly created. Use UISimpleTextPrintFormatter instead.")]
	public UIPrintFormatter (MonoTouch.Foundation.NSAttributedString attributedText);
```

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

Removed properties:

```
public virtual MonoTouch.Foundation.NSAttributedString AttributedText { get; set; }
```

Added properties:

```
[Obsolete ("This cannot be used directly. Use UISimpleTextPrintFormatter instead.")]
	public virtual MonoTouch.Foundation.NSAttributedString AttributedText { get; set; }
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UIPrintInfo

Added interfaces:

```
MonoTouch.Foundation.INSCopying
	MonoTouch.Foundation.INSCoding
```

Added methods:

```
public virtual MonoTouch.Foundation.NSObject Copy (MonoTouch.Foundation.NSZone zone);
```

### Type Changed: MonoTouch.UIKit.UIProgressView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIReferenceLibraryViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIRefreshControl

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIScrollView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UISearchBar

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

Added properties:

```
public virtual UITextSpellCheckingType SpellCheckingType { get; set; }
```

### Type Changed: MonoTouch.UIKit.UISegmentedControl

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UISimpleTextPrintFormatter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.UIKit.UISlider

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UISplitViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIStepper

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UISwitch

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UITabBar

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UITabBarController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UITableView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UITableViewCell

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UITableViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UITableViewHeaderFooterView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UITextField

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UITextInputMode

Added interfaces:

```
MonoTouch.Foundation.INSSecureCoding
	MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UITextView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIToolbar

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIVideoEditorController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIViewPrintFormatter

Added interfaces:

```
MonoTouch.Foundation.INSCopying
```

### Type Changed: MonoTouch.UIKit.UIWebView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.UIKit.UIWindow

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### New Type MonoTouch.UIKit.UIWindowLevel

```
public static class UIWindowLevel {
	// properties
	public static float Alert { get; }
	public static float Normal { get; }
	public static float StatusBar { get; }
}
```

   


 <hr>

# mscorlib.dll

## New Namespace System.Runtime.InteropServices.WindowsRuntime

### New Type System.Runtime.InteropServices.WindowsRuntime.DefaultInterfaceAttribute

```
public sealed class DefaultInterfaceAttribute : System.Attribute {
	// constructors
	public DefaultInterfaceAttribute (System.Type defaultInterface);
	// properties
	public System.Type DefaultInterface { get; }
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.DesignerNamespaceResolveEventArgs

```
public class DesignerNamespaceResolveEventArgs : System.EventArgs {
	// constructors
	public DesignerNamespaceResolveEventArgs (string namespaceName);
	// properties
	public string NamespaceName { get; }
	public System.Collections.ObjectModel.Collection<string> ResolvedAssemblyFiles { get; }
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.EventRegistrationToken

```
public struct EventRegistrationToken {
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (EventRegistrationToken left, EventRegistrationToken right);
	public static bool op_Inequality (EventRegistrationToken left, EventRegistrationToken right);
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.EventRegistrationTokenTable`1

```
public sealed class EventRegistrationTokenTable`1 {
	// constructors
	public EventRegistrationTokenTable`1 ();
	// properties
	public T InvocationList { get; set; }
	// methods
	public EventRegistrationToken AddEventHandler (T handler);
	public static System.Runtime.InteropServices.WindowsRuntime.EventRegistrationTokenTable<T> GetOrCreateEventRegistrationTokenTable (System.Runtime.InteropServices.WindowsRuntime.EventRegistrationTokenTable<T> refEventTable);
	public void RemoveEventHandler (T handler);
	public void RemoveEventHandler (EventRegistrationToken token);
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.IActivationFactory

```
public interface IActivationFactory {
	// methods
	public virtual object ActivateInstance ();
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.InterfaceImplementedInVersionAttribute

```
public sealed class InterfaceImplementedInVersionAttribute : System.Attribute {
	// constructors
	public InterfaceImplementedInVersionAttribute (System.Type interfaceType, byte majorVersion, byte minorVersion, byte buildVersion, byte revisionVersion);
	// properties
	public byte BuildVersion { get; }
	public System.Type InterfaceType { get; }
	public byte MajorVersion { get; }
	public byte MinorVersion { get; }
	public byte RevisionVersion { get; }
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.NamespaceResolveEventArgs

```
public class NamespaceResolveEventArgs : System.EventArgs {
	// constructors
	public NamespaceResolveEventArgs (string namespaceName, System.Reflection.Assembly requestingAssembly);
	// properties
	public string NamespaceName { get; }
	public System.Reflection.Assembly RequestingAssembly { get; }
	public System.Collections.ObjectModel.Collection<System.Reflection.Assembly> ResolvedAssemblies { get; }
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.ReadOnlyArrayAttribute

```
public sealed class ReadOnlyArrayAttribute : System.Attribute {
	// constructors
	public ReadOnlyArrayAttribute ();
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.ReturnValueNameAttribute

```
public sealed class ReturnValueNameAttribute : System.Attribute {
	// constructors
	public ReturnValueNameAttribute (string name);
	// properties
	public string Name { get; }
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.WindowsRuntimeMarshal

```
public static class WindowsRuntimeMarshal {
	// methods
	public static void AddEventHandler<T> (System.Func<T,System.Runtime.InteropServices.WindowsRuntime.EventRegistrationToken> addMethod, System.Action<EventRegistrationToken> removeMethod, T handler);
	public static void FreeHString (System.IntPtr ptr);
	public static IActivationFactory GetActivationFactory (System.Type type);
	public static string PtrToStringHString (System.IntPtr ptr);
	public static void RemoveAllEventHandlers (System.Action<EventRegistrationToken> removeMethod);
	public static void RemoveEventHandler<T> (System.Action<EventRegistrationToken> removeMethod, T handler);
	public static System.IntPtr StringToHString (string s);
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.WindowsRuntimeMetadata

```
public static class WindowsRuntimeMetadata {
	// events
	public event System.EventHandler<DesignerNamespaceResolveEventArgs> DesignerNamespaceResolve;
	public event System.EventHandler<NamespaceResolveEventArgs> ReflectionOnlyNamespaceResolve;
	// methods
	public static System.Collections.Generic.IEnumerable<string> ResolveNamespace (string namespaceName, System.Collections.Generic.IEnumerable<string> packageGraphFilePaths);
	public static System.Collections.Generic.IEnumerable<string> ResolveNamespace (string namespaceName, string windowsSdkFilePath, System.Collections.Generic.IEnumerable<string> packageGraphFilePaths);
}
```

### New Type System.Runtime.InteropServices.WindowsRuntime.WriteOnlyArrayAttribute

```
public sealed class WriteOnlyArrayAttribute : System.Attribute {
	// constructors
	public WriteOnlyArrayAttribute ();
}
```

   


 <hr>

# System.dll

## Namespace System.Collections.Specialized

### New Type System.Collections.Specialized.IOrderedDictionary

```
public interface IOrderedDictionary : System.Collections.IDictionary, System.Collections.ICollection, System.Collections.IEnumerable {
	// properties
	public virtual object Item { get; set; }
	// methods
	public virtual System.Collections.IDictionaryEnumerator GetEnumerator ();
	public virtual void Insert (int index, object key, object value);
	public virtual void RemoveAt (int index);
}
```

### New Type System.Collections.Specialized.OrderedDictionary

```
[Serializable]
public class OrderedDictionary : IOrderedDictionary, System.Collections.IDictionary, System.Collections.ICollection, System.Collections.IEnumerable, System.Runtime.Serialization.ISerializable, System.Runtime.Serialization.IDeserializationCallback {
	// constructors
	public OrderedDictionary ();
	public OrderedDictionary (int capacity);
	public OrderedDictionary (System.Collections.IEqualityComparer comparer);
	public OrderedDictionary (int capacity, System.Collections.IEqualityComparer comparer);
	protected OrderedDictionary (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
	// properties
	public virtual int Count { get; }
	public virtual bool IsReadOnly { get; }
	public virtual object Item { get; set; }
	public virtual object Item { get; set; }
	public virtual System.Collections.ICollection Keys { get; }
	public virtual System.Collections.ICollection Values { get; }
	// methods
	public virtual void Add (object key, object value);
	public OrderedDictionary AsReadOnly ();
	public virtual void Clear ();
	public virtual bool Contains (object key);
	public virtual void CopyTo (System.Array array, int index);
	public virtual System.Collections.IDictionaryEnumerator GetEnumerator ();
	public virtual void GetObjectData (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
	public virtual void Insert (int index, object key, object value);
	protected virtual void OnDeserialization (object sender);
	public virtual void Remove (object key);
	public virtual void RemoveAt (int index);
}
```

## Namespace System.ComponentModel

### New Type System.ComponentModel.AmbientValueAttribute

```
public sealed class AmbientValueAttribute : System.Attribute {
	// constructors
	public AmbientValueAttribute (bool value);
	public AmbientValueAttribute (string value);
	public AmbientValueAttribute (float value);
	public AmbientValueAttribute (object value);
	public AmbientValueAttribute (long value);
	public AmbientValueAttribute (int value);
	public AmbientValueAttribute (short value);
	public AmbientValueAttribute (double value);
	public AmbientValueAttribute (char value);
	public AmbientValueAttribute (byte value);
	public AmbientValueAttribute (System.Type type, string value);
	// properties
	public object Value { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
}
```

### New Type System.ComponentModel.AttributeProviderAttribute

```
public class AttributeProviderAttribute : System.Attribute {
	// constructors
	public AttributeProviderAttribute (System.Type type);
	public AttributeProviderAttribute (string typeName, string propertyName);
	public AttributeProviderAttribute (string typeName);
	// properties
	public string PropertyName { get; }
	public string TypeName { get; }
}
```

### New Type System.ComponentModel.CancelEventHandler

```
public sealed delegate CancelEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CancelEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (object sender, CancelEventArgs e, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (object sender, CancelEventArgs e);
}
```

### New Type System.ComponentModel.ComplexBindingPropertiesAttribute

```
public sealed class ComplexBindingPropertiesAttribute : System.Attribute {
	// constructors
	public ComplexBindingPropertiesAttribute (string dataSource, string dataMember);
	public ComplexBindingPropertiesAttribute (string dataSource);
	public ComplexBindingPropertiesAttribute ();
	// fields
	public static ComplexBindingPropertiesAttribute Default;
	// properties
	public string DataMember { get; }
	public string DataSource { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
}
```

### New Type System.ComponentModel.ComponentEditor

```
public abstract class ComponentEditor {
	// constructors
	protected ComponentEditor ();
	// methods
	public bool EditComponent (object component);
	public virtual bool EditComponent (ITypeDescriptorContext context, object component);
}
```

### New Type System.ComponentModel.ComponentResourceManager

```
public class ComponentResourceManager : System.Resources.ResourceManager {
	// constructors
	public ComponentResourceManager ();
	public ComponentResourceManager (System.Type t);
	// methods
	public void ApplyResources (object value, string objectName);
	public virtual void ApplyResources (object value, string objectName, System.Globalization.CultureInfo culture);
}
```

### New Type System.ComponentModel.Container

```
public class Container : IContainer, System.IDisposable {
	// constructors
	public Container ();
	// properties
	public virtual ComponentCollection Components { get; }
	// methods
	protected override void ~Container ();
	public virtual void Add (IComponent component);
	public virtual void Add (IComponent component, string name);
	protected virtual ISite CreateSite (IComponent component, string name);
	protected virtual void Dispose (bool disposing);
	public virtual void Dispose ();
	protected virtual object GetService (System.Type service);
	public virtual void Remove (IComponent component);
	protected void RemoveWithoutUnsiting (IComponent component);
	protected virtual void ValidateName (IComponent component, string name);
}
```

### New Type System.ComponentModel.ContainerFilterService

```
public abstract class ContainerFilterService {
	// constructors
	protected ContainerFilterService ();
	// methods
	public virtual ComponentCollection FilterComponents (ComponentCollection components);
}
```

### New Type System.ComponentModel.DataObjectAttribute

```
public sealed class DataObjectAttribute : System.Attribute {
	// constructors
	public DataObjectAttribute ();
	public DataObjectAttribute (bool isDataObject);
	// fields
	public static DataObjectAttribute DataObject;
	public static DataObjectAttribute Default;
	public static DataObjectAttribute NonDataObject;
	// properties
	public bool IsDataObject { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public override bool IsDefaultAttribute ();
}
```

### New Type System.ComponentModel.DataObjectFieldAttribute

```
public sealed class DataObjectFieldAttribute : System.Attribute {
	// constructors
	public DataObjectFieldAttribute (bool primaryKey);
	public DataObjectFieldAttribute (bool primaryKey, bool isIdentity);
	public DataObjectFieldAttribute (bool primaryKey, bool isIdentity, bool isNullable);
	public DataObjectFieldAttribute (bool primaryKey, bool isIdentity, bool isNullable, int length);
	// properties
	public bool IsIdentity { get; }
	public bool IsNullable { get; }
	public int Length { get; }
	public bool PrimaryKey { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
}
```

### New Type System.ComponentModel.DataObjectMethodAttribute

```
public sealed class DataObjectMethodAttribute : System.Attribute {
	// constructors
	public DataObjectMethodAttribute (DataObjectMethodType methodType);
	public DataObjectMethodAttribute (DataObjectMethodType methodType, bool isDefault);
	// properties
	public bool IsDefault { get; }
	public DataObjectMethodType MethodType { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public override bool Match (object obj);
}
```

### New Type System.ComponentModel.DataObjectMethodType

```
[Serializable]
public enum DataObjectMethodType {
	Delete = 4,
	Fill = 0,
	Insert = 3,
	Select = 1,
	Update = 2,
}
```

### New Type System.ComponentModel.DateTimeOffsetConverter

```
public class DateTimeOffsetConverter : System.ComponentModel.TypeConverter {
	// constructors
	public DateTimeOffsetConverter ();
	// methods
	public override bool CanConvertFrom (ITypeDescriptorContext context, System.Type sourceType);
	public override bool CanConvertTo (ITypeDescriptorContext context, System.Type destinationType);
	public override object ConvertFrom (ITypeDescriptorContext context, System.Globalization.CultureInfo culture, object value);
	public override object ConvertTo (ITypeDescriptorContext context, System.Globalization.CultureInfo culture, object value, System.Type destinationType);
}
```

### New Type System.ComponentModel.DefaultBindingPropertyAttribute

```
public sealed class DefaultBindingPropertyAttribute : System.Attribute {
	// constructors
	public DefaultBindingPropertyAttribute ();
	public DefaultBindingPropertyAttribute (string name);
	// fields
	public static DefaultBindingPropertyAttribute Default;
	// properties
	public string Name { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
}
```

### New Type System.ComponentModel.ExtenderProvidedPropertyAttribute

```
public sealed class ExtenderProvidedPropertyAttribute : System.Attribute {
	// constructors
	public ExtenderProvidedPropertyAttribute ();
	// properties
	public PropertyDescriptor ExtenderProperty { get; }
	public IExtenderProvider Provider { get; }
	public System.Type ReceiverType { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public override bool IsDefaultAttribute ();
}
```

### New Type System.ComponentModel.HandledEventArgs

```
public class HandledEventArgs : System.EventArgs {
	// constructors
	public HandledEventArgs ();
	public HandledEventArgs (bool defaultHandledValue);
	// properties
	public bool Handled { get; set; }
}
```

### New Type System.ComponentModel.HandledEventHandler

```
public sealed delegate HandledEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public HandledEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (object sender, HandledEventArgs e, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (object sender, HandledEventArgs e);
}
```

### New Type System.ComponentModel.IIntellisenseBuilder

```
public interface IIntellisenseBuilder {
	// properties
	public virtual string Name { get; }
	// methods
	public virtual bool Show (string language, string value, System.String& newValue);
}
```

### New Type System.ComponentModel.ImmutableObjectAttribute

```
public sealed class ImmutableObjectAttribute : System.Attribute {
	// constructors
	public ImmutableObjectAttribute (bool immutable);
	// fields
	public static ImmutableObjectAttribute Default;
	public static ImmutableObjectAttribute No;
	public static ImmutableObjectAttribute Yes;
	// properties
	public bool Immutable { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public override bool IsDefaultAttribute ();
}
```

### New Type System.ComponentModel.INestedContainer

```
public interface INestedContainer : IContainer, System.IDisposable {
	// properties
	public virtual IComponent Owner { get; }
}
```

### New Type System.ComponentModel.INestedSite

```
public interface INestedSite : ISite, System.IServiceProvider {
	// properties
	public virtual string FullName { get; }
}
```

### New Type System.ComponentModel.InheritanceAttribute

```
public sealed class InheritanceAttribute : System.Attribute {
	// constructors
	public InheritanceAttribute ();
	public InheritanceAttribute (InheritanceLevel inheritanceLevel);
	// fields
	public static InheritanceAttribute Default;
	public static InheritanceAttribute Inherited;
	public static InheritanceAttribute InheritedReadOnly;
	public static InheritanceAttribute NotInherited;
	// properties
	public InheritanceLevel InheritanceLevel { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public override bool IsDefaultAttribute ();
	public override string ToString ();
}
```

### New Type System.ComponentModel.InheritanceLevel

```
[Serializable]
public enum InheritanceLevel {
	Inherited = 1,
	InheritedReadOnly = 2,
	NotInherited = 3,
}
```

### New Type System.ComponentModel.InitializationEventAttribute

```
public sealed class InitializationEventAttribute : System.Attribute {
	// constructors
	public InitializationEventAttribute (string eventName);
	// properties
	public string EventName { get; }
}
```

### New Type System.ComponentModel.InstallerTypeAttribute

```
public class InstallerTypeAttribute : System.Attribute {
	// constructors
	public InstallerTypeAttribute (string typeName);
	public InstallerTypeAttribute (System.Type installerType);
	// properties
	public virtual System.Type InstallerType { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
}
```

### New Type System.ComponentModel.InstanceCreationEditor

```
public abstract class InstanceCreationEditor {
	// constructors
	protected InstanceCreationEditor ();
	// properties
	public virtual string Text { get; }
	// methods
	public virtual object CreateInstance (ITypeDescriptorContext context, System.Type type);
}
```

### New Type System.ComponentModel.InvalidAsynchronousStateException

```
[Serializable]
public class InvalidAsynchronousStateException : System.ArgumentException, System.Runtime.Serialization.ISerializable {
	// constructors
	public InvalidAsynchronousStateException ();
	public InvalidAsynchronousStateException (string message);
	public InvalidAsynchronousStateException (string message, System.Exception innerException);
	protected InvalidAsynchronousStateException (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
}
```

### New Type System.ComponentModel.LookupBindingPropertiesAttribute

```
public sealed class LookupBindingPropertiesAttribute : System.Attribute {
	// constructors
	public LookupBindingPropertiesAttribute (string dataSource, string displayMember, string valueMember, string lookupMember);
	public LookupBindingPropertiesAttribute ();
	// fields
	public static LookupBindingPropertiesAttribute Default;
	// properties
	public string DataSource { get; }
	public string DisplayMember { get; }
	public string LookupMember { get; }
	public string ValueMember { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
}
```

### New Type System.ComponentModel.MaskedTextProvider

```
public class MaskedTextProvider : System.ICloneable {
	// constructors
	public MaskedTextProvider (string mask);
	public MaskedTextProvider (string mask, bool restrictToAscii);
	public MaskedTextProvider (string mask, System.Globalization.CultureInfo culture);
	public MaskedTextProvider (string mask, char passwordChar, bool allowPromptAsInput);
	public MaskedTextProvider (string mask, System.Globalization.CultureInfo culture, bool restrictToAscii);
	public MaskedTextProvider (string mask, System.Globalization.CultureInfo culture, char passwordChar, bool allowPromptAsInput);
	public MaskedTextProvider (string mask, System.Globalization.CultureInfo culture, bool allowPromptAsInput, char promptChar, char passwordChar, bool restrictToAscii);
	// properties
	public bool AllowPromptAsInput { get; }
	public bool AsciiOnly { get; }
	public int AssignedEditPositionCount { get; }
	public int AvailableEditPositionCount { get; }
	public System.Globalization.CultureInfo Culture { get; }
	public static char DefaultPasswordChar { get; }
	public int EditPositionCount { get; }
	public System.Collections.IEnumerator EditPositions { get; }
	public bool IncludeLiterals { get; set; }
	public bool IncludePrompt { get; set; }
	public static int InvalidIndex { get; }
	public bool IsPassword { get; set; }
	public char Item { get; }
	public int LastAssignedPosition { get; }
	public int Length { get; }
	public string Mask { get; }
	public bool MaskCompleted { get; }
	public bool MaskFull { get; }
	public char PasswordChar { get; set; }
	public char PromptChar { get; set; }
	public bool ResetOnPrompt { get; set; }
	public bool ResetOnSpace { get; set; }
	public bool SkipLiterals { get; set; }
	// methods
	public bool Add (char input);
	public bool Add (string input);
	public bool Add (char input, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool Add (string input, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public void Clear ();
	public void Clear (MaskedTextResultHint& resultHint);
	public virtual object Clone ();
	public int FindAssignedEditPositionFrom (int position, bool direction);
	public int FindAssignedEditPositionInRange (int startPosition, int endPosition, bool direction);
	public int FindEditPositionFrom (int position, bool direction);
	public int FindEditPositionInRange (int startPosition, int endPosition, bool direction);
	public int FindNonEditPositionFrom (int position, bool direction);
	public int FindNonEditPositionInRange (int startPosition, int endPosition, bool direction);
	public int FindUnassignedEditPositionFrom (int position, bool direction);
	public int FindUnassignedEditPositionInRange (int startPosition, int endPosition, bool direction);
	public static bool GetOperationResultFromHint (MaskedTextResultHint hint);
	public bool InsertAt (string input, int position, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool InsertAt (char input, int position, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool InsertAt (string input, int position);
	public bool InsertAt (char input, int position);
	public bool IsAvailablePosition (int position);
	public bool IsEditPosition (int position);
	public static bool IsValidInputChar (char c);
	public static bool IsValidMaskChar (char c);
	public static bool IsValidPasswordChar (char c);
	public bool Remove ();
	public bool Remove (System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool RemoveAt (int startPosition, int endPosition, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool RemoveAt (int startPosition, int endPosition);
	public bool RemoveAt (int position);
	public bool Replace (string input, int startPosition, int endPosition, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool Replace (char input, int startPosition, int endPosition, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool Replace (string input, int position, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool Replace (char input, int position, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool Replace (string input, int position);
	public bool Replace (char input, int position);
	public bool Set (string input, System.Int32& testPosition, MaskedTextResultHint& resultHint);
	public bool Set (string input);
	public string ToDisplayString ();
	public string ToString (bool ignorePasswordChar, bool includePrompt, bool includeLiterals, int startPosition, int length);
	public string ToString (bool includePrompt, bool includeLiterals, int startPosition, int length);
	public string ToString (bool ignorePasswordChar, int startPosition, int length);
	public string ToString (int startPosition, int length);
	public override string ToString ();
	public string ToString (bool ignorePasswordChar);
	public string ToString (bool includePrompt, bool includeLiterals);
	public bool VerifyChar (char input, int position, MaskedTextResultHint& hint);
	public bool VerifyEscapeChar (char input, int position);
	public bool VerifyString (string input);
	public bool VerifyString (string input, System.Int32& testPosition, MaskedTextResultHint& resultHint);
}
```

### New Type System.ComponentModel.MaskedTextResultHint

```
[Serializable]
public enum MaskedTextResultHint {
	AlphanumericCharacterExpected = -2,
	AsciiCharacterExpected = -1,
	CharacterEscaped = 1,
	DigitExpected = -3,
	InvalidInput = -51,
	LetterExpected = -4,
	NoEffect = 2,
	NonEditPosition = -54,
	PositionOutOfRange = -55,
	PromptCharNotAllowed = -52,
	SideEffect = 3,
	SignedDigitExpected = -5,
	Success = 4,
	UnavailableEditPosition = -53,
	Unknown = 0,
}
```

### New Type System.ComponentModel.NestedContainer

```
public class NestedContainer : System.ComponentModel.Container, INestedContainer, IContainer, System.IDisposable {
	// constructors
	public NestedContainer (IComponent owner);
	// properties
	public virtual IComponent Owner { get; }
	protected virtual string OwnerName { get; }
	// methods
	protected override ISite CreateSite (IComponent component, string name);
	protected override void Dispose (bool disposing);
	protected override object GetService (System.Type service);
}
```

### New Type System.ComponentModel.ParenthesizePropertyNameAttribute

```
public sealed class ParenthesizePropertyNameAttribute : System.Attribute {
	// constructors
	public ParenthesizePropertyNameAttribute ();
	public ParenthesizePropertyNameAttribute (bool needParenthesis);
	// fields
	public static ParenthesizePropertyNameAttribute Default;
	// properties
	public bool NeedParenthesis { get; }
	// methods
	public override bool Equals (object o);
	public override int GetHashCode ();
	public override bool IsDefaultAttribute ();
}
```

### New Type System.ComponentModel.PropertyTabAttribute

```
public class PropertyTabAttribute : System.Attribute {
	// constructors
	public PropertyTabAttribute ();
	public PropertyTabAttribute (string tabClassName);
	public PropertyTabAttribute (System.Type tabClass);
	public PropertyTabAttribute (string tabClassName, PropertyTabScope tabScope);
	public PropertyTabAttribute (System.Type tabClass, PropertyTabScope tabScope);
	// properties
	public System.Type[] TabClasses { get; }
	protected System.String[] TabClassNames { get; }
	public PropertyTabScope[] TabScopes { get; }
	// methods
	public override bool Equals (object other);
	public bool Equals (PropertyTabAttribute other);
	public override int GetHashCode ();
	protected void InitializeArrays (System.String[] tabClassNames, PropertyTabScope[] tabScopes);
	protected void InitializeArrays (System.Type[] tabClasses, PropertyTabScope[] tabScopes);
}
```

### New Type System.ComponentModel.PropertyTabScope

```
[Serializable]
public enum PropertyTabScope {
	Component = 3,
	Document = 2,
	Global = 1,
	Static = 0,
}
```

### New Type System.ComponentModel.ProvidePropertyAttribute

```
public sealed class ProvidePropertyAttribute : System.Attribute {
	// constructors
	public ProvidePropertyAttribute (string propertyName, string receiverTypeName);
	public ProvidePropertyAttribute (string propertyName, System.Type receiverType);
	// properties
	public string PropertyName { get; }
	public string ReceiverTypeName { get; }
	public override object TypeId { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
}
```

### New Type System.ComponentModel.RunInstallerAttribute

```
public class RunInstallerAttribute : System.Attribute {
	// constructors
	public RunInstallerAttribute (bool runInstaller);
	// fields
	public static RunInstallerAttribute Default;
	public static RunInstallerAttribute No;
	public static RunInstallerAttribute Yes;
	// properties
	public bool RunInstaller { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public override bool IsDefaultAttribute ();
}
```

### New Type System.ComponentModel.SettingsBindableAttribute

```
public sealed class SettingsBindableAttribute : System.Attribute {
	// constructors
	public SettingsBindableAttribute (bool bindable);
	// fields
	public static SettingsBindableAttribute No;
	public static SettingsBindableAttribute Yes;
	// properties
	public bool Bindable { get; }
	// methods
	public override bool Equals (object obj);
	public override int GetHashCode ();
}
```

### New Type System.ComponentModel.SyntaxCheck

```
public static class SyntaxCheck {
	// methods
	public static bool CheckMachineName (string value);
	public static bool CheckPath (string value);
	public static bool CheckRootedPath (string value);
}
```

### New Type System.ComponentModel.TypeDescriptionProviderAttribute

```
public sealed class TypeDescriptionProviderAttribute : System.Attribute {
	// constructors
	public TypeDescriptionProviderAttribute (string typeName);
	public TypeDescriptionProviderAttribute (System.Type type);
	// properties
	public string TypeName { get; }
}
```

### New Type System.ComponentModel.WarningException

```
[Serializable]
public class WarningException : System.SystemException, System.Runtime.Serialization.ISerializable {
	// constructors
	public WarningException (string message);
	public WarningException (string message, string helpUrl);
	public WarningException (string message, string helpUrl, string helpTopic);
	public WarningException ();
	public WarningException (string message, System.Exception innerException);
	protected WarningException (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
	// properties
	public string HelpTopic { get; }
	public string HelpUrl { get; }
	// methods
	public override void GetObjectData (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
}
```

## Namespace System.ComponentModel.Design

### New Type System.ComponentModel.Design.ActiveDesignerEventArgs

```
public class ActiveDesignerEventArgs : System.EventArgs {
	// constructors
	public ActiveDesignerEventArgs (IDesignerHost oldDesigner, IDesignerHost newDesigner);
	// properties
	public IDesignerHost NewDesigner { get; }
	public IDesignerHost OldDesigner { get; }
}
```

### New Type System.ComponentModel.Design.ActiveDesignerEventHandler

```
public sealed delegate ActiveDesignerEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public ActiveDesignerEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (object sender, ActiveDesignerEventArgs e, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (object sender, ActiveDesignerEventArgs e);
}
```

### New Type System.ComponentModel.Design.CheckoutException

```
[Serializable]
public class CheckoutException : System.Runtime.InteropServices.ExternalException, System.Runtime.Serialization.ISerializable {
	// constructors
	public CheckoutException ();
	public CheckoutException (string message);
	public CheckoutException (string message, int errorCode);
	public CheckoutException (string message, System.Exception innerException);
	protected CheckoutException (System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context);
	// fields
	public static CheckoutException Canceled;
}
```

### New Type System.ComponentModel.Design.DesignerCollection

```
public class DesignerCollection : System.Collections.ICollection, System.Collections.IEnumerable {
	// constructors
	public DesignerCollection (IDesignerHost[] designers);
	public DesignerCollection (System.Collections.IList designers);
	// properties
	public int Count { get; }
	public virtual IDesignerHost Item { get; }
	// methods
	public System.Collections.IEnumerator GetEnumerator ();
}
```

### New Type System.ComponentModel.Design.DesignerEventArgs

```
public class DesignerEventArgs : System.EventArgs {
	// constructors
	public DesignerEventArgs (IDesignerHost host);
	// properties
	public IDesignerHost Designer { get; }
}
```

### New Type System.ComponentModel.Design.DesignerEventHandler

```
public sealed delegate DesignerEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public DesignerEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (object sender, DesignerEventArgs e, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (object sender, DesignerEventArgs e);
}
```

### New Type System.ComponentModel.Design.DesignerOptionService

```
public abstract class DesignerOptionService : IDesignerOptionService {
	// constructors
	protected DesignerOptionService ();
	// properties
	public DesignerOptionService.DesignerOptionCollection Options { get; }
	// methods
	protected DesignerOptionService.DesignerOptionCollection CreateOptionCollection (DesignerOptionService.DesignerOptionCollection parent, string name, object value);
	protected virtual void PopulateOptionCollection (DesignerOptionService.DesignerOptionCollection options);
	protected virtual bool ShowDialog (DesignerOptionService.DesignerOptionCollection options, object optionObject);

	// inner types
	public sealed class DesignerOptionCollection : System.Collections.IList, System.Collections.ICollection, System.Collections.IEnumerable {
		// properties
		public virtual int Count { get; }
		public DesignerOptionService.DesignerOptionCollection Item { get; }
		public DesignerOptionService.DesignerOptionCollection Item { get; }
		public string Name { get; }
		public DesignerOptionService.DesignerOptionCollection Parent { get; }
		public System.ComponentModel.PropertyDescriptorCollection Properties { get; }
		// methods
		public virtual void CopyTo (System.Array array, int index);
		public virtual System.Collections.IEnumerator GetEnumerator ();
		public int IndexOf (DesignerOptionService.DesignerOptionCollection item);
		public bool ShowDialog ();

		// inner types
		public sealed class WrappedPropertyDescriptor : System.ComponentModel.PropertyDescriptor {
			// constructors
			public DesignerOptionService (System.ComponentModel.PropertyDescriptor property, object component);
			// properties
			public override System.ComponentModel.AttributeCollection Attributes { get; }
			public override System.Type ComponentType { get; }
			public override bool IsReadOnly { get; }
			public override System.Type PropertyType { get; }
			// methods
			public override bool CanResetValue (object ignored);
			public override object GetValue (object ignored);
			public override void ResetValue (object ignored);
			public override void SetValue (object ignored, object value);
			public override bool ShouldSerializeValue (object ignored);
		}
	}
}
```

### New Type System.ComponentModel.Design.HelpContextType

```
[Serializable]
public enum HelpContextType {
	Ambient = 0,
	Selection = 2,
	ToolWindowSelection = 3,
	Window = 1,
}
```

### New Type System.ComponentModel.Design.HelpKeywordAttribute

```
[Serializable]
public sealed class HelpKeywordAttribute : System.Attribute {
	// constructors
	public HelpKeywordAttribute ();
	public HelpKeywordAttribute (string keyword);
	public HelpKeywordAttribute (System.Type t);
	// fields
	public static HelpKeywordAttribute Default;
	// properties
	public string HelpKeyword { get; }
	// methods
	public override bool Equals (object other);
	public override int GetHashCode ();
	public override bool IsDefaultAttribute ();
}
```

### New Type System.ComponentModel.Design.HelpKeywordType

```
[Serializable]
public enum HelpKeywordType {
	F1Keyword = 0,
	FilterKeyword = 2,
	GeneralKeyword = 1,
}
```

### New Type System.ComponentModel.Design.IComponentDiscoveryService

```
public interface IComponentDiscoveryService {
	// methods
	public virtual System.Collections.ICollection GetComponentTypes (IDesignerHost designerHost, System.Type baseType);
}
```

### New Type System.ComponentModel.Design.IComponentInitializer

```
public interface IComponentInitializer {
	// methods
	public virtual void InitializeExistingComponent (System.Collections.IDictionary defaultValues);
	public virtual void InitializeNewComponent (System.Collections.IDictionary defaultValues);
}
```

### New Type System.ComponentModel.Design.IDesignerEventService

```
public interface IDesignerEventService {
	// properties
	public virtual IDesignerHost ActiveDesigner { get; }
	public virtual DesignerCollection Designers { get; }
	// events
	public event ActiveDesignerEventHandler ActiveDesignerChanged;
	public event DesignerEventHandler DesignerCreated;
	public event DesignerEventHandler DesignerDisposed;
	public event System.EventHandler SelectionChanged;
}
```

### New Type System.ComponentModel.Design.IDesignerFilter

```
public interface IDesignerFilter {
	// methods
	public virtual void PostFilterAttributes (System.Collections.IDictionary attributes);
	public virtual void PostFilterEvents (System.Collections.IDictionary events);
	public virtual void PostFilterProperties (System.Collections.IDictionary properties);
	public virtual void PreFilterAttributes (System.Collections.IDictionary attributes);
	public virtual void PreFilterEvents (System.Collections.IDictionary events);
	public virtual void PreFilterProperties (System.Collections.IDictionary properties);
}
```

### New Type System.ComponentModel.Design.IDesignerHostTransactionState

```
public interface IDesignerHostTransactionState {
	// properties
	public virtual bool IsClosingTransaction { get; }
}
```

### New Type System.ComponentModel.Design.IDesignerOptionService

```
public interface IDesignerOptionService {
	// methods
	public virtual object GetOptionValue (string pageName, string valueName);
	public virtual void SetOptionValue (string pageName, string valueName, object value);
}
```

### New Type System.ComponentModel.Design.IDictionaryService

```
public interface IDictionaryService {
	// methods
	public virtual object GetKey (object value);
	public virtual object GetValue (object key);
	public virtual void SetValue (object key, object value);
}
```

### New Type System.ComponentModel.Design.IEventBindingService

```
public interface IEventBindingService {
	// methods
	public virtual string CreateUniqueMethodName (System.ComponentModel.IComponent component, System.ComponentModel.EventDescriptor e);
	public virtual System.Collections.ICollection GetCompatibleMethods (System.ComponentModel.EventDescriptor e);
	public virtual System.ComponentModel.EventDescriptor GetEvent (System.ComponentModel.PropertyDescriptor property);
	public virtual System.ComponentModel.PropertyDescriptorCollection GetEventProperties (System.ComponentModel.EventDescriptorCollection events);
	public virtual System.ComponentModel.PropertyDescriptor GetEventProperty (System.ComponentModel.EventDescriptor e);
	public virtual bool ShowCode ();
	public virtual bool ShowCode (int lineNumber);
	public virtual bool ShowCode (System.ComponentModel.IComponent component, System.ComponentModel.EventDescriptor e);
}
```

### New Type System.ComponentModel.Design.IExtenderListService

```
public interface IExtenderListService {
	// methods
	public virtual System.ComponentModel.IExtenderProvider[] GetExtenderProviders ();
}
```

### New Type System.ComponentModel.Design.IExtenderProviderService

```
public interface IExtenderProviderService {
	// methods
	public virtual void AddExtenderProvider (System.ComponentModel.IExtenderProvider provider);
	public virtual void RemoveExtenderProvider (System.ComponentModel.IExtenderProvider provider);
}
```

### New Type System.ComponentModel.Design.IHelpService

```
public interface IHelpService {
	// methods
	public virtual void AddContextAttribute (string name, string value, HelpKeywordType keywordType);
	public virtual void ClearContextAttributes ();
	public virtual IHelpService CreateLocalContext (HelpContextType contextType);
	public virtual void RemoveContextAttribute (string name, string value);
	public virtual void RemoveLocalContext (IHelpService localContext);
	public virtual void ShowHelpFromKeyword (string helpKeyword);
	public virtual void ShowHelpFromUrl (string helpUrl);
}
```

### New Type System.ComponentModel.Design.IInheritanceService

```
public interface IInheritanceService {
	// methods
	public virtual void AddInheritedComponents (System.ComponentModel.IComponent component, System.ComponentModel.IContainer container);
	public virtual System.ComponentModel.InheritanceAttribute GetInheritanceAttribute (System.ComponentModel.IComponent component);
}
```

### New Type System.ComponentModel.Design.IMenuCommandService

```
public interface IMenuCommandService {
	// properties
	public virtual DesignerVerbCollection Verbs { get; }
	// methods
	public virtual void AddCommand (MenuCommand command);
	public virtual void AddVerb (DesignerVerb verb);
	public virtual MenuCommand FindCommand (CommandID commandID);
	public virtual bool GlobalInvoke (CommandID commandID);
	public virtual void RemoveCommand (MenuCommand command);
	public virtual void RemoveVerb (DesignerVerb verb);
	public virtual void ShowContextMenu (CommandID menuID, int x, int y);
}
```

### New Type System.ComponentModel.Design.IResourceService

```
public interface IResourceService {
	// methods
	public virtual System.Resources.IResourceReader GetResourceReader (System.Globalization.CultureInfo info);
	public virtual System.Resources.IResourceWriter GetResourceWriter (System.Globalization.CultureInfo info);
}
```

### New Type System.ComponentModel.Design.ISelectionService

```
public interface ISelectionService {
	// properties
	public virtual object PrimarySelection { get; }
	public virtual int SelectionCount { get; }
	// events
	public event System.EventHandler SelectionChanged;
	public event System.EventHandler SelectionChanging;
	// methods
	public virtual bool GetComponentSelected (object component);
	public virtual System.Collections.ICollection GetSelectedComponents ();
	public virtual void SetSelectedComponents (System.Collections.ICollection components, SelectionTypes selectionType);
	public virtual void SetSelectedComponents (System.Collections.ICollection components);
}
```

### New Type System.ComponentModel.Design.ITreeDesigner

```
public interface ITreeDesigner : IDesigner, System.IDisposable {
	// properties
	public virtual System.Collections.ICollection Children { get; }
	public virtual IDesigner Parent { get; }
}
```

### New Type System.ComponentModel.Design.ITypeDiscoveryService

```
public interface ITypeDiscoveryService {
	// methods
	public virtual System.Collections.ICollection GetTypes (System.Type baseType, bool excludeGlobalTypes);
}
```

### New Type System.ComponentModel.Design.SelectionTypes

```
[Serializable]
[Flags]
public enum SelectionTypes {
	Add = 64,
	Auto = 1,
	[Obsolete ("This value has been deprecated. Use SelectionTypes.Primary instead.")]
	Click = 16,

	[Obsolete ("This value has been deprecated. It is no longer supported.")]
	MouseDown = 4,

	[Obsolete ("This value has been deprecated. It is no longer supported.")]
	MouseUp = 8,

	[Obsolete ("This value has been deprecated. Use SelectionTypes.Auto instead.")]
	Normal = 1,

	Primary = 16,
	Remove = 128,
	Replace = 2,
	Toggle = 32,
	[Obsolete ("This value has been deprecated. It is no longer supported.")]
	Valid = 31,

}
```

### New Type System.ComponentModel.Design.ServiceContainer

```
public class ServiceContainer : IServiceContainer, System.IServiceProvider, System.IDisposable {
	// constructors
	public ServiceContainer ();
	public ServiceContainer (System.IServiceProvider parentProvider);
	// properties
	protected virtual System.Type[] DefaultServices { get; }
	// methods
	public virtual void AddService (System.Type serviceType, object serviceInstance);
	public virtual void AddService (System.Type serviceType, ServiceCreatorCallback callback);
	public virtual void AddService (System.Type serviceType, object serviceInstance, bool promote);
	public virtual void AddService (System.Type serviceType, ServiceCreatorCallback callback, bool promote);
	public virtual void Dispose ();
	protected virtual void Dispose (bool disposing);
	public virtual object GetService (System.Type serviceType);
	public virtual void RemoveService (System.Type serviceType, bool promote);
	public virtual void RemoveService (System.Type serviceType);
}
```

### New Type System.ComponentModel.Design.StandardToolWindows

```
public class StandardToolWindows {
	// constructors
	public StandardToolWindows ();
	// fields
	public static System.Guid ObjectBrowser;
	public static System.Guid OutputWindow;
	public static System.Guid ProjectExplorer;
	public static System.Guid PropertyBrowser;
	public static System.Guid RelatedLinks;
	public static System.Guid ServerExplorer;
	public static System.Guid TaskList;
	public static System.Guid Toolbox;
}
```

### New Type System.ComponentModel.Design.TypeDescriptionProviderService

```
public abstract class TypeDescriptionProviderService {
	// constructors
	protected TypeDescriptionProviderService ();
	// methods
	public virtual System.ComponentModel.TypeDescriptionProvider GetProvider (object instance);
	public virtual System.ComponentModel.TypeDescriptionProvider GetProvider (System.Type type);
}
```

## Namespace System.ComponentModel.Design.Serialization

### New Type System.ComponentModel.Design.Serialization.ComponentSerializationService

```
public abstract class ComponentSerializationService {
	// constructors
	protected ComponentSerializationService ();
	// methods
	public virtual SerializationStore CreateStore ();
	public virtual System.Collections.ICollection Deserialize (SerializationStore store);
	public virtual System.Collections.ICollection Deserialize (SerializationStore store, System.ComponentModel.IContainer container);
	public void DeserializeTo (SerializationStore store, System.ComponentModel.IContainer container, bool validateRecycledTypes);
	public void DeserializeTo (SerializationStore store, System.ComponentModel.IContainer container);
	public virtual void DeserializeTo (SerializationStore store, System.ComponentModel.IContainer container, bool validateRecycledTypes, bool applyDefaults);
	public virtual SerializationStore LoadStore (System.IO.Stream stream);
	public virtual void Serialize (SerializationStore store, object value);
	public virtual void SerializeAbsolute (SerializationStore store, object value);
	public virtual void SerializeMember (SerializationStore store, object owningObject, System.ComponentModel.MemberDescriptor member);
	public virtual void SerializeMemberAbsolute (SerializationStore store, object owningObject, System.ComponentModel.MemberDescriptor member);
}
```

### New Type System.ComponentModel.Design.Serialization.ContextStack

```
public sealed class ContextStack {
	// constructors
	public ContextStack ();
	// properties
	public object Current { get; }
	public object Item { get; }
	public object Item { get; }
	// methods
	public void Append (object context);
	public object Pop ();
	public void Push (object context);
}
```

### New Type System.ComponentModel.Design.Serialization.DefaultSerializationProviderAttribute

```
public sealed class DefaultSerializationProviderAttribute : System.Attribute {
	// constructors
	public DefaultSerializationProviderAttribute (string providerTypeName);
	public DefaultSerializationProviderAttribute (System.Type providerType);
	// properties
	public string ProviderTypeName { get; }
}
```

### New Type System.ComponentModel.Design.Serialization.DesignerLoader

```
public abstract class DesignerLoader {
	// constructors
	protected DesignerLoader ();
	// properties
	public virtual bool Loading { get; }
	// methods
	public virtual void BeginLoad (IDesignerLoaderHost host);
	public virtual void Dispose ();
	public virtual void Flush ();
}
```

### New Type System.ComponentModel.Design.Serialization.DesignerSerializerAttribute

```
public sealed class DesignerSerializerAttribute : System.Attribute {
	// constructors
	public DesignerSerializerAttribute (string serializerTypeName, string baseSerializerTypeName);
	public DesignerSerializerAttribute (string serializerTypeName, System.Type baseSerializerType);
	public DesignerSerializerAttribute (System.Type serializerType, System.Type baseSerializerType);
	// properties
	public string SerializerBaseTypeName { get; }
	public string SerializerTypeName { get; }
	public override object TypeId { get; }
}
```

### New Type System.ComponentModel.Design.Serialization.IDesignerLoaderHost

```
public interface IDesignerLoaderHost : System.ComponentModel.Design.IDesignerHost, System.ComponentModel.Design.IServiceContainer, System.IServiceProvider {
	// methods
	public virtual void EndLoad (string baseClassName, bool successful, System.Collections.ICollection errorCollection);
	public virtual void Reload ();
}
```

### New Type System.ComponentModel.Design.Serialization.IDesignerLoaderHost2

```
public interface IDesignerLoaderHost2 : IDesignerLoaderHost, System.ComponentModel.Design.IDesignerHost, System.ComponentModel.Design.IServiceContainer, System.IServiceProvider {
	// properties
	public virtual bool CanReloadWithErrors { get; set; }
	public virtual bool IgnoreErrorsDuringReload { get; set; }
}
```

### New Type System.ComponentModel.Design.Serialization.IDesignerLoaderService

```
public interface IDesignerLoaderService {
	// methods
	public virtual void AddLoadDependency ();
	public virtual void DependentLoadComplete (bool successful, System.Collections.ICollection errorCollection);
	public virtual bool Reload ();
}
```

### New Type System.ComponentModel.Design.Serialization.IDesignerSerializationManager

```
public interface IDesignerSerializationManager : System.IServiceProvider {
	// properties
	public virtual ContextStack Context { get; }
	public virtual System.ComponentModel.PropertyDescriptorCollection Properties { get; }
	// events
	public event ResolveNameEventHandler ResolveName;
	public event System.EventHandler SerializationComplete;
	// methods
	public virtual void AddSerializationProvider (IDesignerSerializationProvider provider);
	public virtual object CreateInstance (System.Type type, System.Collections.ICollection arguments, string name, bool addToContainer);
	public virtual object GetInstance (string name);
	public virtual string GetName (object value);
	public virtual object GetSerializer (System.Type objectType, System.Type serializerType);
	public virtual System.Type GetType (string typeName);
	public virtual void RemoveSerializationProvider (IDesignerSerializationProvider provider);
	public virtual void ReportError (object errorInformation);
	public virtual void SetName (object instance, string name);
}
```

### New Type System.ComponentModel.Design.Serialization.IDesignerSerializationProvider

```
public interface IDesignerSerializationProvider {
	// methods
	public virtual object GetSerializer (IDesignerSerializationManager manager, object currentSerializer, System.Type objectType, System.Type serializerType);
}
```

### New Type System.ComponentModel.Design.Serialization.IDesignerSerializationService

```
public interface IDesignerSerializationService {
	// methods
	public virtual System.Collections.ICollection Deserialize (object serializationData);
	public virtual object Serialize (System.Collections.ICollection objects);
}
```

### New Type System.ComponentModel.Design.Serialization.INameCreationService

```
public interface INameCreationService {
	// methods
	public virtual string CreateName (System.ComponentModel.IContainer container, System.Type dataType);
	public virtual bool IsValidName (string name);
	public virtual void ValidateName (string name);
}
```

### New Type System.ComponentModel.Design.Serialization.MemberRelationship

```
public struct MemberRelationship {
	// constructors
	public MemberRelationship (object owner, System.ComponentModel.MemberDescriptor member);
	// fields
	public static MemberRelationship Empty;
	// properties
	public bool IsEmpty { get; }
	public System.ComponentModel.MemberDescriptor Member { get; }
	public object Owner { get; }
	// methods
	public override bool Equals (object o);
	public override int GetHashCode ();
	public static bool op_Equality (MemberRelationship left, MemberRelationship right);
	public static bool op_Inequality (MemberRelationship left, MemberRelationship right);
}
```

### New Type System.ComponentModel.Design.Serialization.MemberRelationshipService

```
public abstract class MemberRelationshipService {
	// constructors
	protected MemberRelationshipService ();
	// properties
	public MemberRelationship Item { get; set; }
	public MemberRelationship Item { get; set; }
	// methods
	protected virtual MemberRelationship GetRelationship (MemberRelationship source);
	protected virtual void SetRelationship (MemberRelationship source, MemberRelationship relationship);
	public virtual bool SupportsRelationship (MemberRelationship source, MemberRelationship relationship);
}
```

### New Type System.ComponentModel.Design.Serialization.ResolveNameEventArgs

```
public class ResolveNameEventArgs : System.EventArgs {
	// constructors
	public ResolveNameEventArgs (string name);
	// properties
	public string Name { get; }
	public object Value { get; set; }
}
```

### New Type System.ComponentModel.Design.Serialization.ResolveNameEventHandler

```
public sealed delegate ResolveNameEventHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public ResolveNameEventHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (object sender, ResolveNameEventArgs e, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (object sender, ResolveNameEventArgs e);
}
```

### New Type System.ComponentModel.Design.Serialization.RootDesignerSerializerAttribute

```
public sealed class RootDesignerSerializerAttribute : System.Attribute {
	// constructors
	public RootDesignerSerializerAttribute (string serializerTypeName, string baseSerializerTypeName, bool reloadable);
	public RootDesignerSerializerAttribute (string serializerTypeName, System.Type baseSerializerType, bool reloadable);
	public RootDesignerSerializerAttribute (System.Type serializerType, System.Type baseSerializerType, bool reloadable);
	// properties
	public bool Reloadable { get; }
	public string SerializerBaseTypeName { get; }
	public string SerializerTypeName { get; }
	public override object TypeId { get; }
}
```

### New Type System.ComponentModel.Design.Serialization.SerializationStore

```
public abstract class SerializationStore : System.IDisposable {
	// constructors
	protected SerializationStore ();
	// properties
	public virtual System.Collections.ICollection Errors { get; }
	// methods
	public virtual void Close ();
	protected virtual void Dispose (bool disposing);
	public virtual void Save (System.IO.Stream stream);
}
```

   


 <hr>

# System.Xml.Linq.dll

## New Namespace System.Xml.Schema

### New Type System.Xml.Schema.Extensions

```
public static class Extensions {
	// methods
	public static IXmlSchemaInfo GetSchemaInfo (System.Xml.Linq.XAttribute source);
	public static IXmlSchemaInfo GetSchemaInfo (System.Xml.Linq.XElement source);
	public static void Validate (System.Xml.Linq.XElement source, XmlSchemaObject partialValidationType, XmlSchemaSet schemas, ValidationEventHandler validationEventHandler);
	public static void Validate (System.Xml.Linq.XDocument source, XmlSchemaSet schemas, ValidationEventHandler validationEventHandler, bool addSchemaInfo);
	public static void Validate (System.Xml.Linq.XDocument source, XmlSchemaSet schemas, ValidationEventHandler validationEventHandler);
	public static void Validate (System.Xml.Linq.XAttribute source, XmlSchemaObject partialValidationType, XmlSchemaSet schemas, ValidationEventHandler validationEventHandler, bool addSchemaInfo);
	public static void Validate (System.Xml.Linq.XAttribute source, XmlSchemaObject partialValidationType, XmlSchemaSet schemas, ValidationEventHandler validationEventHandler);
	public static void Validate (System.Xml.Linq.XElement source, XmlSchemaObject partialValidationType, XmlSchemaSet schemas, ValidationEventHandler validationEventHandler, bool addSchemaInfo);
}
```

   


 <hr>

# MonoTouch.Dialog-1.dll

## Namespace MonoTouch.Dialog

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement

### Type Changed: MonoTouch.Dialog.BaseBooleanImageElement.TextWithImageCellView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.Dialog.DialogViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.Dialog.GlassButton

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.Dialog.MessageSummaryView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

### Type Changed: MonoTouch.Dialog.RefreshTableHeaderView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

   


 <hr>

# MonoTouch.NUnitLite.dll

## Namespace MonoTouch.NUnit.UI

### Type Changed: MonoTouch.NUnit.UI.TouchViewController

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

   


 <hr>

# OpenTK.dll

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

   


 <hr>

# OpenTK-1.0.dll

## Namespace OpenTK.Platform.iPhoneOS

### Type Changed: OpenTK.Platform.iPhoneOS.iPhoneOSGameView

Added interfaces:

```
MonoTouch.Foundation.INSCoding
```

   


 <hr>
