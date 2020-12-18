Memory usage after installation is only 40MB.
Disk usage 2.6 GB while regular slackware full instalation takes 10GB.
It is required to install initrd before first reboot as this set of packages is using generic kernel, not huge.

#LANG=en_US.uUTF-8 df -h
Filesystem      Size  Used Avail Use% Mounted on
tmpfs            32M  348K   32M   2% /run
devtmpfs        7.9G     0  7.9G   0% /dev
/dev/vda3      1005G  2.6G  952G   1% /
tmpfs           7.9G     0  7.9G   0% /dev/shm
cgroup_root     8.0M     0  8.0M   0% /sys/fs/cgroup
/dev/vda1       190M   37M  140M  21% /boot

#LANG=en_US.uUTF-8 free -m
              total        used        free      shared  buff/cache   available
Mem:          16016          42       15885           0          88       15764
Swap:          2047           0        2047


You can download tar archive here:

Slackware 15
http://public.pionica.com/pubfiles/linux/tagfiles15.tar

Slackware 14.2
http://public.pionica.com/pubfiles/linux/tagfiles142.tar

In order to use PHP gd module you need to install additionally:

x/fontconfig
x/libXpm
x/libX11
x/libxcb
x/libXau
x/libXdmcp

Missing libraries (will not be included without good reason):

x/libXt
x/libXext
x/libSM
x/libICE
x/libXaw
x/libXmu
x/libXt
x/libglut
x/libGL
x/libcairo

To install QEMU (http://www.slackware.com/~alien/slackbuilds/qemu/) you will need to manually install these dependencies:

ap/flac
l/pulseaudio
l/SDL2
l/SDL2_image
l/gtk+3
l/pango
l/atk
l/cairo
l/gdk-pixbuf2
l/libsndfile
l/fribidi
l/libxkbcommon
l/at-spi2-atk
l/at-spi2-core
l/vorbis
l/opus
l/libogg
x/libepoxy
x/mesa
x/pixman
x/libglvnd
x/libXext
x/libXrender
x/libXinerama
x/libXrandr
x/libXcomposite
x/libXfixes
x/libXdamage
x/libXcursor
x/libXi
x/wayland
x/libdrm

Missing dependencies after installing libraries for QEMU (they will not be included without good reason). Because of that you will probably not be able to use sound card device in Virtual Machines, however Windows sound is working through Windows Remote Desktop client:

libXft needed by pango-view
libGLEW needed by glthreads glxpixmap glinfo and few others from MESA
libGLU needed by glthreads glxpixmap glinfo and few others from MESA
liborc needed by pulseaudio
libspeexdsp needed by pulseaudio
libgtk-X11 needed by iodbcadm-gtk
libgdk-X11 needed by iodbcadm-gtk


Feel free to send me any change requests in post on the forum: https://www.linuxquestions.org/questions/slackware-14/slackware-set-of-packages-for-headless-server-no-gui-4175686983

