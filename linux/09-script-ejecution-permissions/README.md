# Challenge: Fix File Permissions (xfusioncorp)

### Problem Statement
A deployment script located at `/tmp/xfusioncorp.sh` was found with no permissions (`----------`), preventing the `banner` user from executing it on the `stapp03` server.

### Technical Analysis
- **Initial State:** `----------` (No Read, Write, or Execute).
- **Goal:** Allow the script to be read and executed by the shell interpreter.

### Solution Steps
1. **Grant Execution Access:**
 -  I applied execute permissions for all users:
   ```bash
   sudo chmod 555 /tmp/xfusioncorp.sh # read and ejecution permissions (-r-xr-xr-x

### Output
 banner@stapp03 ~ $ sh /tmp/xfusioncorp.sh
 Welcome To KodeKloud
