.. _get-list-of-customer-accounts:

Get a list of customer accounts
-------------------------------

This operation returns a list that shows customer accounts to which the user
has access based on their tenants.

These tables show the possible response codes for this operation:

.. list-table::
  :widths: 10 60
  :header-rows: 1

  * - Method
    - URI

  * - GET
    - /v1/customer_accounts

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

Request:
^^^^^^^^

This table shows the query parameters for the request:

.. list-table::
  :widths: 10 19 50
  :header-rows: 1

  * - NAME
    - Type
    - Description

  * - metadataKey
    - String
    - Parameter to filter by whether or not an customer account has a metadata with a key of metadataKey.

  * - metadataValue
    - String
    - Parameter to filter by whether or not an customer account has a metadata with a value of metadataValue. This query parameter should only be used in combination with 'metadataKey' query parameter. If 'metadataValue' query parameter is present in the request without 'metadataKey' query parameter, then the request is considered as a Bad Request.

  * - domain
    - String
    - Parameter to filter by whether or not an customer account is within the specified domain.

  * - accountType
    - String
    - Parameter to filter by whether or not an customer account is of a specified customer account type.

  * - marker
    - String
    - Specifies the first record to be retrieved. The combination of accountType and accountNumber forms the marker, for example, CLOUD:440369.

  * - limit
    - Int
    - The number of results to return past the given marker. The default is 50.

  * - direction
    - String
    - Direction in which you want to page through the results.

This operation does not require a request body.

Response:
^^^^^^^^^

**XML response:**

.. literalinclude:: methods/responses/get-customer-accounts-response-xml
   :language: xml

**JSON response:**

.. literalinclude:: methods/responses/get-customer-accounts-response-json
   :language: json

