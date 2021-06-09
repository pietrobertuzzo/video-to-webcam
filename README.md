# video-to-webcam
Simple script using ffmpeg and v4l2loopback to pipe a video stream to a dummy webcam signal.

# usage

First, make sure the desired output exists:

`ls /dev/video*`

video0 is usually your webcam.

If not, try this:

`sudo modprobe v4l2loopback`

This should create '/dev/video1' and '/dev/video2' output streams. Use the latter. You can simply use the command as such:

`. /path/to/repository/vtw file.mp4 /dev/video2 `

The `-h` flag is available as a quick reminder on the arguments' order. You can also create a soft link to invoke the script as a command:

`ln -s ~/path/to/repo/vtw $PATH/vtw`
