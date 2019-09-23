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
1) Open a terminal

   Windows: `run cmd.exe`

   macOS: open `terminal`

2) Type `keybase update` and press enter.
3) You should see your current version as:

   `YYYY/MM/DD HH:MM:SS INFO Checking for update, current version is 4.5.0-*`

## Android:
(This is a work in progress)
1) Open the google play store and update the KeyBase App

# Finding your configuration path
## Desktops:
1) In that same terminal (you still have it open right?) type `keybase status` and press enter
2) look for the output in the `Service:` section that starts with `log:`

   (Mine says `C:\Users\haukened\AppData\Local\Keybase\keybase.kbfs.log` but your may vary depending on operating system and installation)
   
3) Remove the log filename from that to get the `PATH` to the directory

   (in my example that would be `C:\Users\haukened\AppData\Local\Keybase\`)
   
## Android:
(Work in Progress)

# Creating the debug file
4) Go to that folder in your file explorer, terminal, or whatever you like to use

   Most Command Lines: `cd C:\Users\haukened\AppData\Local\Keybase\`
   
5) Create a new text file in that location called keybase.app.debug

   Windows: `haukened> notepad.exe c:\Users\haukened\AppData\Local\Keybase\keybase.app.debug`
   
   *nix: TBD
   
   Android: TBD
   
6) In that file, place the following:

   `{ "featureFlagsOverride": "darkMode" }`

7) Save the file
8) Restart KeyBase (or on windows you can just reboot, if you don't know how to exit keybase and restart the service)
9) In the KeyBase client, go to `Settings` -> `Advanced` -> `Dark Mode` and select the radio button for dark mode.
10) Enjoy your status as one of the cool kids.
11) (Optional) If you're 21+ and a consenting adult, have a beer.


