# GeekCord
A fork and continuation of SmartCord and GooseMod Untethered.

#### Disclaimer
**Using GeekCord, or any other client mod, is against [Discord's Terms of Service](https://discordapp.com/terms). Use it at your own risk.**\
It's very unlikely any action will be taken against you (if you don't abuse), but we take no responsibility if anything happens.

#### Installing
Download/clone this repository to wherever you want your GeekCord files to reside.

Find Discord's installation directory:\
Windows: `%homepath%\AppData\Local\discord`\
macOS: `~/Library/Application Support/discord`\
GNU/Linux: `~/.config/discord`\
Replace `discord` with `discordcanary` as needed.

In Discord's installation directory, find `x.x.xxx/modules/discord_desktop_core/index.js`, where `x.x.xxx` is your current version of the Discord client, and open it.

At the top, add these lines:\
`process.env.injDir = '<path>';`\
``require(`${process.env.injDir}/injection.js`);``\
where `<path>` is the location of the GeekCord directory.

Make sure to escape paths. E.g: `C:\Users\<Username>\Documents\GeekCord` should be `C:\\Users\\<Username>\\Documents\\GeekCord`

Install [BusyBox-w32](https://frippery.org/busybox) (Windows; install to `Windows` directory) or BusyBox ([GNU/Linux](https://busybox.net/downloads/binaries), [macOS](https://github.com/xdevs23/busybox-osx)) and run *httpd*:\
`busybox httpd -p 127.0.0.1 -h <path/to/GeekCord/API>`

Restart your Discord client.

#### Notes
GooseMod data is not saved. (I'm working on a fix.)

SmartCord settings and plugins can only be modified by editing the `config.json` file. (For convenience, this repository includes a pre-set `config.json` file.)
