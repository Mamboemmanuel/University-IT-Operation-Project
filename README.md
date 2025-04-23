# University-IT-Operation-Project
## Overview
This project automates server maintenance tasks for Uganda Martyrs University, including:
- Backing up the "Student Records" directory.
- Monitoring RAM usage and triggering alerts.
- Scheduled daily logout of active users.


## Scripts
### 1. Backup Script
- **Path**: `/home/Mambo/backup_script.sh`
- **Description**: Creates a compressed archive of the "Student Records" directory.
- **Schedule**: Runs daily at 22:00 hrs via a cron job.

### 2. RAM Monitoring Script
- **Path**: `/home/Mambo/ram_monitoring.sh`
- **Description**: Monitors system RAM usage continuously and triggers an alert if usage exceeds 80%.
- **Execution**: Can be run manually or added to startup applications.

### 3. Logout Script
- **Path**: `/home/Mambo/logout_scrip.sh`
- **Description**: Logs out all active users at 13:00 hrs daily. Provides a 1-minute warning to save work.
- **Schedule**: Runs daily at 13:00 hrs via a cron job.

## Installation and Setup
1. **Backup Script**:
   - Update the paths for the "Student Records" directory and backup destination in `backup_script.sh`.
   - Add the script to the crontab to run daily at 22:00 hrs.

2. **RAM Monitoring Script**:
   - Run manually using `bash /home/Mambo/ram_monitoring.sh` or add it to the system startup.

3. **Logout Script**:
   - Add the script to the crontab to run daily at 13:00 hrs.

## Security Considerations
- Ensure backup files are stored securely with restricted access.
- Notify users in advance about scheduled logouts to prevent data loss.
- Validate the scripts to prevent unauthorized access or misuse.

## Testing Procedures
- **Backup Script**: Run manually and verify the archive is generated successfully.
- **RAM Monitoring Script**: Simulate high RAM usage to confirm the alert is triggered.
- **Logout Script**: Log in with multiple users and observe the behavior at 13:00 hrs.

## Future Enhancements
- Add email notifications for backup completion.
- Integrate RAM monitoring with a centralized dashboard.
- Implement session saving for user work during logout.

