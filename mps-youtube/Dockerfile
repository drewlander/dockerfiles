# Run with:
# For OSX: (video would be over network via Xquartz, so no, dont do it)
# brew install pulseaudio
# pulseaudio --load=module-native-protocol-tcp --exit-idle-time=-1 --daemon
#docker run --rm -v $HOME:$HOME -w $HOME -it \
#  -e PULSE_SERVER=<your-ip> \
#  -e HOME=$HOME  \
#  mpsyt



# For Linux (tested on arch)
# (if ou want X, add the X11 and DISPLAY
# docker run --rm -it -v /tmp/.X11-unix:/tmp/.X11-unix \
#-e DISPLAY \
#--device /dev/dri \
#--device /dev/snd \
#--device /dev/video0 \
#--device /dev/input \
#-it --rm --name mpsyt mpsyt


FROM python:latest
MAINTAINER Justin Garrison <justinleegarrison@gmail.com>

RUN apt-get update && apt-get install -y mplayer mpv pulseaudio
RUN pip install mps-youtube youtube-dl
RUN apt-get clean && apt-get purge

ENTRYPOINT ["mpsyt"]
