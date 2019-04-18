---
id: F96E9D41-D0FE-4A4B-A423-FB34FEED11EA
title: "From 7.0.6 to 7.1.3"
---

# monotouch.dll

## Namespace MonoTouch

### Type Changed: MonoTouch.Constants

Removed fields:

```
public static const string Version = "7.0.6";
```

Added fields:

```
public static const string Version = "7.1.3";
```

## Namespace MonoTouch.AVFoundation

### Type Changed: MonoTouch.AVFoundation.AVAudioSession

Added properties:

```
public static MonoTouch.Foundation.NSString PortCarAudio { get; }
```

### Type Changed: MonoTouch.AVFoundation.AVAudioSessionErrorCode

Added values:

```
CodeCannotStartRecording = 561145187,
```

## Namespace MonoTouch.CoreBluetooth

### Type Changed: MonoTouch.CoreBluetooth.CBError

Added values:

```
ConnectionFailed = 10,
```

### Type Changed: MonoTouch.CoreBluetooth.CBUUID

Added properties:

```
public virtual string Uuid { get; }
```

## Namespace MonoTouch.CoreMedia

### Type Changed: MonoTouch.CoreMedia.CMBufferQueue

Added methods:

```
public static CMBufferQueue FromCallbacks (int count, CMBufferGetTime getDecodeTimeStamp, CMBufferGetTime getPresentationTimeStamp, CMBufferGetTime getDuration, CMBufferGetBool isDataReady, CMBufferCompare compare, MonoTouch.Foundation.NSString dataBecameReadyNotification, CMBufferGetSize getTotalSize);
	public int GetTotalSize ();
```

### Type Changed: MonoTouch.CoreMedia.CMTime

Added methods:

```
public static CMTime Multiply (CMTime time, int multiplier, int divisor);
```

### New Type MonoTouch.CoreMedia.CMBufferGetSize

```
public sealed delegate CMBufferGetSize : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public CMBufferGetSize (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (MonoTouch.ObjCRuntime.INativeObject buffer, System.AsyncCallback callback, object object);
	public virtual int EndInvoke (System.IAsyncResult result);
	public virtual int Invoke (MonoTouch.ObjCRuntime.INativeObject buffer);
}
```

## Namespace MonoTouch.iAd

### New Type MonoTouch.iAd.ADClient

```
public class ADClient : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public ADClient (MonoTouch.Foundation.NSCoder coder);
	public ADClient (MonoTouch.Foundation.NSObjectFlag t);
	public ADClient (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public static ADClient SharedClient { get; }
	// methods
	public virtual void DetermineAppInstallationAttribution (AttributedToiAdCompletionHandler completionHandler);
}
```

### New Type MonoTouch.iAd.AttributedToiAdCompletionHandler

```
public sealed delegate AttributedToiAdCompletionHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	public AttributedToiAdCompletionHandler (object object, System.IntPtr method);
	// methods
	public virtual System.IAsyncResult BeginInvoke (bool attributedToiAd, System.AsyncCallback callback, object object);
	public virtual void EndInvoke (System.IAsyncResult result);
	public virtual void Invoke (bool attributedToiAd);
}
```

## Namespace MonoTouch.MediaPlayer

### New Type MonoTouch.MediaPlayer.IMPPlayableContentDataSource

