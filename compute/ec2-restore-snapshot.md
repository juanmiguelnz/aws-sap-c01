### Restore EC2 Snapshot - Root Volumes
1. Create a new volume from a Snapshot you want to restore.
2. Take note of the device name that you want to replace in the Root device entry or Block Devices entries.
3. Stop the EC2 Instance.
4. Detach the volume you want to replace from the EC2 Instance.
5. Attach the new volume you created from the Snapshot. Use the same device name that you noted earlier.

### Restore EC2 Snapshot - Non-Root Volumes
