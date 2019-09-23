# So you want keybase dark mode...

I assume you're here because you just can't possibly wait for keybase dark mode.  If you're not, you're likely lost - head on over to [Google](https://google.com) to find what you're looking for there.

Below we'll detail how you can get dark mode (preview) enabled before the release in the official keybase app, but proceed with caution - ***the authors of this document are NOT responsible for nasty things that it or you might do to your computer/phone/tablet by following these instructions***

# Can I use this?
Currently, these platforms are able to:

| Windows | macOS | \*Nix | Android | iPhone |
|---------|-------|-------|---------|--------|
|   Yes   |  Yes  |  Yes  |   Yes   |   No   |

# Getting up to date
First things first, you should be working with an up-to-date keybase client.

## Desktops:
1)  Open a terminal
1.1) Windows: `run cmd.exe`
1.2) macOS: open `terminal`
1.3) Linux with Gnome 3: open Activities and type `terminal`, click on the icon when it appears
1.4) Linux with other desktops: Open the main apps menu, and look for the terminal app
2) Type `keybase update` and press enter.
3) You should see your current version as:
`YYYY/MM/DD HH:MM:SS INFO Checking for update, current version is 4.5.0-*`
## Android:
(This is a work in progress)
1) Open the google play store and update the KeyBase App

# Finding your configuration path
## Desktops:
### Windows:
1) In that same terminal (you still have it open right?) type `keybase status` and press enter
2) look for the output in the `Service:` section that starts with `log:`
(Mine says `C:\Users\haukened\AppData\Local\Keybase\keybase.kbfs.log` but yours may vary depending on Windows version and installation)
3) Remove the log filename from that to get the `PATH` to the directory
(in my example that would be `C:\Users\haukened\AppData\Local\Keybase\`)
### Linux:
The path can usually be reached on any Linux system at `~/.cache/keybase/`. If that doesn't seem to exist, use the following steps to find it:
1) In that same terminal (you still have it open right?) type `keybase status` and press enter
2) look for the output in the `Service:` section that starts with `log:`
(Mine says `/home/brian/.cache/keybase/keybase.service.log` but yours may vary depending on Linux distribution and installation)
3) Remove the log filename from that to get the `PATH` to the directory
(in my example that would be `/home/brian/.cache/keybase/`)
## Android:
(Work in Progress)

# Creating the debug file
4) Go to that folder in your file explorer, terminal, or whatever you like to use
4.1) Most Command Lines: `cd C:\Users\haukened\AppData\Local\Keybase\` or `cd ~/.cache/keybase/`
5) Create a new text file in that location called keybase.app.debug
5.1) Windows: `haukened> notepad.exe c:\Users\haukened\AppData\Local\Keybase\keybase.app.debug`
5.2) In a Linux terminal, `$ nano ~/.cache/keybase/keybase.app.debug` or open any graphical text editor
5.3) Android: TBD
6) In that file, place the following:
`{ "featureFlagsOverride": "darkMode" }`
7) Save the file
8) Restart KeyBase (or you can just reboot, if you don't know how to exit keybase and restart the service)
9) In the KeyBase client, go to `Settings` -> `Advanced` -> `Dark Mode` and select the radio button for dark mode.
10) Enjoy your status as one of the cool kids.
11) (Optional) If you're 21+ and a consenting adult, have a beer.


