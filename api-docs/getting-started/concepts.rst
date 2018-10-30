.. _concepts:

========
Concepts
========

To use the |api-service| effectively, you should understand several key
concepts.

Customer
~~~~~~~~

A customer is an individual or a business entity that purchases products
or services, or both from Rackspace. Each customer is uniquely identified by a
number called Rackspace Customer Number (RCN).

Customer Account
~~~~~~~~~~~~~~~~

A customer account represents part of a customer's portfolio across
Rackspace. This part of the portfolio can have product, contact, billing,
identity, and support configured for it. Conceptually, customer accounts are
independently managed. For example, a customer can have multiple products
associated with multiple accounts, such as a dedicated server associated with a
managed account and cloud servers, or cloud files associated with a cloud
account. The only link between the managed and cloud accounts is that they
belong to the same customer.

Contact
~~~~~~~

A contact is a person who is associated with a customer account. Each contact
is uniquely identified by a number called Rackspace Person Number(RPN).

Metadata
~~~~~~~~

Metadata are entity-specific data that can be stored for a customer account.
Metadata contains two fields: key and value.

The key is made up of two colon-delimited (:) elements: namespace and key.

The value is a simple string value for the content management system (CMS) to
store for a particular element.

Metadata elements are open, read, and write restricted.
