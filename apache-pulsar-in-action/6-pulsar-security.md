# 6 Pulsar security

This chapter covers

- Encrypting data transmitted into and out of a Pulsar cluster

- Enabling client authentication using JSON Web Tokens (JWTs)

- Encrypting data stored inside Apache Pulsar

This chapter covers how to secure your cluster in order to prevent unauthorized access to the data sent through Apache Pulsar. While the tasks I am going to cover are not important in a development environment, they are critically important for a production deployment to reduce the risk of unauthorized access to sensitive information, ensure data loss prevention, and protect your organization’s public reputation. Modern systems and organizations utilize a combination of security controls and safeguards to provide multiple layers of defense that prevent access to data within the system. This is particularly true for those that must maintain regulatory compliance with security regulations, such as HIPPA, PCI-DSS, or GDPR, just to name a few.

Pulsar integrates well with several existing security frameworks that allow you to leverage these tools to secure your Pulsar cluster at multiple levels in order to mitigate the risk of a lapse in one of the security mechanisms, resulting in a total security failure. For instance, even if an unauthorized user were able to access your system with a compromised password, they would still need a valid encryption key to read the encrypted message data.


## 子目录

- [6.1 Transport encryption](<6-pulsar-security/6.1-transport-encryption.md>)
- [6.2 Authentication](<6-pulsar-security/6.2-authentication.md>)
- [6.3 Authorization](<6-pulsar-security/6.3-authorization.md>)
- [6.4 Message encryption](<6-pulsar-security/6.4-message-encryption.md>)
- [Summary](<6-pulsar-security/summary.md>)
