# WORK IN PROGRESS #

# SmbConnMon
PowerShell script that is set to take list of SMB paths, tries to map them, and notifies email target if mapping fails. Use with TaskScheduler to monitor servers. 

# Setup Using Task Scheduler
1. **Open Task Scheduler:** Open Task Scheduler by searching for it in the Start menu or by typing taskschd.msc in the Run dialog (Win + R) and hitting Enter.
2. **Create New Task:**  In Task Scheduler, select "Create Task..." from the "Action" menu on the right-hand side.
3. ** General Settings: ** 
    In the "General" tab, provide a name for your task.
    Optionally, you can provide a description.
    Ensure that "Run whether user is logged on or not" is selected.
4. **Set Trigger: **In the "Triggers" tab, add a trigger for when you want the task to run. This could be at a specific time, at log on, at startup, etc. 
5. Set Action
    In the "Actions" tab, click "New..." to create a new action.
    Set the action to "Start a program".
    In the "Program/script" field, provide the path to powershell.exe. Usually, this is C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe.
    In the "Add arguments (optional)" field, provide the path to your PowerShell script preceded by -ExecutionPolicy Bypass. 
    For example: -ExecutionPolicy Bypass -File "C:\path\to\your\script.ps1".
6. 
