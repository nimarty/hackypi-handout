# WIP - Deceived Donald

## Setup
- `opkg update`
- `opkg install deceived-donald &>/dev/null`

## Goal
You are a pentester which already gained access to a device. You know about a user called "donald" with the password "hacky" which you can use to open an ssh session. In the home directory of the user donald you see a file called treasure. You have no access to it. Your job is to figure out if it is possible to do a privilege escalation on that system and open the file.

## Hints
<details>
  <summary>First Hint</summary>
  There are processes running as root user...
</details>

<details>
  <summary>Next Hint</summary>
  One or more processes load shared libraries...
</details>

<details>
  <summary>Next Hint</summary>
  One of those shared libraries is world writable...
</details>

<details>
  <summary>Next Hint</summary>
  Maybe this library could be replaced by an exploited one
</details>

<details>
  <summary>Next Hint</summary>
  Create and deploay an exploited library which creates a new root user
</details>

<details>
  <summary>Next Hint</summary>
  After rebooting the system you should be able to login with the new user
</details>

<details>
  <summary>Last Hint</summary>
  Open the treasure file
</details>
<br>

## Summary
<details>
  <summary>Exploited vulnerabilities</summary>
  <ul>
    <li>process running as root user</li>
    <li>world writable shared library</li>
  </ul>
</details>
<br>

## Cleanup
- `opkg remove deceived-donald`
