---
id: D2F157A7-15FF-49AF-B490-01C25DF170F2
title: "From 6.3.1 to 6.3.2"
---

<html><head><title>Comparison between monotouch-6.3.1.0.dll and monotouch-6.3.2.0.dll</title></head>
<body>
<h2>Namespace: MonoTouch</h2>
<h3>Type Changed: MonoTouch.Constants</h3>
<p>Removed:</p><pre>
 	public const string Version = "6.3.1";
</pre>
<p>Added:</p><pre>
 	public const string Version = "6.3.2";
</pre>
<h2>Namespace: MonoTouch.Foundation</h2>
<h3>Type Changed: MonoTouch.Foundation.NSUrlCredential</h3>
<p>Removed:</p><pre>
 	public NSUrlCredential (IntPtr SecTrustRef_trust, bool ignored);
</pre>
<p>Added:</p><pre>
 	public NSUrlCredential (IntPtr trust, bool ignored);
</pre>
<h2>Namespace: MonoTouch.UIKit</h2>
<h3>Type Changed: MonoTouch.UIKit.UICollectionViewLayoutAttributes</h3>
<p>Added:</p><pre>
 	public static T CreateForCell&lt;T&gt; (MonoTouch.Foundation.NSIndexPath indexPath) where T : UICollectionViewLayoutAttributes;
</pre>
<h3>Type Changed: MonoTouch.UIKit.UITableViewController</h3>
<p>Added:</p><pre>
 	public virtual void AccessoryButtonTapped (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual UITableViewCellAccessory AccessoryForRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual bool CanEditRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual bool CanMoveRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual bool CanPerformAction (UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
 	public virtual void CellDisplayingEnded (UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void CommitEditingStyle (UITableView tableView, UITableViewCellEditingStyle editingStyle, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual MonoTouch.Foundation.NSIndexPath CustomizeMoveTarget (UITableView tableView, MonoTouch.Foundation.NSIndexPath sourceIndexPath, MonoTouch.Foundation.NSIndexPath proposedIndexPath);
 	public virtual void DidEndEditing (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual UITableViewCellEditingStyle EditingStyleForRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void FooterViewDisplayingEnded (UITableView tableView, UIView footerView, int section);
 	public virtual UITableViewCell GetCell (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual float GetHeightForFooter (UITableView tableView, int section);
 	public virtual float GetHeightForHeader (UITableView tableView, int section);
 	public virtual float GetHeightForRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual UIView GetViewForFooter (UITableView tableView, int section);
 	public virtual UIView GetViewForHeader (UITableView tableView, int section);
 	public virtual void HeaderViewDisplayingEnded (UITableView tableView, UIView headerView, int section);
 	public virtual int IndentationLevel (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void MoveRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath sourceIndexPath, MonoTouch.Foundation.NSIndexPath destinationIndexPath);
 	public virtual int NumberOfSections (UITableView tableView);
 	public virtual void PerformAction (UITableView tableView, MonoTouch.ObjCRuntime.Selector action, MonoTouch.Foundation.NSIndexPath indexPath, MonoTouch.Foundation.NSObject sender);
 	public virtual void RowDeselected (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void RowHighlighted (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
 	public virtual void RowSelected (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual int RowsInSection (UITableView tableview, int section);
 	public virtual void RowUnhighlighted (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
 	public virtual int SectionFor (UITableView tableView, string title, int atIndex);
 	public virtual string [] SectionIndexTitles (UITableView tableView);
 	public virtual bool ShouldHighlightRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowIndexPath);
 	public virtual bool ShouldIndentWhileEditing (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual bool ShouldShowMenu (UITableView tableView, MonoTouch.Foundation.NSIndexPath rowAtindexPath);
 	public virtual string TitleForDeleteConfirmation (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual string TitleForFooter (UITableView tableView, int section);
 	public virtual string TitleForHeader (UITableView tableView, int section);
 	public virtual void WillBeginEditing (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual MonoTouch.Foundation.NSIndexPath WillDeselectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void WillDisplay (UITableView tableView, UITableViewCell cell, MonoTouch.Foundation.NSIndexPath indexPath);
 	public virtual void WillDisplayFooterView (UITableView tableView, UIView footerView, int section);
 	public virtual void WillDisplayHeaderView (UITableView tableView, UIView headerView, int section);
 	public virtual MonoTouch.Foundation.NSIndexPath WillSelectRow (UITableView tableView, MonoTouch.Foundation.NSIndexPath indexPath);
</pre>
</body>
</html>
