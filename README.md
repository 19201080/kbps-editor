### **[KBPS](http://et-nd.co/works/kbps/) EDITOR**  ###
An editor to create, edit, and export augmented music from .wav files.

----------

### Context ###
When creating [kbps](http://et-nd.co/works/kbps/), i faced the need to build an editor so as to prototype songs in the format i had created. This format blends music (two audio tracks) with electrical power (four power tracks). When the music is played on the player, it can be heard on speakers and felt through domestic appliances ([video](https://vimeo.com/210164088)). I started with existing songs in wave format, but needed an editor to listen to the music and edit it, a bit like a DAW. The editor also needed to export the output file so that it could be played on the player without any additional step.
<br>
### Problem ###
In a previous prototype, i used openFrameworks to build the editor and the player as well, but this solution was super heavy and the raspberry pi couldn’t handle long songs. Thus, i switched to pure data to build a lightweight player the rpi could easily work with.
<br>
The output i gave the rpi was a puredata patch, along with a music file and four files (one for every power track). The editor had to control various file formats. I could have built it in pure data, but i chose not to, as its interface is quite arid and i needed to spend some time working within the editor.
<br>
### Solution ###
I decided to use max. It is quite versatile, and the new (v7) interface was easy on the eyes. I didn’t put any work on the aesthetic aspect of the editor, as it is a purely functional tool i built for myself. Basically, it is a timeline interface. The first two timelines are the stereo tracks of the music file, while the four other ones are the power tracks. The music can be played, paused, etc. like in a regular daw. The power tracks can be edited live with a keyboard or controller while the music plays, but they can also be edited with the mouse for finer control.
<br>
When the file is ready, you can save the music, power tracks, and pd patch in a folder. Put this folder in a usb drive, plug it in the player, and it works.
<br>
#### Improvements ####
There are little switches in the editor to get a preview of the effect while playing back the music. But to get a better look, I would often arrange a quick setup with the player and a few lamps, ssh into the player, transfer the output from the editor, and play it there. So the first improvement would be to program a wireless mode in the editor itself to directly connect the editor to the player and have a real-life feedback while composing. The second improvement would be to transform the editor from a max patch to a max for live plugin (easier on the eyes, and with a smoother learning curve for the friends I later shared the editor with).
<br>
