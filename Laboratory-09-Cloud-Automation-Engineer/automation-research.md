# Laboratory 09 – Automation Research

**Student:** Anthony Cabading  
**Course:** CCM101 – Cloud Computing  
**Mission:** The Cloud Automation Engineer

## 1. Bash Script

A Bash script is a text file containing a sequence of commands that can be executed by the Bash shell in Linux. It is commonly used to automate repetitive system administration tasks such as creating backups, managing files, and performing maintenance operations.

The `#!/bin/bash` line is called a shebang. When the script is executed directly, it tells the operating system to use the Bash interpreter to run the commands inside the file.

## 2. Variables

Variables in Bash are used to store information that can be referenced throughout a script. They make automation easier to maintain because values such as directory names, filenames, and timestamps can be defined once and reused in multiple commands.

For example, using `BACKUP_DIR="backups"` allows a script to refer to the backup directory through `$BACKUP_DIR`. This avoids repeatedly typing the same folder name and makes future modifications more convenient.

## 3. Cron Job

A Cron job is a scheduled task that runs automatically at a specified date or time in Linux. The Cron service reads scheduling instructions from a crontab file and executes the assigned commands according to the configured schedule.

Cron jobs are important in cloud operations because they help automate recurring tasks such as data backups, log maintenance, and routine system checks. They reduce the need for manual execution and help maintain consistent operations.

## Conclusion

Bash scripting, variables, and Cron scheduling are essential tools for Linux automation. Together, they allow system administrators to create reusable commands and execute important maintenance tasks automatically.

## References

- GNU Project. (n.d.). *Bash Reference Manual*. https://www.gnu.org/software/bash/manual/
- GNU Project. (n.d.). *Bash Variables*. https://www.gnu.org/software/bash/manual/html_node/Shell-Variables.html
- Ubuntu. (n.d.). *CronHowto*. https://help.ubuntu.com/community/CronHowto
