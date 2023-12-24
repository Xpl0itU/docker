FROM alpine:3.19

LABEL Author="Xpl0itU <DaThinkingChair@protonmail.com>"

RUN apk -U upgrade -y && \
    apk add pacman pkgconfig git curl wget bzip2 xz make libarchive-tools doxygen gnupg rsync cmake zip unzip ninja python patch && \
    apk cache clean

ENV LANG en_US.UTF-8

ENV DEVKITPRO=/opt/devkitpro
ENV PATH=${DEVKITPRO}/tools/bin:$PATH

RUN ln -s /proc/mounts /etc/mtab && \
    pacman-key --recv BC26F752D25B92CE272E0F44F7FD5492264BB9D0 --keyserver keyserver.ubuntu.com && \
    pacman-key --lsign BC26F752D25B92CE272E0F44F7FD5492264BB9D0 && \
    wget https://pkg.devkitpro.org/devkitpro-keyring.pkg.tar.xz && \
    pacman -U devkitpro-keyring.pkg.tar.xz && \
    echo -e "[dkp-libs]\nServer = https://downloads.devkitpro.org/packages" >> /etc/pacman.conf && \
    echo -e "[dkp-linux]\nServer = https://downloads.devkitpro.org/packages/linux" >> /etc/pacman.conf && \
    yes | dkp-pacman -Scc
