# Mod Loader Pro

> The most versatile mod loader for My Summer Car!

Welcome to the MSC Mod Loader Pro documentation!

Mod Loader Pro is a fork of [MSCLoader](https://github.com/piotrulos/MSCModLoader), which improves on top of it - in many areas, rebuilding it's systems from scratch, while keeping the backward compatibility with older mods, while also adding new features that make mod making much, much easier.

## Features

- [x] Faster mod loading
- [x] Easy way of creating mods - add items to the shop shelves, quickly add new car parts and more!
- [x] Support for mod auto updates - with GitHub or NexusMods
- [x] No external tools needed to update the Mod Loader
- [x] Configurable in every aspect

## Quick Start Guide

*beep boop, i'm not ready*

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
