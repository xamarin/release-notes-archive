---
id: F0464107-67C6-4B25-6333-E185A7AECAEB
title: "From 5.2.5 to 5.3.0"
---

<a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

Removed:

```
public const string Version = "5.2.5";
```

Added:

```
public const string Version = "5.3.0";
        public const string CoreMidiLibrary = "/System/Library/Frameworks/CoreMIDI.framework/CoreMIDI";
```

 <a name="Namespace:_MonoTouch.AVFoundation" class="injected"></a>


# Namespace: MonoTouch.AVFoundation

 <a name="Type_Changed:_MonoTouch.AVFoundation.AVAudioPlayer" class="injected"></a>


## Type Changed: MonoTouch.AVFoundation.AVAudioPlayer

Removed:

```
public virtual bool PlayAtTimetime (double time);
```

Added:

```
public virtual bool PlayAtTime (double time);
        public bool PlayAtTimetime (double time);
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

 <a name="Namespace:_MonoTouch.AddressBook" class="injected"></a>


# Namespace: MonoTouch.AddressBook

 <a name="Type_Changed:_MonoTouch.AddressBook.ABAddressBook" class="injected"></a>


## Type Changed: MonoTouch.AddressBook.ABAddressBook

Added:

```
public ABSource[] GetAllSources ();
        public ABSource GetDefaultSource ();
        public ABSource GetSource (int sourceID);
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
        DAVSearch
}
```

 <a name="Namespace:_MonoTouch.AddressBookUI" class="injected"></a>


# Namespace: MonoTouch.AddressBookUI

 <a name="" class="injected"></a>


## Type Changed: MonoTouch.AddressBookUI.ABPeoplePickerNavigationController 

Added:

```
public static ABPeoplePickerNavigationControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static ABPeoplePickerNavigationControllerAppearance Appearance {
                get;
        }
        
        public class ABPeoplePickerNavigationControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Namespace:_MonoTouch.CoreData" class="injected"></a>


# Namespace: MonoTouch.CoreData

 <a name="Type_Changed:_MonoTouch.CoreData.NSPersistentStoreCoordinator" class="injected"></a>


