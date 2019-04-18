---
id: 34500BCB-D2D5-AD96-42CF-37D68F4FCA0D
title: "From 3.0.11 to 3.0.12"
---

&nbsp;

 <a name="Namespace:_MonoTouch" class="injected"></a>


# Namespace: MonoTouch

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

 <a name="Type_Changed:_MonoTouch.Constants" class="injected"></a>


## Type Changed: MonoTouch.Constants

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

Removed:

```
public const string Version = "3.0.11";
```

Added:

```
public const string Version = "3.0.12";
```

 <a name="Namespace:_MonoTouch.CoreAnimation" class="injected"></a>


# Namespace: MonoTouch.CoreAnimation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

 <a name="Type_Changed:_MonoTouch.CoreAnimation.CAKeyFrameAnimation" class="injected"></a>


## Type Changed: MonoTouch.CoreAnimation.CAKeyFrameAnimation

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

Added:

```
public static MonoTouch.Foundation.NSString CalculationDiscrete {
                get;
        }
        public static MonoTouch.Foundation.NSString CalculationLinear {
                get;
        }
        public static MonoTouch.Foundation.NSString CalculationPaced {
                get;
        }
```

 <a name="Namespace:_MonoTouch.CoreData" class="injected"></a>


# Namespace: MonoTouch.CoreData

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

 <a name="New_Type:_MonoTouch.CoreData.NSAtomicStore" class="injected"></a>


