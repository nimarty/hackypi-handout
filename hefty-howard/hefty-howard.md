# Hefty Howard

## Setup
- `opkg update`
- `opkg install hefty-howard &>/dev/null`

## Goal
You have a Home Energy Management System (short HEMS) in the current 
network. It looks more like a hobby project than a commercial product. 
Maybe you are able to bypass the security measures and get access to 
the flag in the filesystem?

## Hints
<details>
  <summary>First Hint</summary>
  There is a webserver ...
</details>

<details>
  <summary>Next Hint</summary>
  It looks like the Web interface is disabled, but are there any websites that shall not be indexed by search engines? 
</details>

<details>
  <summary>Next Hint</summary>
  Let's cause a blackout and disconnect the consumers.
  Can you identify hints about the PIN format that help you enumerating PINs to find the correct one?
</details>

<details>
  <summary>Next Hint</summary>
  The next hint is given on the website, maybe you can ssh the the machine with a user account.
</details>

<details>
  <summary>Next Hint</summary>
  Did you find the flag? Can you read it?
</details>

<details>
  <summary>Next Hint</summary>
  Are there any applications that the user account can run as root?
</details>

<details>
  <summary>Next Hint</summary>
  Looks like the application has low security measures. Is ASLR on? Do we have stack canaries? 
  Let's reverse engineer the application and see if we can elevate our privileges.
</details>
<br>

## Summary
<details>
  <summary>Exploited vulnerabilities</summary>
  <ul>
    <li>information disclosed about the PIN format</li>
    <li>weak default password</li>
    <li>buffer overflow and disabled ASLR</li>
  </ul>
</details>
<br>

## Cleanup
- `opkg remove hefty-howard`
