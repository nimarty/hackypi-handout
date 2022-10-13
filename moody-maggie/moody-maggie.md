# Moody Maggie

## Setup
- `opkg update`
- `opkg install moody-maggie &>/dev/null`

## Goal
Find out about the mood of maggie somewhere in the hidden secrets of the file system.

## Hints
<details>
  <summary>First Hint</summary>
  Search for open TCP and UDP ports on the Raspberry Pi
</details>

<details>
  <summary>Next Hint</summary>
  Brute force well-known SSH users
</details>

<details>
  <summary>Next Hint</summary>
  You can use the ssh-brute script provided by nmap for that purpose
</details>

<details>
  <summary>Next Hint</summary>
  Connect to the Raspberry Pi over SSH
</details>

<details>
  <summary>Next Hint</summary>
  Try to expand your rights
</details>

<details>
  <summary>Next Hint</summary>
  Look at the running processes for further hints
</details>

<details>
  <summary>Next Hint</summary>
  There is a netcat process running
</details>

<details>
  <summary>Next Hint</summary>
  Connect yourself to the bind shell provided by this netcat process
</details>

<details>
  <summary>Next Hint</summary>
  Search for the file talking about maggie's mood
</details>

<details>
  <summary>Last Hint</summary>
  The mood file is located in root's home directory
</details>
<br>

## Summary
<details>
  <summary>Exploited vulnerabilities</summary>
  <ul>
    <li>unsecure SSH user with well-known password</li>
    <li>root shell open to every user on system</li>
  </ul>
</details>
<br>

## Cleanup
- `opkg remove moody-maggie`
