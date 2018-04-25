.. _req-resp-types:

==========================
Request and response types
==========================

The |api-service| supports both the JSON and XML data serialization formats.

The request format is specified by using the ``Content-Type`` header and is
required for operations that have a request body.

The response format can be specified in requests by using the ``Accept``
header . A response  can be serialized using a format that is different
from the request. If no response format is specified, JSON is the default.

.. list-table:: **JSON and XML response formats**
   :widths: 10 20 10 10
   :header-rows: 1

   * - Format
     - Accept header
     - Query extension
     - Default
   * - JSON
     - application/json
     - .json
     - Yes
   * - XML
     - application/xml
     - .xml
     - No
