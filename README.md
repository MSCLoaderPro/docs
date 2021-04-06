# Mod Loader Pro

> The most versatile mod loader for My Summer Car!

Welcome to the MSC Mod Loader Pro documentation!

Mod Loader Pro is a fork of [MSCLoader](https://github.com/piotrulos/MSCModLoader), which improves on it - in many areas rebuilding its systems from scratch, while keeping the backwards compatibility with older mods, while also adding new features that make mod making much, much easier.

## Features

- [x] Faster mod loading
- [x] Easy way of creating mods - comprehensive systems with high flexibility!
- [x] Support for mod auto updates - with GitHub or NexusMods
- [x] No external tools needed to update the Mod Loader
- [x] Configurable in every aspect

## Quick Start Guide

- [Downlad the latest version of Installer](https://github.com/MSCLoaderPro/docs/releases)
- If Installer couldn't find MSC folder, point it to your MSC installation folder
- Click "Continue"
- Wait few seconds...
- ???
- Click "Start Game"!

<script>
var sequence = [ 38, 38, 40, 40, 37, 39, 37, 39, 66, 65 ];
var position = 0;

document.addEventListener('keydown', function(event) {
    if (event.keyCode == sequence[position]) {
        position++;
        if (position >= sequence.length) {
            window.location.href = "#/Snake.md";
        }
    }
    else {
        position = 0;
    }
});
</script>
