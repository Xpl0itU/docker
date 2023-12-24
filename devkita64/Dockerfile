FROM ghcr.io/xpl0itu/toolchain-base

LABEL Author="Xpl0itU <DaThinkingChair@protonmail.com>"

RUN sudo pacman -Syyu --noconfirm && \
    sudo pacman -S --needed --noconfirm switch-dev && \
    sudo pacman -S --needed --noconfirm switch-portlibs && \
    sudo pacman -S --needed --noconfirm devkitARM && \
    yes | pacman -Scc

ENV DEVKITARM=/opt/devkitpro/devkitARM

