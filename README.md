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

[Example of workflow features](http://a.pomf.se/fccmjz.webm)

###Notes
**F7, F8, F9 Section**

![suggested hotkey layout](http://i.imgur.com/Lkb1g1D.png)
*suggested hotkey layout for this section*

This section assumes you have followed instructions [here](http://www.reddit.com/r/osx/comments/21dp3w/anyone_looking_for_a_good_command_line_music/cgcixe7) to use [Karabiner](https://pqrs.org/osx/karabiner/) to change the function of your media keys.

*Known Issues*

I can't quite get the notification for F8 to work. It seems there's a delay in the process, so when it checks if the song is playing it's not always correct. Any help here would be great.

**Now Playing Notification**

*To Do*

Have track number position (*i.e.(#2/13)*) identify number in album as opposed to position in entire playlist

**Playlist Section**

*To Do*

~~Determine notification function when playlist is too large to display in entirety. Likely limit to a certain number of lines~~ (Script now limits output to 8 items)

**Lyrics Section**

I'd mostly ignore this section. I wrote it up when ncmpcpp's lyrics function wasn't working for me, but the problem has since been fixed and lyrics work properly in ncmpcpp making this pretty useless since it's not as good.

*Maybe To Do*

Implement similar functionality to ncmpcpp's lyric fetch involving multiple databases and local search

**Add Album / Add Artist Section**

For this section be sure to set the search scope to wherever your music files are located. File type should be public.folder.

*Known Issues*

I'm not sure how to set the depth of the scope. The result being that artists will show up in an album search and vice versa. I haven't had much time to search for a fix on this, but if anyone has an idea please let me know.

**To Listen Section**

`Under Construction`

This section is nowhere close to completed. The idea is to search a 'To Listen' folder for albums you want to listen to. It'd then add the albums to both iTunes and mpd+ncmpcpp. I haven't had time to work on this as I'm currently auditing my current music library and have deleted all albums from iTunes. Check back in the summer when I have more time to work on this kind of stuff.

***
```
  Not for commercial use

  Please share any improvements made to workflows
```