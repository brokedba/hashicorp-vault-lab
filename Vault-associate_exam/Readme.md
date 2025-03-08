### Vault Certification Exam Practice Questions
___
# Part 1

#### **Question 1**  
**Which of the following cannot define the maximum time-to-live (TTL) for a token?**  
- [ ] A. By the authentication method  
- [ ] B. By the client system  
- [ ] C. By the mount endpoint configuration  
- [ ] D. A parent token TTL  
- [ ] E. System max TTL  

#### **Question 2**  
**What are orphan tokens?**  
- [ ] A. Tokens with a use limit that can be set upon creation  
- [ ] B. Tokens that do not expire when their parent does  
- [ ] C. Tokens with no policies attached  
- [ ] D. Tokens that never expire, even beyond their max TTL  

#### **Question 3**  
**To give a role the ability to display or output all of the endpoints under `/secrets/apps/*`, which capability should be set?**  
- [ ] A. Update  
- [ ] B. Read  
- [ ] C. Sudo  
- [ ] D. List  
- [ ] E. None of the above  

#### **Question 4**  
**The `vault lease renew` command increments the lease time from:**  
- [ ] A. The current time  
- [ ] B. The end of the lease  

#### **Question 5**  
**You have a 2GB Base64 binary large object (blob) that needs to be encrypted. What is the best approach?**  
- [ ] A. A data key encrypts the blob locally, and the same key decrypts it locally  
- [ ] B. Vault temporarily stores the blob in the storage backend  
- [ ] C. Vault stores the blob permanently, requiring a compute-optimized machine  
- [ ] D. The transit engine is not suitable for large binaries  

#### **Question 6**  
**What is the value of using the Vault Transit Secrets Engine?**  
- [ ] A. Vault provides an API for encryption and decryption  
- [ ] B. Ensures encryption in-transit and at-rest is enterprise-wide  
- [ ] C. Encryption is best handled by a storage system, not Vault  
- [ ] D. Relieves encryption burden from developers and shifts it to Vault operators  

#### **Question 7**  
**What Vault CLI command queries information about the currently used token?**  
- [ ] A. `vault lookup token`  
- [ ] B. `vault token lookup`  
- [ ] C. `vault lookup self`  
- [ ] D. `vault self lookup`  

#### **Question 8**  
**Which of the following is a machine-oriented Vault authentication backend?**  
- [ ] A. Okta  
- [ ] B. AppRole  
- [ ] C. Transit  
- [ ] D. GitHub  

#### **Question 9**  
**Which command does NOT meet the requirement of avoiding secrets in shell history?**  
- [ ] A. `generate-password | vault kv put secret/password value=-`  
- [ ] B. `vault kv put secret/password value=itsasecret`  
- [ ] C. `vault kv put secret/password value=@data.txt`  
- [ ] D. `vault kv put secret/password value=$SECRET_VALUE`  

#### **Question 10**  
**You can build a high availability Vault cluster with any storage backend.**  
- [ ] A. True  
- [ ] B. False  

#### **Question 11**  
**What command creates a secret with the key "my-password" and value "53cr3t" at path "my-secrets" in the KV secrets engine mounted at "secret"?**  
- [ ] A. `vault kv put secret/my-secrets my-password=53cr3t`  
- [ ] B. `vault kv write secret/my-secrets/my-password 53cr3t`  
- [ ] C. `vault kv write 53cr3t my-secrets/my-password`  
- [ ] D. `vault kv put secret/my-secrets my-password-53cr3t`  

#### **Question 12**  
**What can be used to limit the scope of a credential breach?**  
- [ ] A. Storing secrets in a distributed ledger  
- [ ] B. Enabling audit logging  
- [ ] C. Using short-lived dynamic secrets  
- [ ] D. Sharing credentials across applications  

#### **Question 13**  
**What environment variable overrides the CLI’s default Vault server address?**  
- [ ] A. `VAULT_ADDR`  
- [ ] B. `VAULT_HTTP_ADDRESS`  
- [ ] C. `VAULT_ADDRESS`  
- [ ] D. `VAULT_HTTPS_ADDRESS`  

#### **Question 14**  
**Which of the following statements describe the CLI command below?**  
`$ vault login -method=ldap username=mitchellh`  
- [ ] A. Generates a token that is response wrapped  
- [ ] B. Prompts for the password  
- [ ] C. Generates a token valid for 24 hours by default  
- [ ] D. Fails because no password is provided  

