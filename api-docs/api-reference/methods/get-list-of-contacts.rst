.. _get-list-of-contacts:

Get a list of contacts
----------------------

This operation returns a list of contacts associated with a customer account.

.. list-table::
  :widths: 10 60
  :header-rows: 1

  * - Method
    - URI

  * - GET
    - /v1/customer_accounts/{accountType}/{accountId}/contacts{?role, username, emailAddress, marker, limit}


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
  :widths: 10 19 50
  :header-rows: 1

  * - NAME
    - Type
    - Description

  * - role
    - String
    - The role of the contact. This parameter is used as a filter to list all
      contacts with the given role. Sample values of ``role`` are ``BILLING``
      and ``PRIMARY``.

  * - username
    - String
    - The username of the contact.

  * - emailAddress
    - String
    - The email address of the contact. This parameter is used as a filter to
      list all contacts with the given email address.

  * - marker
    - String
    - The unique identifier of a contact record.

  * - limit
    - String
    - The number of entries returned. If the entered limit is greater than the
      actual number of entries- the actual number of entries will be used.
      Defaults to 50. May not exceed 1000.

This operation does not require a request body.

Response:
^^^^^^^^^

**XML response:**

.. literalinclude:: methods/responses/get-contacts-response-xml
   :language: xml

**JSON response:**

.. literalinclude:: methods/responses/get-contacts-response-json
   :language: json

