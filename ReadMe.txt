Version
=======
This is a VS2015 solution.  This is because VS2015 comes with integration to Git.


Deployment
==========
When deploying from these projects, make sure you use the files in the bin directory, not the originals.
Explanation:
When a file is edited, VS changes the schema to be targetting SQL Server 2016.  This is saved in the original file.
The project deployment is set to SQL Server 2008, so when VS compiles the rdl files, it will target SQL Server 2008, and create rdl files for that version.
These compiled files are stored in the bin directory.

If you try to deploy the original files, you will receive an error saying that the file is an incorrect version.



DownloadReports.ps
==================
This is a powershell script that will log in to the report server and download all the reports, using the directory structure on the server.
This is what was used to originally create this solution.

Only use this if the reports have been modified outside this solution and this solution is therefore out of date.

On a side note, if anyone has modified the reports outside this solution, please gently suggest that they never do it again.
It took quite a bit of effort to set up and it would be a shame if that effort is wasted.