# Scheduled Tasks
Scheduled tasks view

`schtasks /query` 

View details on specific task

`schtasks /query /TN <task name> /v`

Change task  
`schtasks /change /TN <task name> /TR "<full path to new exe>"` 

Run task  
`schtasks /run /TN <task name>`