## Type Changed: MonoTouch.CoreData.NSPersistentStoreCoordinator

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
                get;
        }
        public static MonoTouch.Foundation.NSString ValidateXMLStoreOption {
                get;
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
        
        public static void Restart ();
        
        public static MonoTouch.Foundation.NSString NetworkBonjourServiceType {
                get;
        }
        public static MonoTouch.Foundation.NSString NetworkNotificationContactsDidChange {
                get;
        }
        public static MonoTouch.Foundation.NSString NetworkNotificationSessionDidChange {
                get;
        }
}
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
        
        public static MidiDevice GetDevice (int deviceIndex);
        public static MidiDevice GetExternalDevice (int deviceIndex);
        public MidiEntity GetEntity (int entityIndex);
        
        public static int DeviceCount {
                get;
        }
        public static int ExternalDeviceCount {
                get;
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
        
        public static int DestinationCount {
                get;
        }
        public static int SourceCount {
                get;
        }
        public string EndpointName {
                get;
        }
        public MidiEntity Entity {
                get;
        }
        public bool IsNetworkSession {
                get;
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
        
        public int Destinations {
                get;
        }
        public MidiDevice Device {
                get;
        }
        public int Sources {
                get;
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
        
        public MidiNetworkSession ();
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
        public IntPtr Handle {
                get;
        }
        public string Image {
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
        }
        public int ReceiveChannels {
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
        public int TransmitChannels {
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

 <a name="Namespace:_MonoTouch.EventKitUI" class="injected"></a>


# Namespace: MonoTouch.EventKitUI

 <a name="Type_Changed:_MonoTouch.EventKitUI.EKEventEditViewController" class="injected"></a>


## Type Changed: MonoTouch.EventKitUI.EKEventEditViewController

Added:

```
public static EKEventEditViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static EKEventEditViewControllerAppearance Appearance {
                get;
        }
        
        public class EKEventEditViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="Type_Changed:_MonoTouch.Foundation.NSHttpCookie" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSHttpCookie

Added:

```
public NSHttpCookie (string name, string value);
        public NSHttpCookie (string name, string value, string path);
        public NSHttpCookie (string name, string value, string path, string domain);
        public NSHttpCookie (System.Net.Cookie cookie);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSKeyedArchiver" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSKeyedArchiver

Removed:

```
public static NSData ArchiveRootObjectToFile (NSObject root, string file);
```

Added:

```
public static bool ArchiveRootObjectToFile (NSObject root, string file);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSObject" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSObject

Added:

```
public virtual NSObject Copy ();
        public virtual NSObject MutableCopy ();
        public virtual void PerformSelector (MonoTouch.ObjCRuntime.Selector sel, NSObject obj, double delay);
        public virtual int RetainCount {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlCredentialStorage" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlCredentialStorage

Removed:

```
Could not find MonoTouch.Foundation.NSUrlCredentialStorage
```

Added:

```
public class NSUrlCredentialStorage : NSObject {
        
        public NSUrlCredentialStorage ();
        public NSUrlCredentialStorage (NSCoder coder);
        public NSUrlCredentialStorage (NSObjectFlag t);
        public NSUrlCredentialStorage (IntPtr handle);
        
        protected override void Dispose (bool disposing);
        public virtual NSDictionary GetCredentials (NSUrlProtectionSpace forProtectionSpace);
        public virtual NSUrlCredential GetDefaultCredential (NSUrlProtectionSpace forProtectionSpace);
        public virtual void RemoveCredential (NSUrlCredential credential, NSUrlProtectionSpace forProtectionSpace);
        public virtual void SetCredential (NSUrlCredential credential, NSUrlProtectionSpace forProtectionSpace);
        public virtual void SetDefaultCredential (NSUrlCredential credential, NSUrlProtectionSpace forProtectionSpace);
        
        public virtual NSDictionary AllCredentials {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSUrlCredentialStorage SharedCredentialStorage {
                get;
        }
 }
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSUrlProtectionSpace" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSUrlProtectionSpace

Added:

```
public static NSString AuthenticationMethodClientCertificat {
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

 <a name="Namespace:_MonoTouch.GameKit" class="injected"></a>


# Namespace: MonoTouch.GameKit

 <a name="Type_Changed:_MonoTouch.GameKit.GKAchievementViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKAchievementViewController

Added:

```
public static GKAchievementViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static GKAchievementViewControllerAppearance Appearance {
                get;
        }
        
        public class GKAchievementViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKFriendRequestComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKFriendRequestComposeViewController

Added:

```
public static GKFriendRequestComposeViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static GKFriendRequestComposeViewControllerAppearance Appearance {
                get;
        }
        
        public class GKFriendRequestComposeViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKLeaderboardViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKLeaderboardViewController

Added:

```
public static GKLeaderboardViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static GKLeaderboardViewControllerAppearance Appearance {
                get;
        }
        
        public class GKLeaderboardViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.GameKit.GKTurnBasedMatchmakerViewController" class="injected"></a>


## Type Changed: MonoTouch.GameKit.GKTurnBasedMatchmakerViewController

Added:

```
public static GKTurnBasedMatchmakerViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static GKTurnBasedMatchmakerViewControllerAppearance Appearance {
                get;
        }
        
        public class GKTurnBasedMatchmakerViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Namespace:_MonoTouch.MessageUI" class="injected"></a>


# Namespace: MonoTouch.MessageUI

 <a name="Type_Changed:_MonoTouch.MessageUI.MFMailComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.MessageUI.MFMailComposeViewController

Added:

```
public static MFMailComposeViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MFMailComposeViewControllerAppearance Appearance {
                get;
        }
        
        public class MFMailComposeViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Type_Changed:_MonoTouch.MessageUI.MFMessageComposeViewController" class="injected"></a>


## Type Changed: MonoTouch.MessageUI.MFMessageComposeViewController

Added:

```
public static MFMessageComposeViewControllerAppearance AppearanceWhenContainedIn (params Type [] containers);
        public static MFMessageComposeViewControllerAppearance Appearance {
                get;
        }
        
        public class MFMessageComposeViewControllerAppearance : MonoTouch.UIKit.UIAppearance {
        }
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

Added:

```
public static void void_objc_msgSend_intptr_intptr_double (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3);
        public static void void_objc_msgSendSuper_intptr_intptr_double (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, double arg3);
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

 <a name="Namespace:_MonoTouch.UIKit" class="injected"></a>


# Namespace: MonoTouch.UIKit

 <a name="Type_Changed:_MonoTouch.UIKit.UIApplication" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIApplication

Added:

```
public static void EnsureUIThread ();
        
        public static bool CheckForIllegalCrossThreadCalls;
```

 <a name="Changed:_MonoTouch.UIKit.UIDocument" class="injected"></a>


## Changed: MonoTouch.UIKit.UIDocument

Removed:

```
public UIDocument ();
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIDocumentInteractionController" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIDocumentInteractionController

Added:

```
public virtual void DismissPreview (bool animated);
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

 <a name="New_Type:_MonoTouch.UIKit.UIKitThreadAccessException" class="injected"></a>


## New Type: MonoTouch.UIKit.UIKitThreadAccessException

```
public class UIKitThreadAccessException : Exception {
        
        public UIKitThreadAccessException ();
}
```

 <a name="Type_Changed:_MonoTouch.UIKit.UILongPressGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UILongPressGestureRecognizer

Added:

```
public UILongPressGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UILongPressGestureRecognizer (Action<UILongPressGestureRecognizer> action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIPanGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIPanGestureRecognizer

Added:

```
public UIPanGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UIPanGestureRecognizer (Action<UIPanGestureRecognizer> action);
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
```

 <a name="Type_Changed:_MonoTouch.UIKit.UISwipeGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UISwipeGestureRecognizer

Added:

```
public UISwipeGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UISwipeGestureRecognizer (Action<UISwipeGestureRecognizer> action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UITapGestureRecognizer" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UITapGestureRecognizer

Added:

```
public UITapGestureRecognizer (MonoTouch.Foundation.NSAction action);
        public UITapGestureRecognizer (Action<UITapGestureRecognizer> action);
```

 <a name="Type_Changed:_MonoTouch.UIKit.UIView" class="injected"></a>


## Type Changed: MonoTouch.UIKit.UIView

Added:

```
public static void Animate (double duration, MonoTouch.Foundation.NSAction animation, UICompletionHandler completion);
        public static void Animate (double duration, double delay, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, UICompletionHandler completion);
        public static void Transition (UIView withView, double duration, UIViewAnimationOptions options, MonoTouch.Foundation.NSAction animation, UICompletionHandler completion);
        public static void Transition (UIView fromView, UIView toView, double duration, UIViewAnimationOptions options, UICompletionHandler completion);
```
