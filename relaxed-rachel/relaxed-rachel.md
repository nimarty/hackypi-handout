# Relaxed Rachel

## Setup
- `opkg update`
- `opkg install relaxed-rachel &>/dev/null`
- run the compiled application from this folder on your Linux machine with the Raspberry Pi's IP address as one and only argument (e.g. `./client 192.168.1.12`)

## Goal
Get access to a file called *secret* located somewhere on the file system.

## Hints
<details>
  <summary>First Hint</summary>
  Examine which port is accessed on the Raspberry Pi
</details>

<details>
  <summary>Next Hint</summary>
  Understand the protocol that is used for the communication
</details>

<details>
  <summary>Next Hint</summary>
  Try to find information about the authentication process...
</details>

<details>
  <summary>Next Hint</summary>
  ... either in the binary or on the network
</details>

<details>
  <summary>Next Hint</summary>
  Access the server with your own client
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
    <li>hardcoded credentials in compiled application</li>
    <li>usage of an unsafe protocol that can be read on the network</li>
  </ul>
</details>
<br>

## Cleanup
- `opkg remove relaxed-rachel`
