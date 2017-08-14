# Kash's Plan of Attack

## High Level

* Detect that music is playing
* Record a couple of seconds
* Identify song based on recording
* Look up album artwork based on identified song
* Find the primary and secondary album artwork color
* Light up LEDs based on on the two colors

## Breakdown

### Detect that music is playing
* Notice a spike in noice?
* Continuously record and sample?
* Non-automatic/activate myself?

### Record a couple of seconds
* PyAudio to record 3 second sample then send to detection server
* Use arduino or raspi?

### Identify song based on recording
* Set up detection api endpoint that accepts a stream of music and identifies music
* Dejavu seems like a good tool to identify, but requires I have samples of songs to match against
* Could use Discogs API to know my library and download songs automatically
* Would have to set up something that monitors my library and adds new content when the library is updated

### Look up album artwork based on identified song
* Looks like Discogs has a good api for this as well. Tying into that with the library management could be good
* Last.fm has an API it appears
* Amazon may have an API as well

### Find the primary and secondary album artwork color
![iTunes 11 Album Design](http://www.abhinayashutosh.com/blog/wp-content/uploads/2013/01/iTunes-11-Album-Details-1024x634.png)
* This could be the most difficult part of the project. It looks like there are some open source projects that do work similar to iTunes 11 (which is what we're going for)
* [Blog About iTunes 11](https://panic.com/blog/itunes-11-and-colors/)
* [Japanese Blog](http://fladdict.net/blog/2012/11/itunes11_colorpicker.html)
* [Stackoverflow Answer](https://stackoverflow.com/questions/13637892/how-does-the-algorithm-to-color-the-song-list-in-itunes-11-work/13675803#13675803)


### Light up LEDs based on on the two colors
* I think this should be fairly easy if we get the right type of LED strips that are programable
