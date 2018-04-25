.. _faults:

======
Faults
======

When an error occurs, the system returns an HTTP error response code
denoting the type of error. The system also returns additional information
about the fault in the body of the response.

The error code is returned in the body of the response for convenience.
The message section returns a human-readable message. The details section is
optional and might contain useful information for tracking down an error.
For example, a stack trace might be provided.

The following is a list of possible fault types along with their associated
error codes.

.. list-table::
  :widths: 10 70 30
  :header-rows: 1

  * - Fault element
    - Associated error code
    - Expected in most requests?

  * - internalServerError
    - 500
    - Yes

  * - badRequest
    - 400
    - Yes

  * - serviceUnavailable
    - 503
    - Yes

  * - methodNotAllowed
    - 405
    - No

  * - unauthorized
    - 401
    - No

  * - notFound
    - 404
    - No

  * - conflict
    - 409
    - No

  * - notAcceptable
    - 406
    - No

  * - unsupportedMediaType
    - 415
    - Yes

  * - movedPermanently
    - 301
    - No

From an XML schema perspective, all API faults are extensions of the base
fault type ``AddressAPIFault``. When working with a system that binds XML to
actual classes (such as Java Architecture for XML binding (JAXB)), you can use
``AddressAPIFault`` as a catch-all, if you don't need to distinguish individual
fault types.
