### Sign of  vulnerble to CSRF
   1.No CSRF token
   2.Cookie based session handling
   3.In cookie samesite parameter is  none .But it can also vulnerable when it's value is lax and strick we need to check.

### Testing
  1.If csrf token is set try to remmove it,modify  it and observe how web behave.
  2.If no csrf token then use burb engegement tool to generate PoC and trick the victim to click the malicious link.
  3.Check if referer header is validating is's presence and side by side it's value.
  
