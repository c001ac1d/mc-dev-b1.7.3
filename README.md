# Decompiled and buildable Beta 1.7.3 server
This is a fork of the official CraftBukkit mc-dev repository which was (at some point in time) supported for new versions of the game.

This repository is reverted back to commit `1.7.3` (hash `1a792ed860ebe2c6d4c40c52f3bc7b9e0789ca23`) and edited to be buildable by most modern tools.

The goal is to provide easy access to a buildable and working version of a Beta 1.7.3 server, as it gained relevancy lately.
# Usage
You can open this repository as a raw java project through Eclipse or IntelliJ Idea, or initialize a build system of your liking.

Point your IDE/Build system to launch `MinecraftServer` as the main class, and run the application.
# Warning
Make sure to not connect to the server straight away after you first launch it, because you will be greeted with an instant client crash.

You should set `online-mode` to `false` in your `server.properties` file. The reason for this is that Mojang's authentication servers nowadays use a modern version that Beta 1.7.3 is not capable of working with.

The client tries to initiate a legacy authentication process, gets an unexpected response, and immediately crashes.

Setting `online-mode` to `false` disables the authentication step and avoids the crash.