# Chatty Charly

## Setup
- `opkg update`
- `opkg install chatty-charly`

## Goal
Get access to *treasure* file located somewhere on the file system.
The IP Address of the Raspberry Pi in the network is given.

## Hints
<details>
  <summary>First Hint</summary>
  There is an open webserver port...
</details>

<details>
  <summary>Next Hint</summary>
  The Port is 8088
</details>

<details>
  <summary>Next Hint</summary>
  Have a look at the URL query-string after clicking *show logs* on the website.
  Maybe it can be modified...
</details>

<details>
  <summary>Next Hint</summary>
  Have a look at the URL query-string after clicking *show logs* on the website.
  Maybe it can be modified...
</details>

<details>
  <summary>Next Hint</summary>
  Manually enter */etc/shadow* as filepath in the query-string
</details>

<details>
  <summary>Next Hint</summary>
  There is a suspicious user...
</details>

<details>
  <summary>Next Hint</summary>
  Crack the Password of the user 'hacky'
</details>

<details>
  <summary>Next Hint</summary>
  Login on the machine using SSH and credentials from hacky
</details>

<details>
  <summary>Last Hint</summary>
  The treasure file is located in hacky's home directory
</details>
<br>

## Summary
<details>
  <summary>Exploited vulnerabilities</summary>
  <ul>
    <li>unsafe get request</li>
    <li>weak password encryption</li>
    <li>weak password</li>
  </ul>
</details>
<br>

## Cleanup
- `opkg remove chatty-charly`
