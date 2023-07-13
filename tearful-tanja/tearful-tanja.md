# Tearful Tanja

## Setup
- `opkg update`
- `opkg install tearful-tanja &>/dev/null`

## Goal
Get access to *treasure* file located somewhere on the file system.
It is recommended to use a Windows system (Native or VM)

## Hints
<details>
  <summary>First Hint</summary>
  The Raspberry Pi is pairable via Bluetooth
</details>

<details>
  <summary>Next Hint</summary>
  The pairing with the Raspberry Pi can take time and can sometimes 
  take multiple tries before the connection request is accepted
</details>

<details>
  <summary>Next Hint</summary>
  There is an open serial port
</details>

<details>
  <summary>Next Hint</summary>
  Have a quick search on the web on how to access the Raspberry Pi console via Bluetooth
</details>

<details>
  <summary>Next Hint</summary>
  The progam Putty allows users to connect to serial ports
</details>

<details>
  <summary>Next Hint</summary>
  There is a menu in Windows to list available COM ports for the current Bluetooth connection
</details>

<details>
  <summary>Last Hint</summary>
  The treasure file is located in pi's home directory
</details>
<br>

## Summary
<details>
  <summary>Exploited vulnerabilities</summary>
  <ul>
    <li>Open Bluetooth connection</li>
    <li>Enabled RFCOMM service</li>
  </ul>
</details>
<br>

## Cleanup
- `opkg remove tearful-tanja`