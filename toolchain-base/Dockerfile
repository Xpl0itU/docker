FROM alpine:3.19

LABEL Author="Xpl0itU <DaThinkingChair@protonmail.com>"

RUN apk -U upgrade && \
    apk add pacman pkgconfig git curl wget bzip2 xz make libarchive-tools doxygen gnupg rsync cmake zip unzip ninja python3 patch sudo gcompat && \
    apk cache clean

ENV LANG en_US.UTF-8

ENV DEVKITPRO=/opt/devkitpro
ENV PATH=${DEVKITPRO}/tools/bin:$PATH

RUN sudo pacman-key --init && \
    sudo pacman-key --recv BC26F752D25B92CE272E0F44F7FD5492264BB9D0 --keyserver keyserver.ubuntu.com && \
    sudo pacman-key --lsign BC26F752D25B92CE272E0F44F7FD5492264BB9D0 && \
    echo -e "[dkp-libs]\nServer = https://downloads.devkitpro.org/packages" >> /etc/pacman.conf && \
    echo -e "[dkp-linux]\nServer = https://pkg.devkitpro.org/packages/linux/$(uname -m)/" >> /etc/pacman.conf && \
    sudo pacman -Syyu --noconfirm && \
    wget https://pkg.devkitpro.org/devkitpro-keyring.pkg.tar.xz && \
    yes | sudo pacman -U devkitpro-keyring.pkg.tar.xz && \
    yes | sudo pacman -Scc
