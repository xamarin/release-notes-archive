---
id: 48A67D73-890B-4235-A397-86E1F50FAE80
title: "Mono.Android.Support.v4.dll"
---

# Mono.Android.Support.v4.dll

<h2 id='Android.Support.V4.App'>Namespace: Android.Support.V4.App</h2>

<h3 id='Android.Support.V4.App.ActionBarDrawerToggle'>New Type: Android.Support.V4.App.ActionBarDrawerToggle</h3>

```
public class ActionBarDrawerToggle : Java.Lang.Object, DrawerLayout.Android.Support.V4.Widget.IDrawerListener {
	
	protected ActionBarDrawerToggle (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public ActionBarDrawerToggle (Android.App.Activity p0, Android.Support.V4.Widget.DrawerLayout p1, int p2, int p3, int p4);
	
	public virtual void OnConfigurationChanged (Android.Content.Res.Configuration p0);
	public virtual void OnDrawerClosed (Android.Views.View p0);
	public virtual void OnDrawerOpened (Android.Views.View p0);
	public virtual void OnDrawerSlide (Android.Views.View p0, float p1);
	public virtual void OnDrawerStateChanged (int p0);
	public virtual bool OnOptionsItemSelected (Android.Views.IMenuItem p0);
	public virtual void SyncState ();
	
	public virtual bool DrawerIndicatorEnabled {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public class ActionBarDrawerToggleImplBase : Java.Lang.Object, IActionBarDrawerToggleImpl {
		
		protected ActionBarDrawerToggleImplBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual Android.Graphics.Drawables.Drawable GetThemeUpIndicator (Android.App.Activity p0);
		public virtual Java.Lang.Object SetActionBarDescription (Java.Lang.Object p0, Android.App.Activity p1, int p2);
		public virtual Java.Lang.Object SetActionBarUpIndicator (Java.Lang.Object p0, Android.App.Activity p1, Android.Graphics.Drawables.Drawable p2, int p3);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class ActionBarDrawerToggleImplHC : Java.Lang.Object, IActionBarDrawerToggleImpl {
		
		protected ActionBarDrawerToggleImplHC (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual Android.Graphics.Drawables.Drawable GetThemeUpIndicator (Android.App.Activity p0);
		public virtual Java.Lang.Object SetActionBarDescription (Java.Lang.Object p0, Android.App.Activity p1, int p2);
		public virtual Java.Lang.Object SetActionBarUpIndicator (Java.Lang.Object p0, Android.App.Activity p1, Android.Graphics.Drawables.Drawable p2, int p3);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public interface IActionBarDrawerToggleImpl : IDisposable, Android.Runtime.IJavaObject {
		
		Android.Graphics.Drawables.Drawable GetThemeUpIndicator (Android.App.Activity p0);
		Java.Lang.Object SetActionBarDescription (Java.Lang.Object p0, Android.App.Activity p1, int p2);
		Java.Lang.Object SetActionBarUpIndicator (Java.Lang.Object p0, Android.App.Activity p1, Android.Graphics.Drawables.Drawable p2, int p3);
	}
	public class SlideDrawable : Android.Graphics.Drawables.Drawable, Drawable.Android.Graphics.Drawables.ICallback {
		
		protected SlideDrawable (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public SlideDrawable (Android.Graphics.Drawables.Drawable p0);
		
		public override void Draw (Android.Graphics.Canvas p0);
		public virtual void InvalidateDrawable (Android.Graphics.Drawables.Drawable p0);
		public virtual void ScheduleDrawable (Android.Graphics.Drawables.Drawable p0, Java.Lang.IRunnable p1, long p2);
		public override void SetAlpha (int p0);
		public override void SetColorFilter (Android.Graphics.ColorFilter p0);
		public virtual void SetOffsetBy (float p0);
		public virtual void UnscheduleDrawable (Android.Graphics.Drawables.Drawable p0, Java.Lang.IRunnable p1);
		
		public virtual float Offset {
			get;
			set;
		}
		public override int Opacity {
			get;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Android.Support.V4.App.ActivityCompat'>Type Changed: Android.Support.V4.App.ActivityCompat</h3>

Added:

```
public static void StartActivity (Android.App.Activity p0, Android.Content.Intent p1, Android.OS.Bundle p2);
 	public static void StartActivityForResult (Android.App.Activity p0, Android.Content.Intent p1, int p2, Android.OS.Bundle p3);
```

<h3 id='Android.Support.V4.App.ActivityOptionsCompat'>New Type: Android.Support.V4.App.ActivityOptionsCompat</h3>

```
public class ActivityOptionsCompat : Java.Lang.Object {
	
	protected ActivityOptionsCompat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	protected ActivityOptionsCompat ();
	
	public static ActivityOptionsCompat MakeCustomAnimation (Android.Content.Context p0, int p1, int p2);
	public static ActivityOptionsCompat MakeScaleUpAnimation (Android.Views.View p0, int p1, int p2, int p3, int p4);
	public static ActivityOptionsCompat MakeThumbnailScaleUpAnimation (Android.Views.View p0, Android.Graphics.Bitmap p1, int p2, int p3);
	public virtual Android.OS.Bundle ToBundle ();
	public virtual void Update (ActivityOptionsCompat p0);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public class ActivityOptionsImplJB : ActivityOptionsCompat {
		
		protected ActivityOptionsImplJB (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	}
}
```

<h3 id='Android.Support.V4.App.FragmentActivity'>Type Changed: Android.Support.V4.App.FragmentActivity</h3>

Added:

```
set;
```

<h3 id='Android.Support.V4.App.NotificationCompat'>Type Changed: Android.Support.V4.App.NotificationCompat</h3>

Added:

```
public virtual BigPictureStyle BigLargeIcon (Android.Graphics.Bitmap p0);
```

<h2 id='Android.Support.V4.Content'>Namespace: Android.Support.V4.Content</h2>

<h3 id='Android.Support.V4.Content.FileProvider'>New Type: Android.Support.V4.Content.FileProvider</h3>

```
public class FileProvider : Android.Content.ContentProvider {
	
