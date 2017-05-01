Community
==========


``Get()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Communities/{id}

**Parameters**

``String id``


**Security**

**********************

``FindCommunitiesForTenant()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Communities

**Parameters**

``String tenantId``
``String skip``
``String take``
``String query``


**Security**

**********************

``FindCommunitiesForUser()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Users/{userId}/Communities

**Parameters**

``String userId``
``String skip``
``String take``
``String query``


**Security**

**********************

``CreateNew()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Communities

**Parameters**

``Community community``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "Description": "description",
  "TenantIds": null
}


**Security**

**********************

``Update()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	PUT api/Communities/{id}

**Parameters**

``String id``
``Community community``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "Description": "description",
  "TenantIds": null
}


**Security**

**********************

``AddTenant()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	PUT api/Communities/{communityId}/Tenants/{tenantId}

**Parameters**

``String communityId``
``String tenantId``


**Security**

**********************

``RemoveTenant()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Communities/{communityId}/Tenants/{tenantId}

**Parameters**

``String communityId``
``String tenantId``


**Security**

**********************

``Delete()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Communities/{id}

**Parameters**

``String id``


**Security**

**********************
Display
==========


``Get()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Displays/{id}

**Parameters**

``String tenantId``
``String id``


**Security**

**********************

``Find()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Displays

**Parameters**

``String tenantId``
``String skip``
``String take``
``String q``
``String folderId``


**Security**

**********************

``FindAllDisplaysForUser()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Users/{userId}/Displays

**Parameters**

``String userId``
``String skip``
``String take``
``String query``


**Security**

**********************

``CreateNew()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/Displays

**Parameters**

``String tenantId``
``Display display``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "Description": "description",
  "Content": "content",
  "Folder": null,
  "TenantId": "tenantid",
  "Owner": null,
  "AccessControlList": null
}


**Security**

**********************

``Update()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	PUT api/Tenants/{tenantId}/Displays/{id}

**Parameters**

``String tenantId``
``String id``
``Display display``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "Description": "description",
  "Content": "content",
  "Folder": null,
  "TenantId": "tenantid",
  "Owner": null,
  "AccessControlList": null
}


**Security**

**********************

``Delete()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/Displays/{id}

**Parameters**

``String tenantId``
``String id``


**Security**

**********************
DisplayFolder
==========


``Get()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Folders/{id}

**Parameters**

``String tenantId``
``String id``


**Security**

**********************

``GetChildFolders()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Folders

**Parameters**

``String tenantId``
``String skip``
``String take``
``String parentId``


**Security**

**********************

``CreateNew()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/Folders

**Parameters**

``String tenantId``
``DisplayFolder displayFolder``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "Description": "description",
  "Parent": null,
  "TenantId": "tenantid",
  "Owner": null,
  "AccessControlList": null
}


**Security**

**********************

``Update()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	PUT api/Tenants/{tenantId}/Folders/{id}

**Parameters**

``String tenantId``
``String id``
``DisplayFolder displayFolder``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "Description": "description",
  "Parent": null,
  "TenantId": "tenantid",
  "Owner": null,
  "AccessControlList": null
}


**Security**

**********************

``Delete()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/Folders/{id}

**Parameters**

``String tenantId``
``String id``


**Security**

**********************
Feature
==========

GlobalGroup
==========

Group
==========


``GetGroup()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Groups/{groupId}

**Parameters**

``String tenantId``
``String groupId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``GetGroups()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Groups

**Parameters**

``String tenantId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``GetGroupMembers()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Groups/{groupId}/Users

**Parameters**

``String tenantId``
``String groupId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``Create()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/Groups

**Parameters**

``String tenantId``
``Group group``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "AzureActiveDirectoryGroupName": "azureactivedirectorygroupname",
  "Description": "description"
}


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``Delete()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/Groups/{groupId}

**Parameters**

``String tenantId``
``String groupId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``AddUserToGroup()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/Groups/{groupId}/Users

**Parameters**

``String tenantId``
``String groupId``
``CreateUser user``

**Body**

::

{
  "SendNotification": false,
  "IsAdministrator": false,
  "Id": "id",
  "FirstName": "firstname",
  "LastName": "lastname",
  "LoginName": "loginname",
  "ContactEmail": "contactemail",
  "ContactPhone": "contactphone",
  "UPN": "upn",
  "Password": "password"
}


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``RemoveUserFromGroup()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/Groups/{groupId}/Users/{userId}

