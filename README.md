# howto
HOWTO is a tiny shell integration that automatically displays helpful instructions when you cd into a directory that contains a file named howto.<br>
It's like a built-in reminder or mini manual for your project folders — no need to open README files manually. Just drop a howto file in any directory, and the shell will show it as soon as you enter.
## Supported shells
- [x] **bash**
- [x] **zsh**
- [x] **fish**
- [x] **sh**
- [x] dash
- [ ] ksh
- [ ] mksh
- [ ] elvish
- [ ] xonsh
## Use cases
- Remind yourself to build or run project
- Leave setup instructions for teammates
- Explain folder structure
- Show development notes or warnings
## Using
### Method 1. Installation
Instruments you need:
- git

First, you need to install `howto`. To install `howto`, just run these commands:
```
git clone https://github.com/msh356/howto
cd howto
```
and then activate profile for your shell:
```
source profiles/$(basename $SHELL)profile
```
This will activate a profile for your shell.
### Method 2. Online
Instruments you need:
- Network connection
- curl

To run HOWTO from internet, you can use this command:
```
source <(curl -s https://raw.githubusercontent.com/msh356/howto/refs/heads/master/profiles/$(basename $SHELL)profile)
```
> **‼️ `fish` does NOT support this syntax.** For using in fish, you need to run this command:
> `curl -s https://raw.githubusercontent.com/msh356/howto/refs/heads/master/profiles/$(basename $SHELL)profile | source`
### Testing
If you wanna test HOWTO, you can just enter the HOWTO folder. If all is correct, you will see something like this:
```
msh@msh-pc:~/howto$ cd ..
msh@msh-pc:~$ cd howto
                                  _         _       _   _                 _ 
   ___ ___  _ __   __ _ _ __ __ _| |_ _   _| | __ _| |_(_) ___  _ __  ___| |
  / __/ _ \| '_ \ / _` | '__/ _` | __| | | | |/ _` | __| |/ _ \| '_ \/ __| |
 | (_| (_) | | | | (_| | | | (_| | |_| |_| | | (_| | |_| | (_) | | | \__ \_|
  \___\___/|_| |_|\__, |_|  \__,_|\__|\__,_|_|\__,_|\__|_|\___/|_| |_|___(_)

You're succesfully installed HOWTO. You can copy bashprofile, zshprofile or
fishprofile contents to their config files, using commands:
-bashprofile----------------------------------------------------------------
cat profiles/bashprofile >> ~/.bashrc
-zshprofile-----------------------------------------------------------------
cat profiles/zshprofile >> ~/.zshrc
-fishprofile----------------------------------------------------------------
cat profiles/fishprofile >> ~/.config/fish/config.fish
msh@msh-pc:~/howto$
```
### Permanent installing
To run HOWTO from shell start, you can copy profiles to your config files:
#### bash
```
cp ~/.bashrc ~/.bashrc.old
cat profiles/bashprofile >> ~/.bashrc
```
If something goes wrong:
```
rm ~/.bashrc
cp ~/.bashrc.old ~/.bashrc
```
#### zsh
```
cp ~/.zshrc ~/.zshrc.old
cat profiles/zshprofile >> ~/.zshrc
```
If something goes wrong:
```
rm ~/.zshrc
cp ~/.zshrc.old ~/.zshrc
```
#### (da)sh
```
cp ~/.profile ~/.profile.old
cat profiles/dashprofile >> ~/.profile
```
If something goes wrong:
```
rm ~/.profile
cp ~/.profile.old ~/.profile
```
#### fish
```
cp ~/.config/config.fish ~/.config/config.fish.old
cat profiles/fishprofile >> ~/.config/config.fish
```
If something goes wrong:
```
rm ~/.config/config.fish
cp ~/.config/config.fish.old ~/.config/config.fish
```
