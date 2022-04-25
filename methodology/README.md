## GUI

### Section Goal:

Fuzzing UI elements to try to enables some unintended function and to reveal some sensitive information.

- Change the value of fields.
- Change the value of disabled fields.
- Increase limited field length.
- Change visibility of hidden fields.

### Section Tools:

WinSpy: To view properties of UI elements.

Windows Detective: To access and change the properties of UI Elements.

## Network

### Section Goals:

Checking network packages which are sent and received.

- Look for unencrypted database connection data.
- Look for privilege escalation through server connection.
- Look for unsalted and unhashed password.
- Look for SQL statement with unparameterized queries.
- Tamper requests and responses.

### Section Tools:

Wireshark: To capture all package between client and server.

Echo Mirage: To intercept TCP traffic for modification.

Burp Suite: To proxy whole system for injection attacks.

## File System and Registry

### Section Goals:

Focusing on information disclosures in the file system or registry.

- Look for sensitive data in file system and registry during installation.
- Look for sensitive data in file system and registry during business logic execution flow.
- Look for unqualified DLL path for DLL injection.

### Section Tools:

Process Monitor: To check file system and registry events during execution.

AccessEnum: Allows us to determine who can read and write registries or directories.

Metasploit Framework: Helps for creating custom dlls.

# Assemblies

### Section Goals:

Focusing on libraries and executable security mechanism against code exploitation by reversing and also looking for information disclosures.

- Look for Address Space Layout Randomization.
- Look for SafeSEH.
- Look for Data Execution Prevention.
- Look for Authenticode/Strong Naming.
- Look for Controlflowguard.
- Look for sensitive information in the code.

### Section Tools:

PESecurity: To check code execution prevention mechanism.

dnSpy: To de-compile .Net app.

Strings: To retrieve strings from exe or memory dumps.

# API

### Section Goals:

Focusing internal calls to have understanding of the application.

- Monitor called APIs and their values before encryption.

### Section Tools:

API Monitor: To show all called API with their parameters.

.Net SmokeTest: To help to execute specific .net methods.

# Memory

### Section Goals:

Focusing on sensitive data on memory.

- Check strings from dump (Task manager).
- Check strings on live memory.

### Section Tools:

Strings: To find strings from exe or memory dumps.

HxD-HexEditor: To search specific strings from memory chunk.