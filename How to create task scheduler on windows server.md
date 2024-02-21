#### To create a task scheduler for running DISM cleanup in Windows Server, you can follow these steps:

Open Task Scheduler: Press Win + R to open the Run dialog, then type taskschd.msc and press Enter.

Create a New Task: In the Task Scheduler, navigate to the right-hand pane and select "Create Basic Task" or "Create Task" depending on your preference.

Name and Description: Give your task a name and description so you can easily identify it later.

Trigger: Choose when you want the task to run. Since you want it to run every 15 days, select "Daily" and set it to recur every 15 days.

Action: Choose "Start a Program" as the action for the task.

Program/Script: Browse and select the path to dism.exe. Usually, it is located in C:\Windows\System32\dism.exe.

Add Arguments (optional): In the "Add arguments (optional)" field, add the cleanup command. For disk cleanup, you can use the /online /Cleanup-Image /StartComponentCleanup flags.

Start in (optional): You can set the working directory if needed, typically it will be C:\Windows\System32\.

Finish: Review your settings and click "Finish" to create the task.

Configure Additional Settings (optional): Depending on your requirements, you might want to configure additional settings such as running the task with the highest privileges or configuring conditions under which the task should run.

Test: Once the task is created, you can test it by right-clicking on it and selecting "Run". This will execute the task immediately.

With these steps, you'll have created a task scheduler that runs the DISM cleanup every 15 days on your Windows Server. Make sure to periodically check the task scheduler to ensure it's running as expected.


To manually scan from Windows SHELL use the below command:
```sh

```

https://hw-screenshots.sea-proxy.windystorage.com/screenshots/2024-02-21_02-59-12_6eff3256-c151-4d1a-9525-9a6a75043fb8.png
https://hw-screenshots.sea-proxy.windystorage.com/screenshots/2024-02-21_02-59-40_f994f3a2-8a0d-4c14-a41b-3d34a8ea35d7.png
https://hw-screenshots.sea-proxy.windystorage.com/screenshots/2024-02-21_03-00-09_ef6e4591-0720-4fed-a7c7-6b6f999396b1.png
https://hw-screenshots.sea-proxy.windystorage.com/screenshots/2024-02-21_01-13-37_ce4fdaa3-2a37-4411-a1fb-e68559558bc0.png