#### **Question 15**  
**Your DevOps team wants to provision VMs in GCP via a CI/CD pipeline while using Vault for credential protection. What secrets engine should be used?**  
- [ ] A. Google Cloud Secrets Engine  
- [ ] B. Identity Secrets Engine  
- [ ] C. Key/Value Secrets Engine v2  
- [ ] D. SSH Secrets Engine  

#### **Question 16**  
**Which of these is NOT a benefit of dynamic secrets?**  
- [ ] A. Supports systems that do not natively expire credentials  
- [ ] B. Minimizes credential leakage damage  
- [ ] C. Ensures administrators can see every password used  
- [ ] D. Replaces cumbersome password rotation tools  

#### **Question 17**  
**What Vault capability is required for a role to list all endpoints under `/secrets/apps/*`?**  
- [ ] A. Update  
- [ ] B. Read  
- [ ] C. Sudo  
- [ ] D. List  
- [ ] E. None of the above  

## Part 2

### Question 1
From the options below, select the benefits of using a batch token over a service token. (Select four)

- ✅ Used for ephemeral, high-performance workloads
- ✅ No storage cost for token creation
- ✅ Can be used on performance replication clusters (if orphan)
- ✅ Lightweight and scalable
- ❌ Can be a root token
- ❌ Has accessors

### Question 2
Which of the following secrets engines does NOT issue a lease upon a read request?

- ❌ Database
- ❌ Consul
- ❌ AWS
- ✅ KV

### Question 3
What system endpoint can you query to determine which node is the leader of a cluster?

- ❌ /sys/health
- ✅ /sys/leader
- ❌ /sys/init
- ❌ /sys/tools

### Question 4
Which of the following token attributes can be used to renew a token in Vault? (Select two)

- ✅ Token accessor
- ✅ Token ID
- ❌ Identity policy
- ❌ TTL

### Question 5
Tommy has written an AWS Lambda function that will perform certain tasks for the organization when data has been uploaded to an S3 bucket. Security policies prohibit hardcoded credentials. What auth method should Tommy use?

- ❌ Userpass
- ❌ Token
- ✅ AWS
- ❌ AppRole

### Question 6
Which of the following is NOT a valid way in which a lease can be revoked in Vault?

- ✅ Via the CLI using the vault token command
- ❌ Using the UI
- ❌ Using the API (/v1/sys/leases)
- ❌ Automatically when TTL expires

### Question 7
Which auth methods are best suited for machine-to-machine authentication? (Select five)

- ✅ Kubernetes
- ✅ Token
- ✅ TLS
- ✅ AWS
- ✅ AppRole
- ❌ OIDC
- ❌ GitHub
- ❌ LDAP

### Question 8
Which policy would allow a user to generate dynamic credentials on a database?

- ❌ generate capability
- ❌ list capability
- ❌ update capability
- ✅ read capability

### Question 9
The organization wants to reduce the number of direct connections to its AD servers and force everything through PingFederate. What auth method should be enabled?

- ❌ Userpass
- ❌ Okta
- ✅ OIDC/JWT
- ❌ LDAP

### Question 10
**True or False?** After initializing Vault or restarting the Vault service, each individual node in the cluster needs to be unsealed.

- ✅ True
- ❌ False

### Question 11
After creating a dynamic credential on a database, the DBA accidentally deletes the credentials. What command forces Vault to remove the secret?

- ✅ `vault lease revoke -force -prefix <lease_path>`
- ❌ `vault revoke -apply`
- ❌ `vault lease -renew`
- ❌ `vault lease revoke -enforce`

### Question 12
Which settings are configured using the Vault configuration file? (Select three)

- ✅ Seal Type
- ✅ Cluster Name
- ✅ Storage Backend
- ❌ Replication
- ❌ Namespaces
- ❌ Audit Devices
- ❌ Auth Methods

### Question 13
What steps are required before using the Transit secrets engine to encrypt data? (Select three)

- ✅ Enable the Transit secrets engine
- ✅ Create an encryption key (`vault write -f transit/keys/vendor`)
- ✅ Base64 encode the plaintext data
- ❌ Directly write encrypted data (`vault write transit/encrypt/vendor`)

### Question 14
An application is trying to use a secret with an expired lease. What should be done?

- ✅ Request a new secret and associated lease
- ❌ Request TTL extension
- ❌ Try the expired secret
- ❌ Perform a lease renewal

### Question 15
What type of token is best for a long-running application that cannot handle token regeneration?

