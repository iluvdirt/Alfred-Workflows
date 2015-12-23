#Alfred-Workflows
***
##Mpd+Ncmpcpp Controller

This workflow assumes you have mpd+ncmpcpp installed in `/usr/local/bin/` (default Homebrew install location) - be sure to change accordingly. Notifications have only been tested with Growl. Most notifications work with notification center, but I know of the top of my head that the lyrics and playlist features won't display properly. I use icons from [here](http://www.deviantart.com/art/Google-JFK-Icons-ICO-and-PNG-270715545), all credit goes to the author for their work.

**Features**

*	Use Media Keys (F7, F8, F9 on MBP) to control playback
*	Display notification for currently playing track
*	Clear current playlist
*	Display notification with tracklist of current playlist
*	Add any number of random albums to the playlist
*	Display notification for lyrics of current track
*	Add album to playlist
*	Add all albums of an artist to playlist


###Notes
**F7, F8, F9 Section**

![suggested hotkey layout](http://i.imgur.com/Lkb1g1D.png)
*suggested hotkey layout for this section*

This section assumes you have followed instructions [here](http://www.reddit.com/r/osx/comments/21dp3w/anyone_looking_for_a_good_command_line_music/cgcixe7) to use [Karabiner](https://pqrs.org/osx/karabiner/) to change the function of your media keys.

This section allows you to control playback of mpd+ncmpcpp with your media keys.

**Now Playing Notification**

This section outputs a notification in the following format

![](http://i.imgur.com/kIg5wkU.png)

*Maybe To Do*

Have track number position (*i.e.(#2/13)*) identify number in album as opposed to position in entire playlist

**Playlist Section**

Next 10 songs in playlist are output in a notification.

![](http://i.imgur.com/e8Sj89D.png)

**Random Section**

This section requires `coreutils` from Homebrew. 

**Lyrics Section**

I'd mostly ignore this section. I wrote it up when ncmpcpp's lyrics function wasn't working for me, but the problem has since been fixed and lyrics work properly in ncmpcpp making this pretty useless since it's not as good.

**Add Album / Add Artist Section**

For this section be sure to set the search scope to wherever your music files are located. File type should be public.folder (drag a folder into File Type area).

*Instructions*

For this to work as intended, add a tag entitled "Artists" to all Artist folders in directory. Assuming all Artist folders are at the same folder depth cmd+a -> right click -> Tags... -> "Artists" -> Enter.

![](http://i.imgur.com/blRldH4.png)

This will tag all your folders to be compatible with the workflow. I use [Hazel](http://www.noodlesoft.com/hazel.php) to automate this tagging process.

If you don't want to do tags this section will still work, Artist folders will just show up in Album searches and vice versa.

*Notes*

Pressing shift when adding an Artist / Album will append it to the playlist. Default action clears the playlist then adds the Artist / Album.

**To Listen Section**

![](http://i.imgur.com/m54Z4yw.png)

*Prerequisites* 

The folders in your "To Listen" folder must have the following naming format: *Artist - Album*

Your music directory must be organized in the following structure: *Music Directory/Artist/Artist's Albums/Album's Songs* (If this is unclear, the folder structure I'm attempting to describe is the same that is set by default if you use iTunes to organize your library)

*Setup*

Set your "To Listen" directory by clicking the "Browse in Alfred" button on the top right. Also, be sure to edit the music directory set in the bash script.

*Usuage*

Press the Hotkey assigned to the "Browse in Alfred" button.

Navigate to the album you would like to add and press the right-arrow key on your keyboard.

Navigate to the file action that says "Add Album" and hit enter.

*How it works*

When the script is run it does the following:

Checks the Artist name of the folder you are adding and sees if that Artist already exists in your music directory. If it does, then it will rename the folder to the Album name and move it to the Artist folder. If it does not, it will create a new Artist folder in your music directory then place the Album folder in it. Once this is completed the script updates your mpd library, clears the current playlist, creates a new one with the album you just added, and starts playing.

*Notes*

I have added an alternate script that instead takes the naming structure of *Artist - Album (Year)* and makes a copy of the folder instead of moving and renaming. This script is meant to be used if you need to keep something seeding.

![](https://fat.gfycat.com/ShowyUntidyFlycatcher.gif)

***
```
  Not for commercial use

  Please share any improvements made to workflows
```