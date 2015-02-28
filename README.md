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

This section allows you to control playback of mpd+ncmpcpp with your media keys.

**Now Playing Notification**

This section outputs a notification in the following format

![](http://i.imgur.com/wUS29Wo.png)

*Maybe To Do*

Have track number position (*i.e.(#2/13)*) identify number in album as opposed to position in entire playlist

**Playlist Section**

Tracklist of current playlist is output in a notification (limited to 10 items)

![](http://i.imgur.com/e8Sj89D.png)

*To Do*

Change notification to only show songs that have not been played in playlist

**Lyrics Section**

I'd mostly ignore this section. I wrote it up when ncmpcpp's lyrics function wasn't working for me, but the problem has since been fixed and lyrics work properly in ncmpcpp making this pretty useless since it's not as good.

*Pretty Unlikely To Do*

Implement similar functionality to ncmpcpp's lyric fetch involving multiple databases and local search

**Add Album / Add Artist Section**

For this section be sure to set the search scope to wherever your music files are located. File type should be public.folder (drag a folder into File Type area).

*Instructions*

For this to work as intended, add a tag entitled "Artists" to all Artist folders in directory. Assuming all Artist folders are at the same folder depth cmd+a -> right click -> Tags... -> "Artists" -> Enter.

![](http://i.imgur.com/blRldH4.png)

This will tag all your folders to be compatible with the workflow. I use [Hazel](http://www.noodlesoft.com/hazel.php) to automate this tagging process.

If you don't want to do tags this section will still work, Artist folders will just show up in Album searches and vice versa.

**To Listen Section**

`Under Construction`

This section is nowhere close to completed. The idea is to search a 'To Listen' folder for albums you want to listen to. It'd then add the albums to both iTunes and mpd+ncmpcpp. I haven't had time to work on this as I'm currently auditing my current music library and have deleted all albums from iTunes. Check back in the summer when I have more time to work on this kind of stuff.

***
```
  Not for commercial use

  Please share any improvements made to workflows
```