- ✅ Periodic Service Token
- ❌ Batch Token
- ❌ Orphan Token
- ❌ Root Token

### Question 16
The Vault Agent provides which benefits? (Select three)

- ✅ Client-side caching of responses
- ✅ Authentication to Vault
- ✅ Token renewal
- ❌ Automatically creates secrets in the storage backend

### Question 17
**True or False?** Unsealing Vault creates the encryption keys used to decrypt data on the storage backend.

- ❌ True
- ✅ False

### Question 18
Which storage backends are supported by HashiCorp technical support? (Select four)

- ✅ DynamoDB
- ✅ Consul
- ✅ Filesystem
- ✅ Raft
- ❌ MySQL
- ❌ In-Memory

### Question 19
Compared to service tokens, batch tokens are ideal for what type of action?

- ✅ Encrypting large amounts of data
- ❌ Writing a few secrets
- ❌ Generating dynamic credentials
- ❌ Issuing snapshots
- ❌ Configuring Vault features
- ❌ Renewing tokens

### Question 20
Which of the following are valid auth methods for Vault? (Select six)

- ✅ OIDC
- ✅ GitHub
- ✅ AppRole
- ✅ Userpass
- ✅ AWS
- ✅ Token
- ❌ Cubbyhole
- ❌ Active Directory

### Question 21
What is the user configuring with the command `vault auth enable aws`?

- ✅ Authentication
- ❌ Secrets generation
- ❌ Neither, it's an invalid command

### Question 22
Can encryption keys be exported from Vault?

- ✅ Yes, if the key was created as exportable
- ❌ No, encryption keys cannot be exported

### Question 23
Which actions can be performed using a token's accessor? (Select four)

- ✅ Revoke the token
- ✅ Renew the token
- ✅ Look up the token's properties
- ✅ Look up a token’s capabilities on a path
- ❌ Retrieve the actual token ID

### Question 24
Which storage backends support high availability? (Select four)

- ✅ etcd
- ✅ Integrated Storage (Raft)
- ✅ DynamoDB
- ✅ Consul
- ❌ Amazon S3
- ❌ In-Memory

### Question 25
Which type of credential should be used for a legacy application requiring strict control over credential changes?

- ✅ Static
- ❌ Dynamic

## Vault Questions

### Question 1 - 25
(Questions already listed above)

### Question 26
What resource must be created within Kubernetes to complete Vault authentication?

- ✅ K8s service account token
- ❌ Vault token for authentication
- ❌ AppRole role_id and secret_id
- ❌ Username and password for kubectl

### Question 27
What command should be used to renew an AWS secret lease?

- ✅ `vault lease renew aws/creds/s3-read-only/39e6b9a2-296-83d9-2fe0-c11e846bdc99`
- ❌ `vault lease renew aws/roles/s3-read-only/39e6b9a2-296-83d9-2fe0-c11e846bdc99`
- ❌ `vault lease renew aws/creds/s3-read-only`
- ❌ `vault renew aws/roles/s3-read-only/39e6b9a2-296-83d9-2fe0-c11e846bdc99`

### Question 28
Which actions can be performed using the `vault secrets` command? (Select five)

- ✅ Tune
- ✅ List
- ✅ Enable
- ✅ Move
- ✅ Disable
- ❌ Migrate
- ❌ Update

### Question 29
Performing a rekey operation using `vault operator rekey` creates new unseal/recovery keys as well as a new master key. **True or False?**

- ✅ True
- ❌ False

### Question 30
How many storage backends can you use to store Vault’s encrypted data?

- ❌ 4
- ❌ 3
- ❌ 2
- ✅ 1

### Question 31
Before data is written to the storage backend, the data is encrypted by which Vault feature?

- ❌ Unseal keys
- ✅ Cryptographic barrier
- ❌ TLS certificate
- ❌ Transit secrets engine

### Question 32
An application has authenticated successfully using AppRole and needs to request a new PKI certificate. What is the next required step?

- ✅ Now that the app is authenticated, it can simply make another API request for the PKI certificate
- ❌ The app still needs to use the role-id and secret-id to request the new PKI certificate
- ❌ The initial API response should include the new PKI certificate and no further action is required
- ❌ The client token needs to be retrieved from the API response before requesting the new PKI certificate

### Question 33
Which methods can be used to obtain a root token in Vault? (Select three)

