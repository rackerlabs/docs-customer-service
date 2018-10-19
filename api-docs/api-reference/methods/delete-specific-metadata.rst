.. _delete-specific-metadata:

Delete specific metadata
------------------------

This operation deletes the metadata that matches the specified key.

.. list-table::
  :widths: 10 60
  :header-rows: 1

  * - Method
    - URI

  * - DELETE
    - /v1/customer_accounts/{accountType}/{accountId}/metadata/{metadataKey}

These tables show the possible response codes for this operation:

.. list-table::
   :widths: 79
   :header-rows: 1

   * - Normal response codes:
   * - 204 (No Content)

.. list-table::
   :widths: 79
   :header-rows: 1

   * - Error response codes:
   * - 500 (Internal Server Error)
   * - 400 (Bad Request)
   * - 401 (Unauthorized)
   * - 403 (Forbidden)
   * - 503 (Service Unavailable)
   * - 404 (Not Found)


Request
^^^^^^^^

This table shows the URI parameters for the request:

.. list-table::
  :widths: 10 19 50
  :header-rows: 1

  * - NAME
    - Type
    - Description

  * - {accountType}
    - String
    - The type of Rackspace customer account.

  * - {accountId}
    - String
    - Unique identifier of a Rackspace customer account.

  * - {metadataKey}
    - String
    - The unique key for a metadata entry.

This operation does not require a request body.

Response
^^^^^^^^^

This operation does not return a response body.