```
public interface IMPPlayableContentDataSource : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.MediaPlayer.IMPPlayableContentDelegate

```
public interface IMPPlayableContentDelegate : MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
}
```

### New Type MonoTouch.MediaPlayer.MPChangePlaybackRateCommand

```
public class MPChangePlaybackRateCommand : MonoTouch.MediaPlayer.MPRemoteCommand, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPChangePlaybackRateCommand (MonoTouch.Foundation.NSCoder coder);
	public MPChangePlaybackRateCommand (MonoTouch.Foundation.NSObjectFlag t);
	public MPChangePlaybackRateCommand (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MonoTouch.Foundation.NSNumber[] SupportedPlaybackRates { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.MediaPlayer.MPChangePlaybackRateCommandEvent

```
public class MPChangePlaybackRateCommandEvent : MonoTouch.MediaPlayer.MPRemoteCommandEvent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPChangePlaybackRateCommandEvent (MonoTouch.Foundation.NSCoder coder);
	public MPChangePlaybackRateCommandEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPChangePlaybackRateCommandEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float PlaybackRate { get; }
}
```

### New Type MonoTouch.MediaPlayer.MPContentItem

```
public class MPContentItem : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPContentItem (MonoTouch.Foundation.NSCoder coder);
	public MPContentItem (MonoTouch.Foundation.NSObjectFlag t);
	public MPContentItem (System.IntPtr handle);
	public MPContentItem (string identifier);
	// properties
	public virtual MPMediaItemArtwork Artwork { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string Identifier { get; }
	public virtual float PlaybackProgress { get; set; }
	public virtual string Subtitle { get; set; }
	public virtual string Title { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.MediaPlayer.MPFeedbackCommand

```
public class MPFeedbackCommand : MonoTouch.MediaPlayer.MPRemoteCommand, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPFeedbackCommand (MonoTouch.Foundation.NSCoder coder);
	public MPFeedbackCommand (MonoTouch.Foundation.NSObjectFlag t);
	public MPFeedbackCommand (System.IntPtr handle);
	// properties
	public virtual bool Active { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public virtual string LocalizedTitle { get; set; }
}
```

### New Type MonoTouch.MediaPlayer.MPFeedbackCommandEvent

```
public class MPFeedbackCommandEvent : MonoTouch.MediaPlayer.MPRemoteCommandEvent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPFeedbackCommandEvent (MonoTouch.Foundation.NSCoder coder);
	public MPFeedbackCommandEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPFeedbackCommandEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Negative { get; }
}
```

### New Type MonoTouch.MediaPlayer.MPPlayableContentDataSource

```
public class MPPlayableContentDataSource : MonoTouch.Foundation.NSObject, IMPPlayableContentDataSource, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPPlayableContentDataSource ();
	public MPPlayableContentDataSource (MonoTouch.Foundation.NSCoder coder);
	public MPPlayableContentDataSource (MonoTouch.Foundation.NSObjectFlag t);
	public MPPlayableContentDataSource (System.IntPtr handle);
	// methods
	public virtual void BeginLoadingChildItems (MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public virtual bool ChildItemsDisplayPlaybackProgress (MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual MPContentItem ContentItem (MonoTouch.Foundation.NSIndexPath indexPath);
	public virtual int NumberOfChildItems (MonoTouch.Foundation.NSIndexPath indexPath);
}
```

### New Type MonoTouch.MediaPlayer.MPPlayableContentDataSource_Extensions

```
public static class MPPlayableContentDataSource_Extensions {
	// methods
	public static void BeginLoadingChildItems (IMPPlayableContentDataSource This, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
	public static bool ChildItemsDisplayPlaybackProgress (IMPPlayableContentDataSource This, MonoTouch.Foundation.NSIndexPath indexPath);
	public static MPContentItem ContentItem (IMPPlayableContentDataSource This, MonoTouch.Foundation.NSIndexPath indexPath);
	public static int NumberOfChildItems (IMPPlayableContentDataSource This, MonoTouch.Foundation.NSIndexPath indexPath);
}
```

### New Type MonoTouch.MediaPlayer.MPPlayableContentDelegate

```
public class MPPlayableContentDelegate : MonoTouch.Foundation.NSObject, IMPPlayableContentDelegate, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPPlayableContentDelegate ();
	public MPPlayableContentDelegate (MonoTouch.Foundation.NSCoder coder);
	public MPPlayableContentDelegate (MonoTouch.Foundation.NSObjectFlag t);
	public MPPlayableContentDelegate (System.IntPtr handle);
	// methods
	public virtual void PlayableContentManager (MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
}
```

### New Type MonoTouch.MediaPlayer.MPPlayableContentDelegate_Extensions

```
public static class MPPlayableContentDelegate_Extensions {
	// methods
	public static void PlayableContentManager (IMPPlayableContentDelegate This, MPPlayableContentManager contentManager, MonoTouch.Foundation.NSIndexPath indexPath, System.Action<MonoTouch.Foundation.NSError> completionHandler);
}
```

### New Type MonoTouch.MediaPlayer.MPPlayableContentManager

```
public class MPPlayableContentManager : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPPlayableContentManager (MonoTouch.Foundation.NSCoder coder);
	public MPPlayableContentManager (MonoTouch.Foundation.NSObjectFlag t);
	public MPPlayableContentManager (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public MPPlayableContentDataSource DataSource { get; set; }
	public MPPlayableContentDelegate Delegate { get; set; }
	public static MPPlayableContentManager Shared { get; }
	public virtual MonoTouch.Foundation.NSObject WeakDataSource { get; set; }
	public virtual MonoTouch.Foundation.NSObject WeakDelegate { get; set; }
	// methods
	public virtual void BeginUpdates ();
	protected override void Dispose (bool disposing);
	public virtual void EndUpdates ();
	public virtual void ReloadData ();
}
```

### New Type MonoTouch.MediaPlayer.MPRatingCommand

```
public class MPRatingCommand : MonoTouch.MediaPlayer.MPRemoteCommand, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPRatingCommand (MonoTouch.Foundation.NSCoder coder);
	public MPRatingCommand (MonoTouch.Foundation.NSObjectFlag t);
	public MPRatingCommand (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float MaximumRating { get; set; }
	public virtual float MinimumRating { get; set; }
}
```

### New Type MonoTouch.MediaPlayer.MPRatingCommandEvent

```
public class MPRatingCommandEvent : MonoTouch.MediaPlayer.MPRemoteCommandEvent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPRatingCommandEvent (MonoTouch.Foundation.NSCoder coder);
	public MPRatingCommandEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPRatingCommandEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual float Rating { get; }
}
```

### New Type MonoTouch.MediaPlayer.MPRemoteCommand

```
public class MPRemoteCommand : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPRemoteCommand (MonoTouch.Foundation.NSCoder coder);
	public MPRemoteCommand (MonoTouch.Foundation.NSObjectFlag t);
	public MPRemoteCommand (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual bool Enabled { get; set; }
	// methods
	public virtual void AddTarget (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
	public virtual MonoTouch.Foundation.NSObject AddTarget (System.Action<MPRemoteCommandEvent> handler);
	public virtual void RemoveTarget (MonoTouch.Foundation.NSObject target);
	public virtual void RemoveTarget (MonoTouch.Foundation.NSObject target, MonoTouch.ObjCRuntime.Selector action);
}
```

### New Type MonoTouch.MediaPlayer.MPRemoteCommandCenter

```
public class MPRemoteCommandCenter : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPRemoteCommandCenter ();
	public MPRemoteCommandCenter (MonoTouch.Foundation.NSCoder coder);
	public MPRemoteCommandCenter (MonoTouch.Foundation.NSObjectFlag t);
	public MPRemoteCommandCenter (System.IntPtr handle);
	// properties
	public virtual MPFeedbackCommand BookmarkCommand { get; }
	public virtual MPChangePlaybackRateCommand ChangePlaybackRateCommand { get; }
	public override System.IntPtr ClassHandle { get; }
	public virtual MPFeedbackCommand DislikeCommand { get; }
	public virtual MPFeedbackCommand LikeCommand { get; }
	public virtual MPRemoteCommand NextTrackCommand { get; }
	public virtual MPRemoteCommand PauseCommand { get; }
	public virtual MPRemoteCommand PlayCommand { get; }
	public virtual MPRemoteCommand PreviousTrackCommand { get; }
	public virtual MPRatingCommand RatingCommand { get; }
	public virtual MPRemoteCommand SeekBackwardCommand { get; }
	public virtual MPRemoteCommand SeekForwardCommand { get; }
	public static MPRemoteCommandCenter Shared { get; }
	public virtual MPSkipIntervalCommand SkipBackwardCommand { get; }
	public virtual MPSkipIntervalCommand SkipForwardCommand { get; }
	public virtual MPRemoteCommand StopCommand { get; }
	public virtual MPRemoteCommand TogglePlayPauseCommand { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.MediaPlayer.MPRemoteCommandEvent

```
public class MPRemoteCommandEvent : MonoTouch.Foundation.NSObject, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPRemoteCommandEvent (MonoTouch.Foundation.NSCoder coder);
	public MPRemoteCommandEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPRemoteCommandEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MPRemoteCommand Command { get; }
	public virtual double Timestamp { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.MediaPlayer.MPRemoteCommandHandlerStatus

```
[Serializable]
public enum MPRemoteCommandHandlerStatus {
	CommandFailed = 200,
	NoSuchContent = 100,
	Success = 0,
}
```

### New Type MonoTouch.MediaPlayer.MPSeekCommandEvent

```
public class MPSeekCommandEvent : MonoTouch.MediaPlayer.MPRemoteCommandEvent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPSeekCommandEvent (MonoTouch.Foundation.NSCoder coder);
	public MPSeekCommandEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPSeekCommandEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual MPSeekCommandEventType Type { get; }
}
```

### New Type MonoTouch.MediaPlayer.MPSeekCommandEventType

```
[Serializable]
public enum MPSeekCommandEventType {
	BeginSeeking = 0,
	EndSeeking = 1,
}
```

### New Type MonoTouch.MediaPlayer.MPSkipIntervalCommand

```
public class MPSkipIntervalCommand : MonoTouch.MediaPlayer.MPRemoteCommand, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPSkipIntervalCommand (MonoTouch.Foundation.NSCoder coder);
	public MPSkipIntervalCommand (MonoTouch.Foundation.NSObjectFlag t);
	public MPSkipIntervalCommand (System.IntPtr handle);
	// properties
	public virtual MonoTouch.Foundation.NSArray _PreferredIntervals { get; set; }
	public override System.IntPtr ClassHandle { get; }
	public System.Double[] PreferredIntervals { get; set; }
	// methods
	protected override void Dispose (bool disposing);
}
```

### New Type MonoTouch.MediaPlayer.MPSkipIntervalCommandEvent

```
public class MPSkipIntervalCommandEvent : MonoTouch.MediaPlayer.MPRemoteCommandEvent, MonoTouch.ObjCRuntime.INativeObject, System.IDisposable {
	// constructors
	public MPSkipIntervalCommandEvent (MonoTouch.Foundation.NSCoder coder);
	public MPSkipIntervalCommandEvent (MonoTouch.Foundation.NSObjectFlag t);
	public MPSkipIntervalCommandEvent (System.IntPtr handle);
	// properties
	public override System.IntPtr ClassHandle { get; }
	public virtual double Interval { get; }
}
```

## Namespace MonoTouch.ObjCRuntime

### Type Changed: MonoTouch.ObjCRuntime.Messaging

Added methods:

```
public static System.IntPtr IntPtr_objc_msgSend_float_PointF (System.IntPtr receiver, System.IntPtr selector, float arg1, System.Drawing.PointF arg2);
	public static System.IntPtr IntPtr_objc_msgSend_SizeF_PointF (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, System.Drawing.PointF arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_float_PointF (System.IntPtr receiver, System.IntPtr selector, float arg1, System.Drawing.PointF arg2);
	public static System.IntPtr IntPtr_objc_msgSendSuper_SizeF_PointF (System.IntPtr receiver, System.IntPtr selector, System.Drawing.SizeF arg1, System.Drawing.PointF arg2);
```

### Type Changed: MonoTouch.ObjCRuntime.Platform

Added values:

```
iOS_7_1 = 459008,
	Mac_10_10 = 2825744883384320,
```

## Namespace MonoTouch.OpenGLES

### Type Changed: MonoTouch.OpenGLES.EAGLContext

Added properties:

```
public virtual bool IsMultiThreaded { get; set; }
```

## Namespace MonoTouch.SpriteKit

### Type Changed: MonoTouch.SpriteKit.SKAction

Added methods:

```
public static SKAction SetTexture (SKTexture texture, bool resize);
```

### Type Changed: MonoTouch.SpriteKit.SKPhysicsBody

Added methods:

```
public static SKPhysicsBody BodyWithBodies (SKPhysicsBody[] bodies);
	public static SKPhysicsBody BodyWithCircleOfRadius (float radius, System.Drawing.PointF center);
	public static SKPhysicsBody BodyWithRectangleOfSize (System.Drawing.SizeF size, System.Drawing.PointF center);
```

### Type Changed: MonoTouch.SpriteKit.SKView

Added properties:

```
public virtual bool ShowsPhysics { get; set; }
```

## Namespace MonoTouch.StoreKit

### Type Changed: MonoTouch.StoreKit.SKReceiptRefreshRequest

Added methods:

```
public static void TerminateForInvalidReceipt ();
```

   


 <hr>

# MonoTouch.NUnitLite.dll

## Namespace NUnit.Framework.Api

### Type Changed: NUnit.Framework.Api.ITest

Added properties:

```
public virtual bool IsSuite { get; }
```

### Type Changed: NUnit.Framework.Api.ITestResult

Removed properties:

```
public virtual FailureSite FailureSite { get; }
```

### Removed Type NUnit.Framework.Api.FailureSite 

## Namespace NUnit.Framework.Internal

### Type Changed: NUnit.Framework.Internal.RandomGenerator

Removed methods:

```
public object GetEnum (System.Type enumType);
```

Added methods:

```
public T GetEnum<T> ();
```

### Type Changed: NUnit.Framework.Internal.Randomizer

Removed constructors:

```
public Randomizer ();
```

Removed properties:

```
public static int RandomSeed { get; }
```

Added properties:

```
public static int InitialSeed { get; set; }
```

Added methods:

```
public static Randomizer CreateRandomizer ();
```

### Type Changed: NUnit.Framework.Internal.Reflect

Removed methods:

```
public static bool HasMethodWithAttribute (System.Type fixtureType, System.Type attributeType, bool inherit);
```

Added methods:

```
public static bool HasMethodWithAttribute (System.Type fixtureType, System.Type attributeType);
```

### Type Changed: NUnit.Framework.Internal.Test

Added properties:

```
public object Fixture { get; set; }
	public virtual bool IsSuite { get; }
```

Added methods:

```
public virtual WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);
```

### Type Changed: NUnit.Framework.Internal.TestExecutionContext

Removed properties:

```
public RandomGenerator Random { get; }
```

Added properties:

```
public RandomGenerator RandomGenerator { get; }
```

### Type Changed: NUnit.Framework.Internal.TestMethod

Removed methods:

```
public virtual Commands.TestCommand GetTestCommand ();
```

Added methods:

```
public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);
	public virtual Commands.TestCommand MakeTestCommand ();
```

### Type Changed: NUnit.Framework.Internal.TestResult

Removed properties:

```
public virtual NUnit.Framework.Api.FailureSite FailureSite { get; }
```

Removed methods:

```
public virtual void RecordException (System.Exception ex, NUnit.Framework.Api.FailureSite site);
	public void SetResult (NUnit.Framework.Api.ResultState resultState, string message, string stackTrace, NUnit.Framework.Api.FailureSite site);
```

### Type Changed: NUnit.Framework.Internal.TestSuite

Added methods:

```
public override WorkItems.WorkItem CreateWorkItem (NUnit.Framework.Api.ITestFilter childFilter);
```

### Type Changed: NUnit.Framework.Internal.TestSuiteResult

Removed methods:

```
public override void RecordException (System.Exception ex, NUnit.Framework.Api.FailureSite site);
```

## Namespace NUnit.Framework.Internal.WorkItems

### Type Changed: NUnit.Framework.Internal.WorkItems.CompositeWorkItem

Removed constructors:

```
public CompositeWorkItem (NUnit.Framework.Internal.TestSuite suite, NUnit.Framework.Internal.TestExecutionContext context, NUnit.Framework.Api.ITestFilter childFilter);
```

Added constructors:

```
public CompositeWorkItem (NUnit.Framework.Internal.TestSuite suite, NUnit.Framework.Api.ITestFilter childFilter);
```

### Type Changed: NUnit.Framework.Internal.WorkItems.SimpleWorkItem

Removed constructors:

```
public SimpleWorkItem (NUnit.Framework.Internal.TestMethod test, NUnit.Framework.Internal.TestExecutionContext context);
	public SimpleWorkItem (NUnit.Framework.Internal.Commands.TestCommand command, NUnit.Framework.Internal.TestExecutionContext context);
```

Added constructors:

```
public SimpleWorkItem (NUnit.Framework.Internal.TestMethod test);
	public SimpleWorkItem (NUnit.Framework.Internal.Commands.TestCommand command);
```

### Type Changed: NUnit.Framework.Internal.WorkItems.WorkItem

Removed constructors:

```
public WorkItem (NUnit.Framework.Internal.Test test, NUnit.Framework.Internal.TestExecutionContext context);
```

Added constructors:

```
public WorkItem (NUnit.Framework.Internal.Test test);
```

Removed properties:

```
protected NUnit.Framework.Internal.TestExecutionContext PriorContext { get; }
```

Removed methods:

```
public static WorkItem CreateWorkItem (NUnit.Framework.Internal.Test test, NUnit.Framework.Internal.TestExecutionContext context, NUnit.Framework.Api.ITestFilter filter);
	public virtual void Execute ();
```

Added methods:

```
public virtual void Execute (NUnit.Framework.Internal.TestExecutionContext context);
```

## Namespace NUnitLite.Runner

### Type Changed: NUnitLite.Runner.CommandLineOptions

Added properties:

```
public int InitialSeed { get; }
```

### Type Changed: NUnitLite.Runner.NUnit2XmlOutputWriter

Removed constructors:

```
public NUnit2XmlOutputWriter ();
```

Added constructors:

```
public NUnit2XmlOutputWriter (System.DateTime startTime);
```

### Type Changed: NUnitLite.Runner.NUnit3XmlOutputWriter

Removed constructors:

```
public NUnit3XmlOutputWriter ();
```

Added constructors:

```
public NUnit3XmlOutputWriter (System.DateTime runStartTime);
```

   


 <hr>
