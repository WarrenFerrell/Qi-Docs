QiStream API calls
==================

The API calls in this section are all used to create and manipulate QiStreams. See .. _Qi Types: https://github.com/osisoft/Qi-Docs/blob/Qi_Edits/docs/Qi_Streams.rst for a list of supported QiTypes, a discussion of compound indexes, and general information about QiTypes. 


``GetStream()``
----------------

Returns a QiStream object from the specified namespace that matches the specified namespace and streamId.


**Syntax**


::

    QiStream GetStream(string tenantId, string namespaceId, string streamId);
    Task<QiStream> GetStreamAsync (string tenantId, string namespaceId, string streamId);

*Http*

::

    GET Qi/{tenantId}/{namespaceId}/Streams/{streamId}

**Parameters**

``string tenantID``
  The tenant identifier for the request
``string namespaceId``
  The namespace identifier for the request
``string streamId``
  The ID of the stream to retrieve

**Optional parameters**

  None
  
**Returns**
  A QiStream object for the specified streamId and namespace

Security
  Allowed by administrator and user accounts



``GetStreams()``
----------------

Returns all streams from the specified namespace.

**Syntax**

::

    IEnumerable<QiStream> GetStreams (string tenantId, string namespaceId);
    Task<IEnumerable<QiStream>> GetStreamsAsync (string tenantId, string namespaceId);

*Http*

::

    GET Qi/{tenantId}/{namespaceId}/Streams

**Parameters**

``string tenantID``
  The tenant identifier for the request
``string namespaceId``
  The namespace identifier for the request

**Optional parameters**

  None
  
**Returns**
  IEnumerable of all QiStreams in the namespace of the defined tenant.

Security
  Allowed by administrator and user accounts
  


``GetStreams()`` (GetStreams() overload)
----------------

Searches for and returns streams that fit search criteria

**Syntax**

::

   IEnumerable<QiStream> GetStreams(string searchText, int skip, int count);
   Task<IEnumerable<QiStream>> GetStreamsAsync (string searchText, int skip, int count);
  

*Http*

::

    GET Qi/{tenantId}/{namespaceId}/Streams  

**Parameters**

``string tenantID``
  The tenant identifier for the request
``string namespaceId``
  The namespace identifier for the request
``searchText``
  The text to search for.
 
**Optional parameters**

``skip``
  The number of matched stream names to skip over before returning the matching streams.
``count``
  The maximum number of streams to return. 

  
**Returns**
  An Ienumerable object of streams that fit search criteria.

Security
  Allowed by administrator and user accounts
  
  


``GetOrCreateStream()``
----------------

Returns a stream that matches the QiStream qistream within the specified namespace, or creates the stream if it does not already exist. If the stream exists, it is returned to the caller unchanged.

**Syntax**

::

    QiStream GetOrCreateStream (string tenantId, string namespaceId, QiStream qistream);
    Task<QiStream> GetOrCreateStreamAsync (string tenantId, string namespaceId, QiStream qistream);

*Http*

::

    POST Qi/{tenantId}/{namespaceId}/Streams

**Parameters**

``string tenantID``
  The tenant identifier for the request
``string namespaceId``
  The namespace identifier for the request
``qistream``
  Qi Stream object
 
**Optional parameters**

  None
  
**Returns**
  An QiStream

Security
  Allowed by administrator accounts
  


``UpdateStream()``
----------------

Updates a specified stream in a specified namespace with the properties in the specified QiStream qistream. The following changes are permitted:

• Name

• BehaviorId

• Description

An exception is thrown on unpermitted change attempt (and the stream is
left unchanged)

The *UpdateStream()* method applies to the entire entity. Optional fields
that are omitted from the entity will remove the field from the stream if the fields had been set previously.


**Syntax**

::

    void UpdateStream(string tenantId, string namespaceId, string streamId, QiStream qistream);
    Task UpdateStreamAsync(string tenantId, string namespaceId, string streamId, QiStream qistream);

*Http*

::

    PUT Qi/{tenantId}/{namespaceId}/Streams/{streamId}

**Parameters**

``string tenantID``
  The tenant identifier for the request
``string namespaceId``
  The namespace identifier for the request
``streamId``
  Identifier of the stream to modify
``qistream``
  Updated stream object
 
**Optional parameters**

  None
  
**Returns**
  A QiStream

Security
  Allowed by administrator accounts
  



``DeleteStream()``
----------------

Deletes a stream that matches the QiStream entity within the specified tenantId and namespace.

**Syntax**

::

    void DeleteStream(string tenantId, string namespaceId, string streamId);
    Task DeleteStreamAsync(string tenantId, string namespaceId, string streamId);

*Http*

::

    DELETE Qi/{tenantId}/{namespaceId}/Streams/{streamId}

**Parameters**

``string tenantID``
  The tenant identifier for the request
``string namespaceId``
  The namespace identifier for the request.
``streamId``
  The identifier of the stream to delete.

  **Optional parameters**

  None
  
**Returns**
  A QiStream

Security
  Allowed by administrator accounts
  