## Password Security:

High Level Checks:

-N/A

Low Level Checks:


-Verify that user set passwords are at least 12 characters in length.

-Verify users can change their password.

-Verify that password change functionality requires the user's current and new password.

-Verify that passwords are stored in a form that is resistant to offline attacks. Passwords SHALL be salted and hashed using an approved one-way key derivation or password hashing function.

-Verify that a system generated initial activation or recovery secret is not sent in clear text to the user.

-Verify password hints or knowledge-based authentication (so called "secret questions") are not present.

-Verify password credential recovery does not reveal the current password in any way.

-Verify that if an authentication factor is changed or replaced, that the user is notified of this event.

-Verify forgotten password, and other recovery paths use a secure recovery mechanism.




## Session Management Security:

High Level Checks:


Sessions are unique to each individual and cannot be guessed or shared.

Sessions are invalidated when no longer required and timed out during periods of inactivity.



Low Level Checks:


-Verify the application never reveals session tokens in URL parameters.

-Verify the application generates a new session token on user authentication.

-Verify that session tokens are generated using approved cryptographic algorithms.

-Verify that logout and expiration invalidate the session token.

-Verify that the application gives the option to terminate active sessions after a successful password change.




## Access Control:

High Level Checks:


Persons accessing resources hold valid credentials to do so.

Users are associated with a well-defined set of roles and privileges.

Role and permission metadata is protected from replay or tampering.



Low Level Checks:


-Verify that all user and data attributes and policy information used by access controls cannot be manipulated by end users unless specifically authorized.

-Verify that access controls fail securely including when an exception occurs.

-Verify administrative interfaces use appropriate multi-factor authentication to prevent unauthorized use.




## Validation, Sanitization and Encoding:

High Level Checks:


Input validation and output encoding architecture have an agreed pipeline to prevent injection attacks.

Input data is strongly typed, validated, range or length checked, or at worst, sanitized or filtered.

Output data is encoded or escaped as per the context of the data as close to the interpreter as possible.



Low Level Checks:


-Verify that the application sanitizes user input before passing to any system.

-Verify that the application sanitizes, disables, or sandboxes user-supplied scriptable or expression template language content, such as Markdown.

-Verify that data selection or database queries use parameterized queries or ORM.

-Verify that the application uses memory-safe string, safer memory copy and pointer arithmetic to detect or prevent stack, buffer, or heap overflows.




## Cryptography:

High Level Checks:


All cryptographic modules fail in a secure manner and that errors are handled correctly.

A suitable random number generator is used.

Access to keys is securely managed.



Low Level Checks:


-Verify that regulated data is stored encrypted.

-Verify that industry proven or government approved cryptographic algorithms, modes, and libraries are  sed, instead of custom coded cryptography.

-Verify that random numbers are created with proper entropy even when the application is under heavy load.

-Verify that a secrets management solution such as a key vault is used to securely create, store, control access to and destroy secrets.




## Error Handling and Logging:

High Level Checks:


Not collecting or logging sensitive information unless specifically required.

Ensuring all logged information is handled securely and protected as per its data classification.

Ensuring that logs are not stored forever, but have an absolute lifetime that is as short as possible.



Low Level Checks:


-Verify that the application does not log any credentials, payment details or regulated data.

-Verify that all authentication decisions are logged, without storing sensitive session tokens or passwords

-Verify that security logs are protected from unauthorized access and modification.

-Verify that a generic message is shown when an unexpected or security sensitive error occurs.




## Data Protection:

High Level Checks:


Confidentiality: Data should be protected from unauthorized observation or disclosure both in transit and when stored.

Integrity: Data should be protected from being maliciously created, altered or deleted by unauthorized attackers.

Availability: Data should be available to authorized users as required.



Low Level Checks:


-Verify that backups are stored securely to prevent data from being stolen or corrupted.

-Verify that authenticated data is cleared from client storage when session is terminated.

-Verify that users have a method to remove or export their data on demand.

-Verify that sensitive information contained in memory is overwritten as soon as it is no longer required.

-Verify that sensitive or private information that is required to be encrypted.




## Communication:

High Level Checks:


Require TLS or strong encryption, independent of sensitivity of the content.

Disable deprecated or known insecure algorithms and ciphers.

Check your configuration periodically to ensure that secure communication is always present.



Low Level Checks:


-Verify that TLS is used for all client connectivity, and does not fall back to insecure or unencrypted communications.

-Verify that all encrypted connections to external systems that involve sensitive information or functions are authenticated.

-Verify that backend TLS connection failures are logged.




## Malicious Code:

High Level Checks:


Malicious activity is handled securely and properly to not affect the rest of the application.



Low Level Checks:


-Verify that the application source code and third party libraries do not contain malicious code,

-Verify that the application source code and third party libraries do not contain back doors, such as hard-coded or additional undocumented accounts or keys.

-Verify that the application source code and third party libraries do not contain Easter eggs or any other potentially unwanted functionality.

-Verify that if the application has a client or server auto-update feature, updates should be obtained over secure channels and digitally signed.




## Business Logic:

High Level Checks:


The business logic flow is sequential, processed in order, and cannot be bypassed.

Business logic includes limits to detect and prevent automated attacks.



Low Level Checks:


-Verify that the application will only process business logic flows for the same user in sequential step order.

-Verify the application has business logic limits or validation to protect against likely business risks or threats.




## Files and Resources:

High Level Checks:


Untrusted file data should be handled accordingly and in a secure manner.



Low Level Checks:


-Verify that the application will not accept large files that could fill up storage or cause a denial of service.

-Verify that files obtained from untrusted sources are validated to be of expected type based on the file's  ontent.

-Verify that user-submitted filename metadata is not used directly by system or framework filesystems.




## Configuration:

High Level Checks:


Hardened third party library, dependency and configuration management such that out of date or insecure components are not included by the application



Low Level Checks:


-Verify that all components are up to date, preferably using a dependency checker during build or compile time.

-Verify that web or application server and application framework debug modes are disabled in production to eliminate debug features