**Parameters**

``String tenantId``
``String groupId``
``String userId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************
Namespace
==========


``GetAll()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Namespaces

**Parameters**

``String tenantId``


**Security**
Any OSIsoft Cloud Services user

**********************

``GetNamespaceById()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Namespaces/{Id}

**Parameters**

``String id``
``String tenantId``


**Security**
Any OSIsoft Cloud Services user

**********************

``Create()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/Namespaces

**Parameters**

``Namespace namespaceObj``
``Boolean IsServerTest``

**Body**

::

{
  "Id": "id",
  "TenantId": "tenantid",
  "Description": "description",
  "TierId": "tierid",
  "ThroughputUnits": 0,
  "StorageUnits": 0,
  "CalculationUnits": 0,
  "State": 0
}


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``Delete()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/Namespaces/{Id}

**Parameters**

``String id``
``String tenantId``
``Boolean IsServerTest``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``Update()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	PUT api/Tenants/{tenantId}/Namespaces/{Id}

**Parameters**

``String id``
``String tenantId``
``Namespace namespaceObj``
``Boolean IsServerTest``

**Body**

::

{
  "Id": "id",
  "TenantId": "tenantid",
  "Description": "description",
  "TierId": "tierid",
  "ThroughputUnits": 0,
  "StorageUnits": 0,
  "CalculationUnits": 0,
  "State": 0
}


**Security**
OSIsoft Cloud Services tenant administrator

**********************
Role
==========


``Get()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Roles/{id}

**Parameters**

``String id``


**Security**

**********************

``GetTenantRole()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Roles/{id}

**Parameters**

``String tenantId``
``String id``


**Security**

**********************

``GetCommunityRole()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Communities/{communityId}/Roles/{id}

**Parameters**

``String communityId``
``String id``


**Security**

**********************

``CreateNewTenantRole()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/Roles

**Parameters**

``String tenantId``
``Role role``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "Description": "description",
  "RoleType": 0,
  "TenantId": "tenantid",
  "CommunityId": "communityid"
}


**Security**

**********************

``CreateNewCommunityRole()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Communities/{communityId}/Roles

**Parameters**

``String communityId``
``Role role``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "Description": "description",
  "RoleType": 0,
  "TenantId": "tenantid",
  "CommunityId": "communityid"
}


**Security**

**********************

``Update()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	PUT api/Roles/{id}

**Parameters**

``String id``
``Role role``

**Body**

::

{
  "Id": "id",
  "Name": "name",
  "Description": "description",
  "RoleType": 0,
  "TenantId": "tenantid",
  "CommunityId": "communityid"
}


**Security**

**********************

``Delete()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Roles/{id}

**Parameters**

``String id``


**Security**

**********************
ServiceBlog
==========


``GetByPage()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/ServiceBlog/Entries

**Parameters**

``String skip``
``String take``


**Security**
Any OSIsoft Cloud Services user

**********************
ServiceBlogTemplate
==========

Service
==========

Tenant
==========


``GetTenant()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}

**Parameters**

``String tenantId``


**Security**
Any OSIsoft Cloud Services user

**********************

``TenantExists()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	HEAD api/Tenants/{tenantId}

**Parameters**

``String tenantId``


**Security**
Any OSIsoft Cloud Services user

**********************
TenantFeatureState
==========


``Get()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Features/{id}

**Parameters**

``String tenantId``
``String id``


**Security**
Any OSIsoft Cloud Services user

**********************
TenantServiceState
==========

Applications
==========


``CreateClientApiKeySet()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/ClientApiKeySets

**Parameters**

``ClientApiKeySet keySet``

**Body**

::

{
  "AppUri": "appuri",
  "CreateFirstKey": false,
  "DisplayName": "displayname",
  "RequiredResource": null,
  "TenantId": "tenantid"
}


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``GetOrCreateClientApiKeySet()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/GetOrCreateClientApiKeySets

**Parameters**

``ClientApiKeySet keySet``

**Body**

::

{
  "AppUri": "appuri",
  "CreateFirstKey": false,
  "DisplayName": "displayname",
  "RequiredResource": null,
  "TenantId": "tenantid"
}


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``AppUriExists()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Applications/Exists

**Parameters**

``String tenantId``
``String applicationId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``DeleteClientApiKeySet()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/ClientApiKeySets/{applicationId}

**Parameters**

