---
id: 9A0D1093-D48B-5FAA-D61B-F590D607D33C
title: "from 5.2.13 to 5.4.0"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.2.13";
```

Added:

```
public const string Version = "5.4.0";
        public const string AddressBookUILibrary = "/System/Library/Frameworks/AddressBookUI.framework/AddressBookUI";
        public const string CoreMidiLibrary = "/System/Library/Frameworks/CoreMIDI.framework/CoreMIDI";
        public const string QuickLookLibrary = "/System/Library/Frameworks/QuickLook.framework/QuickLook";
        public const string NewsstandKitLibrary = "/System/Library/Frameworks/NewsstandKit.framework/NewsstandKit";
        public const string ExternalAccessoryLibrary = "/System/Library/Frameworks/ExternalAccessory.framework/ExternalAccessory";
        public const string AudioUnitLibrary = "/System/Library/Frameworks/AudioToolbox.framework/AudioToolbox";
```

 <a name="New_Type:_MonoTouch.MonoNativeFunctionWrapperAttribute" class="injected"></a>


## New Type: MonoTouch.MonoNativeFunctionWrapperAttribute

```
public class MonoNativeFunctionWrapperAttribute : Attribute {
        
        public MonoNativeFunctionWrapperAttribute ();
}
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAsset

Removed:

```
public AVAsset ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetExportSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetExportSession

Removed:

```
public AVAssetExportSession ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetImageGenerator" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetImageGenerator

Removed:

```
public AVAssetImageGenerator ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReader" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReader

Removed:

```
public AVAssetReader ();
        public AVAssetReader (AVAsset asset, IntPtr ptrToNsError);
        public static AVAssetReader _FromAsset (AVAsset asset, IntPtr ptrToNsError);
