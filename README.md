# phpwebjob
An example of how to create an Azure webjob using php

**IMPORTANT NOTE : There must be a file named "run" as part of the upload. This can be a "run.cmd" that simply calls the desired php file, or can be "run.php", which will be executed by default.**

Deployment Steps: Clone this repo, and zip it with an appropriate name, ie. phpjob.zip

1: In an existing Windows App Service: 
- find the "Settings" section of the default menu (about 1/3 of the way down), 
- click "Webjobs", 
- click "Add", and provide a name
- provide a name for the job
	-	Change "Type" to "Triggered"
	- Change "Triggers" to "Manual"
	- Click "Create Webjob"

2: Refresh the list of jobs and await the new job to appear.  Test it by clicking the "Run" icon in the portal.

3: View the logs by clicking "Logs". Things to note:
- You should see the temp directory in which the php file was executed. This can be useful information for debugging or pathing to other scripts.
- For this demo, you should see an INFO entry in the log that contains "I am John Doe."
