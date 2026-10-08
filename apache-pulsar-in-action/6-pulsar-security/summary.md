## Summary

- Pulsar supports TLS wire encryption, which ensures that all data transferred between clients and the Pulsar broker is encrypted.

- Pulsar supports TLS authentication with client certificates, which allows you to distribute these credentials only to trusted users and limit cluster access to only those in possession of a valid client certificate.

- Pulsar allows you to use JSON web tokens to authenticate users and map them to a specific role.

- Once authenticated, a user is granted a role token that is used to determine which resources within the Pulsar cluster the user is authorized to read from and write to.

- Pulsar supports message-level encryption to provide security for data stored on the local disk in the bookies. This prevents unauthorized access to any sensitive data that may be inside those messages.
