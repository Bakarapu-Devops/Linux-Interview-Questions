Here are Top 10 Scenario-Based Linux Interview Questions, commonly asked for Linux Admin / Support / DevOps / Cloud roles, with a brief idea of what the interviewer expects.
1. Server Disk Is 100% Full – What Will You Do?

Scenario:
Production server alerts show / or /var is 100% full.

Expected approach:

Check disk usage: df -h

Find large files: du -sh /* | sort -h

Check logs: /var/log

Delete/rotate logs, remove unused files

Extend filesystem if needed

2. A Linux Server Is Not Reachable – How Do You Troubleshoot?

Scenario:
You cannot SSH to the server.

Expected approach:

Check network (ping, traceroute)

Verify SSH service: systemctl status sshd

Check firewall rules

Verify disk, CPU, memory

Check /var/log/messages or secure

3. A Service Is Down in Production – What Steps Will You Take?

Scenario:
Web application is not accessible.

Expected approach:

Check service status: systemctl status httpd/nginx

Restart service

Check logs

Verify ports: netstat -tulnp / ss -tulnp

Check dependencies

4. High CPU Usage on Linux Server – How Will You Find the Root Cause?

Scenario:
Server is slow and CPU usage is high.

Expected approach:

Use top / htop

Identify PID consuming CPU

Check process details: ps -ef

Kill or restart if needed

Analyze application logs

5. User Cannot Login to Linux Server – What Could Be the Reasons?

Scenario:
User reports login failure.

Expected checks:

Password expired or locked

Disk full

Shell access disabled

/etc/passwd & /etc/shadow

SSH configuration

6. A File Was Accidentally Deleted – How Will You Recover It?

Scenario:
Critical file deleted by mistake.

Expected approach:

Check backups

Restore from snapshot (LVM, cloud)

Check open file handles (lsof)

Verify recycle/backup strategy

7. Server Reboots Automatically – How Do You Investigate?

Scenario:
Unexpected server reboots.

Expected approach:

Check logs: /var/log/messages, journalctl

Check hardware logs

Look for OOM (Out Of Memory)

Review cron jobs

Check kernel panic history

8. Permission Denied Error for a File – How Do You Fix It?

Scenario:
Application cannot access a file.

Expected approach:

Check permissions: ls -l

Verify ownership

Check SELinux: getenforce

Use chmod, chown, or restorecon

9. How Will You Schedule a Task to Run Automatically?

Scenario:
Need to run a script daily at 2 AM.

Expected approach:

Use crontab -e

Verify cron service

Check cron logs

Use absolute paths in scripts

10. System Is Running Out of Memory – What Will You Do?

Scenario:
Memory alerts on server.

Expected approach:

Check memory usage: free -m

Identify memory-heavy processes

Check swap usage

Restart leaking applications

Add RAM or optimize application

Bonus Tip for Interviews

Always answer in this order:

Command you’ll run

What you expect

Action you’ll take

Prevention steps