	protected FileProvider (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public FileProvider ();
	
	public static Android.Net.Uri GetUriForFile (Android.Content.Context p0, string p1, Java.IO.File p2);
	public override int Delete (Android.Net.Uri p0, string p1, string [] p2);
	public override string GetType (Android.Net.Uri p0);
	public override Android.Net.Uri Insert (Android.Net.Uri p0, Android.Content.ContentValues p1);
	public override bool OnCreate ();
	public override Android.Database.ICursor Query (Android.Net.Uri p0, string [] p1, string p2, string [] p3, string p4);
	public override int Update (Android.Net.Uri p0, Android.Content.ContentValues p1, string p2, string [] p3);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public interface IPathStrategy : IDisposable, Android.Runtime.IJavaObject {
		
		Java.IO.File GetFileForUri (Android.Net.Uri p0);
		Android.Net.Uri GetUriForFile (Java.IO.File p0);
	}
	public class SimplePathStrategy : Java.Lang.Object, IPathStrategy {
		
		protected SimplePathStrategy (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public SimplePathStrategy (string p0);
		
		public virtual void AddRoot (string p0, Java.IO.File p1);
		public virtual Java.IO.File GetFileForUri (Android.Net.Uri p0);
		public virtual Android.Net.Uri GetUriForFile (Java.IO.File p0);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h2 id='Android.Support.V4.View'>Namespace: Android.Support.V4.View</h2>

<h3 id='Android.Support.V4.View.GestureDetectorCompat'>Type Changed: Android.Support.V4.View.GestureDetectorCompat</h3>

Removed:

```
public class GestureDetectorCompatImplJellybeanMr1 : Java.Lang.Object, IGestureDetectorCompatImpl {
 		protected GestureDetectorCompatImplJellybeanMr1 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
 		public GestureDetectorCompatImplJellybeanMr1 (Android.Content.Context p0, GestureDetector.Android.Views.IOnGestureListener p1, Android.OS.Handler p2);
```

Added:

```
public class GestureDetectorCompatImplJellybeanMr2 : Java.Lang.Object, IGestureDetectorCompatImpl {
 		protected GestureDetectorCompatImplJellybeanMr2 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
 		public GestureDetectorCompatImplJellybeanMr2 (Android.Content.Context p0, GestureDetector.Android.Views.IOnGestureListener p1, Android.OS.Handler p2);
```

<h3 id='Android.Support.V4.View.GravityCompat'>New Type: Android.Support.V4.View.GravityCompat</h3>

```
public class GravityCompat : Java.Lang.Object {
	
	protected GravityCompat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public GravityCompat ();
	
	public static void Apply (int p0, int p1, int p2, Android.Graphics.Rect p3, int p4, int p5, Android.Graphics.Rect p6, int p7);
	public static void Apply (int p0, int p1, int p2, Android.Graphics.Rect p3, Android.Graphics.Rect p4, int p5);
	public static void ApplyDisplay (int p0, Android.Graphics.Rect p1, Android.Graphics.Rect p2, int p3);
	public static int GetAbsoluteGravity (int p0, int p1);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int End = 8388613;
	public const int RelativeHorizontalGravityMask = 8388615;
	public const int RelativeLayoutDirection = 8388608;
	public const int Start = 8388611;
	
	public class GravityCompatImplBase : Java.Lang.Object, IGravityCompatImpl {
		
		protected GravityCompatImplBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual void Apply (int p0, int p1, int p2, Android.Graphics.Rect p3, int p4, int p5, Android.Graphics.Rect p6, int p7);
		public virtual void Apply (int p0, int p1, int p2, Android.Graphics.Rect p3, Android.Graphics.Rect p4, int p5);
		public virtual void ApplyDisplay (int p0, Android.Graphics.Rect p1, Android.Graphics.Rect p2, int p3);
		public virtual int GetAbsoluteGravity (int p0, int p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class GravityCompatImplJellybeanMr1 : Java.Lang.Object, IGravityCompatImpl {
		
		protected GravityCompatImplJellybeanMr1 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual void Apply (int p0, int p1, int p2, Android.Graphics.Rect p3, int p4, int p5, Android.Graphics.Rect p6, int p7);
		public virtual void Apply (int p0, int p1, int p2, Android.Graphics.Rect p3, Android.Graphics.Rect p4, int p5);
		public virtual void ApplyDisplay (int p0, Android.Graphics.Rect p1, Android.Graphics.Rect p2, int p3);
		public virtual int GetAbsoluteGravity (int p0, int p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public interface IGravityCompatImpl : IDisposable, Android.Runtime.IJavaObject {
		
		void Apply (int p0, int p1, int p2, Android.Graphics.Rect p3, int p4, int p5, Android.Graphics.Rect p6, int p7);
		void Apply (int p0, int p1, int p2, Android.Graphics.Rect p3, Android.Graphics.Rect p4, int p5);
		void ApplyDisplay (int p0, Android.Graphics.Rect p1, Android.Graphics.Rect p2, int p3);
		int GetAbsoluteGravity (int p0, int p1);
	}
}
```

<h3 id='Android.Support.V4.View.KeyEventCompat'>Type Changed: Android.Support.V4.View.KeyEventCompat</h3>

Removed:

```
public class HoneycombKeyEventVersionImpl : Java.Lang.Object, IKeyEventVersionImpl {
 		public virtual bool MetaStateHasModifiers (int p0, int p1);
 		public virtual bool MetaStateHasNoModifiers (int p0);
 		public virtual int NormalizeMetaState (int p0);
```

Added:

```
public static bool IsTracking (Android.Views.KeyEvent p0);
 	public static void StartTracking (Android.Views.KeyEvent p0);
 		public virtual bool IsTracking (Android.Views.KeyEvent p0);
 		public virtual void StartTracking (Android.Views.KeyEvent p0);
 	public class EclairKeyEventVersionImpl : BaseKeyEventVersionImpl {
 		
 		protected EclairKeyEventVersionImpl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
 		
 		public override bool IsTracking (Android.Views.KeyEvent p0);
 		public override void StartTracking (Android.Views.KeyEvent p0);
 		
 		protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
 	}
 	public class HoneycombKeyEventVersionImpl : EclairKeyEventVersionImpl {
 		public override bool MetaStateHasModifiers (int p0, int p1);
 		public override bool MetaStateHasNoModifiers (int p0);
 		public override int NormalizeMetaState (int p0);
 		bool IsTracking (Android.Views.KeyEvent p0);
 		void StartTracking (Android.Views.KeyEvent p0);
```

<h3 id='Android.Support.V4.View.PagerAdapter'>Type Changed: Android.Support.V4.View.PagerAdapter</h3>

Added:

```
public virtual void RegisterDataSetObserver (Android.Database.DataSetObserver p0);
 	public virtual void UnregisterDataSetObserver (Android.Database.DataSetObserver p0);
```

<h3 id='Android.Support.V4.View.ViewCompat'>Type Changed: Android.Support.V4.View.ViewCompat</h3>

Added:

```
public static int GetLayoutDirection (Android.Views.View p0);
 	public static Android.Views.IViewParent GetParentForAccessibility (Android.Views.View p0);
 	public static void SetLayerPaint (Android.Views.View p0, Android.Graphics.Paint p1);
 	public static void SetLayoutDirection (Android.Views.View p0, int p1);
 	public const int LayoutDirectionInherit = 2;
 	public const int LayoutDirectionLocale = 3;
 	public const int LayoutDirectionLtr = 0;
 	public const int LayoutDirectionRtl = 1;
 		public virtual int GetLayoutDirection (Android.Views.View p0);
 		public virtual Android.Views.IViewParent GetParentForAccessibility (Android.Views.View p0);
 		public virtual void SetLayerPaint (Android.Views.View p0, Android.Graphics.Paint p1);
 		public virtual void SetLayoutDirection (Android.Views.View p0, int p1);
 		public override void SetLayerPaint (Android.Views.View p0, Android.Graphics.Paint p1);
 		int GetLayoutDirection (Android.Views.View p0);
 		Android.Views.IViewParent GetParentForAccessibility (Android.Views.View p0);
 		void SetLayerPaint (Android.Views.View p0, Android.Graphics.Paint p1);
 		void SetLayoutDirection (Android.Views.View p0, int p1);
 		public override int GetLayoutDirection (Android.Views.View p0);
 		public override void SetLayerPaint (Android.Views.View p0, Android.Graphics.Paint p1);
 		public override void SetLayoutDirection (Android.Views.View p0, int p1);
 		public override Android.Views.IViewParent GetParentForAccessibility (Android.Views.View p0);
```

<h3 id='Android.Support.V4.View.ViewCompatJB'>Type Changed: Android.Support.V4.View.ViewCompatJB</h3>

Added:

```
public static Android.Views.IViewParent GetParentForAccessibility (Android.Views.View p0);
```

<h3 id='Android.Support.V4.View.ViewCompatJellybeanMr1'>Type Removed: Android.Support.V4.View.ViewCompatJellybeanMr1</h3>

<h3 id='Android.Support.V4.View.ViewGroupCompat'>Type Changed: Android.Support.V4.View.ViewGroupCompat</h3>

Removed:

```
public class ViewGroupCompatIcsImpl : ViewGroupCompatStubImpl {
```

Added:

```
public static void SetMotionEventSplittingEnabled (Android.Views.ViewGroup p0, bool p1);
 		void SetMotionEventSplittingEnabled (Android.Views.ViewGroup p0, bool p1);
 	public class ViewGroupCompatHCImpl : ViewGroupCompatStubImpl {
 		
 		protected ViewGroupCompatHCImpl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
 		
 		public override void SetMotionEventSplittingEnabled (Android.Views.ViewGroup p0, bool p1);
 		
 		protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
 	}
 	public class ViewGroupCompatIcsImpl : ViewGroupCompatHCImpl {
 		public virtual void SetMotionEventSplittingEnabled (Android.Views.ViewGroup p0, bool p1);
```

<h3 id='Android.Support.V4.View.ViewPager'>Type Changed: Android.Support.V4.View.ViewPager</h3>

Removed:

```
public ViewPager (Android.Content.Context p0, Android.Util.IAttributeSet p1);
```

Added:

```
public ViewPager (Android.Content.Context p0, Android.Util.IAttributeSet p1);
```

<h2 id='Android.Support.V4.Widget'>Namespace: Android.Support.V4.Widget</h2>

<h3 id='Android.Support.V4.Widget.CursorAdapter'>Type Changed: Android.Support.V4.Widget.CursorAdapter</h3>

Removed:

```
public CursorAdapter (Android.Content.Context p0, Android.Database.ICursor p1);
```

Added:

```
public CursorAdapter (Android.Content.Context p0, Android.Database.ICursor p1);
```

<h3 id='Android.Support.V4.Widget.DrawerLayout'>New Type: Android.Support.V4.Widget.DrawerLayout</h3>

```
public class DrawerLayout : Android.Views.ViewGroup {
	
	protected DrawerLayout (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public DrawerLayout (Android.Content.Context p0);
	public DrawerLayout (Android.Content.Context p0, Android.Util.IAttributeSet p1, int p2);
	public DrawerLayout (Android.Content.Context p0, Android.Util.IAttributeSet p1);
	
	public virtual void CloseDrawer (int p0);
	public virtual void CloseDrawer (Android.Views.View p0);
	public virtual void CloseDrawers ();
	public virtual int GetDrawerLockMode (int p0);
	public virtual int GetDrawerLockMode (Android.Views.View p0);
	public virtual bool IsDrawerOpen (int p0);
	public virtual bool IsDrawerOpen (Android.Views.View p0);
	public virtual bool IsDrawerVisible (int p0);
	public virtual bool IsDrawerVisible (Android.Views.View p0);
	protected override void OnLayout (bool p0, int p1, int p2, int p3, int p4);
	public virtual void OpenDrawer (int p0);
	public virtual void OpenDrawer (Android.Views.View p0);
	public virtual void SetDrawerListener (IDrawerListener p0);
	public virtual void SetDrawerLockMode (int p0);
	public virtual void SetDrawerLockMode (int p0, int p1);
	public virtual void SetDrawerLockMode (int p0, Android.Views.View p1);
	public virtual void SetDrawerShadow (Android.Graphics.Drawables.Drawable p0, int p1);
	public virtual void SetDrawerShadow (int p0, int p1);
	public virtual void SetScrimColor (int p0);
	
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public const int LockModeLockedClosed = 1;
	public const int LockModeLockedOpen = 2;
	public const int LockModeUnlocked = 0;
	public const int StateDragging = 1;
	public const int StateIdle = 0;
	public const int StateSettling = 2;
	
	public event EventHandler DrawerClosed;
	public event EventHandler DrawerOpened;
	public event EventHandler DrawerSlide;
	public event EventHandler DrawerStateChanged;
	
	public class AccessibilityDelegate : Android.Support.V4.View.AccessibilityDelegateCompat {
		
		protected AccessibilityDelegate (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual bool Filter (Android.Views.View p0);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class DrawerClosedEventArgs : EventArgs {
		
		public DrawerClosedEventArgs (Android.Views.View p0);
		
		public Android.Views.View P0 {
			get;
		}
	}
	public class DrawerOpenedEventArgs : EventArgs {
		
		public DrawerOpenedEventArgs (Android.Views.View p0);
		
		public Android.Views.View P0 {
			get;
		}
	}
	public class DrawerSlideEventArgs : EventArgs {
		
		public DrawerSlideEventArgs (Android.Views.View p0, float p1);
		
		public Android.Views.View P0 {
			get;
		}
		public float P1 {
			get;
		}
	}
	public class DrawerStateChangedEventArgs : EventArgs {
		
		public DrawerStateChangedEventArgs (int p0);
		
		public int P0 {
			get;
		}
	}
	public interface IDrawerListener : IDisposable, Android.Runtime.IJavaObject {
		
		void OnDrawerClosed (Android.Views.View p0);
		void OnDrawerOpened (Android.Views.View p0);
		void OnDrawerSlide (Android.Views.View p0, float p1);
		void OnDrawerStateChanged (int p0);
	}
	public class LayoutParams : ViewGroup.Android.Views.MarginLayoutParams {
		
		protected LayoutParams (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public LayoutParams (Android.Content.Context p0, Android.Util.IAttributeSet p1);
		public LayoutParams (int p0, int p1);
		public LayoutParams (int p0, int p1, int p2);
		public LayoutParams (LayoutParams p0);
		public LayoutParams (ViewGroup.Android.Views.LayoutParams p0);
		public LayoutParams (ViewGroup.Android.Views.MarginLayoutParams p0);
		
		public int Gravity {
			get;
			set;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	protected class SavedState : View.Android.Views.BaseSavedState {
		
		protected SavedState (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public SavedState (Android.OS.Parcel p0);
		public SavedState (Android.OS.IParcelable p0);
		
		public static Android.OS.IParcelableCreator Creator {
			get;
			set;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public abstract class SimpleDrawerListener : Java.Lang.Object, IDrawerListener {
		
		protected SimpleDrawerListener (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public SimpleDrawerListener ();
		
		public virtual void OnDrawerClosed (Android.Views.View p0);
		public virtual void OnDrawerOpened (Android.Views.View p0);
		public virtual void OnDrawerSlide (Android.Views.View p0, float p1);
		public virtual void OnDrawerStateChanged (int p0);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class ViewDragCallback : Callback {
		
		protected ViewDragCallback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public ViewDragCallback (DrawerLayout __self, int p1);
		
		public virtual void RemoveCallbacks ();
		public virtual void SetDragger (ViewDragHelper p0);
		public override bool TryCaptureView (Android.Views.View p0, int p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Android.Support.V4.Widget.ScrollerCompat'>New Type: Android.Support.V4.Widget.ScrollerCompat</h3>

```
public class ScrollerCompat : Java.Lang.Object {
	
	protected ScrollerCompat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static ScrollerCompat Create (Android.Content.Context p0);
	public static ScrollerCompat Create (Android.Content.Context p0, Android.Views.Animations.IInterpolator p1);
	public virtual void AbortAnimation ();
	public virtual bool ComputeScrollOffset ();
	public virtual void Fling (int p0, int p1, int p2, int p3, int p4, int p5, int p6, int p7);
	public virtual void Fling (int p0, int p1, int p2, int p3, int p4, int p5, int p6, int p7, int p8, int p9);
	public virtual void NotifyHorizontalEdgeReached (int p0, int p1, int p2);
	public virtual void NotifyVerticalEdgeReached (int p0, int p1, int p2);
	public virtual void StartScroll (int p0, int p1, int p2, int p3);
	public virtual void StartScroll (int p0, int p1, int p2, int p3, int p4);
	
	public virtual float CurrVelocity {
		get;
	}
	public virtual int CurrX {
		get;
	}
	public virtual int CurrY {
		get;
	}
	public virtual int FinalX {
		get;
	}
	public virtual int FinalY {
		get;
	}
	public virtual bool IsFinished {
		get;
	}
	public virtual bool IsOverScrolled {
		get;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public interface IScrollerCompatImpl : IDisposable, Android.Runtime.IJavaObject {
		
		void AbortAnimation (Java.Lang.Object p0);
		bool ComputeScrollOffset (Java.Lang.Object p0);
		Java.Lang.Object CreateScroller (Android.Content.Context p0, Android.Views.Animations.IInterpolator p1);
		void Fling (Java.Lang.Object p0, int p1, int p2, int p3, int p4, int p5, int p6, int p7, int p8);
		void Fling (Java.Lang.Object p0, int p1, int p2, int p3, int p4, int p5, int p6, int p7, int p8, int p9, int p10);
		float GetCurrVelocity (Java.Lang.Object p0);
		int GetCurrX (Java.Lang.Object p0);
		int GetCurrY (Java.Lang.Object p0);
		int GetFinalX (Java.Lang.Object p0);
		int GetFinalY (Java.Lang.Object p0);
		bool IsFinished (Java.Lang.Object p0);
		bool IsOverScrolled (Java.Lang.Object p0);
		void NotifyHorizontalEdgeReached (Java.Lang.Object p0, int p1, int p2, int p3);
		void NotifyVerticalEdgeReached (Java.Lang.Object p0, int p1, int p2, int p3);
		void StartScroll (Java.Lang.Object p0, int p1, int p2, int p3, int p4);
		void StartScroll (Java.Lang.Object p0, int p1, int p2, int p3, int p4, int p5);
	}
	public class ScrollerCompatImplBase : Java.Lang.Object, IScrollerCompatImpl {
		
		protected ScrollerCompatImplBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual void AbortAnimation (Java.Lang.Object p0);
		public virtual bool ComputeScrollOffset (Java.Lang.Object p0);
		public virtual Java.Lang.Object CreateScroller (Android.Content.Context p0, Android.Views.Animations.IInterpolator p1);
		public virtual void Fling (Java.Lang.Object p0, int p1, int p2, int p3, int p4, int p5, int p6, int p7, int p8);
		public virtual void Fling (Java.Lang.Object p0, int p1, int p2, int p3, int p4, int p5, int p6, int p7, int p8, int p9, int p10);
		public virtual float GetCurrVelocity (Java.Lang.Object p0);
		public virtual int GetCurrX (Java.Lang.Object p0);
		public virtual int GetCurrY (Java.Lang.Object p0);
		public virtual int GetFinalX (Java.Lang.Object p0);
		public virtual int GetFinalY (Java.Lang.Object p0);
		public virtual bool IsFinished (Java.Lang.Object p0);
		public virtual bool IsOverScrolled (Java.Lang.Object p0);
		public virtual void NotifyHorizontalEdgeReached (Java.Lang.Object p0, int p1, int p2, int p3);
		public virtual void NotifyVerticalEdgeReached (Java.Lang.Object p0, int p1, int p2, int p3);
		public virtual void StartScroll (Java.Lang.Object p0, int p1, int p2, int p3, int p4);
		public virtual void StartScroll (Java.Lang.Object p0, int p1, int p2, int p3, int p4, int p5);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class ScrollerCompatImplGingerbread : Java.Lang.Object, IScrollerCompatImpl {
		
		protected ScrollerCompatImplGingerbread (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual void AbortAnimation (Java.Lang.Object p0);
		public virtual bool ComputeScrollOffset (Java.Lang.Object p0);
		public virtual Java.Lang.Object CreateScroller (Android.Content.Context p0, Android.Views.Animations.IInterpolator p1);
		public virtual void Fling (Java.Lang.Object p0, int p1, int p2, int p3, int p4, int p5, int p6, int p7, int p8);
		public virtual void Fling (Java.Lang.Object p0, int p1, int p2, int p3, int p4, int p5, int p6, int p7, int p8, int p9, int p10);
		public virtual float GetCurrVelocity (Java.Lang.Object p0);
		public virtual int GetCurrX (Java.Lang.Object p0);
		public virtual int GetCurrY (Java.Lang.Object p0);
		public virtual int GetFinalX (Java.Lang.Object p0);
		public virtual int GetFinalY (Java.Lang.Object p0);
		public virtual bool IsFinished (Java.Lang.Object p0);
		public virtual bool IsOverScrolled (Java.Lang.Object p0);
		public virtual void NotifyHorizontalEdgeReached (Java.Lang.Object p0, int p1, int p2, int p3);
		public virtual void NotifyVerticalEdgeReached (Java.Lang.Object p0, int p1, int p2, int p3);
		public virtual void StartScroll (Java.Lang.Object p0, int p1, int p2, int p3, int p4);
		public virtual void StartScroll (Java.Lang.Object p0, int p1, int p2, int p3, int p4, int p5);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class ScrollerCompatImplIcs : ScrollerCompatImplGingerbread {
		
		protected ScrollerCompatImplIcs (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public override float GetCurrVelocity (Java.Lang.Object p0);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Android.Support.V4.Widget.SearchViewCompat'>Type Changed: Android.Support.V4.Widget.SearchViewCompat</h3>

Added:

```
public static string GetQuery (Android.Views.View p0);
 	public static Java.Lang.ICharSequence GetQueryFormatted (Android.Views.View p0);
 	public static bool IsIconified (Android.Views.View p0);
 	public static bool IsQueryRefinementEnabled (Android.Views.View p0);
 	public static bool IsSubmitButtonEnabled (Android.Views.View p0);
 	public static void SetIconified (Android.Views.View p0, bool p1);
 	public static void SetImeOptions (Android.Views.View p0, int p1);
 	public static void SetInputType (Android.Views.View p0, int p1);
 	public static void SetMaxWidth (Android.Views.View p0, int p1);
 	public static void SetOnCloseListener (Android.Views.View p0, OnCloseListenerCompat p1);
 	public static void SetQuery (Android.Views.View p0, Java.Lang.ICharSequence p1, bool p2);
 	public static void SetQuery (Android.Views.View p0, string p1, bool p2);
 	public static void SetQueryHint (Android.Views.View p0, Java.Lang.ICharSequence p1);
 	public static void SetQueryHint (Android.Views.View p0, string p1);
 	public static void SetQueryRefinementEnabled (Android.Views.View p0, bool p1);
 	public static void SetSearchableInfo (Android.Views.View p0, Android.Content.ComponentName p1);
 	public static void SetSubmitButtonEnabled (Android.Views.View p0, bool p1);
 		Java.Lang.ICharSequence GetQueryFormatted (Android.Views.View p0);
 		bool IsIconified (Android.Views.View p0);
 		bool IsQueryRefinementEnabled (Android.Views.View p0);
 		bool IsSubmitButtonEnabled (Android.Views.View p0);
 		Java.Lang.Object NewOnCloseListener (OnCloseListenerCompat p0);
 		void SetIconified (Android.Views.View p0, bool p1);
 		void SetImeOptions (Android.Views.View p0, int p1);
 		void SetInputType (Android.Views.View p0, int p1);
 		void SetMaxWidth (Android.Views.View p0, int p1);
 		void SetOnCloseListener (Java.Lang.Object p0, Java.Lang.Object p1);
 		void SetQuery (Android.Views.View p0, Java.Lang.ICharSequence p1, bool p2);
 		void SetQueryHint (Android.Views.View p0, Java.Lang.ICharSequence p1);
 		void SetQueryRefinementEnabled (Android.Views.View p0, bool p1);
 		void SetSearchableInfo (Android.Views.View p0, Android.Content.ComponentName p1);
 		void SetSubmitButtonEnabled (Android.Views.View p0, bool p1);
 	}
 	public abstract class OnCloseListenerCompat : Java.Lang.Object {
 		
 		protected OnCloseListenerCompat (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
 		public OnCloseListenerCompat ();
 		
 		public virtual bool OnClose ();
 		
 		protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
 		public string GetQuery (Android.Views.View p0);
 		public override Java.Lang.ICharSequence GetQueryFormatted (Android.Views.View p0);
 		public override bool IsIconified (Android.Views.View p0);
 		public override bool IsQueryRefinementEnabled (Android.Views.View p0);
 		public override bool IsSubmitButtonEnabled (Android.Views.View p0);
 		public override Java.Lang.Object NewOnCloseListener (OnCloseListenerCompat p0);
 		public override void SetIconified (Android.Views.View p0, bool p1);
 		public override void SetMaxWidth (Android.Views.View p0, int p1);
 		public override void SetOnCloseListener (Java.Lang.Object p0, Java.Lang.Object p1);
 		public override void SetQuery (Android.Views.View p0, Java.Lang.ICharSequence p1, bool p2);
 		public override void SetQueryHint (Android.Views.View p0, Java.Lang.ICharSequence p1);
 		public override void SetQueryRefinementEnabled (Android.Views.View p0, bool p1);
 		public override void SetSearchableInfo (Android.Views.View p0, Android.Content.ComponentName p1);
 		public override void SetSubmitButtonEnabled (Android.Views.View p0, bool p1);
 		
 		protected override IntPtr ThresholdClass {
 			get;
 		}
 		protected override Type ThresholdType {
 			get;
 		}
 	}
 	public class SearchViewCompatIcsImpl : SearchViewCompatHoneycombImpl {
 		
 		protected SearchViewCompatIcsImpl (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
 		
 		public override Android.Views.View NewSearchView (Android.Content.Context p0);
 		public override void SetImeOptions (Android.Views.View p0, int p1);
 		public override void SetInputType (Android.Views.View p0, int p1);
 		public string GetQuery (Android.Views.View p0);
 		public virtual Java.Lang.ICharSequence GetQueryFormatted (Android.Views.View p0);
 		public virtual bool IsIconified (Android.Views.View p0);
 		public virtual bool IsQueryRefinementEnabled (Android.Views.View p0);
 		public virtual bool IsSubmitButtonEnabled (Android.Views.View p0);
 		public virtual Java.Lang.Object NewOnCloseListener (OnCloseListenerCompat p0);
 		public virtual void SetIconified (Android.Views.View p0, bool p1);
 		public virtual void SetImeOptions (Android.Views.View p0, int p1);
 		public virtual void SetInputType (Android.Views.View p0, int p1);
 		public virtual void SetMaxWidth (Android.Views.View p0, int p1);
 		public virtual void SetOnCloseListener (Java.Lang.Object p0, Java.Lang.Object p1);
 		public virtual void SetQuery (Android.Views.View p0, Java.Lang.ICharSequence p1, bool p2);
 		public void SetQuery (Android.Views.View p0, string p1, bool p2);
 		public virtual void SetQueryHint (Android.Views.View p0, Java.Lang.ICharSequence p1);
 		public void SetQueryHint (Android.Views.View p0, string p1);
 		public virtual void SetQueryRefinementEnabled (Android.Views.View p0, bool p1);
 		public virtual void SetSearchableInfo (Android.Views.View p0, Android.Content.ComponentName p1);
 		public virtual void SetSubmitButtonEnabled (Android.Views.View p0, bool p1);
```

<h3 id='Android.Support.V4.Widget.SearchViewCompatISearchViewCompatImplExtensions'>New Type: Android.Support.V4.Widget.SearchViewCompatISearchViewCompatImplExtensions</h3>

```
public static class SearchViewCompatISearchViewCompatImplExtensions {
	
	public static string GetQuery (ISearchViewCompatImpl self, Android.Views.View p0);
	public static void SetQuery (ISearchViewCompatImpl self, Android.Views.View p0, string p1, bool p2);
	public static void SetQueryHint (ISearchViewCompatImpl self, Android.Views.View p0, string p1);
}
```

<h3 id='Android.Support.V4.Widget.SimpleCursorAdapter'>Type Changed: Android.Support.V4.Widget.SimpleCursorAdapter</h3>

Added:

```
set;
 		set;
```

<h3 id='Android.Support.V4.Widget.SlidingPaneLayout'>New Type: Android.Support.V4.Widget.SlidingPaneLayout</h3>

```
public class SlidingPaneLayout : Android.Views.ViewGroup {
	
	protected SlidingPaneLayout (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	public SlidingPaneLayout (Android.Content.Context p0, Android.Util.IAttributeSet p1);
	public SlidingPaneLayout (Android.Content.Context p0, Android.Util.IAttributeSet p1, int p2);
	public SlidingPaneLayout (Android.Content.Context p0);
	
	protected virtual bool CanScroll (Android.Views.View p0, bool p1, int p2, int p3, int p4);
	public virtual bool CanSlide ();
	public virtual bool ClosePane ();
	protected override void OnLayout (bool p0, int p1, int p2, int p3, int p4);
	public virtual bool OpenPane ();
	public virtual void SetPanelSlideListener (IPanelSlideListener p0);
	public virtual void SetShadowDrawable (Android.Graphics.Drawables.Drawable p0);
	public virtual void SetShadowResource (int p0);
	public virtual void SmoothSlideClosed ();
	public virtual void SmoothSlideOpen ();
	
	public virtual int CoveredFadeColor {
		get;
		set;
	}
	public virtual bool IsOpen {
		get;
	}
	public virtual bool IsSlideable {
		get;
	}
	public virtual int ParallaxDistance {
		get;
		set;
	}
	public virtual int SliderFadeColor {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	
	public event EventHandler PanelClosed;
	public event EventHandler PanelOpened;
	public event EventHandler PanelSlide;
	
	public class AccessibilityDelegate : Android.Support.V4.View.AccessibilityDelegateCompat {
		
		protected AccessibilityDelegate (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual bool Filter (Android.Views.View p0);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class DisableLayerRunnable : Java.Lang.Object, Java.Lang.IRunnable {
		
		protected DisableLayerRunnable (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual void Run ();
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class DragHelperCallback : Callback {
		
		protected DragHelperCallback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public override bool TryCaptureView (Android.Views.View p0, int p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public interface IPanelSlideListener : IDisposable, Android.Runtime.IJavaObject {
		
		void OnPanelClosed (Android.Views.View p0);
		void OnPanelOpened (Android.Views.View p0);
		void OnPanelSlide (Android.Views.View p0, float p1);
	}
	public interface ISlidingPanelLayoutImpl : IDisposable, Android.Runtime.IJavaObject {
		
		void InvalidateChildRegion (SlidingPaneLayout p0, Android.Views.View p1);
	}
	public class LayoutParams : ViewGroup.Android.Views.MarginLayoutParams {
		
		protected LayoutParams (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public LayoutParams ();
		public LayoutParams (int p0, int p1);
		public LayoutParams (ViewGroup.Android.Views.LayoutParams p0);
		public LayoutParams (ViewGroup.Android.Views.MarginLayoutParams p0);
		public LayoutParams (LayoutParams p0);
		public LayoutParams (Android.Content.Context p0, Android.Util.IAttributeSet p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
		public float Weight {
			get;
			set;
		}
	}
	public class PanelClosedEventArgs : EventArgs {
		
		public PanelClosedEventArgs (Android.Views.View p0);
		
		public Android.Views.View P0 {
			get;
		}
	}
	public class PanelOpenedEventArgs : EventArgs {
		
		public PanelOpenedEventArgs (Android.Views.View p0);
		
		public Android.Views.View P0 {
			get;
		}
	}
	public class PanelSlideEventArgs : EventArgs {
		
		public PanelSlideEventArgs (Android.Views.View p0, float p1);
		
		public Android.Views.View P0 {
			get;
		}
		public float P1 {
			get;
		}
	}
	public class SavedState : View.Android.Views.BaseSavedState {
		
		protected SavedState (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public static Android.OS.IParcelableCreator Creator {
			get;
			set;
		}
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class SimplePanelSlideListener : Java.Lang.Object, IPanelSlideListener {
		
		protected SimplePanelSlideListener (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public SimplePanelSlideListener ();
		
		public virtual void OnPanelClosed (Android.Views.View p0);
		public virtual void OnPanelOpened (Android.Views.View p0);
		public virtual void OnPanelSlide (Android.Views.View p0, float p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class SlidingPanelLayoutImplBase : Java.Lang.Object, ISlidingPanelLayoutImpl {
		
		protected SlidingPanelLayoutImplBase (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public virtual void InvalidateChildRegion (SlidingPaneLayout p0, Android.Views.View p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class SlidingPanelLayoutImplJB : SlidingPanelLayoutImplBase {
		
		protected SlidingPanelLayoutImplJB (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public override void InvalidateChildRegion (SlidingPaneLayout p0, Android.Views.View p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
	public class SlidingPanelLayoutImplJBMR1 : SlidingPanelLayoutImplBase {
		
		protected SlidingPanelLayoutImplJBMR1 (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		
		public override void InvalidateChildRegion (SlidingPaneLayout p0, Android.Views.View p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```

<h3 id='Android.Support.V4.Widget.ViewDragHelper'>New Type: Android.Support.V4.Widget.ViewDragHelper</h3>

```
public class ViewDragHelper : Java.Lang.Object {
	
	protected ViewDragHelper (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
	
	public static ViewDragHelper Create (Android.Views.ViewGroup p0, Callback p1);
	public static ViewDragHelper Create (Android.Views.ViewGroup p0, float p1, Callback p2);
	public virtual void Abort ();
	public virtual void Cancel ();
	protected virtual bool CanScroll (Android.Views.View p0, bool p1, int p2, int p3, int p4, int p5);
	public virtual void CaptureChildView (Android.Views.View p0, int p1);
	public virtual bool CheckTouchSlop (int p0);
	public virtual bool CheckTouchSlop (int p0, int p1);
	public virtual bool ContinueSettling (bool p0);
	public virtual Android.Views.View FindTopChildUnder (int p0, int p1);
	public virtual void FlingCapturedView (int p0, int p1, int p2, int p3);
	public virtual bool IsCapturedViewUnder (int p0, int p1);
	public virtual bool IsEdgeTouched (int p0);
	public virtual bool IsEdgeTouched (int p0, int p1);
	public virtual bool IsPointerDown (int p0);
	public virtual bool IsViewUnder (Android.Views.View p0, int p1, int p2);
	public virtual void ProcessTouchEvent (Android.Views.MotionEvent p0);
	public virtual void SetEdgeTrackingEnabled (int p0);
	public virtual bool SettleCapturedViewAt (int p0, int p1);
	public virtual bool ShouldInterceptTouchEvent (Android.Views.MotionEvent p0);
	public virtual bool SmoothSlideViewTo (Android.Views.View p0, int p1, int p2);
	
	public virtual int ActivePointerId {
		get;
	}
	public virtual Android.Views.View CapturedView {
		get;
	}
	public virtual int EdgeSize {
		get;
	}
	public virtual float MinVelocity {
		get;
		set;
	}
	protected override IntPtr ThresholdClass {
		get;
	}
	protected override Type ThresholdType {
		get;
	}
	public virtual int TouchSlop {
		get;
	}
	public virtual int ViewDragState {
		get;
	}
	
	public const int DirectionAll = 3;
	public const int DirectionHorizontal = 1;
	public const int DirectionVertical = 2;
	public const int EdgeAll = 15;
	public const int EdgeBottom = 8;
	public const int EdgeLeft = 1;
	public const int EdgeRight = 2;
	public const int EdgeTop = 4;
	public const int InvalidPointer = -1;
	public const int StateDragging = 1;
	public const int StateIdle = 0;
	public const int StateSettling = 2;
	
	public abstract class Callback : Java.Lang.Object {
		
		protected Callback (IntPtr javaReference, Android.Runtime.JniHandleOwnership transfer);
		public Callback ();
		
		public virtual int ClampViewPositionHorizontal (Android.Views.View p0, int p1, int p2);
		public virtual int ClampViewPositionVertical (Android.Views.View p0, int p1, int p2);
		public virtual int GetOrderedChildIndex (int p0);
		public virtual int GetViewHorizontalDragRange (Android.Views.View p0);
		public virtual int GetViewVerticalDragRange (Android.Views.View p0);
		public virtual void OnEdgeDragStarted (int p0, int p1);
		public virtual bool OnEdgeLock (int p0);
		public virtual void OnEdgeTouched (int p0, int p1);
		public virtual void OnViewCaptured (Android.Views.View p0, int p1);
		public virtual void OnViewDragStateChanged (int p0);
		public virtual void OnViewPositionChanged (Android.Views.View p0, int p1, int p2, int p3, int p4);
		public virtual void OnViewReleased (Android.Views.View p0, float p1, float p2);
		public abstract bool TryCaptureView (Android.Views.View p0, int p1);
		
		protected override IntPtr ThresholdClass {
			get;
		}
		protected override Type ThresholdType {
			get;
		}
	}
}
```
