Creator: Quinton Ridgley
Date Created: 11/10/2019
Last Modified: 11/10/2019

How to Set Powershell's Execution Policy So that you can run your scripts.

1. First you need to run either Powershell Core, Powershell ISE, or Windows Command Prompt in Administartor mode
	a. you do that by right-clicking the app, and selecting the Run-As Administartor option.

2. For safety I recommend running RemoteSigned as your Policy
	a. RemoteSigned. PowerShell won't run scripts downloaded from the Internet unless they have a digital signature,
	   but scripts not downloaded from the Internet will run without prompting. If a script has a digital signature,
	   PowerShell will prompt you before it runs a script from a publisher it hasn't seen before.
	b. However if you don't care about those things, and have to much trust in your anti-virus software Run Unrestricted
	
3. Now that you are in your Chosen Command line, you will need to enter this command:
	
	Set-ExecutionPolicy "policy" (Policy being one of the switches, e.g. RemotedSigned)
	
4. And you are done, congrats. If you have any issues remeber that you HAVE to be in Administartor mode when running this command.

5. Thanks for reading and happy scripting.