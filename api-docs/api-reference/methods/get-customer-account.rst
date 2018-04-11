.. _get-customer-account:

Get customer account
--------------------

This operation returns details of a customer account identified by an
account ID.

.. list-table::
  :widths: 10 60
  :header-rows: 1

  * - Method
    - URI

  * - GET
    - /v1/customer_accounts/{accountType}/{accountId}

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

This operation does not require a request body.

Response:
^^^^^^^^^

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

**XML response:**

Get customer account response - ``CLOUD`` account:

.. literalinclude:: methods/responses/get-customer-account-response-cloud-xml
   :language: xml

Get customer account response - ``ManagedHosting`` account:

.. literalinclude:: methods/responses/get-customer-account-response-managed-hosting-xml
   :language: xml

Get customer account response - ``FAWS`` account:

.. literalinclude:: methods/responses/get-customer-account-response-faws-xml
   :language: xml


**JSON response:**

Get customer account response - ``CLOUD`` account:

.. literalinclude:: methods/responses/get-customer-account-response-cloud-json
   :language: json

Get customer account response - ``ManagedHosting`` account:

.. literalinclude:: methods/responses/get-customer-account-response-managed-hosting-json
   :language: json

Get customer account response - ``FAWS`` account:

.. literalinclude:: methods/responses/get-customer-account-response-faws-json
   :language: json
