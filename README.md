# CrowdstrikeUsbFix
Fix for Crowdstrike issue with USB Bootdevice

Create a bootable Windows PE (Preinstallation Environment) USB:

Download and install the Windows ADK (Assessment and Deployment Kit) and the Windows PE add-on.
Use the Windows ADK to create a bootable Windows PE USB.


Add the script to the USB:

Copy the script provided in the artifact to a file named CrowdstrikeFix.bat on the root of the USB drive.


Modify the Windows PE startup:

Mount the Windows PE image on the USB.
Edit the startnet.cmd file to include a line that runs your CrowdstrikeFix.bat script.


Use the USB to fix the machines:

Insert the USB into each affected machine and boot from it.
The script will run automatically, delete the problematic file, and prompt for a reboot.


Reboot the machine:

After the script completes, remove the USB and reboot the machine normally.
