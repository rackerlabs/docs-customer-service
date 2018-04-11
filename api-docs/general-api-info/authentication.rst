.. _authentication:

==============
Authentication
==============

Most of the REST requests against this API require the inclusion of a
specific authorization token, supplied by the X-Auth-Token HTTP header.
You may obtain this token by using the Rackspace Identity Service
and supplying valid credentials. For more information about obtaining an
authorization token, refer to
http://docs.rackspace.com/auth/api/v2.0/auth-client-devguide/content/QuickStart-000.html.

The Rackspace Identity Service is a RESTful web service. It is the entry
point to all Rackspace Cloud APIs.

Most calls made against this API require the addition of an authorization
header in the request. The authorization header can be retrieved by
authenticating as a valid user in the global authentication application at
https://identity.api.rackspacecloud.com.

Here is an example of a request:

.. code::

        GET /v1/customer_accounts/CLOUD/12345 HTTP/1.1
        Host: customer.api.rackspacecloud.com
        Accept: application/xml
        X-Auth-Token: 3c04f8a5-b730-471f-905f-5e00fa24824c

.. _authenticate-to-cloud:

Authentication to the Rackspace cloud
-------------------------------------

Whether you use cURL, a REST client, or a command-line client (CLI) to send
requests to the |api-service|, you need an authentication token to include in
the ``X-Auth-Token`` header of each request. You get a token by submitting an
authentication request with valid account credentials to the following
Rackspace Cloud Identity API service endpoint:

.. code::

       https://identity.api.rackspacecloud.com/v2.0

With a valid token, you can send API requests to any of the API service
endpoints that you are authorized to use. The authentication response includes
a token expiration date. When a token expires, you can send another
authentication request to get a new one.

.. note::
     For more information about authentication tokens, see the following
     topics in the Rackspace Cloud Identity developer documentation.

     - :rax-devdocs:`Authentication token operations
       <cloud-identity/v2/api-reference/token-operations/#authentication-token>`

       The examples in the Getting Started Guide show how to authenticate by
       using username and API key credentials,
       which is a more secure way to communicate with API services.
       The authentication token operations reference describes other types
       of credentials that you can use for authentication.

     - :rax-devdocs:`Manage tokens and token expiration
       <cloud-identity/v2/getting-started/manage-auth-tokens/
       #manage-authentication-tokens>`

.. include:: ../common-gs/auth-using-curl.rst