``String tenantId``
``String applicationId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``CreateClientApiKeyForApplication()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/ClientApiKeySets/Keys

**Parameters**

``String tenantId``
``String applicationId``
``String description``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``GetClientApiKeyCollectionFromApplication()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/ClientApiKeySets/Keys

**Parameters**

``String tenantId``
``String applicationId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``DeleteClientApiKeyFromApplication()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/ClientApiKeySets/Keys

**Parameters**

``String tenantId``
``String applicationId``
``String keyId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``PurgeCloudServicesApplications()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Applications/PurgeAllCloudServicesApplications

**Parameters**

``String tenantId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``AddRoleToApplication()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	PUT api/Tenants/{tenantId}/Applications/{applicationId}/Roles/{roleId}

**Parameters**

``String applicationId``
``String roleId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``RemoveRoleFromApplication()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/Applications/{applicationId}/Roles/{roleId}

**Parameters**

``String applicationId``
``String roleId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``Find()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Applications/{applicationId}/Roles

**Parameters**

``String applicationId``
``String skip``
``String take``
``String query``


**Security**
OSIsoft Cloud Services tenant administrator

**********************
NamespaceTier
==========


``GetNamespaceTier()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/NamespaceTiers/{id}

**Parameters**

``String id``


**Security**
Any OSIsoft Cloud Services user

**********************

``GetAllNamespaceTiers()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/NamespaceTiers

**Parameters**




**Security**
Any OSIsoft Cloud Services user

**********************
Testing
==========

Utilities
==========


``Ping()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Utilities/ping

**Parameters**




**Security**
Any OSIsoft Cloud Services user

**********************
User
==========


``Get()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Users/{userId}

**Parameters**

``String tenantId``
``String userId``


**Security**
OSIsoft Cloud Services tenant administrator
The OSIsoft Cloud Services user which is the object of this call

**********************

``Get()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Users

**Parameters**

``String tenantId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``GetUserGroups()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Users/{userId}/Groups

**Parameters**

``String tenantId``
``String userId``


**Security**
OSIsoft Cloud Services tenant administrator
The OSIsoft Cloud Services user which is the object of this call

**********************

``IsUserInGroup()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Users/{userId}/Groups/{groupId}

**Parameters**

``String tenantId``
``String userId``
``String groupId``


**Security**
OSIsoft Cloud Services tenant administrator
The OSIsoft Cloud Services user which is the object of this call

**********************

``CreateUser()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/Users/

**Parameters**

``String tenantId``
``CreateUser user``

**Body**

::

{
  "SendNotification": false,
  "IsAdministrator": false,
  "Id": "id",
  "FirstName": "firstname",
  "LastName": "lastname",
  "LoginName": "loginname",
  "ContactEmail": "contactemail",
  "ContactPhone": "contactphone",
  "UPN": "upn",
  "Password": "password"
}


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``Update()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	PUT api/Tenants/{tenantId}/Users/{userId}

**Parameters**

``String tenantId``
``String userId``
``CreateUser user``

**Body**

::

{
  "SendNotification": false,
  "IsAdministrator": false,
  "Id": "id",
  "FirstName": "firstname",
  "LastName": "lastname",
  "LoginName": "loginname",
  "ContactEmail": "contactemail",
  "ContactPhone": "contactphone",
  "UPN": "upn",
  "Password": "password"
}


**Security**
OSIsoft Cloud Services tenant administrator
The OSIsoft Cloud Services user which is the object of this call

**********************

``Delete()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/Users/{userId}

**Parameters**

``String tenantId``
``String userId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``ResetUserPassword()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	POST api/Tenants/{tenantId}/Users/{userId}/PasswordReset

**Parameters**

``String tenantId``
``String userId``


**Security**
OSIsoft Cloud Services tenant administrator

**********************

``AddRoleToUser()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	PUT api/Tenants/{tenantId}/Users/{userId}/Roles/{roleId}

**Parameters**

``String tenantId``
``String userId``
``String roleId``


**Security**

**********************

``RemoveRoleFromUser()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	DELETE api/Tenants/{tenantId}/Users/{userId}/Roles/{roleId}

**Parameters**

``String userId``
``String roleId``


**Security**

**********************

``Find()``
----------------------


**Syntax**

.. highlight:: none

**Http**

::

	GET api/Tenants/{tenantId}/Users/{userId}/Roles

**Parameters**

``String userId``
``String skip``
``String take``
``String query``


**Security**

**********************
