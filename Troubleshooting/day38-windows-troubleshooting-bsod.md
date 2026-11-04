# Day 38 - Windows Event Viewer & BSOD Troubleshooting

## Key Concepts
The Blue Screen of Death (BSOD) happens when Windows hits a critical error. The Event Viewer is Windows' logbook, storing these errors so you can review them after the PC restarts.

## Lab
- Opened Event Viewer and navigated to Windows Logs > System.
- Filtered for "Critical" and "Error" events to find system crashes.
- Documented how to enter Safe Mode (forcing 3 power-offs) to roll back bad drivers.

## Why It Matters
When a user reports a BSOD, the screen disappears. Event Viewer is the only way to find the root cause.

## Interview Q&A
**Q: A user's PC is stuck in a BSOD loop. How do you fix it?**
A: Force the PC off 3 times to trigger Automatic Repair. Boot into Safe Mode and uninstall recent updates or roll back drivers.

<img width="1366" height="709" alt="Day-38-Logs_errors" src="https://github.com/user-attachments/assets/055869a8-3f9c-44ed-8ff9-c475a930e787" />
