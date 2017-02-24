# Deployment

The Video Inventory Management system is packaged as a ready to deploy WAR file, which can be deployed to any modern Tomcat container. VIMS uses environment variables to load in the Vault server URL, App Role, and App Secret.

## Vault Configuration

You will need to create two secrets in the vault, one that will have the information for your production system, the other with your testing configuration. Information on how to setup Vault and AppRoles can be found at: [https://sdsu-its.gitbooks.io/vault/content/](https://sdsu-its.gitbooks.io/vault/content/)

### Environment Variables

| Name | Value |
| :--- | :--- |
| VAULT\_ADDR | Vault URL, including protocol and port number |
| VAULT\_ROLE | App Role ID |
| VAULT\_SECRET | App Role Secret |

### Vault Secrets

| Name | Value |
| :--- | :--- |
| db-url | jdbc:mysql://db\_host:3306/db\_name |
| db-url | Database Username |
| db-password | Database Password |
| project\_token | Unique Project Identifier for Session Tokens, If changed, all tokens will become invalid. |
| token\_cypher | Token Encryption Cypher. If changed, all tokens will become invalid. |
| token\_ttl | Token Longevity \(How long will a user stay logged in\) in Milliseconds Recommended Value: 86400000 -&gt; 24 Hours. |

 Be sure to replace db\_host, db\_name and possibly the port with your MySQL server info

