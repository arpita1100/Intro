# Entity Creation
Procedure - 
1. create entity
2. add pref according to your requirement



Files - 
1. Entity
2. EntityAccessService
3. EntityController
4. EntityCRUDService
5. EntityPref
6. EntityPrefController
7. EntityPrefId
8. EntityPrefRepository
9. EntityPrefService
10. EntityRepository
11. EntityService

### Entity 
- It is a model class that contains all properties of your entity and their related getters and setters.
- A table is also created for the same entity in the database.

### EntityPref
- It contains entity model class, key, categoryID, EntityPrefCategory, etc.
- A table for prefs is also created in the database.

### EntityPrefId
- It is a composite key.

### EntityRepository 
- It is an interface that extends EntityCRUDRepository which is used to perform entity-related operations in a database.

### EntityPrefRepository 
- It is an interface that extends EntityPrefRepository which is used to perform entity pref-related operations in the database.

### EntityCRUDService
- EntityCRUDService extends OrganizationalEntityCRUDService. This class contains all business logic used to perform various CRUD operations of Entity. 
### EntityPrefService
- EntityPrefService extends EntityPrefAccessService. It contains method related to adding prefs, getting access to entity prefs, etc.
### EntityService
- It contains reference to both EntityCRUDService as well as EntityPrefService. All Root levels Prefs are maintained using this service class.

### EntityController
- It extends EntityAccessController class.
- It is a controller that is responsible for communicating with Frontend code. All End-points related to an entity are mentioned in this class.
### EntityPrefController
- It extends EntityPrefController class.
- This controller contains end-points related to entity pref.

### EntityAccessService
- It is used to manage access privileges according to their role in an organization.
