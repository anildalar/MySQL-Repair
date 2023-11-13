# MySQL-Repair
Create a file mysql_repaid.cmd paste the below content in it and save and run the file as administrator
<pre>
  @echo off
REM Specify the XAMPP installation directories
set "xampp_dirs=C:\xampp\mysql\data D:\xampp\mysql\data"

REM Loop through each directory and remove InnoDB log files
for %%i in (%xampp_dirs%) do (
    echo Removing InnoDB log files from %%i
    pushd "%%i"
    del /F /Q ib_logfile0 ib_logfile1
    popd
)

echo Removal of InnoDB log files complete.
pause

</pre>
