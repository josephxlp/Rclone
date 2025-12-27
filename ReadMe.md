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

rclone listremotes
-------------------------------------------------------------------------------------------
mkdir -p $HOME/RcloneOneDrive


WX1::
-------------------------------------------------------------------------------------------
  rclone mount "OneDrive": $HOME/RcloneOneDrive --vfs-cache-mode full

#can i run this with tmux so the terminal is available for other tasks?
>
rclone mount "OneDriveRclone": $HOME/RcloneOneDrive --vfs-cache-mode full
>
Note: This command will occupy your terminal. If you want it to run in the background so you can keep using the terminal, add an & at the end: 
>
rclone mount "OneDriveRclone": $HOME/RcloneOneDrive --vfs-cache-mode full &
>
fusermount -u $HOME/RcloneOneDrive

-------------------------------------

tmux new-session -d -s onedrive 'rclone mount "OneDrive": $HOME/RcloneOneDrive --vfs-cache-mode full'
>
tmux attach-session -t onedrive

