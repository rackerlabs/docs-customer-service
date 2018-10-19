.. _get-list-of-customer-account-history:

Get a list of customer account history
--------------------------------------

This operation returns a list of all customer account history changes.

.. list-table::
  :widths: 10 60
  :header-rows: 1

  * - Method
    - URI

  * - GET
    - /v1/customer_accounts/{accountType}/{accountId}/history{?changeType}

These tables show the possible response codes for this operation:

.. list-table::
   :widths: 79
   :header-rows: 1

   * - Normal response codes:
   * - 200 (OK)

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

This table shows the query parameters for the request:

.. list-table::
  :widths: 10 25 44
  :header-rows: 1

  * - NAME
    - Type
    - Description

  * - changeType
    - AccountChangeType
    - Optional change type to filter results.

This operation does not require a request body.

Response
^^^^^^^^^

**XML response**

.. literalinclude:: methods/responses/get-customer-account-history-response-xml
   :language: xml

**JSON response**

.. literalinclude:: methods/responses/get-customer-account-history-response-json
   :language: json
