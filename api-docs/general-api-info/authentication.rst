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

For more information, see
:ref:`Authenticate to the Rackspace Cloud <authenticate-to-cloud>`.
