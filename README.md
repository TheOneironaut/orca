# Orca RTL for Windows

[![Build Orca RTL](https://github.com/TheOneironaut/orca/actions/workflows/build.yml/badge.svg)](https://github.com/TheOneironaut/orca/actions/workflows/build.yml)

## Download

**[Download the latest Windows installer](https://github.com/TheOneironaut/orca/releases/download/rtl-latest/orca-rtl-windows-setup.exe)**

[Release details and SHA-256](https://github.com/TheOneironaut/orca/releases/tag/rtl-latest)

This repository is intentionally minimal. It does only three things:

1. Downloads the latest `stablyai/orca` source.
2. Applies the small Native Chat RTL patch in [`patches/native-chat-rtl.patch`](patches/native-chat-rtl.patch).
3. Builds and publishes an unsigned Windows installer.

The patch affects chat content only:

- Hebrew and Arabic prompts use automatic RTL direction and start alignment.
- Hebrew and Arabic Markdown responses use automatic RTL direction.
- Code blocks remain left-to-right.
- The rest of the Orca interface remains unchanged.

A single GitHub Actions workflow checks for upstream changes every six hours. When Orca changes, it applies the patch, runs lint and type checking, builds the Windows installer, and replaces the rolling `rtl-latest` release.

> Windows SmartScreen may warn because this community build is unsigned.

Original project: [stablyai/orca](https://github.com/stablyai/orca)