```

Added:

```
public AVAssetReader (AVAsset asset, out MonoTouch.Foundation.NSError error);
        public static AVAssetReader FromAsset (AVAsset asset, out MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderAudioMixOutput

Removed:

```
public AVAssetReaderAudioMixOutput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReaderOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderOutput

Removed:

```
public AVAssetReaderOutput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetReaderTrackOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderTrackOutput

Removed:

```
public AVAssetReaderTrackOutput ();
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetReaderVideoCompositionOutput 

Removed:

```
public AVAssetReaderVideoCompositionOutput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetTrack" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetTrack

Removed:

```
public AVAssetTrack ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetWriter" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriter

Removed:

```
public AVAssetWriter ();
        public AVAssetWriter (MonoTouch.Foundation.NSUrl outputUrl, string outputFileType, IntPtr ptrToNSError);
        public static AVAssetWriter FromUrl (MonoTouch.Foundation.NSUrl outputUrl, string outputFileType, IntPtr ptrToNSError);
```

Added:

```
public AVAssetWriter (MonoTouch.Foundation.NSUrl outputUrl, string outputFileType, out MonoTouch.Foundation.NSError error);
        public static AVAssetWriter FromUrl (MonoTouch.Foundation.NSUrl outputUrl, string outputFileType, out MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAssetWriterInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriterInput

Removed:

```
public AVAssetWriterInput ();
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAssetWriterInputPixelBufferAdaptor 

Removed:

```
public AVAssetWriterInputPixelBufferAdaptor ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioPlayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioPlayer

Removed:

```
public virtual bool PlayAtTimetime (double time);
```

Added:

```
public virtual bool PlayAtTime (double time);
        [Obsolete("This method was incorrectly named, use PlayAtTime instead")]
        public bool PlayAtTimetime (double time);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioSettings" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioSettings

Removed:

```
public static readonly MonoTouch.Foundation.NSString AVFormatIDKey;
        public static readonly MonoTouch.Foundation.NSString AVSampleRateKey;
        public static readonly MonoTouch.Foundation.NSString AVNumberOfChannelsKey;
        public static readonly MonoTouch.Foundation.NSString AVLinearPCMBitDepthKey;
        public static readonly MonoTouch.Foundation.NSString AVLinearPCMIsBigEndianKey;
        public static readonly MonoTouch.Foundation.NSString AVLinearPCMIsFloatKey;
        public static readonly MonoTouch.Foundation.NSString AVEncoderAudioQualityKey;
        public static readonly MonoTouch.Foundation.NSString AVEncoderBitRateKey;
        public static readonly MonoTouch.Foundation.NSString AVEncoderBitDepthHintKey;
        public static readonly MonoTouch.Foundation.NSString AVSampleRateConverterAudioQualityKey;
```

Added:

```
public static MonoTouch.Foundation.NSString AVChannelLayoutKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVEncoderAudioQualityKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVEncoderBitDepthHintKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVEncoderBitRateKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVEncoderBitRatePerChannelKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVFormatIDKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVLinearPCMBitDepthKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVLinearPCMIsBigEndianKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVLinearPCMIsFloatKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVLinearPCMIsNonInterleaved {
                get;
        }
        public static MonoTouch.Foundation.NSString AVNumberOfChannelsKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVSampleRateConverterAudioQualityKey {
                get;
        }
        public static MonoTouch.Foundation.NSString AVSampleRateKey {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDevice" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDevice

Removed:

```
public AVCaptureDevice ();
```

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveSubjectAreaDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWasConnected (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWasDisconnected (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureDeviceInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureDeviceInput

Removed:

```
public AVCaptureDeviceInput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureFileOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureFileOutput

Removed:

```
public AVCaptureFileOutput ();
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureInput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureInput

Removed:

```
public AVCaptureInput ();
```

Added:

```
public static MonoTouch.Foundation.NSString PortFormatDescriptionDidChangeNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObservePortFormatDescriptionDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureOutput" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureOutput

Removed:

```
public AVCaptureOutput ();
        public virtual MonoTouch.Foundation.NSObject[] Connections {
```

Added:

```
public virtual AVCaptureConnection[] Connections {
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCaptureSession" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCaptureSession

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidStartRunning (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidStopRunning (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveInterruptionEnded (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveRuntimeError (EventHandler<AVCaptureSessionRuntimeErrorEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWasInterrupted (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVCaptureSessionRuntimeErrorEventArgs" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVCaptureSessionRuntimeErrorEventArgs

```
public class AVCaptureSessionRuntimeErrorEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public AVCaptureSessionRuntimeErrorEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MonoTouch.Foundation.NSError Error {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVComposition" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVComposition

Removed:

```
public virtual System.Drawing.SizeF NaturalSize {
                set;
```

Added:

```
[Obsolete("Deprecated in iOS5")]
        public virtual System.Drawing.SizeF NaturalSize {
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVCompositionTrack" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVCompositionTrack

Removed:

```
public AVCompositionTrack ();
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVMetadata" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVMetadata

```
public class AVMetadata {
        
        public AVMetadata ();
        
        public static MonoTouch.Foundation.NSString CommonKeyAlbumName {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyArtwork {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyAuthor {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyContributor {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyCopyrights {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyCreationDate {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyCreator {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyFormat {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyLanguage {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyLastModifiedDate {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyLocation {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyMake {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyModel {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyPublisher {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyRelation {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeySoftware {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeySource {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeySubject {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString CommonKeyType {
                get;
        }
        public static MonoTouch.Foundation.NSString FormatID3Metadata {
                get;
        }
        public static MonoTouch.Foundation.NSString FormatiTunesMetadata {
                get;
        }
        public static MonoTouch.Foundation.NSString FormatQuickTimeMetadata {
                get;
        }
        public static MonoTouch.Foundation.NSString FormatQuickTimeUserData {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyAlbumSortOrder {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyAlbumTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyAttachedPicture {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyAudioEncryption {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyAudioSeekPointIndex {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyBand {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyBeatsPerMinute {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyComments {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyCommercialInformation {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyCommerical {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyComposer {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyConductor {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyContentGroupDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyContentType {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyCopyright {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyCopyrightInformation {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyDate {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyEncodedBy {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyEncodedWith {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyEncodingTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyEncryption {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyEqualization {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyEqualization2 {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyEventTimingCodes {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyFileOwner {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyFileType {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyGeneralEncapsulatedObject {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyGroupIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyInitialKey {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyInternationalStandardRecordingCode {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyInternetRadioStationName {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyInternetRadioStationOwner {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyInvolvedPeopleList {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyLanguage {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyLeadPerformer {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyLength {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyLink {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyLyricist {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyMediaType {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyModifiedBy {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyMood {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyMPEGLocationLookupTable {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyMusicCDIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyMusicianCreditsList {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOfficialArtistWebpage {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOfficialAudioFileWebpage {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOfficialAudioSourceWebpage {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOfficialInternetRadioStationHomepage {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOfficialPublisherWebpage {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOriginalAlbumTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOriginalArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOriginalFilename {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOriginalLyricist {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOriginalReleaseTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOriginalReleaseYear {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyOwnership {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyPartOfASet {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyPayment {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyPerformerSortOrder {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyPlayCounter {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyPlaylistDelay {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyPopularimeter {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyPositionSynchronization {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyPrivate {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyProducedNotice {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyPublisher {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyRecommendedBufferSize {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyRecordingDates {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyRecordingTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyRelativeVolumeAdjustment {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyRelativeVolumeAdjustment2 {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyReleaseTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyReverb {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeySeek {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeySetSubtitle {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeySignature {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeySize {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeySubTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeySynchronizedLyric {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeySynchronizedTempoCodes {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyTaggingTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyTermsOfUse {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyTitleDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyTitleSortOrder {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyTrackNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyUniqueFileIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyUnsynchronizedLyric {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyUserText {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyUserURL {
                get;
        }
        public static MonoTouch.Foundation.NSString ID3MetadataKeyYear {
                get;
        }
        public static MonoTouch.Foundation.NSString ISOUserDataKeyCopyright {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyAccountKind {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyAcknowledgement {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyAlbum {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyAlbumArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyAppleID {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyArranger {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyArtDirector {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyArtistID {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyAuthor {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyBeatsPerMin {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyComposer {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyConductor {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyContentRating {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyCopyright {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyCoverArt {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyCredits {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyDirector {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyDiscCompilation {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyDiscNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyEncodedBy {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyEncodingTool {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyEQ {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyExecProducer {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyGenreID {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyGrouping {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyLinerNotes {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyLyrics {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyOnlineExtras {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyOriginalArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyPerformer {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyPhonogramRights {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyPlaylistID {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyPredefinedGenre {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyProducer {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyPublisher {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyRecordCompany {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyReleaseDate {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeySoloist {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeySongID {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeySongName {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeySoundEngineer {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyThanks {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyTrackNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyTrackSubTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyUserComment {
                get;
        }
        public static MonoTouch.Foundation.NSString iTunesMetadataKeyUserGenre {
                get;
        }
        public static MonoTouch.Foundation.NSString K3GPUserDataKeyAuthor {
                get;
        }
        public static MonoTouch.Foundation.NSString K3GPUserDataKeyCopyright {
                get;
        }
        public static MonoTouch.Foundation.NSString K3GPUserDataKeyDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString K3GPUserDataKeyGenre {
                get;
        }
        public static MonoTouch.Foundation.NSString K3GPUserDataKeyLocation {
                get;
        }
        public static MonoTouch.Foundation.NSString K3GPUserDataKeyPerformer {
                get;
        }
        public static MonoTouch.Foundation.NSString K3GPUserDataKeyRecordingYear {
                get;
        }
        public static MonoTouch.Foundation.NSString K3GPUserDataKeyTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString KeySpaceCommon {
                get;
        }
        public static MonoTouch.Foundation.NSString KeySpaceID3 {
                get;
        }
        public static MonoTouch.Foundation.NSString KeySpaceiTunes {
                get;
        }
        public static MonoTouch.Foundation.NSString KeySpaceQuickTimeMetadata {
                get;
        }
        public static MonoTouch.Foundation.NSString KeySpaceQuickTimeUserData {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyAlbum {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyArranger {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyArtwork {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyAuthor {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyCameraFrameReadoutTime {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyCameraIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyCollectionUser {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyComment {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyComposer {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyCopyright {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyCreationDate {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyCredits {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyDirectionFacing {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyDirectionMotion {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyDirector {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyDisplayName {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyEncodedBy {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyGenre {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyInformation {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyiXML {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyKeywords {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyLocationBody {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyLocationDate {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyLocationISO6709 {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyLocationName {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyLocationNote {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyLocationRole {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyMake {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyModel {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyOriginalArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyPerformer {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyPhonogramRights {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyProducer {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyPublisher {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyRatingUser {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeySoftware {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeMetadataKeyYear {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyAlbum {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyArranger {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyAuthor {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyChapter {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyComment {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyComposer {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyCopyright {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyCreationDate {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyCredits {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyDirector {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyDisclaimer {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyEncodedBy {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyFullName {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyGenre {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyHostComputer {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyInformation {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyKeywords {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyLocationISO6709 {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyMake {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyModel {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyOriginalArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyOriginalFormat {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyOriginalSource {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyPerformers {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyPhonogramRights {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyProducer {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyProduct {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyPublisher {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeySoftware {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeySpecialPlaybackRequirements {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyTaggedCharacteristic {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyTrack {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyTrackName {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyURLLink {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyWarning {
                get;
        }
        public static MonoTouch.Foundation.NSString QuickTimeUserDataKeyWriter {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMetadataItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMetadataItem

Removed:

```
public virtual AVKeyValueStatus StatusOfValueForKeyerror (string key, IntPtr outError);
```

Added:

```
public virtual AVKeyValueStatus StatusOfValueForKeyerror (string key, out MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableComposition" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMutableComposition

Removed:

```
public virtual bool Insert (MonoTouch.CoreMedia.CMTimeRange insertTimeRange, AVAsset sourceAsset, MonoTouch.CoreMedia.CMTime atTime, MonoTouch.Foundation.NSError outError);
```

Added:

```
public virtual bool Insert (MonoTouch.CoreMedia.CMTimeRange insertTimeRange, AVAsset sourceAsset, MonoTouch.CoreMedia.CMTime atTime, out MonoTouch.Foundation.NSError error);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVMutableCompositionTrack" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMutableCompositionTrack

Removed:

```
public AVMutableCompositionTrack ();
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVMutableVideoCompositionInstruction 

Added:

```
public virtual bool EnablePostProcessing {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayer

Removed:

```
public virtual void Seek (MonoTouch.CoreMedia.CMTime time, AVCompletionHandler completion);
        public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
                set;
```

Added:

```
public virtual void Seek (MonoTouch.CoreMedia.CMTime time, AVCompletion completion);
        [Obsolete("Use Seek(CMTime, AVCompletion) instead, the callback contains a `bool finished' parameter")]
        public void Seek (MonoTouch.CoreMedia.CMTime time, AVCompletionHandler completion);
        public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletion completion);
        [Obsolete("Use Seek(CMTime, CMTime, CMTIme, AVCompletion) instead, the callback contains a `bool finished' parameter")]
        public void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVPlayerItem" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVPlayerItem

Removed:

```
public AVPlayerItem ();
        public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
        public static MonoTouch.Foundation.NSString DidPLayToEndTimeNotification {
                set;
```

Added:

```
public virtual void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletion completion);
        [Obsolete("Use Seek(CMTime, CMTime, CMTIme, AVCompletion) instead, the callback contains a `bool finished' parameter")]
        public void Seek (MonoTouch.CoreMedia.CMTime time, MonoTouch.CoreMedia.CMTime toleranceBefore, MonoTouch.CoreMedia.CMTime toleranceAfter, AVCompletionHandler completion);
        public static MonoTouch.Foundation.NSString DidPlayToEndTimeNotification {
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidPlayToEndTime (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveItemFailedToPlayToEndTime (EventHandler<AVPlayerItemErrorEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTimeJumped (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.AVFoundation.AVPlayerItemErrorEventArgs" class="injected"></a>


## New Type: MonoTouch.AVFoundation.AVPlayerItemErrorEventArgs

```
public class AVPlayerItemErrorEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public AVPlayerItemErrorEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MonoTouch.Foundation.NSError Error {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVUrlAsset" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVUrlAsset

Removed:

```
public AVUrlAsset ();
```

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVVideoCompositionValidationHandling 

Removed:

```
public AVVideoCompositionValidationHandling ();
```

 <a name="Namespace:_MonoTouch.Accounts" class="injected"></a>


# Namespace: MonoTouch.Accounts

 <a name="Type_Changed:_MonoTouch.Accounts.ACAccount" class="injected"></a>


## Type Changed: MonoTouch.Accounts.ACAccount

Removed:

```
public virtual string ErrorDomain {
                get;
        }
```

Added:

```
public static MonoTouch.Foundation.NSString ErrorDomain {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Accounts.ACAccountStore" class="injected"></a>


## Type Changed: MonoTouch.Accounts.ACAccountStore

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.AddressBook" class="injected"></a>


# Namespace: MonoTouch.AddressBook

 <a name="Type_Changed:_MonoTouch.AddressBook.ABAddressBook" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABAddressBook

Added:

```
public ABSource[] GetAllSources ();
        public ABSource GetDefaultSource ();
        public ABGroup[] GetGroups (ABRecord source);
        public ABPerson[] GetPeople (ABRecord source);
        public ABPerson[] GetPeople (ABRecord source, ABPersonSortBy sortOrdering);
        public ABSource GetSource (int sourceID);
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABGroup" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABGroup

Added:

```
public ABGroup (ABRecord source);
        public ABRecord Source {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABPerson" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABPerson

Added:

```
public ABPerson (ABRecord source);
        public static ABPerson[] CreateFromVCard (ABRecord source, MonoTouch.Foundation.NSData vCardData);
        public static MonoTouch.Foundation.NSData GetVCards (params ABPerson[] people);
        public MonoTouch.Foundation.NSData GetImage (ABPersonImageFormat format);
        public ABPerson[] GetLinkedPeople ();
        public ABRecord Source {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABPersonPhoneLabel" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABPersonPhoneLabel

Added:

```
public static MonoTouch.Foundation.NSString OtherFax {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AddressBook.ABPropertyType" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABPropertyType

Removed:

```
public enum ABPropertyType : ushort {
```

Added:

```
public enum ABPropertyType : uint {
```

 <a name="New_Type:_MonoTouch.AddressBook.ABSource" class="injected"></a>


## New Type: MonoTouch.AddressBook.ABSource

```
public class ABSource : ABRecord {
        
        public string Name {
                get;
                set;
        }
        public ABSourceType SourceType {
                get;
                set;
        }
        
        [Obsolete("Use ABSourceType.SearchableMask")]
        public const int SearchableMask = 16777216;
}
```

 <a name="New_Type:_MonoTouch.AddressBook.ABSourceProperty" class="injected"></a>


## New Type: MonoTouch.AddressBook.ABSourceProperty

```
[Serializable]
public enum ABSourceProperty {
        Name,
        Type
}
```

 <a name="New_Type:_MonoTouch.AddressBook.ABSourceType" class="injected"></a>


## New Type: MonoTouch.AddressBook.ABSourceType

```
[Serializable]
public enum ABSourceType {
        Local,
        Exchange,
        ExchangeGAL,
        MobileMe,
        LDAP,
        CardDAV,
        DAVSearch,
        SearchableMask
}
```

 <a name="Namespace:_MonoTouch.AddressBookUI" class="injected"></a>


# Namespace: MonoTouch.AddressBookUI

 <a name="New_Type:_MonoTouch.AddressBookUI.ABAddressFormatting" class="injected"></a>


## New Type: MonoTouch.AddressBookUI.ABAddressFormatting

```
public static class ABAddressFormatting {
        
        public static string ToString (MonoTouch.Foundation.NSDictionary address, bool addCountryName);
}
```

 <a name="Namespace:_MonoTouch.AssetsLibrary" class="injected"></a>


# Namespace: MonoTouch.AssetsLibrary

 <a name="Type_Changed:_MonoTouch.AssetsLibrary.ALAssetsLibrary" class="injected"></a>


## Type Changed: MonoTouch.AssetsLibrary.ALAssetsLibrary

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveChanged (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.AudioToolbox" class="injected"></a>


# Namespace: MonoTouch.AudioToolbox

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioBufferList" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioBufferList

Added:

```
public AudioBufferList (int count);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioChannelLayout" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioChannelLayout

Added:

```
public MonoTouch.Foundation.NSData AsData ();
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFile" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFile

Added:

```
public AudioStreamPacketDescription[] ReadPacketData (bool useCache, long inStartingPacket, ref int nPackets, byte [] buffer, int offset, ref int count);
        public AudioStreamPacketDescription[] ReadPacketData (bool useCache, long inStartingPacket, ref int nPackets, IntPtr buffer, ref int count);
        public AudioFormat[] AudioFormats {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioFileProperty" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioFileProperty

Added:

```
ReadyToProducePackets,
        AverageBytesPerPacket
```

 <a name="New_Type:_MonoTouch.AudioToolbox.AudioFormat" class="injected"></a>


## New Type: MonoTouch.AudioToolbox.AudioFormat

```
public struct AudioFormat {
        
        public override string ToString ();
        
        public AudioStreamBasicDescription AudioStreamBasicDescription;
        public AudioChannelLayoutTag AudioChannelLayoutTag;
}
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.AudioQueue" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.AudioQueue

Removed:

```
public AudioStreamPacketDescription AudioStreamPacketDescription {
```

Added:

```
public AudioQueueStatus AllocateBuffer (int bufferSize, out AudioQueueBuffer* audioQueueBuffer);
        public AudioQueueStatus EnqueueBuffer (AudioQueueBuffer* audioQueueBuffer, AudioStreamPacketDescription[] desc);
        public AudioStreamBasicDescription AudioStreamPacketDescription {
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.OutputAudioQueue" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.OutputAudioQueue

Added:

```
public OutputAudioQueue (AudioStreamBasicDescription desc, MonoTouch.CoreFoundation.CFRunLoop runLoop, MonoTouch.CoreFoundation.CFString runMode);
        public AudioQueueStatus DisableOfflineRender ();
        public AudioQueueStatus RenderOffline (double timeStamp, AudioQueueBuffer* audioQueueBuffer, int frameCount);
        public AudioQueueStatus SetOfflineRenderFormat (AudioStreamBasicDescription desc, AudioChannelLayout layout);
```

 <a name="Type_Changed:_MonoTouch.AudioToolbox.OutputCompletedEventArgs" class="injected"></a>


## Type Changed: MonoTouch.AudioToolbox.OutputCompletedEventArgs

Added:

```
public OutputCompletedEventArgs (AudioQueueBuffer* audioQueueBuffer);
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAAction" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAAction

Removed:

```
public CAAction ();
```

 <a name="Namespace:_MonoTouch.CoreBluetooth" class="injected"></a>


# Namespace: MonoTouch.CoreBluetooth

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBCentralManager" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBCentralManager

Added:

```
public void RetrievePeripherals (CBUUID[] peripheralUuids);
        public void ScanForPeripherals (CBUUID[] peripheralUuids, MonoTouch.Foundation.NSDictionary options);
```

 <a name="Type_Changed:_MonoTouch.CoreBluetooth.CBPeripheral" class="injected"></a>


## Type Changed: MonoTouch.CoreBluetooth.CBPeripheral

Added:

```
public void DiscoverCharacteristics (CBUUID[] charactersticUUIDs, CBService forService);
        public void DiscoverIncludedServices (CBUUID[] includedServiceUUIDs, CBService forService);
        public void DiscoverServices (CBUUID[] services);
```

 <a name="Namespace:_MonoTouch.CoreData" class="injected"></a>


# Namespace: MonoTouch.CoreData

 <a name="Type_Changed:_MonoTouch.CoreData.NSAtomicStore" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSAtomicStore

Removed:

```
public NSAtomicStore ();
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSAtomicStoreCacheNode" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSAtomicStoreCacheNode

Removed:

```
public NSAtomicStoreCacheNode ();
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSManagedObject" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSManagedObject

Removed:

```
public NSManagedObject ();
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSManagedObjectID" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSManagedObjectID

Removed:

```
public NSManagedObjectID ();
```

 <a name="Type_Changed:_MonoTouch.CoreData.NSPersistentStoreCoordinator" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator

Removed:

```
[Obsolete("Deprecated in MAC OS X 10.5 and later")]
        public static MonoTouch.Foundation.NSDictionary MetadataForPersistentStoreWithUrl (MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public static MonoTouch.Foundation.NSString WillRemoveStoreNotification {
        public static MonoTouch.Foundation.NSString XMLStoreType {
```

Added:

```
public static MonoTouch.Foundation.NSString AddedPersistentStoresKey {
                get;
        }
        public static MonoTouch.Foundation.NSString IgnorePersistentStoreVersioningOption {
                get;
        }
        public static MonoTouch.Foundation.NSString InferMappingModelAutomaticallyOption {
                get;
        }
        public static MonoTouch.Foundation.NSString MigratePersistentStoresAutomaticallyOption {
                get;
        }
        public static MonoTouch.Foundation.NSString PersistentStoreFileProtectionKey {
                get;
        }
        public static MonoTouch.Foundation.NSString PersistentStoreOSCompatibility {
                get;
        }
        public static MonoTouch.Foundation.NSString PersistentStoreTimeoutOption {
                get;
        }
        public static MonoTouch.Foundation.NSString PersistentStoreUbiquitousContentNameKey {
                get;
        }
        public static MonoTouch.Foundation.NSString PersistentStoreUbiquitousContentUrlLKey {
                get;
        }
        public static MonoTouch.Foundation.NSString ReadOnlyPersistentStoreOption {
                get;
        }
        public static MonoTouch.Foundation.NSString RemovedPersistentStoresKey {
                get;
        }
        public static MonoTouch.Foundation.NSString SQLiteAnalyzeOption {
                get;
        }
        public static MonoTouch.Foundation.NSString SQLiteManualVacuumOption {
                get;
        }
        public static MonoTouch.Foundation.NSString SQLitePragmasOption {
                get;
        }
        public static MonoTouch.Foundation.NSString StoreModelVersionHashesKey {
                get;
        }
        public static MonoTouch.Foundation.NSString StoreModelVersionIdentifiersKey {
                get;
        }
        public static MonoTouch.Foundation.NSString StoreUUIDKey {
                get;
        }
        public static MonoTouch.Foundation.NSString UUIDChangedPersistentStoresKey {
        public static MonoTouch.Foundation.NSString WillRemoveStoreNotification {
```

 <a name="Namespace:_MonoTouch.CoreFoundation" class="injected"></a>


# Namespace: MonoTouch.CoreFoundation

 <a name="New_Type:_MonoTouch.CoreFoundation.CFIndex" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFIndex

```
public struct CFIndex {
        
        public static implicit operator int (CFIndex index);
        public static implicit operator CFIndex (int value);
        public static implicit operator long (CFIndex index);
}
```

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFRange" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFRange

Removed:

```
public CFRange (int l, int len);
        public int Location;
        public int Length;
```

Added:

```
public CFRange (int loc, int len);
        public CFRange (long l, long len);
        public override string ToString ();
        
        public int Length {
                get;
        }
        public int Location {
                get;
        }
        public long LongLength {
                get;
        }
        public long LongLocation {
                get;
        }
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFReadStream" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFReadStream

```
public class CFReadStream : CFStream {
        
        public CFReadStream (IntPtr handle);
        
        protected override void DoClose ();
        protected override IntPtr DoGetProperty (MonoTouch.Foundation.NSString name);
        protected override CFStreamStatus DoGetStatus ();
        protected override bool DoOpen ();
        protected override bool DoSetClient (CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
        protected override bool DoSetProperty (MonoTouch.Foundation.NSString name, MonoTouch.ObjCRuntime.INativeObject value);
        public override CFException GetError ();
        public bool HasBytesAvailable ();
        public int Read (byte [] buffer);
        public int Read (byte [] buffer, int offset, int count);
        protected override void ScheduleWithRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
        protected override void UnscheduleFromRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
}
```

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFRunLoop" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFRunLoop

Added:

```
public void AddSource (CFRunLoopSource source, MonoTouch.Foundation.NSString mode);
        public bool ContainsSource (CFRunLoopSource source, MonoTouch.Foundation.NSString mode);
        public bool RemoveSource (CFRunLoopSource source, MonoTouch.Foundation.NSString mode);
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFRunLoopSource" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFRunLoopSource

```
public class CFRunLoopSource : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public void Dispose ();
        public virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public void Invalidate ();
        public void Signal ();
        
        public IntPtr Handle {
                get;
        }
        public bool IsValid {
                get;
        }
        public int Order {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFRunLoopSourceCustom" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFRunLoopSourceCustom

```
public abstract class CFRunLoopSourceCustom : CFRunLoopSource {
        
        protected CFRunLoopSourceCustom ();
        
        public override void Dispose (bool disposing);
        protected abstract void OnCancel (CFRunLoop loop, string mode);
        protected abstract void OnPerform ();
        protected abstract void OnSchedule (CFRunLoop loop, string mode);
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFSocket" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFSocket

```
public class CFSocket : CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public CFSocket ();
        public CFSocket (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto);
        public CFSocket (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, CFRunLoop loop);
        
        public static CFSocket CreateConnectedToSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, double timeout);
        public void Connect (System.Net.IPAddress address, int port, double timeout);
        public void Connect (System.Net.IPEndPoint endpoint, double timeout);
        public void DisableCallBacks (CFSocketCallBackType types);
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        public void EnableCallBacks (CFSocketCallBackType types);
        protected override void Finalize ();
        public CFSocketFlags GetSocketFlags ();
        public void SendData (byte [] data, double timeout);
        public void SetAddress (System.Net.IPAddress address, int port);
        public void SetAddress (System.Net.IPEndPoint endpoint);
        public void SetSocketFlags (CFSocketFlags flags);
        
        public IntPtr Handle {
                get;
        }
        
        public event EventHandler<cfsocketaccepteventargs> AcceptEvent;
        public event EventHandler<cfsocketconnecteventargs> ConnectEvent;
        
        public class CFSocketAcceptEventArgs : EventArgs {
                
                public CFSocketAcceptEventArgs (CFSocketNativeHandle handle, System.Net.IPEndPoint remote);
                
                public CFSocket CreateSocket ();
                public override string ToString ();
                
                public System.Net.IPEndPoint RemoteEndPoint {
                        get;
                }
        }
        public class CFSocketConnectEventArgs : EventArgs {
                
                public CFSocketConnectEventArgs (CFSocketError result);
                
                public override string ToString ();
                
                public CFSocketError Result {
                        get;
                }
        }
}
</cfsocketconnecteventargs></cfsocketaccepteventargs>
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFSocketCallBackType" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFSocketCallBackType

```
[Serializable]
[Flags]
public enum CFSocketCallBackType {
        NoCallBack,
        ReadCallBack,
        AcceptCallBack,
        DataCallBack,
        ConnectCallBack,
        WriteCallBack
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFSocketError" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFSocketError

```
[Serializable]
public enum CFSocketError {
        Success,
        Error,
        Timeout
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFSocketException" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFSocketException

```
public class CFSocketException : Exception {
        
        public CFSocketException (CFSocketError error);
        
        public CFSocketError Error {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFSocketFlags" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFSocketFlags

```
[Serializable]
[Flags]
public enum CFSocketFlags {
        AutomaticallyReenableReadCallBack,
        AutomaticallyReenableAcceptCallBack,
        AutomaticallyReenableDataCallBack,
        AutomaticallyReenableWriteCallBack,
        LeaveErrors,
        CloseOnInvalidate
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFSocketNativeHandle" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFSocketNativeHandle

```
public struct CFSocketNativeHandle {
        
        public override string ToString ();
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFStream" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFStream

```
public abstract class CFStream : CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        protected CFStream (IntPtr handle);
        
        public static void CreateBoundPair (out CFReadStream readStream, out CFWriteStream writeStream, int bufferSize);
        public static MonoTouch.CoreServices.CFHTTPStream CreateForHTTPRequest (MonoTouch.CoreServices.CFHTTPMessage request);
        public static MonoTouch.CoreServices.CFHTTPStream CreateForStreamedHTTPRequest (MonoTouch.CoreServices.CFHTTPMessage request, CFReadStream body);
        public static void CreatePairWithPeerSocketSignature (System.Net.Sockets.AddressFamily family, System.Net.Sockets.SocketType type, System.Net.Sockets.ProtocolType proto, System.Net.IPEndPoint endpoint, out CFReadStream readStream, out CFWriteStream writeStream);
        public static void CreatePairWithSocket (CFSocket socket, out CFReadStream readStream, out CFWriteStream writeStream);
        public static void CreatePairWithSocketToHost (System.Net.IPEndPoint endpoint, out CFReadStream readStream, out CFWriteStream writeStream);
        protected void CheckError ();
        protected void CheckHandle ();
        public void Close ();
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected abstract void DoClose ();
        protected abstract IntPtr DoGetProperty (MonoTouch.Foundation.NSString name);
        protected abstract CFStreamStatus DoGetStatus ();
        protected abstract bool DoOpen ();
        protected abstract bool DoSetClient (CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
        protected abstract bool DoSetProperty (MonoTouch.Foundation.NSString name, MonoTouch.ObjCRuntime.INativeObject value);
        public void EnableEvents (CFRunLoop runLoop, MonoTouch.Foundation.NSString runLoopMode);
        protected override void Finalize ();
        public abstract CFException GetError ();
        public CFStreamStatus GetStatus ();
        protected virtual void OnCallback (CFStreamEventType type);
        protected virtual void OnCanAcceptBytesEvent (StreamEventArgs args);
        protected virtual void OnClosedEvent (StreamEventArgs args);
        protected virtual void OnErrorEvent (StreamEventArgs args);
        protected virtual void OnHasBytesAvailableEvent (StreamEventArgs args);
        protected virtual void OnOpenCompleted (StreamEventArgs args);
        public void Open ();
        protected abstract void ScheduleWithRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
        protected abstract void UnscheduleFromRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
        
        public IntPtr Handle {
                get;
        }
        
        public event EventHandler<streameventargs> CanAcceptBytesEvent;
        public event EventHandler<streameventargs> ClosedEvent;
        public event EventHandler<streameventargs> ErrorEvent;
        public event EventHandler<streameventargs> HasBytesAvailableEvent;
        public event EventHandler<streameventargs> OpenCompletedEvent;
        
        [Serializable]
        protected delegate void CFStreamCallback (IntPtr s, CFStreamEventType type, IntPtr info);
        public class StreamEventArgs : EventArgs {
                
                public StreamEventArgs (CFStreamEventType type);
                
                public override string ToString ();
                
                public CFStreamEventType EventType {
                        get;
                }
        }
}
</streameventargs></streameventargs></streameventargs></streameventargs></streameventargs>
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFStreamClientContext" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFStreamClientContext

```
public struct CFStreamClientContext {
        
        public void Release ();
        public void Retain ();
        public override string ToString ();
        
        public int Version;
        public IntPtr Info;
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFStreamEventType" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFStreamEventType

```
[Serializable]
[Flags]
public enum CFStreamEventType {
        None,
        OpenCompleted,
        HasBytesAvailable,
        CanAcceptBytes,
        ErrorOccurred,
        EndEncountered
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFStreamStatus" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFStreamStatus

```
[Serializable]
public enum CFStreamStatus {
        NotOpen,
        Opening,
        Open,
        Reading,
        Writing,
        AtEnd,
        Closed,
        Error
}
```

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFType" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFType

Added:

```
public string GetDescription (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.CoreFoundation.CFUrl" class="injected"></a>


## Type Changed: MonoTouch.CoreFoundation.CFUrl

Removed:

```
public class CFUrl : IDisposable {
```

Added:

```
public class CFUrl : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        public static int GetTypeID ();
        public string FileSystemPath {
                get;
        }
```

 <a name="New_Type:_MonoTouch.CoreFoundation.CFWriteStream" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.CFWriteStream

```
public class CFWriteStream : CFStream {
        
        public bool CanAcceptBytes ();
        protected override void DoClose ();
        protected override IntPtr DoGetProperty (MonoTouch.Foundation.NSString name);
        protected override CFStreamStatus DoGetStatus ();
        protected override bool DoOpen ();
        protected override bool DoSetClient (CFStreamCallback callback, CFIndex eventTypes, IntPtr context);
        protected override bool DoSetProperty (MonoTouch.Foundation.NSString name, MonoTouch.ObjCRuntime.INativeObject value);
        public override CFException GetError ();
        protected override void ScheduleWithRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
        protected override void UnscheduleFromRunLoop (CFRunLoop loop, MonoTouch.Foundation.NSString mode);
        public int Write (byte [] buffer);
        public int Write (byte [] buffer, int offset, int count);
}
```

 <a name="New_Type:_MonoTouch.CoreFoundation.ICFType" class="injected"></a>


## New Type: MonoTouch.CoreFoundation.ICFType

```
public interface ICFType : MonoTouch.ObjCRuntime.INativeObject {
}
```

 <a name="Namespace:_MonoTouch.CoreGraphics" class="injected"></a>


# Namespace: MonoTouch.CoreGraphics

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPDFDocument" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPDFDocument

Added:

```
public CGPDFDocument (CGDataProvider provider);
```

 <a name="Type_Changed:_MonoTouch.CoreGraphics.CGPath" class="injected"></a>


## Type Changed: MonoTouch.CoreGraphics.CGPath

Removed:

```
public void AddElipseInRect (CGAffineTransform m, System.Drawing.RectangleF rect);
```

Added:

```
[Obsolete("Use AddEllipseInRect instead")]
        public void AddElipseInRect (CGAffineTransform m, System.Drawing.RectangleF rect);
        public void AddEllipseInRect (CGAffineTransform m, System.Drawing.RectangleF rect);
```

 <a name="Namespace:_MonoTouch.CoreImage" class="injected"></a>


# Namespace: MonoTouch.CoreImage

 <a name="Type_Changed:_MonoTouch.CoreImage.CIContext" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIContext

Removed:

```
public static CIContext FromContext (MonoTouch.CoreGraphics.CGContext ctx);
        public static CIContext FromContext (MonoTouch.CoreGraphics.CGContext ctx, CIContextOptions options);
        public MonoTouch.CoreGraphics.CGLayer CreateCGLayer (System.Drawing.SizeF size);
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFeature" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFeature

Added:

```
public static MonoTouch.Foundation.NSString TypeFace {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFilter" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFilter

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIFilterAttributes" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIFilterAttributes

Removed:

```
public static MonoTouch.Foundation.NSString TypeOpaqueColor {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.CoreImage.CIImage" class="injected"></a>


## Type Changed: MonoTouch.CoreImage.CIImage

Removed:

```
protected override void Dispose (bool disposing);
        public virtual CIImage ImageWithColor (CIColor color);
        public virtual MonoTouch.Foundation.NSObject IntPtr (MonoTouch.CoreGraphics.CGLayer layer, MonoTouch.Foundation.NSDictionary d);
        public virtual MonoTouch.CoreGraphics.CGColorSpace ColorSpace {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl Url {
                get;
        }
```

Added:

```
public CIImage (MonoTouch.CoreGraphics.CGLayer layer, MonoTouch.Foundation.NSDictionary d);
        public static CIImage FromCGImage (MonoTouch.CoreGraphics.CGImage image, MonoTouch.CoreGraphics.CGColorSpace colorSpace);
        public static CIImage ImageWithColor (CIColor color);
        
        public static implicit operator CIImage (MonoTouch.CoreGraphics.CGImage image);
```

 <a name="Namespace:_MonoTouch.CoreLocation" class="injected"></a>


# Namespace: MonoTouch.CoreLocation

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLError" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLError

Added:

```
RegionMonitoringResponseDelayed,
        GeocodeFoundNoResult,
        GeocodeFoundPartialResult,
        GeocodeCanceled
```

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLPlacemark" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLPlacemark

Removed:

```
public CLPlacemark ();
```

 <a name="Namespace:_MonoTouch.CoreMedia" class="injected"></a>


# Namespace: MonoTouch.CoreMedia

 <a name="New_Type:_MonoTouch.CoreMedia.CMBufferCompare" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMBufferCompare

```
[Serializable]
public delegate int CMBufferCompare (MonoTouch.ObjCRuntime.INativeObject first, MonoTouch.ObjCRuntime.INativeObject second);
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMBufferGetBool" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMBufferGetBool

```
[Serializable]
public delegate bool CMBufferGetBool (MonoTouch.ObjCRuntime.INativeObject buffer);
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMBufferGetTime" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMBufferGetTime

```
[Serializable]
public delegate CMTime CMBufferGetTime (MonoTouch.ObjCRuntime.INativeObject buffer);
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMBufferQueue" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMBufferQueue

```
public class CMBufferQueue : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public static CMBufferQueue CreateUnsorted (int count);
        public static CMBufferQueue FromCallbacks (int count, CMBufferGetTime getDecodeTimeStamp, CMBufferGetTime getPresentationTimeStamp, CMBufferGetTime getDuration, CMBufferGetBool isDataReady, CMBufferCompare compare, MonoTouch.Foundation.NSString dataBecameReadyNotification);
        public MonoTouch.ObjCRuntime.INativeObject Dequeue ();
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        public void Enqueue (MonoTouch.ObjCRuntime.INativeObject cftypeBuffer);
        protected override void Finalize ();
        
        public IntPtr Handle {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.CoreMedia.CMFormatDescription" class="injected"></a>


## Type Changed: MonoTouch.CoreMedia.CMFormatDescription

Added:

```
public static MonoTouch.Foundation.NSObject[] GetExtensionKeysCommonWithImageBuffers ();
        public System.Drawing.RectangleF GetVideoCleanAperture (bool originIsAtTopLeft);
        public System.Drawing.SizeF GetVideoPresentationDimensions (bool usePixelAspectRatio, bool useCleanAperture);
        public bool VideoMatchesImageBuffer (MonoTouch.CoreVideo.CVImageBuffer imageBuffer);
        public MonoTouch.AudioToolbox.AudioChannelLayout AudioChannelLayout {
                get;
        }
        public MonoTouch.AudioToolbox.AudioFormat[] AudioFormats {
                get;
        }
        public byte [] AudioMagicCookie {
                get;
        }
        public MonoTouch.AudioToolbox.AudioFormat AudioMostCompatibleFormat {
                get;
        }
        public MonoTouch.AudioToolbox.AudioFormat AudioRichestDecodableFormat {
                get;
        }
        public System.Nullable<MonoTouch.AudioToolbox.AudioStreamBasicDescription> AudioStreamBasicDescription {
                get;
        }
        public System.Drawing.Size VideoDimensions {
                get;
        }
```

 <a name="New_Type:_MonoTouch.CoreMedia.CMVideoCodecType" class="injected"></a>


## New Type: MonoTouch.CoreMedia.CMVideoCodecType

```
[Serializable]
public enum CMVideoCodecType {
        YUV422YpCbCr8,
        Animation,
        Cinepak,
        JPEG,
        JPEG_OpenDML,
        SorensonVideo,
        SorensonVideo3,
        H263,
        H264,
        Mpeg4Video,
        Mpeg2Video,
        Mpeg1Video,
        DvcNtsc,
        DvcPal,
        DvcProPal,
        DvcPro50NTSC,
        DvcPro50PAL,
        DvcProHD720p60,
        DvcProHD720p50,
        DvcProHD1080i60,
        DvcProHD1080i50,
        DvcProHD1080p30,
        DvcProHD1080p25,
        AppleProRes4444,
        AppleProRes422HQ,
        AppleProRes422,
        AppleProRes422LT,
        AppleProRes422Proxy
}
```

 <a name="Namespace:_MonoTouch.CoreMidi" class="injected"></a>


# Namespace: MonoTouch.CoreMidi

 <a name="New_Type:_MonoTouch.CoreMidi.IOErrorEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreMidi.IOErrorEventArgs

```
public class IOErrorEventArgs : EventArgs {
        
        public IOErrorEventArgs (MidiDevice device, int errorCode);
        
        public MidiDevice Device {
                get;
                set;
        }
        public int ErrorCode {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.Midi" class="injected"></a>


## New Type: MonoTouch.CoreMidi.Midi

```
public static class Midi {
        
        public static MidiDevice GetDevice (int deviceIndex);
        public static MidiDevice GetExternalDevice (int deviceIndex);
        public static void Restart ();
        
        public static int DestinationCount {
                get;
        }
        public static int DeviceCount {
                get;
        }
        public static int ExternalDeviceCount {
                get;
        }
        public static MonoTouch.Foundation.NSString NetworkBonjourServiceType {
                get;
        }
        public static MonoTouch.Foundation.NSString NetworkNotificationContactsDidChange {
                get;
        }
        public static MonoTouch.Foundation.NSString NetworkNotificationSessionDidChange {
                get;
        }
        public static int SourceCount {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveNetworkNotificationContactsDidChange (System.EventHandler<monotouch.foundation.nsnotificationeventargs> handler);
                public static MonoTouch.Foundation.NSObject ObserveNetworkNotificationSessionDidChange (System.EventHandler<monotouch.foundation.nsnotificationeventargs> handler);
        }
}
</monotouch.foundation.nsnotificationeventargs></monotouch.foundation.nsnotificationeventargs>
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiClient" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiClient

```
public class MidiClient : MidiObject {
        
        public MidiClient (string name);
        
        public MidiPort CreateInputPort (string name);
        public MidiPort CreateOutputPort (string name);
        public MidiEndpoint CreateVirtualSource (string name);
        public override void Dispose (bool disposing);
        public override string ToString ();
        
        public string Name {
                get;
        }
        
        public event EventHandler<ioerroreventargs> IOError;
        public event EventHandler<objectaddedorremovedeventargs> ObjectAdded;
        public event EventHandler<objectaddedorremovedeventargs> ObjectRemoved;
        public event EventHandler<objectpropertychangedeventargs> PropertyChanged;
        public event EventHandler SerialPortOwnerChanged;
        public event EventHandler SetupChanged;
        public event EventHandler ThruConnectionsChanged;
}
</objectpropertychangedeventargs></objectaddedorremovedeventargs></objectaddedorremovedeventargs></ioerroreventargs>
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiDevice" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiDevice

```
public class MidiDevice : MidiObject {
        
        public MidiEntity GetEntity (int entityIndex);
        
        public int AdvanceScheduleTimeMuSec {
                get;
                set;
        }
        public bool CanRoute {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData ConnectionUniqueIDData {
                get;
                set;
        }
        public int ConnectionUniqueIDInt {
                get;
                set;
        }
        public int DeviceID {
                get;
                set;
        }
        public string DisplayName {
                get;
                set;
        }
        public string DriverDeviceEditorApp {
                get;
                set;
        }
        public string DriverOwner {
                get;
                set;
        }
        public int DriverVersion {
                get;
                set;
        }
        public int EntityCount {
                get;
        }
        public string Image {
                get;
                set;
        }
        public bool IsDrumMachine {
                get;
        }
        public bool IsEffectUnit {
                get;
        }
        public bool IsEmbeddedEntity {
                get;
        }
        public bool IsMixer {
                get;
        }
        public bool IsSampler {
                get;
        }
        public string Manufacturer {
                get;
                set;
        }
        public int MaxReceiveChannels {
                get;
        }
        public int MaxSysExSpeed {
                get;
                set;
        }
        public int MaxTransmitChannels {
                get;
                set;
        }
        public string Model {
                get;
                set;
        }
        public string Name {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDictionary NameConfiguration {
                get;
                set;
        }
        public bool Offline {
                get;
                set;
        }
        public bool PanDisruptsStereo {
                get;
                set;
        }
        public bool Private {
                get;
                set;
        }
        public bool ReceivesBankSelectLSB {
                get;
                set;
        }
        public bool ReceivesBankSelectMSB {
                get;
                set;
        }
        public bool ReceivesClock {
                get;
                set;
        }
        public bool ReceivesMTC {
                get;
                set;
        }
        public bool ReceivesNotes {
                get;
                set;
        }
        public bool ReceivesProgramChanges {
                get;
                set;
        }
        public int SingleRealtimeEntity {
                get;
                set;
        }
        public bool SupportsGeneralMidi {
                get;
                set;
        }
        public bool SupportsMMC {
                get;
                set;
        }
        public bool SupportsShowControl {
                get;
                set;
        }
        public bool TransmitsBankSelectLSB {
                get;
                set;
        }
        public bool TransmitsBankSelectMSB {
                get;
                set;
        }
        public bool TransmitsClock {
                get;
                set;
        }
        public bool TransmitsMTC {
                get;
                set;
        }
        public bool TransmitsNotes {
                get;
                set;
        }
        public bool TransmitsProgramChanges {
                get;
                set;
        }
        public int UniqueID {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiEndpoint" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiEndpoint

```
public class MidiEndpoint : MidiObject {
        
        public static MidiEndpoint GetDestination (int destinationIndex);
        public static MidiEndpoint GetSource (int sourceIndex);
        public override void Dispose (bool disposing);
        public void FlushOutput ();
        public MidiError Received (MidiPacket[] packets);
        
        public int AdvanceScheduleTimeMuSec {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData ConnectionUniqueIDData {
                get;
                set;
        }
        public int ConnectionUniqueIDInt {
                get;
                set;
        }
        public string DisplayName {
                get;
                set;
        }
        public string DriverOwner {
                get;
                set;
        }
        public int DriverVersion {
                get;
                set;
        }
        public string EndpointName {
                get;
        }
        public MidiEntity Entity {
                get;
        }
        public int IsBroadcast {
                get;
                set;
        }
        public bool IsNetworkSession {
                get;
        }
        public string Manufacturer {
                get;
                set;
        }
        public int MaxSysExSpeed {
                get;
                set;
        }
        public string Name {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDictionary NameConfiguration {
                get;
                set;
        }
        public bool Offline {
                get;
                set;
        }
        public bool Private {
                get;
                set;
        }
        public int ReceiveChannels {
                get;
                set;
        }
        public int TransmitChannels {
                get;
                set;
        }
        
        public event EventHandler<midipacketseventargs> MessageReceived;
}
</midipacketseventargs>
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiEntity" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiEntity

```
public class MidiEntity : MidiObject {
        
        public MidiEndpoint GetDestination (int idx);
        public MidiEndpoint GetSource (int idx);
        
        public int AdvanceScheduleTimeMuSec {
                get;
                set;
        }
        public bool CanRoute {
                get;
                set;
        }
        public MonoTouch.Foundation.NSData ConnectionUniqueIDData {
                get;
                set;
        }
        public int ConnectionUniqueIDInt {
                get;
                set;
        }
        public int Destinations {
                get;
        }
        public MidiDevice Device {
                get;
        }
        public int DeviceID {
                get;
                set;
        }
        public string DisplayName {
                get;
                set;
        }
        public string DriverOwner {
                get;
                set;
        }
        public int DriverVersion {
                get;
                set;
        }
        public int IsBroadcast {
                get;
                set;
        }
        public bool IsDrumMachine {
                get;
        }
        public bool IsEffectUnit {
                get;
        }
        public bool IsEmbeddedEntity {
                get;
        }
        public bool IsMixer {
                get;
        }
        public bool IsSampler {
                get;
        }
        public int MaxReceiveChannels {
                get;
        }
        public int MaxSysExSpeed {
                get;
                set;
        }
        public int MaxTransmitChannels {
                get;
                set;
        }
        public string Model {
                get;
                set;
        }
        public string Name {
                get;
                set;
        }
        public MonoTouch.Foundation.NSDictionary NameConfiguration {
                get;
                set;
        }
        public bool Offline {
                get;
                set;
        }
        public bool PanDisruptsStereo {
                get;
                set;
        }
        public bool Private {
                get;
                set;
        }
        public bool ReceivesBankSelectLSB {
                get;
                set;
        }
        public bool ReceivesBankSelectMSB {
                get;
                set;
        }
        public bool ReceivesClock {
                get;
                set;
        }
        public bool ReceivesMTC {
                get;
                set;
        }
        public bool ReceivesNotes {
                get;
                set;
        }
        public bool ReceivesProgramChanges {
                get;
                set;
        }
        public int Sources {
                get;
        }
        public bool SupportsGeneralMidi {
                get;
                set;
        }
        public bool SupportsMMC {
                get;
                set;
        }
        public bool SupportsShowControl {
                get;
                set;
        }
        public bool TransmitsBankSelectLSB {
                get;
                set;
        }
        public bool TransmitsBankSelectMSB {
                get;
                set;
        }
        public bool TransmitsClock {
                get;
                set;
        }
        public bool TransmitsMTC {
                get;
                set;
        }
        public bool TransmitsNotes {
                get;
                set;
        }
        public bool TransmitsProgramChanges {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiError" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiError

```
[Serializable]
public enum MidiError {
        Ok,
        InvalidClient,
        InvalidPort,
        WrongEndpointType,
        NoConnection,
        UnknownEndpoint,
        UnknownProperty,
        WrongPropertyType,
        NoCurrentSetup,
        MessageSendErr,
        ServerStartErr,
        SetupFormatErr,
        WrongThread,
        ObjectNotFound,
        IDNotUnique
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiException" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiException

```
public class MidiException : Exception {
        
        public MidiError ErrorCode {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiNetworkConnection" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiNetworkConnection

```
public class MidiNetworkConnection : MonoTouch.Foundation.NSObject {
        
        public MidiNetworkConnection ();
        public MidiNetworkConnection (MonoTouch.Foundation.NSCoder coder);
        public MidiNetworkConnection (MonoTouch.Foundation.NSObjectFlag t);
        public MidiNetworkConnection (IntPtr handle);
        
        public static MidiNetworkConnection FromHost (MidiNetworkHost host);
        protected override void Dispose (bool disposing);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MidiNetworkHost Host {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiNetworkConnectionPolicy" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiNetworkConnectionPolicy

```
[Serializable]
public enum MidiNetworkConnectionPolicy {
        NoOne,
        HostsInContactsList,
        Anyone
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiNetworkHost" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiNetworkHost

```
public class MidiNetworkHost : MonoTouch.Foundation.NSObject {
        
        public MidiNetworkHost ();
        public MidiNetworkHost (MonoTouch.Foundation.NSCoder coder);
        public MidiNetworkHost (MonoTouch.Foundation.NSObjectFlag t);
        public MidiNetworkHost (IntPtr handle);
        
        public static MidiNetworkHost Create (string hostName, MonoTouch.Foundation.NSNetService netService);
        public static MidiNetworkHost Create (string hostName, string address, int port);
        public static MidiNetworkHost Create (string hostName, string netServiceName, string netServiceDomain);
        public virtual bool HasSameAddressAs (MidiNetworkHost other);
        
        public virtual string Address {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string Name {
                get;
        }
        public virtual string NetServiceDomain {
                get;
        }
        public virtual string NetServiceName {
                get;
        }
        public virtual int Port {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiNetworkSession" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiNetworkSession

```
public class MidiNetworkSession : MonoTouch.Foundation.NSObject {
        
        public MidiNetworkSession (MonoTouch.Foundation.NSCoder coder);
        public MidiNetworkSession (MonoTouch.Foundation.NSObjectFlag t);
        public MidiNetworkSession (IntPtr handle);
        
        public virtual bool AddConnection (MidiNetworkConnection connection);
        public virtual bool AddContact (MidiNetworkHost contact);
        protected override void Dispose (bool disposing);
        public virtual bool RemoveConnection (MidiNetworkConnection connection);
        public virtual bool RemoveContact (MidiNetworkHost contact);
        
        public static MidiNetworkSession DefaultSession {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MidiNetworkConnectionPolicy ConnectionPolicy {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSSet Connections {
                get;
        }
        public virtual MonoTouch.Foundation.NSSet Contacts {
                get;
        }
        public virtual MidiEndpoint DestinationEndpoint {
                get;
        }
        public virtual bool Enabled {
                get;
                set;
        }
        public virtual string LocalName {
                get;
        }
        public virtual string NetworkName {
                get;
        }
        public virtual int NetworkPort {
                get;
        }
        public virtual MidiEndpoint SourceEndpoint {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiObject" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiObject

```
public class MidiObject : IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public MidiObject (IntPtr handle);
        
        public void Dispose ();
        public virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public MonoTouch.Foundation.NSData GetData (IntPtr property);
        public MonoTouch.Foundation.NSDictionary GetDictionaryProperties (bool deep);
        public string GetString (IntPtr property);
        public MidiError RemoveProperty (string property);
        public void SetData (IntPtr property, MonoTouch.Foundation.NSData data);
        public void SetString (IntPtr property, string value);
        
        public IntPtr Handle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiPacket" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiPacket

```
public class MidiPacket {
        
        public MidiPacket (long timestamp, ushort length, IntPtr bytes);
        public MidiPacket (long timestamp, byte [] bytes);
        public MidiPacket (long timestamp, byte [] bytes, int start, int len);
        
        public IntPtr Bytes {
                get;
        }
        
        public long TimeStamp;
        public ushort Length;
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiPacketsEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiPacketsEventArgs

```
public class MidiPacketsEventArgs : EventArgs {
        
        public IntPtr PacketListRaw {
                get;
        }
        public MidiPacket[] Packets {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.MidiPort" class="injected"></a>


## New Type: MonoTouch.CoreMidi.MidiPort

```
public class MidiPort : MidiObject {
        
        public MidiError ConnectSource (MidiEndpoint endpoint);
        public MidiError Disconnect (MidiEndpoint endpoint);
        public override void Dispose (bool disposing);
        public MidiError Send (MidiEndpoint endpoint, MidiPacket[] packets);
        public override string ToString ();
        
        public MidiClient Client {
                get;
        }
        public string PortName {
                get;
        }
        
        public event EventHandler<midipacketseventargs> MessageReceived;
}
</midipacketseventargs>
```

 <a name="New_Type:_MonoTouch.CoreMidi.ObjectAddedOrRemovedEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreMidi.ObjectAddedOrRemovedEventArgs

```
public class ObjectAddedOrRemovedEventArgs : EventArgs {
        
        public ObjectAddedOrRemovedEventArgs (MidiObject parent, MidiObject child);
        
        public MidiObject Child {
                get;
        }
        public MidiObject Parent {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreMidi.ObjectPropertyChangedEventArgs" class="injected"></a>


## New Type: MonoTouch.CoreMidi.ObjectPropertyChangedEventArgs

```
public class ObjectPropertyChangedEventArgs : EventArgs {
        
        public ObjectPropertyChangedEventArgs (MidiObject midiObject, string propertyName);
        
        public MidiObject MidiObject {
                get;
        }
        public string PropertyName {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreMotion" class="injected"></a>


# Namespace: MonoTouch.CoreMotion

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMAttitude" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMAttitude

Removed:

```
public CMAttitude ();
```

 <a name="Type_Changed:_MonoTouch.CoreMotion.CMMotionManager" class="injected"></a>


## Type Changed: MonoTouch.CoreMotion.CMMotionManager

Removed:

```
set;
```

 <a name="Namespace:_MonoTouch.CoreServices" class="injected"></a>


# Namespace: MonoTouch.CoreServices

 <a name="New_Type:_MonoTouch.CoreServices.CFHTTPAuthentication" class="injected"></a>


## New Type: MonoTouch.CoreServices.CFHTTPAuthentication

```
public class CFHTTPAuthentication : MonoTouch.CoreFoundation.CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public static CFHTTPAuthentication CreateFromResponse (CFHTTPMessage response);
        public static int GetTypeID ();
        public bool AppliesToRequest (CFHTTPMessage request);
        protected void CheckHandle ();
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public string GetMethod ();
        
        public IntPtr Handle {
                get;
        }
        public bool IsValid {
                get;
        }
        public bool RequiresAccountDomain {
                get;
        }
        public bool RequiresOrderedRequests {
                get;
        }
        public bool RequiresUserNameAndPassword {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreServices.CFHTTPMessage" class="injected"></a>


## New Type: MonoTouch.CoreServices.CFHTTPMessage

```
public class CFHTTPMessage : MonoTouch.CoreFoundation.CFType, IDisposable, MonoTouch.ObjCRuntime.INativeObject {
        
        public static CFHTTPMessage CreateRequest (MonoTouch.CoreFoundation.CFUrl url, MonoTouch.Foundation.NSString method, Version version);
        public static CFHTTPMessage CreateRequest (Uri uri, string method);
        public static CFHTTPMessage CreateRequest (Uri uri, string method, Version version);
        public static int GetTypeID ();
        public bool AddAuthentication (CFHTTPMessage failureResponse, MonoTouch.Foundation.NSString username, MonoTouch.Foundation.NSString password, AuthenticationScheme scheme, bool forProxy);
        public void ApplyCredentialDictionary (CFHTTPAuthentication auth, System.Net.NetworkCredential credential);
        public void ApplyCredentials (CFHTTPAuthentication auth, System.Net.NetworkCredential credential);
        protected void CheckHandle ();
        public void Dispose ();
        protected virtual void Dispose (bool disposing);
        protected override void Finalize ();
        public MonoTouch.Foundation.NSDictionary GetAllHeaderFields ();
        public void SetBody (byte [] buffer);
        public void SetHeaderFieldValue (string name, string value);
        
        public IntPtr Handle {
                get;
        }
        public bool IsHeaderComplete {
                get;
        }
        public bool IsRequest {
                get;
        }
        public System.Net.HttpStatusCode ResponseStatusCode {
                get;
        }
        public string ResponseStatusLine {
                get;
        }
        public Version Version {
                get;
        }
        
        [Serializable]
        public enum AuthenticationScheme {
                Default,
                Basic,
                Negotiate,
                NTLM,
                Digest
        }
}
```

 <a name="New_Type:_MonoTouch.CoreServices.CFHTTPStream" class="injected"></a>


## New Type: MonoTouch.CoreServices.CFHTTPStream

```
public class CFHTTPStream : MonoTouch.CoreFoundation.CFReadStream {
        
        public CFHTTPMessage GetFinalRequest ();
        public CFHTTPMessage GetResponseHeader ();
        
        public bool AttemptPersistentConnection {
                get;
                set;
        }
        public Uri FinalURL {
                get;
        }
        public int RequestBytesWrittenCount {
                get;
        }
        public bool ShouldAutoredirect {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.EventKit" class="injected"></a>


# Namespace: MonoTouch.EventKit

 <a name="Type_Changed:_MonoTouch.EventKit.EKEvent" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEvent

Removed:

```
public EKEvent ();
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKEventStore" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEventStore

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveChanged (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.ExternalAccessory" class="injected"></a>


# Namespace: MonoTouch.ExternalAccessory

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EAAccessory" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EAAccessory

Removed:

```
public EAAccessory ();
```

 <a name="New_Type:_MonoTouch.ExternalAccessory.EAAccessoryEventArgs" class="injected"></a>


## New Type: MonoTouch.ExternalAccessory.EAAccessoryEventArgs

```
public class EAAccessoryEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public EAAccessoryEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public EAAccessory Accessory {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EAAccessoryManager" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EAAccessoryManager

Removed:

```
public EAAccessoryManager ();
```

Added:

```
public static MonoTouch.Foundation.NSString DidConnectNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString DidDisconnectNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidConnect (EventHandler<EAAccessoryEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidDisconnect (EventHandler<EAAccessoryEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.ExternalAccessory.EASession" class="injected"></a>


## Type Changed: MonoTouch.ExternalAccessory.EASession

Removed:

```
public EASession ();
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSArray" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSArray

Added:

```
public virtual NSArray Filter (NSPredicate predicate);
        public virtual NSArray Sort (NSComparator cmptr);
```

 <a name="New_Type:_MonoTouch.Foundation.NSAttributedRangeCallback" class="injected"></a>


## New Type: MonoTouch.Foundation.NSAttributedRangeCallback

```
[Serializable]
public delegate void NSAttributedRangeCallback (NSDictionary attrs, NSRange range, ref bool stop);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSAttributedString

Removed:

```
public static NSString BackgroundColorAttributeName {
                get;
        }
        public static NSString FontAttributeName {
                get;
        }
        public static NSString ForegroundColorAttributeName {
                get;
        }
        public static NSString LigatureAttributeName {
                get;
        }
        public static NSString ParagraphStyleAttributeName {
                get;
        }
        public static NSString StrikethroughStyleAttributeName {
                get;
        }
        public static NSString StrokeWidthAttributeName {
                get;
        }
        public static NSString UnderlineStyleAttributeName {
                get;
        }
```

Added:

```
public virtual void EnumerateAttribute (NSString attributeName, NSRange inRange, NSAttributedStringEnumeration options, NSAttributedStringCallback callback);
        public virtual void EnumerateAttributes (NSRange range, NSAttributedStringEnumeration options, NSAttributedRangeCallback callback);
```

 <a name="New_Type:_MonoTouch.Foundation.NSAttributedStringCallback" class="injected"></a>


## New Type: MonoTouch.Foundation.NSAttributedStringCallback

```
[Serializable]
public delegate void NSAttributedStringCallback (NSObject value, NSRange range, ref bool stop);
```

 <a name="New_Type:_MonoTouch.Foundation.NSAttributedStringEnumeration" class="injected"></a>


## New Type: MonoTouch.Foundation.NSAttributedStringEnumeration

```
[Serializable]
[Flags]
public enum NSAttributedStringEnumeration {
        None,
        Reverse,
        LongestEffectiveRangeNotRequired
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSBundle" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSBundle

Added:

```
public virtual string [] Localizations {
                get;
        }
        public virtual string [] PreferredLocalizations {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSCachedUrlResponse" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCachedUrlResponse

Removed:

```
public NSCachedUrlResponse ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSCalendar" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSCalendar

Removed:

```
public NSCalendar ();
```

 <a name="New_Type:_MonoTouch.Foundation.NSComparator" class="injected"></a>


## New Type: MonoTouch.Foundation.NSComparator

```
[Serializable]
public delegate int NSComparator (NSObject obj1, NSObject obj2);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDate

Removed:

```
public virtual string Description {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDecimalNumber" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDecimalNumber

Removed:

```
protected override void Dispose (bool disposing);
        public virtual NSDecimalNumber NaN {
                get;
        }
```

Added:

```
public static NSDecimalNumber NaN {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSDictionary" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSDictionary

Removed:

```
public virtual string Description {
        public virtual string DescriptionInStringsFileFormat {
```

Added:

```
public virtual string DescriptionInStringsFileFormat {
        public virtual NSObject this [NSString key] {
                get;
                set;
        }
        public virtual NSObject this [string key] {
                set;
```

 <a name="New_Type:_MonoTouch.Foundation.NSDistributedNotificationCenter" class="injected"></a>


## New Type: MonoTouch.Foundation.NSDistributedNotificationCenter

```
public class NSDistributedNotificationCenter {
        
        public NSDistributedNotificationCenter ();
        
        [Obsolete("Use AddObserver (NSObject, Selector, string, NSObject) instead")]
        public void AddObserver (NSObject observer, MonoTouch.ObjCRuntime.Selector aSelector, string aName, string anObject);
        [Obsolete("Use RemoveObserver (NSObject, string, NSObject) instead")]
        public void RemoveObserver (NSObject observer, string aName, string anObject);
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSError" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSError

Removed:

```
[Obsolete("Creating NSErrors without arguments can cause your application to crash unexpectedly if you return it back to Objective-C")]
        public NSError ();
```

Added:

```
[Obsolete("Always specify a domain and error code when creating an NSError instance")]
        public NSError ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSException" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSException

Removed:

```
public NSException ();
```

Added:

```
public NSException (string name, string reason, NSDictionary userInfo);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSExpression" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSExpression

Removed:

```
public NSExpression ();
        public virtual NSExpression FromAggregate (NSExpression[] subexpressions);
```

Added:

```
public static NSExpression FromAggregate (NSExpression[] subexpressions);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSFileVersion" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSFileVersion

Removed:

```
public NSFileVersion ();
        public virtual bool Discardable {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSHttpCookie" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSHttpCookie

Removed:

```
public NSHttpCookie ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSHttpCookieStorage" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSHttpCookieStorage

Removed:

```
public NSHttpCookieStorage ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSInputStream" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSInputStream

Added:

```
protected override void Dispose (bool disposing);
        protected virtual bool GetBuffer (out IntPtr buffer, out uint len);
        public void Notify (MonoTouch.CoreFoundation.CFStreamEventType eventType);
        public virtual int Read (IntPtr buffer, uint len);
        public virtual void ScheduleInCFRunLoop (MonoTouch.CoreFoundation.CFRunLoop runloop, NSString mode);
        protected virtual bool SetCFClientFlags (MonoTouch.CoreFoundation.CFStreamEventType inFlags, IntPtr inCallback, IntPtr inContextPtr);
        public virtual void UnscheduleInCFRunLoop (MonoTouch.CoreFoundation.CFRunLoop runloop, NSString mode);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSJsonSerialization" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSJsonSerialization

Removed:

```
public NSJsonSerialization ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSKeyedArchiver" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSKeyedArchiver

Removed:

```
public NSKeyedArchiver ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSKeyedUnarchiver" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSKeyedUnarchiver

Removed:

```
public NSKeyedUnarchiver ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSLocale" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSLocale

Removed:

```
public NSLocale ();
        public virtual string CanonicalLanguageIdentifierFromString (string str);
        public virtual string CanonicalLocaleIdentifierFromString (string str);
        public virtual NSLocaleLanguageDirection GetCharacterDirection (string isoLanguageCode);
        public virtual NSLocaleLanguageDirection GetLineDirection (string isoLanguageCode);
        public virtual string LocaleIdentifierFromComponents (NSDictionary dict);
```

Added:

```
public static string CanonicalLanguageIdentifierFromString (string str);
        public static string CanonicalLocaleIdentifierFromString (string str);
        public static NSLocaleLanguageDirection GetCharacterDirection (string isoLanguageCode);
        public static NSLocaleLanguageDirection GetLineDirection (string isoLanguageCode);
        public static string LocaleIdentifierFromComponents (NSDictionary dict);
        public string GetCountryCodeDisplayName (string value);
        public string GetCurrencyCodeDisplayName (string value);
        public string GetIdentifierDisplayName (string value);
        public string GetLanguageCodeDisplayName (string value);
        
        public static class Notifications {
                
                public static NSObject ObserveCurrentLocaleDidChange (EventHandler<NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMetadataQuery" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMetadataQuery

Removed:

```
public static NSString LocalComputerScope {
                get;
        }
        public static NSString QueryLocalDocumentsScope {
                get;
        }
        public static NSString QueryNetworkScope {
                get;
        }
        public static NSString UserHomeScope {
                get;
        }
```

Added:

```
public static class Notifications {
                
                public static NSObject ObserveDidFinishGathering (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidStartGathering (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidUpdate (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveGatheringProgress (EventHandler<NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSMutableDictionary" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSMutableDictionary

Added:

```
public override NSObject this [string key] {
                get;
                set;
        }
        public override NSObject this [NSString key] {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNotification" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNotification

Removed:

```
public NSNotification ();
```

 <a name="New_Type:_MonoTouch.Foundation.NSNotificationEventArgs" class="injected"></a>


## New Type: MonoTouch.Foundation.NSNotificationEventArgs

```
public class NSNotificationEventArgs : EventArgs {
        
        public NSNotificationEventArgs (NSNotification notification);
        
        public NSNotification Notification {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumber" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumber

Removed:

```
public NSNumber ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumberFormatter" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumberFormatter

Removed:

```
public virtual string LocalizedStringFromNumbernumberStyle (NSNumber num, NSNumberFormatterStyle nstyle);
```

Added:

```
public static string LocalizedStringFromNumbernumberStyle (NSNumber num, NSNumberFormatterStyle nstyle);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSObject

Removed:

```
public static NSObject GetDefaultPlaceholder (NSObject marker, string binding);
```

Added:

```
public virtual NSObject Copy ();
        public virtual NSObject MutableCopy ();
        public virtual void PerformSelector (MonoTouch.ObjCRuntime.Selector sel, NSObject obj, double delay);
        public override string ToString ();
        public virtual string DebugDescription {
                get;
        }
        public virtual string Description {
                get;
        }
        public virtual int RetainCount {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSOrthography" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSOrthography

Removed:

```
public NSOrthography ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSPredicate" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSPredicate

Removed:

```
public NSPredicate ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRange" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRange

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSRunLoop" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSRunLoop

Removed:

```
public NSRunLoop ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSSet" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSSet

Removed:

```
public class NSSet : NSObject {
        public virtual string Description {
                get;
        }
```

Added:

```
public class NSSet : NSObject, System.Collections.IEnumerable, System.Collections.Generic.IEnumerable<NSObject> {
        public System.Collections.Generic.IEnumerator<NSObject> GetEnumerator ();
        System.Collections.IEnumerator System.Collections.IEnumerable.GetEnumerator ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSString

Added:

```
public static IntPtr CreateNative (string str);
        public static void ReleaseNative (IntPtr handle);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSThread" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSThread

Removed:

```
protected override void Dispose (bool disposing);
        public virtual NSThread MainThread {
                get;
        }
```

Added:

```
public static NSThread MainThread {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimeZone" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimeZone

Removed:

```
public NSTimeZone ();
        public virtual string Description {
                get;
        }
```

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSTimer" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSTimer

Removed:

```
public NSTimer ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUbiquitousKeyValueStore" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUbiquitousKeyValueStore

Added:

```
public static class Notifications {
                
                public static NSObject ObserveDidChangeExternally (EventHandler<NSUbiquitousKeyValueStoreChangeEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSUbiquitousKeyValueStoreChangeEventArgs" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUbiquitousKeyValueStoreChangeEventArgs

```
public class NSUbiquitousKeyValueStoreChangeEventArgs : NSNotificationEventArgs {
        
        public NSUbiquitousKeyValueStoreChangeEventArgs (NSNotification notification);
        
        public string [] ChangedKeys {
                get;
        }
        public NSUbiquitousKeyValueStoreChangeReason ChangeReason {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUndoManager" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUndoManager

Added:

```
public static class Notifications {
                
                public static NSObject ObserveCheckpoint (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidCloseUndoGroup (EventHandler<NSUndoManagerCloseUndoGroupEventArgs> handler);
                public static NSObject ObserveDidOpenUndoGroup (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidRedoChange (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveDidUndoChange (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveWillCloseUndoGroup (EventHandler<NSUndoManagerCloseUndoGroupEventArgs> handler);
                public static NSObject ObserveWillRedoChange (EventHandler<NSNotificationEventArgs> handler);
                public static NSObject ObserveWillUndoChange (EventHandler<NSNotificationEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSUndoManagerCloseUndoGroupEventArgs" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUndoManagerCloseUndoGroupEventArgs

```
public class NSUndoManagerCloseUndoGroupEventArgs : NSNotificationEventArgs {
        
        public NSUndoManagerCloseUndoGroupEventArgs (NSNotification notification);
        
        public Nullable<bool> Discardable {
                get;
        }
}
</bool>
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrl" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrl

Removed:

```
public NSUrl ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlAuthenticationChallenge" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlAuthenticationChallenge

Removed:

```
public NSUrlAuthenticationChallenge ();
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlCredential" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlCredential

Removed:

```
public NSUrlCredential ();
```

 <a name="New_Type:_MonoTouch.Foundation.NSUrlCredentialStorage" class="injected"></a>


## New Type: MonoTouch.Foundation.NSUrlCredentialStorage

```
public class NSUrlCredentialStorage : NSObject {
        
        public NSUrlCredentialStorage (NSCoder coder);
        public NSUrlCredentialStorage (NSObjectFlag t);
        public NSUrlCredentialStorage (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual NSDictionary GetCredentials (NSUrlProtectionSpace forProtectionSpace);
        public virtual NSUrlCredential GetDefaultCredential (NSUrlProtectionSpace forProtectionSpace);
        public virtual void RemoveCredential (NSUrlCredential credential, NSUrlProtectionSpace forProtectionSpace);
        public virtual void SetCredential (NSUrlCredential credential, NSUrlProtectionSpace forProtectionSpace);
        public virtual void SetDefaultCredential (NSUrlCredential credential, NSUrlProtectionSpace forProtectionSpace);
        
        public static NSUrlCredentialStorage SharedCredentialStorage {
                get;
        }
        public virtual NSDictionary AllCredentials {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtectionSpace" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtectionSpace

Removed:

```
public NSUrlProtectionSpace ();
```

Added:

```
public static NSString AuthenticationMethodClientCertificate {
                get;
        }
        public static NSString AuthenticationMethodDefault {
                get;
        }
        public static NSString AuthenticationMethodHTMLForm {
                get;
        }
        public static NSString AuthenticationMethodHTTPBasic {
                get;
        }
        public static NSString AuthenticationMethodHTTPDigest {
                get;
        }
        public static NSString AuthenticationMethodNegotiat {
                get;
        }
        public static NSString AuthenticationMethodNTL {
                get;
        }
        public static NSString AuthenticationMethodServerTrus {
                get;
        }
        public static NSString FTP {
                get;
        }
        public static NSString FTPProxy {
                get;
        }
        public static NSString HTTP {
                get;
        }
        public static NSString HTTPProxy {
                get;
        }
        public static NSString HTTPS {
                get;
        }
        public static NSString HTTPSProxy {
                get;
        }
        public static NSString SOCKSProxy {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocol" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocol

Removed:

```
public class NSUrlProtocol : NSObject {
                set;
        
        public event EventHandler<NSUrlProtocolCachedResponseEventArgs> CachedResponseIsValid;
        public event EventHandler<NSUrlProtocolChallengeEventArgs> CancelledAuthenticationChallenge;
        public event EventHandler<NSUrlProtocolDataEventArgs> DataLoaded;
        public event EventHandler<NSUrlProtocolErrorEventArgs> FailedWithError;
        public event EventHandler FinishedLoading;
        public event EventHandler<NSUrlProtocolChallengeEventArgs> ReceivedAuthenticationChallenge;
        public event EventHandler<NSUrlProtocolResponseEventArgs> ReceivedResponse;
        public event EventHandler<NSUrlProtocolRedirectEventArgs> Redirected;
```

Added:

```
public abstract class NSUrlProtocol : NSObject {
```

 <a name="Type_Removed:_MonoTouch.Foundation.NSUrlProtocolCachedResponseEventArgs" class="injected"></a>


## Type Removed: MonoTouch.Foundation.NSUrlProtocolCachedResponseEventArgs

 <a name="Type_Removed:_MonoTouch.Foundation.NSUrlProtocolChallengeEventArgs" class="injected"></a>


## Type Removed: MonoTouch.Foundation.NSUrlProtocolChallengeEventArgs

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtocolClient" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtocolClient

Removed:

```
public abstract class NSUrlProtocolClient : NSObject {
        public NSUrlProtocolClient ();
        public NSUrlProtocolClient (NSCoder coder);
        public NSUrlProtocolClient (NSObjectFlag t);
        public abstract void CachedResponseIsValid (NSUrlProtocol protocol, NSCachedUrlResponse cachedResponse);
        public abstract void CancelledAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public abstract void DataLoaded (NSUrlProtocol protocol, NSData data);
        public abstract void FailedWithError (NSUrlProtocol protocol, NSError error);
        public abstract void FinishedLoading (NSUrlProtocol protocol);
        public abstract void ReceivedAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public abstract void ReceivedResponse (NSUrlProtocol protocol, NSUrlResponse response, NSUrlCacheStoragePolicy policy);
        public abstract void Redirected (NSUrlProtocol protocol, NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
```

Added:

```
public sealed class NSUrlProtocolClient : NSObject {
        public void CachedResponseIsValid (NSUrlProtocol protocol, NSCachedUrlResponse cachedResponse);
        public void CancelledAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public void DataLoaded (NSUrlProtocol protocol, NSData data);
        public void FailedWithError (NSUrlProtocol protocol, NSError error);
        public void FinishedLoading (NSUrlProtocol protocol);
        public void ReceivedAuthenticationChallenge (NSUrlProtocol protocol, NSUrlAuthenticationChallenge challenge);
        public void ReceivedResponse (NSUrlProtocol protocol, NSUrlResponse response, NSUrlCacheStoragePolicy policy);
        public void Redirected (NSUrlProtocol protocol, NSUrlRequest redirectedToEequest, NSUrlResponse redirectResponse);
```

 <a name="Type_Removed:_MonoTouch.Foundation.NSUrlProtocolDataEventArgs" class="injected"></a>


## Type Removed: MonoTouch.Foundation.NSUrlProtocolDataEventArgs

 <a name="Type_Removed:_MonoTouch.Foundation.NSUrlProtocolErrorEventArgs" class="injected"></a>


## Type Removed: MonoTouch.Foundation.NSUrlProtocolErrorEventArgs

 <a name="Type_Removed:_MonoTouch.Foundation.NSUrlProtocolRedirectEventArgs" class="injected"></a>


## Type Removed: MonoTouch.Foundation.NSUrlProtocolRedirectEventArgs

 <a name="Type_Removed:_MonoTouch.Foundation.NSUrlProtocolResponseEventArgs" class="injected"></a>


## Type Removed: MonoTouch.Foundation.NSUrlProtocolResponseEventArgs

 <a name="Type_Changed:_MonoTouch.Foundation.NSValue" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSValue

Removed:

```
public NSValue ();
```

 <a name="Namespace:_MonoTouch.GLKit" class="injected"></a>


# Namespace: MonoTouch.GLKit

 <a name="Type_Changed:_MonoTouch.GLKit.GLKEffectPropertyTransform" class="injected"></a>


## Type Changed: MonoTouch.GLKit.GLKEffectPropertyTransform

Removed:

```
public virtual OpenTK.Matrix4 TextureMatrix {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.GLKit.GLKTextureInfo" class="injected"></a>


## Type Changed: MonoTouch.GLKit.GLKTextureInfo

Removed:

```
public virtual uint TextureName {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.GLKit.GLKView" class="injected"></a>


## Type Changed: MonoTouch.GLKit.GLKView

Removed:

```
public virtual MonoTouch.Foundation.NSObject InitWithFramecontext (System.Drawing.RectangleF frame, MonoTouch.OpenGLES.EAGLContext context);
```

Added:

```
public GLKView (System.Drawing.RectangleF frame, MonoTouch.OpenGLES.EAGLContext context);
        public event EventHandler<GLKViewDrawEventArgs> DrawInRect;
```

 <a name="Type_Changed:_MonoTouch.GLKit.GLKViewController" class="injected"></a>


## Type Changed: MonoTouch.GLKit.GLKViewController

Added:

```
public virtual void Update ();
```

 <a name="New_Type:_MonoTouch.GLKit.GLKViewDrawEventArgs" class="injected"></a>


## New Type: MonoTouch.GLKit.GLKViewDrawEventArgs

```
public class GLKViewDrawEventArgs : EventArgs {
        
        public GLKViewDrawEventArgs (System.Drawing.RectangleF rect);
        
        public System.Drawing.RectangleF Rect {
                get;
                set;
        }
}
```

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievement" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievement

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementDescription" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementDescription

Removed:

```
public virtual MonoTouch.UIKit.UIImage IncompleteAchievementImage {
                get;
        }
```

Added:

```
public static MonoTouch.UIKit.UIImage IncompleteAchievementImage {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKFriendRequestComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Removed:

```
public virtual void AddRecipientsFromAliases (string [] aliases);
        public virtual void AddRecipientsFromPlayerIDs (string [] emailAddresses);
```

Added:

```
public virtual void AddRecipientsFromPlayerIDs (string [] playerIDs);
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKLocalPlayer" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLocalPlayer

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveAuthenticationDidChangeNotificationName (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKMatch" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKMatch

Removed:

```
public GKMatch ();
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPeerPickerController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPeerPickerController

Removed:

```
set;
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKPlayer" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKPlayer

Removed:

```
public static MonoTouch.Foundation.NSString DidChangeNotificationName {
```

Added:

```
public static MonoTouch.Foundation.NSString DidChangeNotificationNameNotification {
        public MonoTouch.Foundation.NSString DidChangeNotificationName {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidChangeNotificationName (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.ImageIO" class="injected"></a>


# Namespace: MonoTouch.ImageIO

 <a name="New_Type:_MonoTouch.ImageIO.CGImageProperties" class="injected"></a>


## New Type: MonoTouch.ImageIO.CGImageProperties

```
public class CGImageProperties {
        
        public CGImageProperties ();
        
        public static MonoTouch.Foundation.NSString CIFFCameraSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFContinuousDrive {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFFirmware {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFFlashExposureComp {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFFocusMode {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFImageFileName {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFImageName {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFImageSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFLensMaxMM {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFLensMinMM {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFLensModel {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFMeasuredEV {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFMeteringMode {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFOwnerName {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFRecordID {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFReleaseMethod {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFReleaseTiming {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFSelfTimingTime {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFShootingMode {
                get;
        }
        public static MonoTouch.Foundation.NSString CIFFWhiteBalanceIndex {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModel {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModelCMYK {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModelGray {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModelLab {
                get;
        }
        public static MonoTouch.Foundation.NSString ColorModelRGB {
                get;
        }
        public static MonoTouch.Foundation.NSString Depth {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGBackwardVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGCameraSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGLensInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGLocalizedCameraModel {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGUniqueCameraModel {
                get;
        }
        public static MonoTouch.Foundation.NSString DNGVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString DPIHeight {
                get;
        }
        public static MonoTouch.Foundation.NSString DPIWidth {
                get;
        }
        public static MonoTouch.Foundation.NSString EightBIMDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString EightBIMLayerNames {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifApertureValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxFirmware {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxFlashCompensation {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxImageNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxLensID {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxLensInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxLensModel {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxLensSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxOwnerName {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifAuxSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifBodySerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifBrightnessValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifCameraOwnerName {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifCFAPattern {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifColorSpace {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifComponentsConfiguration {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifCompressedBitsPerPixel {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifContrast {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifCustomRendered {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDateTimeDigitized {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDateTimeOriginal {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDeviceSettingDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifDigitalZoomRatio {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureBiasValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureIndex {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureMode {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureProgram {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifExposureTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFileSource {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFlash {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFlashEnergy {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFlashPixVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalLength {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalLenIn35mmFilm {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalPlaneResolutionUnit {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalPlaneXResolution {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifFocalPlaneYResolution {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifGainControl {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifGamma {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifImageUniqueID {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifISOSpeedRatings {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLensMake {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLensModel {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLensSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLensSpecification {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifLightSource {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifMakerNote {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifMaxApertureValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifMeteringMode {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifOECF {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifPixelXDimension {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifPixelYDimension {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifRelatedSoundFile {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSaturation {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSceneCaptureType {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSceneType {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSensingMethod {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSharpness {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifShutterSpeedValue {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSpatialFrequencyResponse {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSpectralSensitivity {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubjectArea {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubjectDistance {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubjectDistRange {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubjectLocation {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubsecTime {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubsecTimeDigitized {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifSubsecTimeOrginal {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifUserComment {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString ExifWhiteBalance {
                get;
        }
        public static MonoTouch.Foundation.NSString FileSize {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFDelayTime {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFHasGlobalColorMap {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFImageColorMap {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFLoopCount {
                get;
        }
        public static MonoTouch.Foundation.NSString GIFUnclampedDelayTime {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSAltitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSAltitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSAreaInformation {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDateStamp {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestBearing {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestBearingRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestDistance {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestDistanceRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestLatitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestLatitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestLongitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDestLongitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDifferental {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSDOP {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSImgDirection {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSImgDirectionRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSLatitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSLatitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSLongitude {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSLongitudeRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSMapDatum {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSMeasureMode {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSSatellites {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSSpeed {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSSpeedRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSStatus {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSTimeStamp {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSTrack {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSTrackRef {
                get;
        }
        public static MonoTouch.Foundation.NSString GPSVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString HasAlpha {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCActionAdvised {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCByline {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCBylineTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCaptionAbstract {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCategory {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCity {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContact {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoAddress {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoCity {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoCountry {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoEmails {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoPhones {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoPostalCode {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoStateProvince {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContactInfoWebURLs {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContentLocationCode {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCContentLocationName {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCopyrightNotice {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCountryPrimaryLocationCode {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCountryPrimaryLocationName {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCreatorContactInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCCredit {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCDateCreated {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCDigitalCreationDate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCDigitalCreationTime {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCEditorialUpdate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCEditStatus {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCExpirationDate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCExpirationTime {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCFixtureIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCHeadline {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCImageOrientation {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCImageType {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCKeywords {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCLanguageIdentifier {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCObjectAttributeReference {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCObjectCycle {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCObjectName {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCObjectTypeReference {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCOriginalTransmissionReference {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCOriginatingProgram {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCProgramVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCProvinceState {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReferenceDate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReferenceNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReferenceService {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReleaseDate {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCReleaseTime {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCRightsUsageTerms {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCScene {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSource {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSpecialInstructions {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCStarRating {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSubjectReference {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSubLocation {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCSupplementalCategory {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCTimeCreated {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCUrgency {
                get;
        }
        public static MonoTouch.Foundation.NSString IPTCWriterEditor {
                get;
        }
        public static MonoTouch.Foundation.NSString IsFloat {
                get;
        }
        public static MonoTouch.Foundation.NSString IsIndexed {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFDensityUnit {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFIsProgressive {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFVersion {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFXDensity {
                get;
        }
        public static MonoTouch.Foundation.NSString JFIFYDensity {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonAspectRatioInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonCameraSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonContinuousDrive {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonFirmware {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonFlashExposureComp {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonImageSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonLensModel {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerCanonOwnerName {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerFujiDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerMinoltaDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonCameraSerialNumber {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonColorMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonDigitalZoom {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonFlashExposureComp {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonFlashSetting {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonFocusDistance {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonFocusMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonImageAdjustment {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonISOSelection {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonISOSetting {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonLensAdapter {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonLensInfo {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonLensType {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonQuality {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonSharpenMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonShootingMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonShutterCount {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerNikonWhiteBalanceMode {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerOlympusDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString MakerPentaxDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString Orientation {
                get;
        }
        public static MonoTouch.Foundation.NSString PixelHeight {
                get;
        }
        public static MonoTouch.Foundation.NSString PixelWidth {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGAuthor {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGChromaticities {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGCopyright {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGCreationTime {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGGamma {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGInterlaceType {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGModificationTime {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGSoftware {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGsRGBIntent {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGTitle {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGXPixelsPerMeter {
                get;
        }
        public static MonoTouch.Foundation.NSString PNGYPixelsPerMeter {
                get;
        }
        public static MonoTouch.Foundation.NSString ProfileName {
                get;
        }
        public static MonoTouch.Foundation.NSString RawDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFArtist {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFCompression {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFDateTime {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFDictionary {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFDocumentName {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFHostComputer {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFImageDescription {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFMake {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFModel {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFOrientation {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFPhotometricInterpretation {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFPrimaryChromaticities {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFResolutionUnit {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFSoftware {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFTransferFunction {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFWhitePoint {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFXResolution {
                get;
        }
        public static MonoTouch.Foundation.NSString TIFFYResolution {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.ImageIO.CGImageSource" class="injected"></a>


## Type Changed: MonoTouch.ImageIO.CGImageSource

Added:

```
public MonoTouch.Foundation.NSDictionary CopyProperties (CGImageOptions options);
        public MonoTouch.Foundation.NSDictionary CopyProperties (CGImageOptions options, int imageIndex);
```

 <a name="Namespace:_MonoTouch.MapKit" class="injected"></a>


# Namespace: MonoTouch.MapKit

 <a name="Type_Changed:_MonoTouch.MapKit.MKMapView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKMapView

Removed:

```
public void AddAnnotation (MKAnnotation[] annotations);
        public void AddAnnotation (MKPlacemark[] placemarks);
        public virtual MKCoordinateRegion ConvertRect (System.Drawing.RectangleF rect, MonoTouch.UIKit.UIView toRegiontFromView);
```

Added:

```
[Obsolete("Use AddAnnotations")]
        public void AddAnnotation (MKAnnotation[] annotations);
        [Obsolete("Use AddPlacemarks")]
        public void AddAnnotation (MKPlacemark[] placemarks);
        public void AddPlacemarks (MKPlacemark[] placemarks);
        public virtual MKCoordinateRegion ConvertRect (System.Drawing.RectangleF rect, MonoTouch.UIKit.UIView toRegionFromView);
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPinAnnotationView" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPinAnnotationView

Removed:

```
public MKPinAnnotationView ();
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKPlacemark" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKPlacemark

Removed:

```
public MKPlacemark ();
```

 <a name="Type_Changed:_MonoTouch.MapKit.MKReverseGeocoder" class="injected"></a>


## Type Changed: MonoTouch.MapKit.MKReverseGeocoder

Removed:

```
public MKReverseGeocoder ();
```

 <a name="Namespace:_MonoTouch.MediaPlayer" class="injected"></a>


# Namespace: MonoTouch.MediaPlayer

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItem" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItem

Added:

```
public MonoTouch.Foundation.NSString AlbumArtist {
                get;
        }
        public ulong AlbumArtistPersistentID {
                get;
        }
        public ulong AlbumPersistentID {
                get;
        }
        public MonoTouch.Foundation.NSString AlbumTitle {
                get;
        }
        public int AlbumTrackCount {
                get;
        }
        public int AlbumTrackNumber {
                get;
        }
        public MonoTouch.Foundation.NSString Artist {
                get;
        }
        public ulong ArtistPersistentID {
                get;
        }
        public MPMediaItemArtwork Artwork {
                get;
        }
        public MonoTouch.Foundation.NSUrl AssetURL {
                get;
        }
        public uint BeatsPerMinute {
                get;
        }
        public MonoTouch.Foundation.NSString Comments {
                get;
        }
        public MonoTouch.Foundation.NSString Composer {
                get;
        }
        public ulong ComposerPersistentID {
                get;
        }
        public int DiscCount {
                get;
        }
        public int DiscNumber {
                get;
        }
        public MonoTouch.Foundation.NSString Genre {
                get;
        }
        public ulong GenrePersistentID {
                get;
        }
        public bool IsCompilation {
                get;
        }
        public MonoTouch.Foundation.NSDate LastPlayedDate {
                get;
        }
        public MonoTouch.Foundation.NSString Lyrics {
                get;
        }
        public MPMediaType MediaType {
                get;
        }
        public ulong PersistentID {
                get;
        }
        public double PlaybackDuration {
                get;
        }
        public int PlayCount {
                get;
        }
        public ulong PodcastPersistentID {
                get;
        }
        public MonoTouch.Foundation.NSString PodcastTitle {
                get;
        }
        public uint Rating {
                get;
        }
        public MonoTouch.Foundation.NSDate ReleaseDate {
                get;
        }
        public int SkipCount {
                get;
        }
        public MonoTouch.Foundation.NSString Title {
                get;
        }
        public MonoTouch.Foundation.NSString UserGrouping {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaItemCollection" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaItemCollection

Removed:

```
public MPMediaItemCollection ();
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaLibrary" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaLibrary

Removed:

```
public static readonly MonoTouch.Foundation.NSString DidChangeNotification;
        public static readonly MonoTouch.Foundation.NSString ChangeTypePlaylists;
        public static readonly MonoTouch.Foundation.NSString ChangeTypesUserInfoKey;
```

Added:

```
public static MonoTouch.Foundation.NSString DidChangeNotification {
                get;
        }
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaPlaylist" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaPlaylist

Removed:

```
public MPMediaPlaylist ();
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMediaQuerySection" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMediaQuerySection

Removed:

```
public MPMediaQuerySection ();
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMoviePlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMoviePlayerController

Removed:

```
public virtual MonoTouch.UIKit.UIColor BackgroundColor {
        public virtual MPMovieControlMode MovieControlMode {
```

Added:

```
public static MonoTouch.Foundation.NSString MediaPlaybackIsPreparedToPlayDidChangeNotification {
                get;
        }
        [Obsolete("Removed in iOS 3.2")]
        public virtual MonoTouch.UIKit.UIColor BackgroundColor {
        [Obsolete("Removed in iOS 3.2")]
        public virtual MPMovieControlMode MovieControlMode {
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidEnterFullscreen (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidExitFullscreen (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDurationAvailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveLoadStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveMediaPlaybackIsPreparedToPlayDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveNaturalSizeAvailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveNowPlayingMovieDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObservePlaybackDidFinish (EventHandler<MPMoviePlayerFinishedEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObservePlaybackStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveScalingModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveSourceTypeAvailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveThumbnailImageRequestDidFinish (EventHandler<MPMoviePlayerThumbnailEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTimedMetadataUpdated (EventHandler<MPMoviePlayerTimedMetadataEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillEnterFullscreen (EventHandler<MPMoviePlayerFullScreenEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillExitFullscreen (EventHandler<MPMoviePlayerFullScreenEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMoviePlayerFinishedEventArgs" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMoviePlayerFinishedEventArgs

```
public class MPMoviePlayerFinishedEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MPMoviePlayerFinishedEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MPMovieFinishReason FinishReason {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMoviePlayerFullScreenEventArgs" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMoviePlayerFullScreenEventArgs

```
public class MPMoviePlayerFullScreenEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MPMoviePlayerFullScreenEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MonoTouch.UIKit.UIViewAnimationCurve AnimationCurve {
                get;
        }
        public double AnimationDuration {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMoviePlayerThumbnailEventArgs" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMoviePlayerThumbnailEventArgs

```
public class MPMoviePlayerThumbnailEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MPMoviePlayerThumbnailEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MonoTouch.Foundation.NSError Error {
                get;
        }
        public MonoTouch.UIKit.UIImage Image {
                get;
        }
        public double Time {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.MediaPlayer.MPMoviePlayerTimedMetadataEventArgs" class="injected"></a>


## New Type: MonoTouch.MediaPlayer.MPMoviePlayerTimedMetadataEventArgs

```
public class MPMoviePlayerTimedMetadataEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MPMoviePlayerTimedMetadataEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public MPTimedMetadata[] TimedMetadata {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPMusicPlayerController" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPMusicPlayerController

Added:

```
public static MonoTouch.Foundation.NSString NowPlayingItemDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString PlaybackStateDidChangeNotification {
                get;
        }
        public static MonoTouch.Foundation.NSString VolumeDidChangeNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveNowPlayingItemDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObservePlaybackStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveVolumeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPNowPlayingInfoCenter" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPNowPlayingInfoCenter

Removed:

```
public MPNowPlayingInfoCenter ();
```

 <a name="Type_Changed:_MonoTouch.MediaPlayer.MPTimedMetadata" class="injected"></a>


## Type Changed: MonoTouch.MediaPlayer.MPTimedMetadata

Removed:

```
public MPTimedMetadata ();
```

 <a name="Namespace:_MonoTouch.MessageUI" class="injected"></a>


# Namespace: MonoTouch.MessageUI

 <a name="New_Type:_MonoTouch.MessageUI.MFMessageAvailabilityChangedEventArgs" class="injected"></a>


## New Type: MonoTouch.MessageUI.MFMessageAvailabilityChangedEventArgs

```
public class MFMessageAvailabilityChangedEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public MFMessageAvailabilityChangedEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public bool TextMessageAvailability {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.MessageUI.MFMessageComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveTextMessageAvailabilityDidChange (EventHandler<MFMessageAvailabilityChangedEventArgs> handler);
        }
```

 <a name="Namespace:_MonoTouch.NewsstandKit" class="injected"></a>


# Namespace: MonoTouch.NewsstandKit

 <a name="Type_Changed:_MonoTouch.NewsstandKit.NKAssetDownload" class="injected"></a>


## Type Changed: MonoTouch.NewsstandKit.NKAssetDownload

Removed:

```
public NKAssetDownload ();
```

 <a name="Type_Changed:_MonoTouch.NewsstandKit.NKIssue" class="injected"></a>


## Type Changed: MonoTouch.NewsstandKit.NKIssue

Removed:

```
public NKIssue ();
```

Added:

```
public static MonoTouch.Foundation.NSString DownloadCompletedNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDownloadCompleted (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.NewsstandKit.NKLibrary" class="injected"></a>


## Type Changed: MonoTouch.NewsstandKit.NKLibrary

Removed:

```
public NKLibrary ();
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

Added:

```
public static IntPtr IntPtr_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6);
        public static IntPtr IntPtr_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6);
        public static void void_objc_msgSend_intptr_intptr_double (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3);
        public static void void_objc_msgSend_IntPtr_NSRange_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, IntPtr arg4);
        public static void void_objc_msgSendSuper_intptr_intptr_double (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3);
        public static void void_objc_msgSendSuper_IntPtr_NSRange_int_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, MonoTouch.Foundation.NSRange arg2, int arg3, IntPtr arg4);
```

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Runtime" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Runtime

Added:

```
public static void StartWWAN (Uri uri, Action<Exception> callback);
```

 <a name="New_Type:_MonoTouch.ObjCRuntime.ThreadSafeAttribute" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.ThreadSafeAttribute

```
public class ThreadSafeAttribute : Attribute {
        
        public ThreadSafeAttribute ();
}
```

 <a name="Namespace:_MonoTouch.OpenGLES" class="injected"></a>


# Namespace: MonoTouch.OpenGLES

 <a name="Type_Changed:_MonoTouch.OpenGLES.EAGLSharegroup" class="injected"></a>


## Type Changed: MonoTouch.OpenGLES.EAGLSharegroup

Removed:

```
public EAGLSharegroup ();
```

 <a name="Namespace:_MonoTouch.StoreKit" class="injected"></a>


# Namespace: MonoTouch.StoreKit

 <a name="Type_Changed:_MonoTouch.StoreKit.SKMutablePayment" class="injected"></a>


## Type Changed: MonoTouch.StoreKit.SKMutablePayment

Added:

```
public static SKMutablePayment PaymentWithProduct (SKProduct product);
        public static SKMutablePayment PaymentWithProduct (string identifier);
```

 <a name="Namespace:_MonoTouch.SystemConfiguration" class="injected"></a>


# Namespace: MonoTouch.SystemConfiguration

 <a name="Type_Changed:_MonoTouch.SystemConfiguration.CaptiveNetwork" class="injected"></a>


## Type Changed: MonoTouch.SystemConfiguration.CaptiveNetwork

Removed:

```
public class CaptiveNetwork {
        public CaptiveNetwork ();
        
        public static MonoTouch.Foundation.NSDictionary CopyCurrentNetworkInfo (string interfaceName);
        public static string [] GetSupportedInterfaces ();
```

Added:

```
public static class CaptiveNetwork {
        [Obsolete("Replaced by TryCopyCurrentNetworkInfo")]
        public static MonoTouch.Foundation.NSDictionary CopyCurrentNetworkInfo (string interfaceName);
        [Obsolete("Replaced by TryGetSupportedInterfaces")]
        public static string [] GetSupportedInterfaces ();
        public static StatusCode TryCopyCurrentNetworkInfo (string interfaceName, out MonoTouch.Foundation.NSDictionary currentNetworkInfo);
        public static StatusCode TryGetSupportedInterfaces (out string [] supportedInterfaces);
```

 <a name="Type_Changed:_MonoTouch.SystemConfiguration.NetworkReachability" class="injected"></a>


## Type Changed: MonoTouch.SystemConfiguration.NetworkReachability

Removed:

```
public bool SetCallback (Notification callback);
```

Added:

```
public NetworkReachability (System.Net.IPAddress localAddress, System.Net.IPAddress remoteAddress);
        public StatusCode GetFlags (out NetworkReachabilityFlags flags);
        [Obsolete("Replaced by SetNotification")]
        public bool SetCallback (Notification callback);
        public StatusCode SetNotification (Notification callback);
```

 <a name="New_Type:_MonoTouch.SystemConfiguration.StatusCode" class="injected"></a>


## New Type: MonoTouch.SystemConfiguration.StatusCode

```
[Serializable]
public enum StatusCode {
        OK,
        Failed,
        InvalidArgument,
        AccessError,
        NoKey,
        KeyExists,
        Locked,
        NeedLock,
        NoStoreSession,
        NoStoreServer,
        NotifierActive,
        NoPrefsSession,
        PrefsBusy,
        NoConfigFile,
        NoLink,
        Stale,
        MaxLink,
        ReachabilityUnknown,
        ConnectionNoService
}
```

 <a name="New_Type:_MonoTouch.SystemConfiguration.StatusCodeError" class="injected"></a>


## New Type: MonoTouch.SystemConfiguration.StatusCodeError

```
public static class StatusCodeError {
        
        public static string GetErrorDescription (StatusCode statusCode);
}
```

 <a name="New_Type:_MonoTouch.SystemConfiguration.SystemConfigurationException" class="injected"></a>


## New Type: MonoTouch.SystemConfiguration.SystemConfigurationException

```
public class SystemConfigurationException : Exception {
        
        public SystemConfigurationException (StatusCode statusErrorCode);
        
        public StatusCode StatusErrorCode {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIAppearance" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIAppearance

Removed:

```
public UIAppearance ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplication

Removed:

```
public static MonoTouch.Foundation.NSString MinimumKeepAliveTimeout {
                set;
```

Added:

```
public static void EnsureUIThread ();
        public static double MinimumKeepAliveTimeout {
        
        public static bool CheckForIllegalCrossThreadCalls;
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidBecomeActive (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidChangeStatusBarFrame (EventHandler<UIStatusBarFrameChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidChangeStatusBarOrientation (EventHandler<UIStatusBarOrientationChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidEnterBackground (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidFinishLaunching (EventHandler<UIApplicationLaunchEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidReceiveMemoryWarning (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveProtectedDataDidBecomeAvailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveProtectedDataWillBecomeUnavailable (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveSignificantTimeChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillChangeStatusBarFrame (EventHandler<UIStatusBarFrameChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillChangeStatusBarOrientation (EventHandler<UIStatusBarOrientationChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillEnterForeground (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillResignActive (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillTerminate (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIApplicationLaunchEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.UIApplicationLaunchEventArgs

```
public class UIApplicationLaunchEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIApplicationLaunchEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public bool LocationLaunch {
                get;
        }
        public MonoTouch.Foundation.NSDictionary RemoteNotifications {
                get;
        }
        public string SourceApplication {
                get;
        }
        public MonoTouch.Foundation.NSUrl Url {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIBezierPath" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIBezierPath

 <a name="Type_Changed:_MonoTouch.UIKit.UIButton" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIButton

Added:

```
public UIButton (UIButtonType type);
                public virtual UIImage BackgroundImageForState (UIControlState state);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIColor" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIColor

Removed:

```
public UIColor ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDatePicker" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDatePicker

Removed:

```
public virtual MonoTouch.Foundation.NSLocale Locale {
```

Added:

```
[Obsolete("Deprecated in iOS 5.0")]
        public virtual MonoTouch.Foundation.NSLocale Locale {
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDevice" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDevice

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveBatteryLevelDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveBatteryStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveOrientationDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveProximityStateDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDocument" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDocument

Added:

```
public static MonoTouch.Foundation.NSString StateChangedNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveStateChanged (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIEvent" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIEvent

Added:

```
public override string ToString ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIGestureRecognizer

Removed:

```
public class Token : MonoTouch.Foundation.NSObject {
```

Added:

```
public UIGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UIGestureRecognizer (MonoTouch.ObjCRuntime.Selector sel, Token token);
        public Token AddTarget (System.Action<MonoTouch.Foundation.NSObject> action);
        public static MonoTouch.ObjCRuntime.Selector ParametrizedSelector;
        
        public class ParameterlessDispatch : Token {
        public class ParametrizedDispatch : Token {
                
                public void Activated (UIGestureRecognizer sender);
        }
        public class Token : MonoTouch.Foundation.NSObject {
                
                public Token ();
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImage" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImage

Removed:

```
public static UIImage FromFileUncached (string filename);
```

Added:

```
[Obsolete("This is identical to FromFile. Caching is done when using FromBundle")]
        public static UIImage FromFileUncached (string filename);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIImagePickerController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIImagePickerController

Removed:

```
public virtual MonoTouch.Foundation.NSNumber[] AvailableCaptureModesForCameraDevice (UIImagePickerControllerCameraDevice cameraDevice);
```

Added:

```
public static MonoTouch.Foundation.NSNumber[] AvailableCaptureModesForCameraDevice (UIImagePickerControllerCameraDevice cameraDevice);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIKeyboard" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIKeyboard

Removed:

```
[Obsolete("Deprecated in iOS 3.2")]
        public static MonoTouch.Foundation.NSString BoundsUserInfoKey {
        [Obsolete("Deprecated in iOS 3.2")]
        public static MonoTouch.Foundation.NSString CenterBeginUserInfoKey {
        [Obsolete("Deprecated in iOS 3.2")]
        public static MonoTouch.Foundation.NSString CenterEndUserInfoKey {
```

Added:

```
public static MonoTouch.Foundation.NSString BoundsUserInfoKey {
        public static MonoTouch.Foundation.NSString CenterBeginUserInfoKey {
        public static MonoTouch.Foundation.NSString CenterEndUserInfoKey {
                get;
        }
        public static MonoTouch.Foundation.NSString DidChangeFrameNotification {
        public static MonoTouch.Foundation.NSString WillChangeFrameNotification {
                get;
        }
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidChangeFrame (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidHide (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidShow (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillChangeFrame (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillHide (EventHandler<UIKeyboardEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillShow (EventHandler<UIKeyboardEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIKeyboardEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.UIKeyboardEventArgs

```
public class UIKeyboardEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIKeyboardEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public UIViewAnimationCurve AnimationCurve {
                get;
        }
        public double AnimationDuration {
                get;
        }
        public System.Drawing.RectangleF FrameBegin {
                get;
        }
        public System.Drawing.RectangleF FrameEnd {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIKitThreadAccessException" class="injected"></a>


## New Type: MonoTouch.UIKit.UIKitThreadAccessException

```
public class UIKitThreadAccessException : Exception {
        
        public UIKitThreadAccessException ();
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UILabel" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UILabel

Added:

```
public virtual UIFont Font {
                        get;
                        set;
                }
                public virtual UIColor HighlightedTextColor {
                        get;
                        set;
                }
                public virtual UIColor ShadowColor {
                        get;
                        set;
                }
                public virtual System.Drawing.SizeF ShadowOffset {
                        get;
                        set;
                }
                public virtual UIColor TextColor {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UILongPressGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UILongPressGestureRecognizer

Added:

```
public UILongPressGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UILongPressGestureRecognizer (Action<UILongPressGestureRecognizer> action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIManagedDocument" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIManagedDocument

Removed:

```
public UIManagedDocument ();
```

Added:

```
public UIManagedDocument (MonoTouch.Foundation.NSUrl url);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIMenuController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIMenuController

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidHideMenu (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidShowMenu (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillHideMenu (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveWillShowMenu (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UINib" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UINib

Removed:

```
public virtual MonoTouch.Foundation.NSObject[] InstantiateWithOwneroptions (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
```

Added:

```
public virtual MonoTouch.Foundation.NSObject[] Instantiate (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
        [Obsolete("Use Instantiate method")]
        public MonoTouch.Foundation.NSObject[] InstantiateWithOwneroptions (MonoTouch.Foundation.NSObject ownerOrNil, MonoTouch.Foundation.NSDictionary optionsOrNil);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPageViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPageViewController

Added:

```
public UIPageViewController (string nibName, MonoTouch.Foundation.NSBundle bundle);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPanGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPanGestureRecognizer

Added:

```
public UIPanGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UIPanGestureRecognizer (Action<UIPanGestureRecognizer> action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPasteboard" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPasteboard

Removed:

```
public UIPasteboard ();
                set;
```

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveChanged (EventHandler<UIPasteboardChangeEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveRemoved (EventHandler<UIPasteboardChangeEventArgs> handler);
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIPasteboardChangeEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.UIPasteboardChangeEventArgs

```
public class UIPasteboardChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIPasteboardChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public string [] TypesAdded {
                get;
        }
        public string [] TypesRemoved {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPinchGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPinchGestureRecognizer

Added:

```
public UIPinchGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UIPinchGestureRecognizer (Action<UIPinchGestureRecognizer> action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPopoverController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPopoverController

Added:

```
public virtual Type PopoverBackgroundViewType {
                get;
                set;
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPrintInfo" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPrintInfo

Removed:

```
public UIPrintInfo ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPrintInteractionController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPrintInteractionController

Removed:

```
public UIPrintInteractionController ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIReferenceLibraryViewController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIReferenceLibraryViewController

Removed:

```
public UIReferenceLibraryViewController ();
```

Added:

```
public UIReferenceLibraryViewController (string nibName, MonoTouch.Foundation.NSBundle bundle);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIRotationGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIRotationGestureRecognizer

Added:

```
public UIRotationGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UIRotationGestureRecognizer (Action<UIRotationGestureRecognizer> action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIScreen" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIScreen

Added:

```
public MonoTouch.CoreAnimation.CADisplayLink CreateDisplayLink (MonoTouch.Foundation.NSAction action);
        
        public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveBrightnessDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidConnect (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidDisconnect (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISearchBar" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISearchBar

Added:

```
public virtual UIColor TintColor {
                        get;
                        set;
                }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISimpleTextPrintFormatter" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISimpleTextPrintFormatter

Removed:

```
public virtual UILineBreakMode LineBreakMode {
                get;
                set;
        }
```

 <a name="New_Type:_MonoTouch.UIKit.UIStatusBarFrameChangeEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStatusBarFrameChangeEventArgs

```
public class UIStatusBarFrameChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIStatusBarFrameChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public System.Drawing.RectangleF StatusBarFrame {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.UIKit.UIStatusBarOrientationChangeEventArgs" class="injected"></a>


## New Type: MonoTouch.UIKit.UIStatusBarOrientationChangeEventArgs

```
public class UIStatusBarOrientationChangeEventArgs : MonoTouch.Foundation.NSNotificationEventArgs {
        
        public UIStatusBarOrientationChangeEventArgs (MonoTouch.Foundation.NSNotification notification);
        
        public UIInterfaceOrientation StatusBarOrientation {
                get;
        }
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISwipeGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISwipeGestureRecognizer

Added:

```
public UISwipeGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UISwipeGestureRecognizer (Action<UISwipeGestureRecognizer> action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITabBarController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITabBarController

 <a name="Type_Changed:_MonoTouch.UIKit.UITableView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITableView

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveSelectionDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITapGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITapGestureRecognizer

Added:

```
public UITapGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UITapGestureRecognizer (Action<UITapGestureRecognizer> action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextField" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextField

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveCurrentInputModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidBeginEditing (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidEndEditing (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextFieldTextDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextInputMode" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextInputMode

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveCurrentInputModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITextView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITextView

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveCurrentInputModeDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidBeginEditing (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidChange (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveTextDidEndEditing (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIWindow" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIWindow

Added:

```
public static class Notifications {
                
                public static MonoTouch.Foundation.NSObject ObserveDidBecomeHidden (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidBecomeKey (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidBecomeVisible (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
                public static MonoTouch.Foundation.NSObject ObserveDidResignKey (System.EventHandler<MonoTouch.Foundation.NSNotificationEventArgs> handler);
        }
```

 <a name="Type_Removed:_MonoTouch.iAd.ADManager" class="injected"></a>


## Type Removed: MonoTouch.iAd.ADManager
