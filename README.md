# avc2ts
Tailored Copy of F5OEO's avc2ts for use in Portsdown 4 Transmitter with 7 inch touchscreen

Thanks to Evariste for the original code here: https://github.com/F5OEO/avc2ts
```

Usage:
avc2ts  -o OutputFile -b BitrateVideo -m BitrateMux -x VideoWidth  -y VideoHeight -f Framerate -n MulticastGroup [-d PTS/PCR][-v][-h] 
-o    path to Transport File Output 
-b    VideoBitrate in bit/s 
-m    Multiplex Bitrate (should be around 1.4 VideoBitrate)
-x    VideoWidth (should be 32 pixel aligned)
-y    VideoHeight (should be 16 pixel aligned)
-f    Framerate (25 for example)
-n    Multicast group (optional) example 230.0.0.1:10000
-d    Delay PTS/PCR in ms
-v    Enable Motion vectors
-i    IDR Period
-t    TypeInput {0=Picamera,1=InternalPatern,2=USB Camera,3=Rpi Display,4=VNC,5=ffmpeg}
-e    Extra Arg:
      - For usb camera name of device (/dev/video0)
      - For VNC : IP address of VNC Server. Password must be datv
      - For ffmpeg : url or file to stream
-u    Optional invert Pi Cam image
-p    Set the PidStart: Set PMT=PIDStart,Pidvideo=PidStart+1,PidAudio=PidStart+2
-s    Set Servicename : Typically CALL
-h    help (print this help).
Example : ./avc2ts -o result.ts -b 1000000 -m 1400000 -x 640 -y 480 -f 25 -n 230.0.0.1:1000

```
