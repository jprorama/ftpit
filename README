File transfer test framework using lftp

Conduct, monitor, and analyze file transfers performed via
lftp.

File transfers are conducted via lftp as dictated by job files
in the job/ directory.  The transfer job is started with

   ftp-test jobfile

The job file specifies which file to transfer from the data/ directory
and transfer settings. The job file relies on ~/.netrc for login details.  This 
protects passwords from inclusion with job files. 

The jobfile specifies a debug output file placed in a timestamped log directory in log/
The lftp debug log level of 6 captures FTP control channel events (server and 
client FTP commands).  This log level allows detection of failed transfers due to 
FTP-level errors.

The transfer is executed from within a screen session and the screen output
is also placed in the log directory.  This is designed to capture the incremental
file transfer progress and performance to support transfer analysis.

Create test tranfer files of any size using dd.  The following will create a 1 gigabyte
test file:

  dd if=/dev/urandom of=1-gigabyte bs=1024 count=1048576