## New Type: MonoTouch.CoreData.NSAtomicStore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSAtomicStore : NSPersistentStore {
        
        public NSAtomicStore ();
        public NSAtomicStore (MonoTouch.Foundation.NSCoder coder);
        public NSAtomicStore (MonoTouch.Foundation.NSObjectFlag t);
        public NSAtomicStore (IntPtr handle);
        public NSAtomicStore (NSPersistentStoreCoordinator coordinator, string configurationName, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options);
        
        public virtual void AddCacheNodes (MonoTouch.Foundation.NSSet cacheNodes);
        public virtual NSAtomicStoreCacheNode CacheNodeForObjectID (NSManagedObjectID objectID);
        public virtual bool Load (out MonoTouch.Foundation.NSError error);
        public virtual NSAtomicStoreCacheNode NewCacheNodeForManagedObject (NSManagedObject managedObject);
        public virtual NSAtomicStore NewReferenceObjectForManagedObject (NSManagedObject managedObject);
        public virtual NSManagedObjectID ObjectIDForEntity (NSEntityDescription entity, MonoTouch.Foundation.NSObject data);
        public virtual NSAtomicStore ReferenceObjectForObjectID (NSManagedObjectID objectID);
        public virtual bool Save (out MonoTouch.Foundation.NSError error);
        public virtual void UpdateCacheNode (NSAtomicStoreCacheNode node, NSManagedObject managedObject);
        public virtual void WillRemoveCacheNodes (MonoTouch.Foundation.NSSet cacheNodes);
        
        public virtual MonoTouch.Foundation.NSSet CacheNodes {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSAtomicStoreCacheNode" class="injected"></a>


## New Type: MonoTouch.CoreData.NSAtomicStoreCacheNode

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSAtomicStoreCacheNode : MonoTouch.Foundation.NSObject {
        
        public NSAtomicStoreCacheNode ();
        public NSAtomicStoreCacheNode (MonoTouch.Foundation.NSCoder coder);
        public NSAtomicStoreCacheNode (MonoTouch.Foundation.NSObjectFlag t);
        public NSAtomicStoreCacheNode (IntPtr handle);
        public NSAtomicStoreCacheNode (NSManagedObjectID moid);
        
        public virtual void SetValue (MonoTouch.Foundation.NSObject value, string key);
        public virtual NSAtomicStoreCacheNode ValueForKey (string key);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSManagedObjectID ObjectID {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary PropertyCache {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSAttributeDescription" class="injected"></a>


## New Type: MonoTouch.CoreData.NSAttributeDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSAttributeDescription : NSPropertyDescription {
        
        public NSAttributeDescription ();
        public NSAttributeDescription (MonoTouch.Foundation.NSCoder coder);
        public NSAttributeDescription (MonoTouch.Foundation.NSObjectFlag t);
        public NSAttributeDescription (IntPtr handle);
        
        public virtual void SetDefaultValue (MonoTouch.Foundation.NSObject value);
        
        public virtual NSAttributeType AttributeType {
                get;
                set;
        }
        public virtual string AttributeValueClassName {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSAttributeDescription DefaultValue {
                get;
        }
        public virtual string ValueTransformerName {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSData VersionHash {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSAttributeType" class="injected"></a>


## New Type: MonoTouch.CoreData.NSAttributeType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
[Serializable]
public enum NSAttributeType : uint {
        Undefined,
        Integer16,
        Integer32,
        Integer64,
        Decimal,
        Double,
        Float,
        String,
        Boolean,
        Date,
        Binary,
        Transformable
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSDeleteRule" class="injected"></a>


## New Type: MonoTouch.CoreData.NSDeleteRule

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
[Serializable]
public enum NSDeleteRule : uint {
        NoAction,
        Nullify,
        Cascade,
        Deny
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSEntityDescription" class="injected"></a>


## New Type: MonoTouch.CoreData.NSEntityDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSEntityDescription : MonoTouch.Foundation.NSObject {
        
        public NSEntityDescription ();
        public NSEntityDescription (MonoTouch.Foundation.NSCoder coder);
        public NSEntityDescription (MonoTouch.Foundation.NSObjectFlag t);
        public NSEntityDescription (IntPtr handle);
        
        public static NSEntityDescription EntityForName (string entityName, NSManagedObjectContext context);
        public static NSEntityDescription InsertNewObjectForEntityForName (string entityName, NSManagedObjectContext context);
        public virtual bool IsKindOfEntity (NSEntityDescription entity);
        public virtual NSRelationshipDescription[] RelationshipsWithDestinationEntity (NSEntityDescription entity);
        
        public virtual bool Abstract {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary AttributesByName {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string ManagedObjectClassName {
                get;
                set;
        }
        public virtual NSManagedObjectModel ManagedObjectModel {
                get;
        }
        public virtual string Name {
                get;
                set;
        }
        public virtual NSPropertyDescription[] Properties {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary PropertiesByName {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary RelationshipsByName {
                get;
        }
        public virtual NSEntityDescription[] Subentities {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary SubentitiesByName {
                get;
        }
        public virtual NSEntityDescription Superentity {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary UserInfo {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSData VersionHash {
                get;
        }
        public virtual string VersionHashModifier {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSEntityMapping" class="injected"></a>


## New Type: MonoTouch.CoreData.NSEntityMapping

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSEntityMapping : MonoTouch.Foundation.NSObject {
        
        public NSEntityMapping ();
        public NSEntityMapping (MonoTouch.Foundation.NSCoder coder);
        public NSEntityMapping (MonoTouch.Foundation.NSObjectFlag t);
        public NSEntityMapping (IntPtr handle);
        
        public virtual NSPropertyMapping[] AttributeMappings {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string DestinationEntityName {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSData DestinationEntityVersionHash {
                get;
                set;
        }
        public virtual string EntityMigrationPolicyClassName {
                get;
                set;
        }
        public virtual NSEntityMappingType MappingType {
                get;
                set;
        }
        public virtual string Name {
                get;
                set;
        }
        public virtual NSPropertyMapping[] RelationshipMappings {
                get;
                set;
        }
        public virtual string SourceEntityName {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSData SourceEntityVersionHash {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSExpression SourceExpression {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary UserInfo {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSEntityMappingType" class="injected"></a>


## New Type: MonoTouch.CoreData.NSEntityMappingType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
[Serializable]
public enum NSEntityMappingType : uint {
        Undefined,
        Custom,
        Add,
        Remove,
        Copy,
        Transform
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSEntityMigrationPolicy" class="injected"></a>


## New Type: MonoTouch.CoreData.NSEntityMigrationPolicy

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSEntityMigrationPolicy : MonoTouch.Foundation.NSObject {
        
        public NSEntityMigrationPolicy ();
        public NSEntityMigrationPolicy (MonoTouch.Foundation.NSCoder coder);
        public NSEntityMigrationPolicy (MonoTouch.Foundation.NSObjectFlag t);
        public NSEntityMigrationPolicy (IntPtr handle);
        
        public virtual bool BeginEntityMapping (NSEntityMapping mapping, NSMigrationManager manager, out MonoTouch.Foundation.NSError error);
        public virtual bool CreateDestinationInstancesForSourceInstance (NSManagedObject sInstance, NSEntityMapping mapping, NSMigrationManager manager, out MonoTouch.Foundation.NSError error);
        public virtual bool CreateRelationshipsForDestinationInstance (NSManagedObject dInstance, NSEntityMapping mapping, NSMigrationManager manager, out MonoTouch.Foundation.NSError error);
        public virtual bool EndEntityMapping (NSEntityMapping mapping, NSMigrationManager manager, out MonoTouch.Foundation.NSError error);
        public virtual bool EndInstanceCreationForEntityMapping (NSEntityMapping mapping, NSMigrationManager manager, out MonoTouch.Foundation.NSError error);
        public virtual bool EndRelationshipCreationForEntityMapping (NSEntityMapping mapping, NSMigrationManager manager, out MonoTouch.Foundation.NSError error);
        public virtual bool PerformCustomValidationForEntityMapping (NSEntityMapping mapping, NSMigrationManager manager, out MonoTouch.Foundation.NSError error);
        
        public override IntPtr ClassHandle {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSFetchedPropertyDescription" class="injected"></a>


## New Type: MonoTouch.CoreData.NSFetchedPropertyDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSFetchedPropertyDescription : NSPropertyDescription {
        
        public NSFetchedPropertyDescription ();
        public NSFetchedPropertyDescription (MonoTouch.Foundation.NSCoder coder);
        public NSFetchedPropertyDescription (MonoTouch.Foundation.NSObjectFlag t);
        public NSFetchedPropertyDescription (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSFetchRequest FetchRequest {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSFetchRequest" class="injected"></a>


## New Type: MonoTouch.CoreData.NSFetchRequest

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSFetchRequest : MonoTouch.Foundation.NSObject {
        
        public NSFetchRequest ();
        public NSFetchRequest (MonoTouch.Foundation.NSCoder coder);
        public NSFetchRequest (MonoTouch.Foundation.NSObjectFlag t);
        public NSFetchRequest (IntPtr handle);
        
        public virtual NSPersistentStore[] AffectedStores {
                get;
                set;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSEntityDescription Entity {
                get;
                set;
        }
        public virtual uint FetchLimit {
                get;
                set;
        }
        public virtual bool IncludesPropertyValues {
                get;
                set;
        }
        public virtual bool IncludesSubentities {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSPredicate Predicate {
                get;
                set;
        }
        public virtual string [] RelationshipKeyPathsForPrefetching {
                get;
                set;
        }
        public virtual NSFetchRequestResultType ResultType {
                get;
                set;
        }
        public virtual bool ReturnsObjectsAsFaults {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSSortDescriptor[] SortDescriptors {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSFetchRequestResultType" class="injected"></a>


## New Type: MonoTouch.CoreData.NSFetchRequestResultType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
[Serializable]
public enum NSFetchRequestResultType : uint {
        ManagedObject,
        ManagedObjectID
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSKeyValueSetMutationKind" class="injected"></a>


## New Type: MonoTouch.CoreData.NSKeyValueSetMutationKind

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
[Serializable]
public enum NSKeyValueSetMutationKind : uint {
        Union,
        Minus,
        Intersect,
        NSKeyValueSet
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSManagedObject" class="injected"></a>


## New Type: MonoTouch.CoreData.NSManagedObject

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSManagedObject : MonoTouch.Foundation.NSObject {
        
        public NSManagedObject ();
        public NSManagedObject (MonoTouch.Foundation.NSCoder coder);
        public NSManagedObject (MonoTouch.Foundation.NSObjectFlag t);
        public NSManagedObject (IntPtr handle);
        public NSManagedObject (NSEntityDescription entity, NSManagedObjectContext context);
        
        public virtual void AwakeFromFetch ();
        public virtual void AwakeFromInsert ();
        public virtual MonoTouch.Foundation.NSDictionary CommittedValuesForKeys (string [] keys);
        public virtual void DidAccessValueForKey (string key);
        public virtual void DidChangeValueForKey (string key);
        public virtual void DidChangeValueForKey (string inKey, NSKeyValueSetMutationKind inMutationKind, MonoTouch.Foundation.NSSet inObjects);
        public virtual void DidSave ();
        public virtual void DidTurnIntoFault ();
        public virtual bool HasFaultForRelationshipNamed (string key);
        public virtual IntPtr PrimitiveValueForKey (string key);
        public virtual void SetPrimitiveValue (IntPtr value, string key);
        public virtual void SetValue (IntPtr value, string key);
        public virtual bool ValidateForDelete (out MonoTouch.Foundation.NSError error);
        public virtual bool ValidateForInsert (out MonoTouch.Foundation.NSError error);
        public virtual bool ValidateForUpdate (out MonoTouch.Foundation.NSError error);
        public virtual bool ValidateValue (MonoTouch.Foundation.NSObject value, string key, out MonoTouch.Foundation.NSError error);
        public virtual IntPtr ValueForKey (string key);
        public virtual void WillAccessValueForKey (string key);
        public virtual void WillChangeValueForKey (string key);
        public virtual void WillChangeValueForKey (string inKey, NSKeyValueSetMutationKind inMutationKind, MonoTouch.Foundation.NSSet inObjects);
        public virtual void WillSave ();
        public virtual void WillTurnIntoFault ();
        
        public virtual MonoTouch.Foundation.NSDictionary ChangedValues {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSEntityDescription Entity {
                get;
        }
        public virtual bool IsDeleted {
                get;
        }
        public virtual bool IsFault {
                get;
        }
        public virtual bool IsInserted {
                get;
        }
        public virtual bool IsUpdated {
                get;
        }
        public virtual NSManagedObjectContext ManagedObjectContext {
                get;
        }
        public virtual NSManagedObjectID ObjectID {
                get;
        }
        public virtual IntPtr ObservationInfo {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSManagedObjectContext" class="injected"></a>


## New Type: MonoTouch.CoreData.NSManagedObjectContext

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSManagedObjectContext : MonoTouch.Foundation.NSObject {
        
        public NSManagedObjectContext ();
        public NSManagedObjectContext (MonoTouch.Foundation.NSCoder coder);
        public NSManagedObjectContext (MonoTouch.Foundation.NSObjectFlag t);
        public NSManagedObjectContext (IntPtr handle);
        
        public virtual void AssignObject (IntPtr object1, NSPersistentStore store);
        public virtual uint CountForFetchRequest (NSFetchRequest request, out MonoTouch.Foundation.NSError error);
        public virtual void DeleteObject (NSManagedObject object1);
        public virtual void DetectConflictsForObject (NSManagedObject object1);
        public virtual MonoTouch.Foundation.NSObject[] ExecuteFetchRequest (NSFetchRequest request, out MonoTouch.Foundation.NSError error);
        public virtual void InsertObject (NSManagedObject object1);
        public virtual void Lock ();
        public virtual void MergeChangesFromContextDidSaveNotification (MonoTouch.Foundation.NSNotification notification);
        public virtual NSManagedObject ObjectRegisteredForID (NSManagedObjectID objectID);
        public virtual NSManagedObject ObjectWithID (NSManagedObjectID objectID);
        public virtual void ObserveValueForKeyPath (string keyPath, IntPtr object1, MonoTouch.Foundation.NSDictionary change, IntPtr context);
        public virtual bool ObtainPermanentIDsForObjects (NSManagedObject[] objects, out MonoTouch.Foundation.NSError error);
        public virtual void ProcessPendingChanges ();
        public virtual void Redo ();
        public virtual void RefreshObject (NSManagedObject object1, bool flag);
        public virtual void Reset ();
        public virtual void Rollback ();
        public virtual bool Save (out MonoTouch.Foundation.NSError error);
        public virtual void Undo ();
        public virtual void Unlock ();
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual MonoTouch.Foundation.NSSet DeletedObjects {
                get;
        }
        public virtual bool HasChanges {
                get;
        }
        public virtual MonoTouch.Foundation.NSSet InsertedObjects {
                get;
        }
        public virtual IntPtr MergePolicy {
                get;
                set;
        }
        public virtual NSPersistentStoreCoordinator PersistentStoreCoordinator {
                get;
                set;
        }
        public virtual bool PropagatesDeletesAtEndOfEvent {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSSet RegisteredObjects {
                get;
        }
        public virtual bool RetainsRegisteredObjects {
                get;
                set;
        }
        public virtual double StalenessInterval {
                get;
                set;
        }
        public virtual bool TryLock {
                get;
        }
        public virtual MonoTouch.Foundation.NSUndoManager UndoManager {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSSet UpdatedObjects {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSManagedObjectID" class="injected"></a>


## New Type: MonoTouch.CoreData.NSManagedObjectID

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSManagedObjectID : MonoTouch.Foundation.NSObject {
        
        public NSManagedObjectID ();
        public NSManagedObjectID (MonoTouch.Foundation.NSCoder coder);
        public NSManagedObjectID (MonoTouch.Foundation.NSObjectFlag t);
        public NSManagedObjectID (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSEntityDescription Entity {
                get;
        }
        public virtual bool IsTemporaryID {
                get;
        }
        public virtual NSPersistentStore PersistentStore {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl URIRepresentation {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSManagedObjectModel" class="injected"></a>


## New Type: MonoTouch.CoreData.NSManagedObjectModel

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSManagedObjectModel : MonoTouch.Foundation.NSObject {
        
        public NSManagedObjectModel ();
        public NSManagedObjectModel (MonoTouch.Foundation.NSCoder coder);
        public NSManagedObjectModel (MonoTouch.Foundation.NSObjectFlag t);
        public NSManagedObjectModel (IntPtr handle);
        public NSManagedObjectModel (MonoTouch.Foundation.NSUrl url);
        
        public static NSManagedObjectModel MergedModelFromBundles (MonoTouch.Foundation.NSBundle[] bundles);
        public static NSManagedObjectModel MergedModelFromBundles (MonoTouch.Foundation.NSBundle[] bundles, MonoTouch.Foundation.NSDictionary metadata);
        public static NSManagedObjectModel ModelByMergingModels (NSManagedObjectModel[] models);
        public static NSManagedObjectModel ModelByMergingModels (NSManagedObjectModel[] models, MonoTouch.Foundation.NSDictionary metadata);
        public virtual string [] EntitiesForConfiguration (string configuration);
        public virtual NSFetchRequest FetchRequestFromTemplateWithName (string name, MonoTouch.Foundation.NSDictionary variables);
        public virtual NSFetchRequest FetchRequestTemplateForName (string name);
        public virtual bool IsConfiguration (string configuration, MonoTouch.Foundation.NSDictionary metadata);
        public virtual void SetEntities (NSEntityDescription[] entities, string configuration);
        public virtual void SetFetchRequestTemplate (NSFetchRequest fetchRequestTemplate, string name);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string [] Configurations {
                get;
        }
        public virtual NSEntityDescription[] Entities {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary EntitiesByName {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary EntityVersionHashesByName {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary FetchRequestTemplatesByName {
                get;
        }
        public virtual IntPtr Init {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary LocalizationDictionary {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSSet VersionIdentifiers {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSMappingModel" class="injected"></a>


## New Type: MonoTouch.CoreData.NSMappingModel

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSMappingModel : MonoTouch.Foundation.NSObject {
        
        public NSMappingModel ();
        public NSMappingModel (MonoTouch.Foundation.NSCoder coder);
        public NSMappingModel (MonoTouch.Foundation.NSObjectFlag t);
        public NSMappingModel (IntPtr handle);
        public NSMappingModel (MonoTouch.Foundation.NSUrl url);
        
        public static NSMappingModel MappingModelFromBundles (MonoTouch.Foundation.NSBundle[] bundles, NSManagedObjectModel sourceModel, NSManagedObjectModel destinationModel);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSEntityMapping[] EntityMappings {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary EntityMappingsByName {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSMigrationManager" class="injected"></a>


## New Type: MonoTouch.CoreData.NSMigrationManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSMigrationManager : MonoTouch.Foundation.NSObject {
        
        public NSMigrationManager ();
        public NSMigrationManager (MonoTouch.Foundation.NSCoder coder);
        public NSMigrationManager (MonoTouch.Foundation.NSObjectFlag t);
        public NSMigrationManager (IntPtr handle);
        public NSMigrationManager (NSManagedObjectModel sourceModel, NSManagedObjectModel destinationModel);
        
        public virtual void AssociateSourceInstance (NSManagedObject sourceInstance, NSManagedObject destinationInstance, NSEntityMapping entityMapping);
        public virtual void CancelMigrationWithError (MonoTouch.Foundation.NSError error);
        public virtual NSEntityDescription DestinationEntityForEntityMapping (NSEntityMapping mEntity);
        public virtual NSManagedObject[] DestinationInstancesForEntityMappingNamed (string mappingName, NSManagedObject[] sourceInstances);
        public virtual bool MigrateStoreFromUrl (MonoTouch.Foundation.NSUrl sourceURL, string sStoreType, MonoTouch.Foundation.NSDictionary sOptions, NSMappingModel mappings, MonoTouch.Foundation.NSUrl dURL, string dStoreType, MonoTouch.Foundation.NSDictionary dOptions, out MonoTouch.Foundation.NSError error);
        public virtual void Reset ();
        public virtual NSEntityDescription SourceEntityForEntityMapping (NSEntityMapping mEntity);
        public virtual NSManagedObject[] SourceInstancesForEntityMappingNamed (string mappingName, NSManagedObject[] destinationInstances);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSEntityMapping CurrentEntityMapping {
                get;
        }
        public virtual NSManagedObjectContext DestinationContext {
                get;
        }
        public virtual NSManagedObjectModel DestinationModel {
                get;
        }
        public virtual NSMappingModel MappingModel {
                get;
        }
        public virtual float MigrationProgress {
                get;
        }
        public virtual NSManagedObjectContext SourceContext {
                get;
        }
        public virtual NSManagedObjectModel SourceModel {
                get;
        }
        public virtual MonoTouch.Foundation.NSDictionary UserInfo {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSPersistentStore" class="injected"></a>


## New Type: MonoTouch.CoreData.NSPersistentStore

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSPersistentStore : MonoTouch.Foundation.NSObject {
        
        public NSPersistentStore ();
        public NSPersistentStore (MonoTouch.Foundation.NSCoder coder);
        public NSPersistentStore (MonoTouch.Foundation.NSObjectFlag t);
        public NSPersistentStore (IntPtr handle);
        public NSPersistentStore (NSPersistentStoreCoordinator root, string name, MonoTouch.Foundation.NSUrl url, MonoTouch.Foundation.NSDictionary options);
        
        public static MonoTouch.Foundation.NSDictionary MetadataForPersistentStoreWithUrl (MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public static bool SetMetadata (MonoTouch.Foundation.NSDictionary metadata, MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public virtual void DidAddToPersistentStoreCoordinator (NSPersistentStoreCoordinator coordinator);
        public virtual void WillRemoveFromPersistentStoreCoordinator (NSPersistentStoreCoordinator coordinator);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string ConfigurationName {
                get;
        }
        public virtual string Identifier {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary Metadata {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary Options {
                get;
        }
        public virtual NSPersistentStoreCoordinator PersistentStoreCoordinator {
                get;
        }
        public virtual bool ReadOnly {
                get;
                set;
        }
        public virtual string Type {
                get;
        }
        public virtual MonoTouch.Foundation.NSUrl Url {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSPersistentStoreCoordinator" class="injected"></a>


## New Type: MonoTouch.CoreData.NSPersistentStoreCoordinator

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSPersistentStoreCoordinator : MonoTouch.Foundation.NSObject {
        
        public NSPersistentStoreCoordinator ();
        public NSPersistentStoreCoordinator (MonoTouch.Foundation.NSCoder coder);
        public NSPersistentStoreCoordinator (MonoTouch.Foundation.NSObjectFlag t);
        public NSPersistentStoreCoordinator (IntPtr handle);
        public NSPersistentStoreCoordinator (NSManagedObjectModel model);
        
        public static MonoTouch.Foundation.NSDictionary MetadataForPersistentStoreOfType (string storeType, MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public static MonoTouch.Foundation.NSDictionary MetadataForPersistentStoreWithUrl (MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public static void RegisterStoreClass (MonoTouch.ObjCRuntime.Class storeClass, string storeType);
        public static bool SetMetadata (MonoTouch.Foundation.NSDictionary metadata, string storeType, MonoTouch.Foundation.NSUrl url, out MonoTouch.Foundation.NSError error);
        public virtual NSPersistentStore AddPersistentStoreWithType (string storeType, string configuration, MonoTouch.Foundation.NSUrl storeURL, MonoTouch.Foundation.NSDictionary options, out MonoTouch.Foundation.NSError error);
        public virtual void Lock ();
        public virtual NSManagedObjectID ManagedObjectIDForURIRepresentation (MonoTouch.Foundation.NSUrl url);
        public virtual MonoTouch.Foundation.NSDictionary MetadataForPersistentStore (NSPersistentStore store);
        public virtual NSPersistentStore MigratePersistentStore (NSPersistentStore store, MonoTouch.Foundation.NSUrl URL, MonoTouch.Foundation.NSDictionary options, string storeType, out MonoTouch.Foundation.NSError error);
        public virtual NSPersistentStore PersistentStoreForUrl (MonoTouch.Foundation.NSUrl URL);
        public virtual bool RemovePersistentStore (NSPersistentStore store, out MonoTouch.Foundation.NSError error);
        public virtual void SetMetadata (MonoTouch.Foundation.NSDictionary metadata, NSPersistentStore store);
        public virtual bool SetUrl (MonoTouch.Foundation.NSUrl url, NSPersistentStore store);
        public virtual void Unlock ();
        public virtual MonoTouch.Foundation.NSUrl UrlForPersistentStore (NSPersistentStore store);
        
        public static MonoTouch.Foundation.NSDictionary RegisteredStoreTypes {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSManagedObjectModel ManagedObjectModel {
                get;
        }
        public virtual NSPersistentStore[] PersistentStores {
                get;
        }
        public virtual bool TryLock {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSPropertyDescription" class="injected"></a>


## New Type: MonoTouch.CoreData.NSPropertyDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSPropertyDescription : MonoTouch.Foundation.NSObject {
        
        public NSPropertyDescription ();
        public NSPropertyDescription (MonoTouch.Foundation.NSCoder coder);
        public NSPropertyDescription (MonoTouch.Foundation.NSObjectFlag t);
        public NSPropertyDescription (IntPtr handle);
        
        public virtual void SetValidationPredicates (MonoTouch.Foundation.NSPredicate[] validationPredicates, string [] validationWarnings);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSEntityDescription Entity {
                get;
        }
        public virtual bool Indexed {
                get;
                set;
        }
        public virtual string Name {
                get;
                set;
        }
        public virtual bool Optional {
                get;
                set;
        }
        public virtual bool Transient {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary UserInfo {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSPredicate[] ValidationPredicates {
                get;
        }
        public virtual string [] ValidationWarnings {
                get;
        }
        public virtual MonoTouch.Foundation.NSData VersionHash {
                get;
        }
        public virtual string VersionHashModifier {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSPropertyMapping" class="injected"></a>


## New Type: MonoTouch.CoreData.NSPropertyMapping

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSPropertyMapping : MonoTouch.Foundation.NSObject {
        
        public NSPropertyMapping ();
        public NSPropertyMapping (MonoTouch.Foundation.NSCoder coder);
        public NSPropertyMapping (MonoTouch.Foundation.NSObjectFlag t);
        public NSPropertyMapping (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual string Name {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSDictionary UserInfo {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSExpression ValueExpression {
                get;
                set;
        }
}
```

 <a name="New_Type:_MonoTouch.CoreData.NSRelationshipDescription" class="injected"></a>


## New Type: MonoTouch.CoreData.NSRelationshipDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSRelationshipDescription : NSPropertyDescription {
        
        public NSRelationshipDescription ();
        public NSRelationshipDescription (MonoTouch.Foundation.NSCoder coder);
        public NSRelationshipDescription (MonoTouch.Foundation.NSObjectFlag t);
        public NSRelationshipDescription (IntPtr handle);
        
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSDeleteRule DeleteRule {
                get;
                set;
        }
        public virtual NSEntityDescription DestinationEntity {
                get;
                set;
        }
        public virtual NSRelationshipDescription InverseRelationship {
                get;
                set;
        }
        public virtual bool IsToMany {
                get;
        }
        public virtual uint MaxCount {
                get;
                set;
        }
        public virtual uint MinCount {
                get;
                set;
        }
        public virtual MonoTouch.Foundation.NSData VersionHash {
                get;
        }
}
```

 <a name="Namespace:_MonoTouch.CoreLocation" class="injected"></a>


# Namespace: MonoTouch.CoreLocation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

 <a name="Type_Changed:_MonoTouch.CoreLocation.CLLocationManager" class="injected"></a>


## Type Changed: MonoTouch.CoreLocation.CLLocationManager

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

Removed:

```
public virtual bool HeadingAvailable {
                get;
        }
```

Added:

```
public static bool _HeadingAvailable {
                get;
        }
```

 <a name="Type_Changed:_MonoTouch.EventKit.EKEvent" class="injected"></a>


## Type Changed: MonoTouch.EventKit.EKEvent

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

Added:

```
set;
```

 <a name="Namespace:_MonoTouch.Foundation" class="injected"></a>


# Namespace: MonoTouch.Foundation

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

 <a name="Type_Changed:_MonoTouch.Foundation.NSAttributedString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSAttributedString

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

Added:

```
public static NSString ForegroundColorAttributeName {
                get;
        }
```

 <a name="New_Type:_MonoTouch.Foundation.NSExpression" class="injected"></a>


## New Type: MonoTouch.Foundation.NSExpression

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public class NSExpression : NSObject {
        
        public NSExpression ();
        public NSExpression (NSCoder coder);
        public NSExpression (NSObjectFlag t);
        public NSExpression (IntPtr handle);
        public NSExpression (NSExpressionType type);
        
        public static NSExpression FromConstant (NSObject obj);
        public static NSExpression FromFuction (string name, NSExpression[] parameters);
        public static NSExpression FromFunction (NSExpressionHandler target, NSExpression[] parameters);
        public static NSExpression FromFunction (NSExpression target, string name, NSExpression[] parameters);
        public static NSExpression FromIntersectSet (NSExpression left, NSExpression right);
        public static NSExpression FromKeyPath (string keyPath);
        public static NSExpression FromMinusSet (NSExpression left, NSExpression right);
        public static NSExpression FromSubquery (NSExpression expression, string variable, NSObject predicate);
        public static NSExpression FromUnionSet (NSExpression left, NSExpression right);
        public static NSExpression FromVariable (string string1);
        public virtual NSExpression ExpressionValueWithObject (NSObject object1, NSMutableDictionary context);
        public virtual NSExpression FromAggregate (NSExpression[] subexpressions);
        
        public static NSExpression ExpressionForEvaluatedObject {
                get;
        }
        public virtual NSExpression[] Arguments {
                get;
        }
        public override IntPtr ClassHandle {
                get;
        }
        public virtual NSObject Collection {
                get;
        }
        public virtual NSObject ConstantValue {
                get;
        }
        public virtual NSExpressionType ExpressionType {
                get;
        }
        public virtual string Function {
                get;
        }
        public virtual string KeyPath {
                get;
        }
        public virtual NSExpression LeftExpression {
                get;
        }
        public virtual NSExpression Operand {
                get;
        }
        public virtual NSPredicate Predicate {
                get;
        }
        public virtual NSExpression RightExpression {
                get;
        }
        public virtual string Variable {
                get;
        }
}
```

 <a name="New_Type:_MonoTouch.Foundation.NSExpressionHandler" class="injected"></a>


## New Type: MonoTouch.Foundation.NSExpressionHandler

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
[Serializable]
public delegate void NSExpressionHandler (NSObject evaluatedObject, NSExpression[] expressions, NSMutableDictionary context);
```

 <a name="New_Type:_MonoTouch.Foundation.NSExpressionType" class="injected"></a>


## New Type: MonoTouch.Foundation.NSExpressionType

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
[Serializable]
public enum NSExpressionType {
        ConstantValue,
        EvaluatedObject,
        Variable,
        KeyPath,
        Function,
        UnionSet,
        IntersectSet,
        MinusSet,
        Subquery,
        NSAggregate,
        Block
}
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSNumber" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSNumber

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

Added:

```
public override string ToString ();
        
        public static implicit operator NSNumber (float value);
        public static implicit operator NSNumber (double value);
        public static implicit operator NSNumber (bool value);
        public static implicit operator NSNumber (sbyte value);
        public static implicit operator NSNumber (byte value);
        public static implicit operator NSNumber (short value);
        public static implicit operator NSNumber (ushort value);
        public static implicit operator NSNumber (int value);
        public static implicit operator NSNumber (uint value);
        public static implicit operator NSNumber (long value);
        public static implicit operator NSNumber (ulong value);
        public static explicit operator byte (NSNumber source);
        public static explicit operator sbyte (NSNumber source);
        public static explicit operator short (NSNumber source);
        public static explicit operator ushort (NSNumber source);
        public static explicit operator int (NSNumber source);
        public static explicit operator uint (NSNumber source);
        public static explicit operator long (NSNumber source);
        public static explicit operator ulong (NSNumber source);
        public static explicit operator float (NSNumber source);
        public static explicit operator double (NSNumber source);
        public static explicit operator bool (NSNumber source);
```

 <a name="Type_Changed:_MonoTouch.Foundation.NSString" class="injected"></a>


## Type Changed: MonoTouch.Foundation.NSString

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

Added:

```
public virtual char _characterAtIndex (int index);
        public char this [int idx] {
                get;
        }
        public virtual int Length {
                get;
        }
```

 <a name="Namespace:_MonoTouch.ObjCRuntime" class="injected"></a>


# Namespace: MonoTouch.ObjCRuntime

 <a name="" class="injected"></a>


#  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Class" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Class

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

Added:

```
public static void RegisterMethods (Type type, System.Collections.Generic.Dictionary<IntPtr,MethodDescription> methods);
```

 <a name="Type_Changed:_MonoTouch.ObjCRuntime.Messaging" class="injected"></a>


## Type Changed: MonoTouch.ObjCRuntime.Messaging

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

Added:

```
public static bool Boolean_objc_msgSend_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8);
        public static bool Boolean_objc_msgSendSuper_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2, IntPtr arg3, IntPtr arg4, IntPtr arg5, IntPtr arg6, IntPtr arg7, IntPtr arg8);
        public static char Char_objc_msgSend_int (IntPtr receiver, IntPtr selector, int arg1);
        public static char Char_objc_msgSendSuper_int (IntPtr receiver, IntPtr selector, int arg1);
        public static uint UInt32_objc_msgSend_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2);
        public static uint UInt32_objc_msgSendSuper_IntPtr_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, IntPtr arg2);
        public static void void_objc_msgSend_IntPtr_UInt32_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3);
        public static void void_objc_msgSendSuper_IntPtr_UInt32_IntPtr (IntPtr receiver, IntPtr selector, IntPtr arg1, uint arg2, IntPtr arg3);
```

 <a name="New_Type:_MonoTouch.ObjCRuntime.MethodDescription" class="injected"></a>


## New Type: MonoTouch.ObjCRuntime.MethodDescription

 <a name="" class="injected"></a>


##  [ <span class="icon"><img src="from_3.0.11_to_3.0.12/Images/icon-trans.gif"></span>](http://ios.xamarin.com/Releases/MonoTouch_3/MonoTouch_3.0.12#)

```
public struct MethodDescription {
        
        public MethodDescription (System.Reflection.MethodBase method, ArgumentSemantic semantic);
}
```
