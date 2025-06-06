<div align="center">
    <img src="fast_mosh_logo.png" />
    <br/>
    <b>Connect quickly to your services with Mosh 🚀</b>
    <br/>
    <br/>
    <a href="https://github.com/tiwiex/fast-mosh/actions/workflows/release.yml">
        <img src="https://github.com/tiwiex/fast-mosh/actions/workflows/release.yml/badge.svg" />
    </a>
    <a href="https://crates.io/crates/fast-mosh">
        <img src="https://img.shields.io/crates/v/fast-mosh.svg" />
    </a>
    <img src="https://img.shields.io/crates/l/fast-mosh.svg">
    <br/>
    <br/>
    <div>
        Fast-Mosh is a fork of [Fast-SSH](https://github.com/Julien-R44/fast-ssh) that uses Mosh instead of SSH for connections. 
    </div>
    <br/>
</div>

# Installation
***MAKE SURE mosh IS INSTALLED ON YOUR CLIENT AND YOUR SERVER***

For Ubuntu, **run apt install mosh**.
If you have installed Cargo then run **cargo install fast-mosh --force** (force ensures an update if you already installed fast-mosh)
Version 0.3.4 addresses an issue in mosh which does not allow scrolling for long outputs. This issue is explained here https://github.com/mobile-shell/mosh/issues/122. In summary: 

**"@RipperSK The root cause of not able to scroll is caused by mosh entering a "alternative screen" mode. It can be disabled using the --no-init flag (see the doc). Just alias mosh='mosh --no-init' and the problem will go away. This comment has been minimized."**

So I have updated the mosh command in main.rs to include arg for --no-init.

Follow a similar instruction for your Linux distro.
For the Mac, use Home Brew and run 

**brew install mosh**
For detailed installation instructions, please refer to the [Fast-SSH README](https://github.com/Julien-R44/fast-ssh#installation). 

**Note:** The primary change in Fast-Mosh is that it uses `mosh` instead of `ssh`. You can use the same installation method with `fast-mosh`.

# Usage
The usage remains the same to Fast-SSH, but instead of executing `ssh`, you will execute `mosh` to connect to your services. 

Mosh ensures session restarts from your ssh connection. No more broken pipes or connections. You can hibernate your computer and your session reconnects once your resume (AS LONG AS THE TERMINAL WAS NOT CLOSED OR SERVER REBOOTED) Just make sure you have mosh installed locally and on the remote server.

For more detailed usage instructions, refer to the [Fast-SSH README](https://github.com/Julien-R44/fast-ssh#documentation).

# Acknowledgements
Fast-Mosh is a fork of [Fast-SSH](https://github.com/Julien-R44/fast-ssh) by Julien-R44. All credits for the original work go to Julien-R44 and the contributors of Fast-SSH. This project adapts Fast-SSH to use Mosh instead of SSH.


