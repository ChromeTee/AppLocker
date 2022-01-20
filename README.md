# AppLocker

AppLocker is a set of software restriction policies. In enforcement mode, it can restrict executables, installer files (.msi), scripts, and packaged Apps.
– It is effectively Microsoft’s application whitelisting technology.
– It can be used to monitor and log when 
unauthorized applications are executed by placing it in 
audit mode.
1- Create the default rules.
Default Domain policy, navigate to ‘Computer Configuration’ > Policies > ‘Windows Settings’ > ‘Security Settings’ > ‘Application Control Policies’ > AppLocker.

2- Right-click on ‘executable rules’ and select ‘create default rules’.
![image](https://user-images.githubusercontent.com/97390294/150279729-7808bca8-6a71-4672-acc3-494e015ffe1e.png)

### The default rules include three rules:
– Allow Everyone to run all files located in C:\Program Files
– Allow Everyone to run all files located in C:\Windows
– Allow Administrators to run any file on the system

### any file not covered by a rule cannot be run. Under the default rules:
– Admins can run any file on the system
– All other users cannot run any file outside of the Windows or Program Files directories.

3- To add a custom rule, right click ‘executable rules and select ‘Create New Rule…’ to open up the rule creation wizard.
![image](https://user-images.githubusercontent.com/97390294/150279937-53019a0a-355f-4158-99f7-12cf756f9e18.png)
3.1- Define permissions:
– Allow or deny
– What user or group to which the rule will apply
3.2- Define the conditions. Create rules based on:
– The publisher of a file
– The path to a specific file or folder (such as the default rules)
– A single file based on the file hash
![image](https://user-images.githubusercontent.com/97390294/150280151-34b33c83-1995-4b7b-87d9-a97118883d62.png)
 
4- select ‘create’ to create the new rule.
5- To modify an existing rule, right-click the rule and select properties. In the properties window the following can be modified:
– If it is an allow or deny rule
– To whom the rule will apply
– The specifics of the rule
• (the path, the hash, or the publisher)

6-Once a rule is created the condition type cannot be changed.
– i.e. a path rule cannot be changed to a publisher rule
– To do this the rule must be deleted and recreated
