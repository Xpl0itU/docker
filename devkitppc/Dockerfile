FROM ghcr.io/xpl0itu/toolchain-base

LABEL Author="Xpl0itU <DaThinkingChair@protonmail.com>"

RUN sudo pacman -Syyu --noconfirm gamecube-dev wii-dev wiiu-dev && \
    sudo pacman -S --needed --noconfirm ppc-portlibs gamecube-portlibs wii-portlibs wiiu-portlibs && \
    sudo pacman -S --needed --noconfirm devkitARM && \
    yes | sudo pacman -Scc

ENV DEVKITPPC=${DEVKITPRO}/devkitPPC
ENV DEVKITARM=/opt/devkitpro/devkitARM