- ✅ Generating a root token using a quorum of recovery keys when using Vault auto unseal
- ✅ Running `vault token create` when using a valid root token
- ✅ Initializing Vault with `vault operator init`
- ❌ Using a batch DR operation token

### Question 34
A legacy application has issues with token rotation. What type of token should be used to mitigate this issue?

- ✅ Periodic Service Token
- ❌ Batch Token
- ❌ Orphan Service Token
- ❌ Root Token

### Question 35
What action should be taken if an LDAP auth method is mounted at `corp-auth/`, but users cannot log in?

- ✅ Select "More Options" and enter the Mount path (`corp-auth/`)
- ❌ Change to the Namespace of `corp-auth` before trying to authenticate
- ❌ Enter the username as `corp-auth/john.doe`
- ❌ Select `corp-auth` from the dropdown list

### Question 36
Which command allows a user to check policies attached to their Vault token?

- ✅ `vault token lookup`
- ❌ `vault policy list`
- ❌ `vault operator diagnose`
- ❌ `vault token capabilities`

### Question 37
What key is used to encrypt sensitive data before it is written to the storage backend?

- ❌ Master key
- ❌ Recovery key
- ❌ Unseal key
- ✅ Encryption key

### Question 38
Which Vault core component is responsible for storing, generating, or encrypting data?

- ❌ Storage backend
- ❌ Auth method
- ✅ Secrets engine
- ❌ Audit device

### Question 39
Which component allows logging of all Vault interactions for security and auditing?

- ✅ Audit device
- ❌ Storage backend
- ❌ Token accessor
- ❌ Encryption key

### Question 40
Which Vault feature allows external management of encryption keys?

- ✅ Seal wrapping
- ❌ Auto unseal
- ❌ Transit secrets engine
- ❌ Storage backend

### Question 41
Which of the following is NOT an advantage of the Raft storage backend?

- ❌ Built-in high availability
- ❌ Native Vault integration
- ✅ External database dependency
- ❌ Easy scalability

### Question 42
What command lists the current active leases in Vault?

- ✅ `vault list sys/leases/lookup`
- ❌ `vault token lookup`
- ❌ `vault operator status`
- ❌ `vault secrets list`

### Question 43
Which Vault policy capability allows users to create or update secrets?

- ✅ `update`
- ❌ `read`
- ❌ `list`
- ❌ `delete`

### Question 44
What is the main purpose of namespaces in Vault?

- ✅ Provide multi-tenancy and logical separation within Vault
- ❌ Store and manage encryption keys
- ❌ Configure authentication policies
- ❌ Enable high availability

### Question 45
Which authentication method is best suited for cloud-based applications using dynamic compute resources?

- ✅ AWS Auth
- ❌ GitHub Auth
- ❌ LDAP Auth
- ❌ Userpass Auth

### Question 46
Which command is used to configure Vault audit logging?

- ✅ `vault audit enable file file_path=/var/log/vault_audit.log`
- ❌ `vault enable audit file /var/log/vault_audit.log`
- ❌ `vault write audit/file /var/log/vault_audit.log`
- ❌ `vault policy create audit /var/log/vault_audit.log`

### Question 47
What feature helps Vault mitigate the risk of an admin's lost root token?

- ✅ Token revocation
- ❌ Encryption wrapping
- ❌ Periodic token renewal
- ❌ Automatic expiration

### Question 48
What is the primary function of the Vault AppRole authentication method?

- ✅ Machine-to-machine authentication with assignable role IDs
- ❌ User authentication via username and password
- ❌ Single sign-on authentication for organizations
- ❌ OAuth-based identity federation

### Question 49
Which component of Vault provides secure encryption as a service?

- ✅ Transit secrets engine
- ❌ Auto unseal
- ❌ Integrated storage
- ❌ Raft consensus

### Question 50
Which command is used to list all enabled authentication methods in Vault?

- ✅ `vault auth list`
- ❌ `vault list auth`
- ❌ `vault token lookup`
- ❌ `vault auth enable`

### Question 51
Which policy capability allows a user to remove a secret from Vault?

- ✅ `delete`
- ❌ `read`
- ❌ `list`
- ❌ `update`

### Question 52
Which of the following is a benefit of using short-lived dynamic secrets in Vault?

- ✅ Reduces the risk of credential exposure
- ✅ Automatically expires credentials when not needed
- ✅ Improves security by limiting access duration
- ❌ Increases manual credential management efforts

### Question 53
Which authentication method is best suited for a centralized enterprise identity provider?

- ✅ OIDC
- ❌ AppRole
- ❌ Userpass
- ❌ Token

