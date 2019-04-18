---
id: C924526D-C9F9-4F37-9341-697C1D810D7F
title: "Mac 3.2 to 3.4"
---

<style scoped="">
	.obsolete { color: gray; }
	.added { color: green; }
	.removed-inline { text-decoration: line-through; }
	.removed-breaking-inline { color: red;}
	.added-breaking-inline { text-decoration: underline; }
	.nonbreaking { color: black; }
	.breaking { color: red; }
</style> <script type="text/javascript">
	// Only some elements have 'data-is-[non-]breaking' attributes. Here we
	// iterate over all descendents elements, and set 'data-is-[non-]breaking'
	// depending on whether there are any descendents with that attribute.
	function propagateDataAttribute (element)
	{
		if (element.hasAttribute ('data-is-propagated'))
			return;

		var i;
		var any_breaking = element.hasAttribute ('data-is-breaking');
		var any_non_breaking = element.hasAttribute ('data-is-non-breaking');
		for (i = 0; i < element.children.length; i++) {
			var el = element.children [i];
			propagateDataAttribute (el);
			any_breaking |= el.hasAttribute ('data-is-breaking');
			any_non_breaking |= el.hasAttribute ('data-is-non-breaking');
		}
		
		if (any_breaking)
			element.setAttribute ('data-is-breaking', null);
		else if (any_non_breaking)
			element.setAttribute ('data-is-non-breaking', null);
		element.setAttribute ('data-is-propagated', null);
	}

	function hideNonBreakingChanges ()
	{
		var topNodes = document.querySelectorAll ('[data-is-topmost]');
		var n;
		var i;
		for (n = 0; n < topNodes.length; n++) {
			propagateDataAttribute (topNodes [n]);
			var elements = topNodes [n].querySelectorAll ('[data-is-non-breaking]');
			for (i = 0; i < elements.length; i++) {
				var el = elements [i];
				if (!el.hasAttribute ('data-original-display'))
					el.setAttribute ('data-original-display', el.style.display);
				el.style.display = 'none';
			}
		}
		
		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
	}

	function showNonBreakingChanges ()
	{
		var elements = document.querySelectorAll ('[data-original-display]');
		var i;
		for (i = 0; i < elements.length; i++) {
			var el = elements [i];
			el.style.display = el.getAttribute ('data-original-display');
		}

		var links = document.getElementsByClassName ('hide-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = '';
		links = document.getElementsByClassName ('restore-nonbreaking');
		for (i = 0; i < links.length; i++)
			links [i].style.display = 'none';
	}
</script># Xamarin.Mac.dll

 [Hide non-breaking changes](javascript: hideNonBreakingChanges (); ) [Show non-breaking changes](javascript: showNonBreakingChanges (); )   
<div data-is-topmost="">
<!-- start namespace AVFoundation --> <div> 
<h2>Namespace AVFoundation</h2>
<!-- start type AVAudioPlayer --> <div>
<h3>Type Changed: AVFoundation.AVAudioPlayer</h3>
<div>
<p>Added constructors:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public AVAudioPlayer (Foundation.NSData data, string fileTypeHint, Foundation.NSError outError);</span>
	<span class='added added-constructor ' data-is-non-breaking="">public AVAudioPlayer (Foundation.NSUrl url, string fileTypeHint, Foundation.NSError outError);</span>
</pre>
</div>

</div> <!-- end type AVAudioPlayer -->
<!-- start type AVAudioPlayerNode --> <div>
<h3>Type Changed: AVFoundation.AVAudioPlayerNode</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ScheduleBufferAsync (AVAudioPcmBuffer buffer);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ScheduleBufferAsync (AVAudioPcmBuffer buffer, AVAudioTime when, AVAudioPlayerNodeBufferOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ScheduleFileAsync (AVAudioFile file, AVAudioTime when);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task ScheduleSegmentAsync (AVAudioFile file, long startFrame, uint numberFrames, AVAudioTime when);</span>
</pre>
</div>

</div> <!-- end type AVAudioPlayerNode -->
<!-- start type AVAudioUnit --> <div>
<h3>Type Changed: AVFoundation.AVAudioUnit</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;AVAudioUnit&gt; FromComponentDescriptionAsync (AudioUnit.AudioComponentDescription audioComponentDescription, AudioUnit.AudioComponentInstantiationOptions options);</span>
</pre>
</div>

</div> <!-- end type AVAudioUnit -->

</div> <!-- end namespace AVFoundation -->
<!-- start namespace AudioUnit --> <div> 
<h2>Namespace AudioUnit</h2>
<!-- start type AUAudioUnit --> <div>
<h3>Type Changed: AudioUnit.AUAudioUnit</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;AUAudioUnit&gt; FromComponentDescriptionAsync (AudioComponentDescription componentDescription, AudioComponentInstantiationOptions options);</span>
</pre>
</div>

</div> <!-- end type AUAudioUnit -->

</div> <!-- end namespace AudioUnit -->
<!-- start namespace Contacts --> <div> 
<h2>Namespace Contacts</h2>
<!-- start type CNContainer --> <div>
<h3>Type Changed: Contacts.CNContainer</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForContainerOfContact (string contactIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForContainerOfGroup (string groupIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForContainers (string[] identifiers);</span>
</pre>
</div>

</div> <!-- end type CNContainer -->
<!-- start type CNContainer_PredicatesExtension --> <div>
<h3>Type Changed: Contacts.CNContainer_PredicatesExtension</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNContainer.CreatePredicateForContainerOfContact instead")]
	public static Foundation.NSPredicate GetPredicateForContainerOfContact (CNContainer This, string contactIdentifier);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNContainer.CreatePredicateForContainerOfGroup instead")]
	public static Foundation.NSPredicate GetPredicateForContainerOfGroup (CNContainer This, string groupIdentifier);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNContainer.CreatePredicateForContainers instead")]
	public static Foundation.NSPredicate GetPredicateForContainers (CNContainer This, string[] identifiers);</span>
</div></pre>

</div> <!-- end type CNContainer_PredicatesExtension -->
<!-- start type CNGroup --> <div>
<h3>Type Changed: Contacts.CNGroup</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForGroups (string[] identifiers);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForGroupsInContainer (string containerIdentifier);</span>
	<span class='added added-method ' data-is-non-breaking="">public static Foundation.NSPredicate CreatePredicateForSubgroupsInGroup (string parentGroupIdentifier);</span>
</pre>
</div>

</div> <!-- end type CNGroup -->
<!-- start type CNGroup_PredicatesExtension --> <div>
<h3>Type Changed: Contacts.CNGroup_PredicatesExtension</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNGroup.CreatePredicateForGroups instead")]
	public static Foundation.NSPredicate GetPredicateForGroups (CNGroup This, string[] identifiers);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNGroup.CreatePredicateForGroupsInContainer instead")]
	public static Foundation.NSPredicate GetPredicateForGroupsInContainer (CNGroup This, string containerIdentifier);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use CNGroup.CreatePredicateForSubgroupsInGroup instead")]
	public static Foundation.NSPredicate GetPredicateForSubgroupsInGroup (CNGroup This, string parentGroupIdentifier);</span>
</div></pre>

</div> <!-- end type CNGroup_PredicatesExtension -->

</div> <!-- end namespace Contacts -->
<!-- start namespace CoreGraphics --> <div> 
<h2>Namespace CoreGraphics</h2>
<!-- start type CGRect --> <div>
<h3>Type Changed: CoreGraphics.CGRect</h3>
<div>
<p>Added properties:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public static CGRect Infinite { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public static CGRect Null { get; }</span>
</pre>
</div>

</div> <!-- end type CGRect -->

</div> <!-- end namespace CoreGraphics -->
<!-- start namespace Darwin --> <div> 
<h2>Namespace Darwin</h2>
<!-- start type KernelQueue --> <div>
<h3>Type Changed: Darwin.KernelQueue</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use any of the overloads that return an int to get how many events were returned from kevent.")]
	public bool KEvent (KernelEvent[] changeList, KernelEvent[] eventList);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use any of the overloads that return an int to get how many events were returned from kevent.")]
	public bool KEvent (KernelEvent[] changeList, KernelEvent[] eventList, TimeSpec timeOut);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use any of the overloads that return an int to get how many events were returned from kevent.")]
	public bool KEvent (KernelEvent[] changeList, int nChanges, KernelEvent[] eventList, int nEvents);</span>
</div><div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use any of the overloads that return an int to get how many events were returned from kevent.")]
	public bool KEvent (KernelEvent[] changeList, int nChanges, KernelEvent[] eventList, int nEvents, TimeSpec timeOut);</span>
</div></pre>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public int KEvent (KernelEvent[] changeList, KernelEvent[] eventList, System.TimeSpan? timeout);</span>
	<span class='added added-method ' data-is-non-breaking="">public int KEvent (KernelEvent[] changeList, int nChanges, KernelEvent[] eventList, int nEvents, TimeSpec? timeout);</span>
</pre>
</div>

</div> <!-- end type KernelQueue -->

</div> <!-- end namespace Darwin -->
<!-- start namespace Foundation --> <div> 
<h2>Namespace Foundation</h2>
<!-- start type NSExtensionContext --> <div>
<h3>Type Changed: Foundation.NSExtensionContext</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; CompleteRequestAsync (NSExtensionItem[] returningItems);</span>
</pre>
</div>

</div> <!-- end type NSExtensionContext -->
<!-- start type NSFileVersion --> <div>
<h3>Type Changed: Foundation.NSFileVersion</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;NSFileVersion[]&gt; GetNonlocalVersionsAsync (NSUrl url);</span>
</pre>
</div>

</div> <!-- end type NSFileVersion -->
<!-- start type NSHttpCookieStorage --> <div>
<h3>Type Changed: Foundation.NSHttpCookieStorage</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSHttpCookie[]&gt; GetCookiesForTaskAsync (NSUrlSessionTask task);</span>
</pre>
</div>

</div> <!-- end type NSHttpCookieStorage -->
<!-- start type NSItemProvider --> <div>
<h3>Type Changed: Foundation.NSItemProvider</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSObject&gt; LoadItemAsync (string typeIdentifier, NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSObject&gt; LoadPreviewImageAsync (NSDictionary options);</span>
</pre>
</div>

</div> <!-- end type NSItemProvider -->
<!-- start type NSString --> <div>
<h3>Type Changed: Foundation.NSString</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual void GetParagraphPositions (uint paragraphStartPosition, uint paragraphEndPosition, uint contentsEndPosition, NSRange range);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual NSRange GetParagraphRange (NSRange range);</span>
</pre>
</div>

</div> <!-- end type NSString -->
<!-- start type NSUrlCredentialStorage --> <div>
<h3>Type Changed: Foundation.NSUrlCredentialStorage</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSDictionary&gt; GetCredentialsAsync (NSUrlProtectionSpace protectionSpace, NSUrlSessionTask task);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NSUrlCredential&gt; GetDefaultCredentialAsync (NSUrlProtectionSpace space, NSUrlSessionTask task);</span>
</pre>
</div>

</div> <!-- end type NSUrlCredentialStorage -->

</div> <!-- end namespace Foundation -->
<!-- start namespace GameController --> <div> 
<h2>Namespace GameController</h2>
<!-- start type GCController --> <div>
<h3>Type Changed: GameController.GCController</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task StartWirelessControllerDiscoveryAsync ();</span>
</pre>
</div>

</div> <!-- end type GCController -->

</div> <!-- end namespace GameController -->
<!-- start namespace GameKit --> <div> 
<h2>Namespace GameKit</h2>
<!-- start type GKAchievement --> <div>
<h3>Type Changed: GameKit.GKAchievement</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKChallengeComposeResult&gt; ChallengeComposeControllerAsync (string message, GKPlayer[] players);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKChallengeComposeResult&gt; ChallengeComposeControllerAsync (string message, GKPlayer[] players, AppKit.NSViewController result);</span>
</pre>
</div>

</div> <!-- end type GKAchievement -->
<!-- start type GKLocalPlayer --> <div>
<h3>Type Changed: GameKit.GKLocalPlayer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKIdentityVerificationSignatureResult&gt; GenerateIdentityVerificationSignatureAsync ();</span>
</pre>
</div>

</div> <!-- end type GKLocalPlayer -->
<!-- start type GKMatch --> <div>
<h3>Type Changed: GameKit.GKMatch</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKPlayer&gt; ChooseBestHostingPlayerAsync ();</span>
</pre>
</div>

</div> <!-- end type GKMatch -->
<!-- start type GKScore --> <div>
<h3>Type Changed: GameKit.GKScore</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKChallengeComposeResult&gt; ChallengeComposeControllerAsync (string message, GKPlayer[] players);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;GKChallengeComposeResult&gt; ChallengeComposeControllerAsync (string message, GKPlayer[] players, AppKit.NSViewController result);</span>
</pre>
</div>

</div> <!-- end type GKScore -->
<div> <!-- start type GKChallengeComposeResult -->
<h3>New Type GameKit.GKChallengeComposeResult</h3>
<pre class='added' data-is-non-breaking="">
public class GKChallengeComposeResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKChallengeComposeResult (AppKit.NSViewController composeController, bool issuedChallenge, string[] sentPlayerIDs);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public AppKit.NSViewController ComposeController { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool IssuedChallenge { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public string[] SentPlayerIDs { get; set; }</span>
}
</pre>
</div> <!-- end type GKChallengeComposeResult -->
<div> <!-- start type GKIdentityVerificationSignatureResult -->
<h3>New Type GameKit.GKIdentityVerificationSignatureResult</h3>
<pre class='added' data-is-non-breaking="">
public class GKIdentityVerificationSignatureResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public GKIdentityVerificationSignatureResult (Foundation.NSUrl publicKeyUrl, Foundation.NSData signature, Foundation.NSData salt, ulong timestamp);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSUrl PublicKeyUrl { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Salt { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData Signature { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public ulong Timestamp { get; set; }</span>
}
</pre>
</div> <!-- end type GKIdentityVerificationSignatureResult -->

</div> <!-- end namespace GameKit -->
<!-- start namespace MapKit --> <div> 
<h2>Namespace MapKit</h2>
<!-- start type MKDirections --> <div>
<h3>Type Changed: MapKit.MKDirections</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MKDirectionsResponse&gt; CalculateDirectionsAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MKETAResponse&gt; CalculateETAAsync ();</span>
</pre>
</div>

</div> <!-- end type MKDirections -->
<!-- start type MKLocalSearchRequest --> <div>
<h3>Type Changed: MapKit.MKLocalSearchRequest</h3>
<div>
<p>Added constructor:</p>
<pre>
	<span class='added added-constructor ' data-is-non-breaking="">public MKLocalSearchRequest (MKLocalSearchCompletion completion);</span>
</pre>
</div>

</div> <!-- end type MKLocalSearchRequest -->
<!-- start type MKMapSnapshotter --> <div>
<h3>Type Changed: MapKit.MKMapSnapshotter</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MKMapSnapshot&gt; StartAsync ();</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;MKMapSnapshot&gt; StartAsync (CoreFoundation.DispatchQueue queue);</span>
</pre>
</div>

</div> <!-- end type MKMapSnapshotter -->

</div> <!-- end namespace MapKit -->
<!-- start namespace MetalKit --> <div> 
<h2>Namespace MetalKit</h2>
<!-- start type MTKTextureLoader --> <div>
<h3>Type Changed: MetalKit.MTKTextureLoader</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromCGImageAsync (CoreGraphics.CGImage cgImage, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromDataAsync (Foundation.NSData data, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromNameAsync (string name, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromNameAsync (string name, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Metal.IMTLTexture[]&gt; FromNamesAsync (string[] names, nfloat scaleFactor, Foundation.NSBundle bundle, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture[]&gt; FromNamesAsync (string[] names, nfloat scaleFactor, Foundation.NSBundle bundle, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture&gt; FromUrlAsync (Foundation.NSUrl url, MTKTextureLoaderOptions options);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Metal.IMTLTexture[]&gt; FromUrlsAsync (Foundation.NSUrl[] urls, Foundation.NSDictionary options);</span>
	<span class='added added-method ' data-is-non-breaking="">public System.Threading.Tasks.Task&lt;Metal.IMTLTexture[]&gt; FromUrlsAsync (Foundation.NSUrl[] urls, MTKTextureLoaderOptions options);</span>
</pre>
</div>

</div> <!-- end type MTKTextureLoader -->

</div> <!-- end namespace MetalKit -->
<!-- start namespace ModelIO --> <div> 
<h2>Namespace ModelIO</h2>
<!-- start type MDLMesh --> <div>
<h3>Type Changed: ModelIO.MDLMesh</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static MDLMesh CreateBox (OpenTK.Vector3 dimensions, OpenTK.Vector3i segments, MDLGeometryType geometryType, bool inwardNormals, IMDLMeshBufferAllocator allocator);</span>
</pre>
</div>

</div> <!-- end type MDLMesh -->

</div> <!-- end namespace ModelIO -->
<!-- start namespace NetworkExtension --> <div> 
<h2>Namespace NetworkExtension</h2>
<!-- start type NEPacketTunnelFlow --> <div>
<h3>Type Changed: NetworkExtension.NEPacketTunnelFlow</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;NEPacketTunnelFlowReadResult&gt; ReadPacketsAsync ();</span>
</pre>
</div>

</div> <!-- end type NEPacketTunnelFlow -->
<!-- start type NEProvider --> <div>
<h3>Type Changed: NetworkExtension.NEProvider</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;bool&gt; DisplayMessageAsync (string message);</span>
</pre>
</div>

</div> <!-- end type NEProvider -->
<!-- start type NWTcpConnectionAuthenticationDelegate --> <div>
<h3>Type Changed: NetworkExtension.NWTcpConnectionAuthenticationDelegate</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'NWTcpConnectionAuthenticationDelegate_Extensions.EvaluateTrustAsync' instead")]
	public virtual System.Threading.Tasks.Task&lt;Security.SecTrust&gt; EvaluateTrustAsync (NWTcpConnection connection, Foundation.NSArray peerCertificateChain);</span>
</div></pre>

</div> <!-- end type NWTcpConnectionAuthenticationDelegate -->
<div> <!-- start type NEPacketTunnelFlowReadResult -->
<h3>New Type NetworkExtension.NEPacketTunnelFlowReadResult</h3>
<pre class='added' data-is-non-breaking="">
public class NEPacketTunnelFlowReadResult {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public NEPacketTunnelFlowReadResult (Foundation.NSData[] packets, Foundation.NSNumber[] protocols);</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSData[] Packets { get; set; }</span>
	<span class='added added-property ' data-is-non-breaking="">public Foundation.NSNumber[] Protocols { get; set; }</span>
}
</pre>
</div> <!-- end type NEPacketTunnelFlowReadResult -->

</div> <!-- end namespace NetworkExtension -->
<!-- start namespace ObjCRuntime --> <div> 
<h2>Namespace ObjCRuntime</h2>
<!-- start type Constants --> <div>
<h3>Type Changed: ObjCRuntime.Constants</h3>
<p>Modified fields:</p>
<pre>
<div data-is-breaking="">	public const string Version = <span class='removed removed-inline removed-breaking-inline'>"3.2.0"</span> <span class='added '>"3.3.0"</span>;
</div></pre>

</div> <!-- end type Constants -->
<!-- start type Dlfcn --> <div>
<h3>Type Changed: ObjCRuntime.Dlfcn</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static CoreGraphics.CGRect GetCGRect (IntPtr handle, string symbol);</span>
</pre>
</div>

</div> <!-- end type Dlfcn -->
<!-- start type MonoPInvokeCallbackAttribute --> <div>
<h3>Type Changed: ObjCRuntime.MonoPInvokeCallbackAttribute</h3>
<div>
<p>Added property:</p>
<pre>
	<span class='added added-property ' data-is-non-breaking="">public System.Type DelegateType { get; set; }</span>
</pre>
</div>

</div> <!-- end type MonoPInvokeCallbackAttribute -->
<!-- start type Runtime --> <div>
<h3>Type Changed: ObjCRuntime.Runtime</h3>
<div>
<p>Added event:</p>
<pre>
	<span class='added added-event ' data-is-non-breaking="">public event AssemblyRegistrationHandler AssemblyRegistration;</span>
</pre>
</div>

</div> <!-- end type Runtime -->
<div> <!-- start type AssemblyRegistrationEventArgs -->
<h3>New Type ObjCRuntime.AssemblyRegistrationEventArgs</h3>
<pre class='added' data-is-non-breaking="">
public class AssemblyRegistrationEventArgs : System.EventArgs {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AssemblyRegistrationEventArgs ();</span>
	// properties
	<span class='added added-property ' data-is-non-breaking="">public System.Reflection.AssemblyName AssemblyName { get; }</span>
	<span class='added added-property ' data-is-non-breaking="">public bool Register { get; set; }</span>
}
</pre>
</div> <!-- end type AssemblyRegistrationEventArgs -->
<div> <!-- start type AssemblyRegistrationHandler -->
<h3>New Type ObjCRuntime.AssemblyRegistrationHandler</h3>
<pre class='added' data-is-non-breaking="">
public sealed delegate AssemblyRegistrationHandler : System.MulticastDelegate, System.ICloneable, System.Runtime.Serialization.ISerializable {
	// constructors
	<span class='added added-constructor ' data-is-non-breaking="">public AssemblyRegistrationHandler (object object, IntPtr method);</span>
	// methods
	<span class='added added-method ' data-is-non-breaking="">public virtual System.IAsyncResult BeginInvoke (object sender, AssemblyRegistrationEventArgs args, System.AsyncCallback callback, object object);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void EndInvoke (System.IAsyncResult result);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual void Invoke (object sender, AssemblyRegistrationEventArgs args);</span>
}
</pre>
</div> <!-- end type AssemblyRegistrationHandler -->

</div> <!-- end namespace ObjCRuntime -->
<!-- start namespace SceneKit --> <div> 
<h2>Namespace SceneKit</h2>
<!-- start type SCNLayer --> <div>
<h3>Type Changed: SceneKit.SCNLayer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PresentSceneAsync (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type SCNLayer -->
<!-- start type SCNRenderer --> <div>
<h3>Type Changed: SceneKit.SCNRenderer</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PresentSceneAsync (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type SCNRenderer -->
<!-- start type SCNSceneRenderer --> <div>
<h3>Type Changed: SceneKit.SCNSceneRenderer</h3>
<p>Obsoleted methods:</p>
<pre>
<div data-is-non-breaking="">	<span class='obsolete obsolete-method' data-is-non-breaking="">[Obsolete ("Use 'SCNSceneRenderer_Extensions.PrepareAsync' instead")]
	public virtual System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects);</span>
</div></pre>
<p>Modified methods:</p>
<pre>
<div data-is-non-breaking="">	public <span class='added '>virtual</span> System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (Foundation.NSObject[] objects)
</div></pre>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">[Obsolete ("Use 'SCNSceneRenderer_Extensions.PresentSceneAsync' instead")]
	public virtual System.Threading.Tasks.Task PresentSceneAsync (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRenderer -->
<!-- start type SCNSceneRenderer_Extensions --> <div>
<h3>Type Changed: SceneKit.SCNSceneRenderer_Extensions</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task&lt;bool&gt; PrepareAsync (ISCNSceneRenderer This, Foundation.NSObject[] objects);</span>
	<span class='added added-method ' data-is-non-breaking="">public static System.Threading.Tasks.Task PresentSceneAsync (ISCNSceneRenderer This, SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type SCNSceneRenderer_Extensions -->
<!-- start type SCNView --> <div>
<h3>Type Changed: SceneKit.SCNView</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task PresentSceneAsync (SCNScene scene, SpriteKit.SKTransition transition, SCNNode pointOfView);</span>
</pre>
</div>

</div> <!-- end type SCNView -->

</div> <!-- end namespace SceneKit -->
<!-- start namespace SpriteKit --> <div> 
<h2>Namespace SpriteKit</h2>
<!-- start type SKEffectNode --> <div>
<h3>Type Changed: SpriteKit.SKEffectNode</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>

</div> <!-- end type SKEffectNode -->
<!-- start type SKEmitterNode --> <div>
<h3>Type Changed: SpriteKit.SKEmitterNode</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>

</div> <!-- end type SKEmitterNode -->
<!-- start type SKNode --> <div>
<h3>Type Changed: SpriteKit.SKNode</h3>
<div>
<p>Added method:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RunActionAsync (SKAction action);</span>
</pre>
</div>

</div> <!-- end type SKNode -->
<!-- start type SKSpriteNode --> <div>
<h3>Type Changed: SpriteKit.SKSpriteNode</h3>
<p>Removed property:</p>

<pre>
	<span class='removed removed-property breaking' data-is-breaking="">public virtual Foundation.NSDictionary&lt;Foundation.NSString,SpriteKit.SKAttributeValue&gt; AttributeValues { get; set; }</span>
</pre>
<p>Removed methods:</p>

<pre>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual SKAttributeValue GetValue (string key);</span>
	<span class='removed removed-method breaking' data-is-breaking="">public virtual void SetValue (SKAttributeValue value, string key);</span>
</pre>

</div> <!-- end type SKSpriteNode -->

</div> <!-- end namespace SpriteKit -->
<!-- start namespace WebKit --> <div> 
<h2>Namespace WebKit</h2>
<!-- start type WKWebsiteDataStore --> <div>
<h3>Type Changed: WebKit.WKWebsiteDataStore</h3>
<div>
<p>Added methods:</p>
<pre>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task&lt;Foundation.NSArray&gt; FetchDataRecordsOfTypesAsync (Foundation.NSSet&lt;Foundation.NSString&gt; dataTypes);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RemoveDataOfTypesAsync (Foundation.NSSet&lt;Foundation.NSString&gt; websiteDataTypes, Foundation.NSDate date);</span>
	<span class='added added-method ' data-is-non-breaking="">public virtual System.Threading.Tasks.Task RemoveDataOfTypesAsync (Foundation.NSSet&lt;Foundation.NSString&gt; dataTypes, WKWebsiteDataRecord[] dataRecords);</span>
</pre>
</div>

</div> <!-- end type WKWebsiteDataStore -->

</div> <!-- end namespace WebKit -->
</div>
