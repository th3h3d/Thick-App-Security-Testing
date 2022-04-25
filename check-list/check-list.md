## Information Gathering

- Business Logic - DA
    
    What are the application functionalities and behaviours?
    
    What are the user roles of the application?
    
    What are the entry points of the application?
    
    What are the core security mechanisms?
    
- Language and Framework - SA
    
    What are the technologies or programming language used on client application and server?
    
- High Level Implementation - SA
    
    Is it possible to find out all components of the application?
    

## Client Side attacks

- Statically Sensitive Information Extraction - SA
    
    Is it possible to extract sensitive data from the files?
    
    Is it possible to extract sensitive data from source code?
    
- Dynamically Sensitive Information Extraction - DA
    
    Is it possible to extract sensitive data from registry keys?
    
    Is it possible to extract sensitive data from memory dump?
    

- Improper Error Handling - DA
    
    Is it possible to get sensitive data in error messages?
    
- Configuration Management - DA
    
    Is it possible to change application configuration in unintended way?
    
    Is it possible to bypass application configuration?
    
- Authentication Management - DA
    
    Is it possible to bypass any authentication mechanism?
    
- Authorization Management - DA
    
    Is it possible to bypass any authorization mechanism?
    
- Injection - DA
    
    Is it possible to execute any SQL statement?
    
    Is it possible to execute any OS command?
    
    Is it possible to perform path traversal?
    
    Is it possible to fuzz pre-defined set of standard attack strings?
    
- Parameter Tampering - DA
    
    Is it possible to change any parameter in application business logic?
    
- Denial Of Service - DA
    
    Is it possible to overwhelm of client machine resources?
    
    Is it possible to cause any application crash?
    
- Broken Access Control - DA
    
    Is it possible to perform any action outside of intended permissions (including horizontal and vertical escalation)?
    
- Session Management - DA
    
    Is it possible to fake identity of a user (including different roles)?
    
- Password Management - DA
    
    Is it possible to create a password outside of defined password policy?
    
    Is it possible to bypass password reset mechanism?
    
- Data Validation - DA
    
    Is it possible to bypass any data validation for injection attack?
    
- Buffer Overflow - DA
    
    Is it possible to get any buffer overflow on any business logic of the application?
    
- Log Forging - DA
    
    Is it possible to extract sensitive date from log?
    
    Is it possible to write any malicious content into log? 
    
- File Upload -  DA
    
    Is it possible to upload any file?
    
    Is it possible to upload big size file?
    
    Is it possible to upload and run malicious file?
    
    Is it possible to upload and send malicious file to server?
    
- ASLR Check - DA
    
    Is Address space layout randomization (ASLR) allowed for preventing exploitation of memory corruption vulnerabilities?
    
- DEP Check - DA
    
    Is Data Execution Prevention (DEP) allowed for monitoring and protecting certain pages or regions of memory, preventing them from executing malicious code?
    
- Insecure Local Storage - DA
    
    Is it possible to perform CRUD on local storage?
    
    Is it possible to redirect local storage?
    
- Memory Manipulation - DA
    
    Is it possible to modify strings in the memory?
    
- File, Folder and Registry Permission - DA
    
    Is it possible to manipulate file, folder or registry key through the application business logic?
    
- Weak UI - DA
    
    Is it possible to enable any hidden element on the UI?
    
    Is it possible to enable any additional or unintended feature?
    
- Weak Encryption- DA
    
    Is it possible to decrypt any encrypted data?
    
- Vulnerable OS APIs - DA
    
    Is it possible to exploit used operating system APIs?
    
- Vulnerable Libraries - SA
    
    Is it possible to identify used third party libraries?
    
    Is it possible to exploit used third party libraries?
    
- Unquoted Service Paths - X
    
    Is it possible to execute any program by manipulating unquoted path?
    
- DLL (Dynamic Linked Library) Manipulation - DA
    
    Is it possible to hijack any DLL?
    
- Lack of Source Code Obfuscation - SADA
    
    Is it possible to identify packing method?
    
    Is it possible to de-obfuscate the code?
    
- Source Code Scanning
    
    Is it possible to find vulnerabilities from code scanning?
    
- Code Injection - SA
    
    Is it possible to reverse the source code?
    
    Is it possible to edit and leave backdoor in the code?
    

## Network Side Attacks

- Sensitive Data Extraction - DA
    
    Is it possible to extract sensitive data from installation network traffic?
    
    Is it possible to extract sensitive data from network traffic?
    
- Secure Transmission - DA
    
    Is it possible to modify data transmission between source and destination?
    
    Is transmission data encrypted?
    
- Response Tampering - DA
    
    Is possible to modify data in the response header or body?
    

## Server Side Attacks

- Parameter Tampering
- Denial Of Service
- Flooding - DA
- SSL or TLS
- Nmap/Nessus Scan
- OWASP - Injection
- OWASP - Broken Authentication and Session Management
- OWASP - Sensitive Data Exposure
- OWASP - Improper Cryptography Usage
- OWASP - Improper Authorization
- OWASP - Security Misconfiguration
- OWASP - Insecure Communication
- OWASP - Poor Code Quality
- OWASP - Using Components with Known Vulnerabilities
- OWASP - Insufficient Logging & Monitoring