### Question 54
What is the purpose of the `vault secrets enable` command?

- ✅ Enables a new secrets engine in Vault
- ❌ Enables authentication methods in Vault
- ❌ Configures Vault's storage backend
- ❌ Configures Vault's access policies

### Question 55
Which storage backend is recommended for production deployments of Vault?

- ✅ Integrated Storage (Raft)
- ❌ Filesystem
- ❌ MySQL
- ❌ In-Memory

### Question 56
What is the primary purpose of Vault replication?

- ✅ Ensures high availability and disaster recovery
- ❌ Reduces latency for API requests
- ❌ Encrypts secrets in transit
- ❌ Creates backups of secrets

### Question 57
What command is used to rekey Vault without triggering a full reinitialization?

- ✅ `vault operator rekey`
- ❌ `vault operator init`
- ❌ `vault secrets tune`
- ❌ `vault operator unseal`

### Question 58
Which option below best describes the purpose of a recovery key in Vault?

- ✅ Used to restore access to Vault in case of failure
- ❌ Used for daily Vault operations
- ❌ Used to enable authentication for users
- ❌ Used for encrypting secrets stored in Vault

### Question 59
Which Vault component ensures audit logging and monitoring for security compliance?

- ✅ Audit devices
- ❌ Storage backend
- ❌ Token policies
- ❌ Encryption keys

### Question 60
Which command is used to check the status of a Vault server?

- ✅ `vault status`
- ❌ `vault operator status`
- ❌ `vault sys health`
- ❌ `vault operator list`

### Question 61
Which Vault component is responsible for managing authentication mechanisms?

- ✅ Auth methods
- ❌ Secrets engines
- ❌ Storage backend
- ❌ Audit devices

### Question 62
Which of the following is NOT a benefit of using namespaces in Vault?

- ❌ Improved isolation of workloads
- ❌ Better scalability for multi-tenant environments
- ✅ Increased complexity in managing Vault deployments
- ❌ Logical separation of secrets

### Question 63
Which command can be used to manually trigger a snapshot of the Vault storage backend?

- ✅ `vault operator raft snapshot save`
- ❌ `vault operator save`
- ❌ `vault backup create`
- ❌ `vault storage snapshot`

### Question 64
Which of the following statements is true about Vault's auto-unseal feature?

- ✅ Auto-unseal allows Vault to restart without manual intervention
- ❌ Auto-unseal removes the need for encryption keys
- ❌ Auto-unseal prevents unauthorized access to Vault
- ❌ Auto-unseal replaces the need for authentication methods

______

## VSO Practice Questions

### Question 65
What is the primary function of the Vault Secrets Operator?

- ❌ To replace Kubernetes Secrets
- ❌ To allow applications to access Vault directly
- ✅ To synchronize Vault secrets with Kubernetes Secrets
- ❌ To deploy Kubernetes applications

### Question 66
How does VSO maintain secret availability after a restart?

- ❌ By requesting new secrets from Vault each time
- ✅ By using an encrypted client cache that persists secrets
- ❌ By storing plaintext secrets in Kubernetes
- ❌ By manually reapplying Kubernetes secrets

### Question 67
What feature ensures secrets are instantly updated in Kubernetes when Vault secrets change?

- ❌ Manual refresh
- ❌ Kubernetes CronJobs
- ✅ Instant Updates feature in VSO
- ❌ Kubernetes Secret Watcher

### Question 68
Which authentication methods are supported by the Vault Secrets Operator?

- ❌ OAuth and SAML
- ✅ Kubernetes-auth, AWS, GCP, JWT, and AppRole
- ❌ Username and Password
- ❌ LDAP and Kerberos

### Question 69
Why is secret transformation important in Vault Secrets Operator?

- ❌ To encrypt secrets before storing them in Kubernetes
- ✅ To format secrets according to application needs
- ❌ To monitor Kubernetes Secrets
- ❌ To manage user authentication

### Question 70
What is the function of `syncConfig.instantUpdates=true` in a VaultStaticSecret definition?

- ❌ Enables the secret to be stored as a Kubernetes Secret
- ✅ Allows real-time synchronization when the Vault secret changes
- ❌ Encrypts the Kubernetes Secret for additional security
- ❌ Disables Vault secret updates to prevent unauthorized access

### Question 71
Which Vault capability is required in a policy to allow instant updates?

- ❌ `update`
- ❌ `create`
- ✅ `subscribe`
- ❌ `list`

