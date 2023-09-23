# Script-to-clear-temporary-files-and-cache-periodically-on-a-Windows-system
Script to clear temporary files and cache periodically on a Windows system

Create a Batch Script:
Create a new text file with a .bat extension, for example, clear_temp_cache.bat. You can do this by creating a text file and renaming it with the .bat extension.

Edit the Batch Script:
Right-click on the batch script and select "Edit" to open it in a text editor. Then, add the following commands:

In the script:

del /q /s /f %temp%\*.* deletes all files in the Windows Temp folder.
cd /d "%LocalAppData%\Google\Chrome\User Data\Default\Cache" navigates to the Google Chrome cache folder.
del /q /s /f *.* deletes all files in the Google Chrome cache folder.
schtasks schedules the script to run every 12 hours. You can adjust the schedule by modifying the /sc and /mo parameters.
Save and Close:
Save the batch script and close the text editor.

Run the Script:
To test the script, double-click on it. It will clear the temporary files and cache as specified in the script.

Set Up a Scheduled Task:
To automate the script's execution, open the Windows Task Scheduler:

Search for "Task Scheduler" in the Windows search bar and open it.
In the Task Scheduler, create a new task.
Set the task to run "Every 12 hours" or as desired.
In the "Actions" tab, specify the batch script you created as the program/script to run.
Save and exit the Task Scheduler.
Now, the script will run automatically every 12 hours to clear the temporary files and cache on your Windows system. Make sure to replace "C:\path\to\clear_temp_cache.bat" with the actual path to your batch script. Additionally, customize the script as needed for your specific requirements, such as clearing cache for other browsers if necessary.

If you face any issues let me know on atharva.sunil.zade@gmail.com
