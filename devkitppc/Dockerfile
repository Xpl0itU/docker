FROM ghcr.io/xpl0itu/toolchain-base

LABEL Author="Xpl0itU <DaThinkingChair@protonmail.com>"

RUN pacman -Syyu --noconfirm gamecube-dev wii-dev wiiu-dev && \
    pacman -S --needed --noconfirm ppc-portlibs gamecube-portlibs wii-portlibs wiiu-portlibs && \
    pacman -S --needed --noconfirm devkitARM && \
    yes | pacman -Scc

ENV DEVKITPPC=${DEVKITPRO}/devkitPPC
ENV DEVKITARM=/opt/devkitpro/devkitARM