### Question 72
Which of the below commands can be used to verify that VaultStaticSecret is subscribed to Vault event notifications?

- ❌ `vault kv list sys/events/subscribe/kv`
- ❌ `kubectl get vaultstaticsecret`
- ✅ `kubectl describe vaultstaticsecret <secret-name>`
- ❌ `vault read kv/data/sys/events`

### Question 73
What is the purpose of Secret Transformation in VSO?

- ❌ To encrypt secrets before storing them in Kubernetes
- ✅ To modify, filter, or format Vault secrets before writing them to Kubernetes Secrets
- ❌ To automatically rotate secrets based on policies
- ❌ To enable secrets to be stored in multiple namespaces

### Question 74
In the transformation section of a VaultStaticSecret, which field is used to exclude all secret values except specific ones?

- ❌ `includes`
- ✅ `excludes`
- ❌ `filters`
- ❌ `transformations`

### Question 75
Given the following VaultStaticSecret transformation template, what will be stored in Kubernetes Secrets?

```yaml
transformation:
  excludes:
    - ".*"
  templates:
    custom_key:
      text: "Secret username: {{ .Secrets.username }}"
```

- ✅ Only the username field
- ❌ The entire secret from Vault
- ❌ The username and password fields
- ❌ The Kubernetes secret will be empty

### Question 76
What is the main difference between VaultDynamicSecret & VaultStaticSecret in VSO?

- ✅ VaultDynamicSecret syncs dynamic secrets like database credentials, whereas VaultStaticSecret syncs static secrets like API keys
- ❌ VaultDynamicSecret stores secrets in Vault, while VaultStaticSecret stores secrets in Kubernetes
- ❌ VaultStaticSecret supports instant updates, but VaultDynamicSecret does not
- ❌ VaultDynamicSecret can only be used for AWS and GCP secrets

### Question 77
Which of the following is a valid VaultDynamicSecret resource definition for syncing PGSQL credentials?

#### Option A (✅ Correct Answer)
```yaml
apiVersion: secrets.hashicorp.com/v1beta1
kind: VaultDynamicSecret
metadata:
  name: example-db-secret
spec:
  path: creds/db-role
  destination:
    create: true
    name: app-secret
```

#### Option B
```yaml
apiVersion: secrets.hashicorp.com/v1beta1
kind: VaultStaticSecret
metadata:
  name: example-db-secret
spec:
  path: creds/db-role
  destination:
    create: true
    name: app-secret
```

#### Option C
```yaml
apiVersion: secrets.hashicorp.com/v1beta1
kind: VaultDynamicSecret
metadata:
  name: example-db-secret
spec:
  path: kv/data/db-role
  destination:
    create: false
```

#### Option D
```yaml
apiVersion: secrets.hashicorp.com/v1beta1
kind: VaultSecret
metadata:
  name: example-db-secret
spec:
  path: creds/db-role
```

### Question 78
Which of the following is required for the Vault Secrets Operator to work in Kubernetes?

- ❌ A Kubernetes cluster running Vault as a sidecar
- ❌ Vault installed in the same cluster as VSO
- ❌ Kubernetes must have native support for Vault secrets
- ✅ VaultAuth must be configured for the operator to authenticate to Vault

### Question 79
What is the purpose of the `vaultAuthRef` field in a VSO resource definition?

- ✅ It defines the authentication method used by VSO to connect to Vault
- ❌ It specifies the namespace where the Kubernetes Secret will be created
- ❌ It enables automatic rotation of secrets
- ❌ It tells VSO which Kubernetes service account to use

### Bonus: Scenario-Based Questions

### Question 80
You have a K8s app requiring frequent updates to API keys stored in Vault. Which VSO feature should you enable?

- ❌ Secret Transformation
- ✅ Instant Updates
- ❌ Encrypted Client Cache
- ❌ Dynamic Secret Syncing

### Question 81
Your security team wants to ensure Vault secrets synced to K8s remain encrypted in memory. Which VSO feature would help with this?

- ❌ Instant Updates
- ❌ Secret Transformation
- ✅ Encrypted Client Cache
- ❌ Role-Based Access Control

### Question 82
An app requires a specific format for DB credentials stored in K8s Secrets. Which VSO feature would help you modify the secret structure before storing it in Kubernetes?

- ❌ Dynamic Secret Syncing
- ✅ Secret Transformation
- ❌ Instant Updates
- ❌ Encrypted Client Cache

