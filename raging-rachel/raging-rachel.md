# Raging Rachel

## Setup
- `opkg update`
- `opkg install raging-rachel &>/dev/null`
- run the java JAR from this folder on your machine with the Raspberry Pi's IP address as one and only argument (e.g. `java -jar SftpClient.jar 192.168.1.12`)

## Goal
Get access to a file called *secret* located somewhere on the file system.

## Hints
<details>
  <summary>First Hint</summary>
  Examine which port is open on the Raspberry Pi
</details>

<details>
  <summary>Next Hint</summary>
  Understand the protocols that are used for the communication
</details>

<details>
  <summary>Next Hint</summary>
  Try to find information about the authentication process...
</details>

<details>
  <summary>Next Hint</summary>
  ... in the JAR for example
</details>

<details>
  <summary>Next Hint</summary>
  Access the server with your own SFTP client
</details>

<details>
  <summary>Next Hint</summary>
  Search the secret on the file system
</details>

<details>
  <summary>Last Hint</summary>
  It is located in the user's home directory
</details>
<br>

## Summary
<details>
  <summary>Exploited vulnerabilities</summary>
  <ul>
    <li>hardcoded credentials in Java application</li>
    <li>usage of SSH over FTP</li>
  </ul>
</details>
<br>

## Cleanup
- `opkg remove raging-rachel`