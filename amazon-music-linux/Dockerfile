# To Run:
# OSX: (I cannot get it to sign in, 
#  input never takes keyboard input. Taybe you will have better luck)
# xhost +
# pulseaudio --load=module-native-protocol-tcp --exit-idle-time=-1 --daemon

# docker run --rm -v $HOME:$HOME -w $HOME -e PULSE_SERVER=${DISPLAY_IP}  -e DISPLAY=$DISPLAY  -v /tmp/.X11-unix:/tmp/.X11-unix --name amazon_music amazon_music  

# For Linux : tested on arch
# docker run --rm -it -v /tmp/.X11-unix:/tmp/.X11-unix \
# -e DISPLAY \
# --device /dev/dri \
# --device /dev/snd \
# --device /dev/video0 \
# --device /dev/input \
# -it --rm --name amazon_music amazon_music



FROM ubuntu:18.04

RUN apt-get update && apt-get install -y curl gnupg2 wget
RUN wget https://github.com/oja/amazon-music-linux/releases/download/v.1.4.0/amazon-music-linux-1.4.0_amd64.deb
RUN apt install -y  ./amazon-music-linux-1.4.0_amd64.deb
ENTRYPOINT ["/usr/bin/amazon-music-linux"]

