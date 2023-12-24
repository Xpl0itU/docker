FROM ghcr.io/xpl0itu/toolchain-base

LABEL Author="Xpl0itU <DaThinkingChair@protonmail.com>"

RUN pacman -Syyu --noconfirm && \
    pacman -S --needed --noconfirm 3ds-dev nds-dev gp32-dev gba-dev gp2x-dev && \
    pacman -S --needed --noconfirm 3ds-portlibs nds-portlibs armv4t-portlibs && \
    yes | pacman -Scc

ENV DEVKITARM=${DEVKITPRO}/devkitARM
