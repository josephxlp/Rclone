# Set up OneDrive in Linux 

rclone listremotes
rclone config delete SharePoint
rclone config delete OneDrive
https://kb.uconn.edu/space/IKB/26050527301/Install+OneDrive+on+Linux


- create local direcory
mkdir ~/OneDrive
- mount remote to local direcory 
rclone --vfs-cache-mode writes mount OneDrive: ~/OneDrive &

https://rclone.org/gui/
rclone rcd --rc-web-gui

https://rclone.org/commands/

https://rclone.org/onedrive/ :: onedrive mounting


create directory and then mount

mkdir -p $HOME/RcloneOneDrive

rclone mount "OneDrive": $HOME/RcloneOneDrive --vfs-cache-mode full

rclone mount "OneDriveRclone": $HOME/RcloneOneDrive --vfs-cache-mode full
