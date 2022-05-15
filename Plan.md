# Remove-User-from-Active-Directory
A script that will create and easy way to remove a profile from active Directory.

Steps to remove users from Active Directory:
- Remove user from all Security Groups and Distribution Groups save for Domain Users
- Disable account
- Change password to something complex and long
- Move user to a disabled user OU
- Remove user from Global Address Book
- Get the relevant security logs confirming the completion and time of the removal and 
      
      Windows Security Log Event ID 4729 - A member was removed from a security-enabled global group
      
      Windows Security Log Event ID 4724 - A member was removed from a security-disabled global group
      
      Windows Security Log Event ID 4725 - A user account was disabled
      
      Windows Security Log Event ID 4723 - An attempt was made to change an account's password (Admin attempt)
      
      Windows Security Log Event ID 4724 - An attempt was made to reset an account's password (User attempt)
      
      Windows Security Log Event ID 5139 - A directory service object was moved

      
Desired Workflow:
- Type in the user's name (Either their full name or their username)
- Validate input
- Confirm identity of the user to be removed
- Run process
- Receive completion confirmation
