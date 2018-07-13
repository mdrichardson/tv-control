# Sony Bravia TV Control

This is a set of batch files that I use to control my Sony Bravia TV. I use them in conjunction with EventGhost, which executes these batch files as part of my home automation scheme.

## Usage

1. Change the IP address in each `*.bat` file to match your TV's
2. Turn on your TV
3. On the TV go to Settings > Network > Home network setup > Remote device/Renderer > On
4. On the TV go to Settings > Network > Home network setup > IP Control > Authentication > Normal and Pre-Shared Key
5. On the TV go to Settings > Network > Home network setup > Remote device/Renderer > Enter Pre-Shared Key > 0000 (or whatever you want your PSK Key to be)
6. On the TV go to Settings > Network > Home network setup > Remote device/Renderer > Simple IP Control > On
7. Run `register.bat` - this authenticates your computer with your TV. You may have to run this every now and then to keep it registered.
8. Run any other `*.bat` to execute the desired function.

You can execute additional commands by:

1. Look in `Available Commands.txt` for your desired command
2. Copy the `value` for that command
3. Copy/Paste one of the other `*.bat` files and rename it to your desired command.
4. Edit your new `*.bat` file and replace the value after `<IRCCCode>` with the value you copied from `Available Commands.txt`

## Requirements

1. curl.exe
2. A Sony Bravia TV that uses this same HTTP API

Note:
There's a [great github repo here](https://github.com/alanreid/bravia) that uses node.js for running all of the commands. I wrote this because I wanted to write something simpler for myself.