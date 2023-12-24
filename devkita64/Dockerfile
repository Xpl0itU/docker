FROM ghcr.io/xpl0itu/toolchain-base

LABEL Author="Xpl0itU <DaThinkingChair@protonmail.com>"

RUN pacman -Syyu --noconfirm && \
    pacman -S --needed --noconfirm switch-dev && \
    pacman -S --needed --noconfirm switch-portlibs && \
    pacman -S --needed --noconfirm devkitARM && \
    yes | pacman -Scc

ENV DEVKITARM=/opt/devkitpro/devkitARM

