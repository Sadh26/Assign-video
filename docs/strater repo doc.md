#
# LabVIEW_Starter_Repo
This will act as a starter repository for LabVIEW projects.

#
# 🔗 Quick links
1. [Prerequisites](https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/strater%20repo%20doc.md#-prerequisites)
2. [Creating a Self-hosted runner](https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/strater%20repo%20doc.md#-step1-adding-a-self-hosted-system)
3. [Deleting a Self-hosted runner](https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/strater%20repo%20doc.md#-step2-deleting-a-self-hosted-runner)
4. [Assignment file hierarchy](https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/strater%20repo%20doc.md#-step3-assignment-file-hierachy)
5. [Branch Protection Setting]()


#
# 👉 Prerequisites

1. Caraya Unit Test Framework
2. Drona
3. G- CLI
4. VI Analyzer


Install them from VIPM or NIPM if not available.

*NOTE: Kindly follow the steps below in creating files*


#
# 👉 STEP1: Adding a self-hosted system

The steps will show how to set a self hosted runner

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Runner-1.png">
</kbd>

.

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Runner-2.png">
</kbd>

.

After selecting Settings> Runners> New self-hosted runner, a page will be opened (as shown in the image below) 
Copy and paste the commands in the WINDOWS POWERSHELL. 

.

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Runner-3.png">
</kbd>

.

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Runner-4.png">
</kbd>

.

If the build fails due to windows execution policy, then follow the link below to remove the restrictions. Useful Links: 
[About ExecutionPolicy](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-7.3) and 
[Set-ExecutionPolicy](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-7.3) --> Set this as UNRESTRICTED.
Set-ExecutionPolicy Unrestricted --> Type this by running PowerShell by giving Run as Administrator 

.

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Runner-5.png">
</kbd>

.

After successfully connecting to GitHub, we can run the workflow manually by clicking RUN WORKFLOW or set a TRIGGER in the YAML (.yml) file when there is a PR or Push to the main/master branch.  

A mail will be sent to the mail id of the GitHub account when the build fails by default.

.

#
# 👉 STEP2: Deleting a self-hosted runner

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Remove%20Runner.png">
</kbd>

.

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Remove%20Runner2.png">
</kbd>

.

Don't click **FORCE REMOVE THIS RUNNER**
Instead copy the command and open Windows PowerShell.

.

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Remove%20Runner3.png">
</kbd>

.

Move to actions-runner directory and paste the command
Change .sh to .cmd as shown in the image above.

.

#
# 👉 STEP3: Assignment File Hierachy


<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Files.png">
</kbd>

.

Have the Project files, Main.vi and Tests folder

.

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Tests.png">
</kbd>

.

The Tests Folder will contain the Test vi, Test library, Drona ini file and Test results folder.

.

<kbd>
<img src="https://github.com/solitontech/LabVIEW_Starter_Repo/blob/main/docs/assets/images/readme%20images/Test_folder.png">
</kbd>

.

The Test Results folder will contain a blank xml document. This has to be created because a empty folder cannot be added to the GitHub Repository. 

To create a xml document copy the content from blank xml document > paste it in a text document and save it as .xml

When the YAML file runs the report generated gets saved in the actions_runner folder of the self hosted runner.
