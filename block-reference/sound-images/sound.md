# Sounds > Sounds

***

> Read our [Sounds](https://www.stencyl.com/help/view/playing-sounds-and-music/) article for an explanation of these blocks.

***

## Playback

### <a name="play-sound4"></a> Play / Loop Sound

![play sound](https://static.stencyl.com/pedia2/block-images/sound-images/sound/play-sound4.png)

Plays (or loops) the chosen sound on the next available channel.

```
playSound([SOUND]);
loopSound([SOUND]);
```

***

### <a name="stop-sounds"></a> Stop all Sounds

![stop all sounds](https://static.stencyl.com/pedia2/block-images/sound-images/sound/stop-sounds.png)

Immediately stops playback of all sounds.

```
stopAllSounds();
```

***

## Volume

### <a name="set-volume"></a> Set Volume

![set volume to number %](https://static.stencyl.com/pedia2/block-images/sound-images/sound/set-volume.png)

Sets the global sound volume level. Individual channels maintain their own volume level, which is multiplied against the global volume level. Specify a value between [0-100] inclusive.

```
setVolumeForAllSounds([NUMBER]/100);
```

***

### <a name="fade-sounds"></a> Fade Volume In / Out

![fade in over number secs](https://static.stencyl.com/pedia2/block-images/sound-images/sound/fade-sounds.png)

Fades the global sound volume level in (to 100%) or out (to 0%) over time, given in seconds.

```
fadeInForAllSounds([NUMBER]);
fadeOutForAllSounds([NUMBER]);
```

***

### <a name="fade-sounds-percent"></a> Fade Volume to Percent

![fade to number % over number secs](https://static.stencyl.com/pedia2/block-images/sound-images/sound/fade-sounds-percent.png)

Fades global volume to the given percent.

```
fadeForAllSounds([NUMBER], [NUMBER]);
```

***

## Channels

### <a name="play-sound-channel"></a> Play / Loop Sound on Channel

![play sound on channel int](https://static.stencyl.com/pedia2/block-images/sound-images/sound/play-sound-channel.png)

Plays (or loops) a sound on the specified channel. If one was previously playing on the channel, it stops and gets replaced.

```
playSoundOnChannel([SOUND], [INT]);
loopSoundOnChannel([SOUND], [INT]);
```

***

### <a name="control-sound-channel"></a> Stop / Pause / Resume Sound on Channel

![stop sound on channel int](https://static.stencyl.com/pedia2/block-images/sound-images/sound/control-sound-channel.png)

Controls playback of a sound on the specified channel (if one is playing). Stopping a sound and resuming will force it start from the beginning.

```
stopSoundOnChannel([INT]);
pauseSoundOnChannel([INT]);
resumeSoundOnChannel([INT]);
```

***

### <a name="set-volume-channel"></a> Set Volume on Channel

![set volume to number % for channel int](https://static.stencyl.com/pedia2/block-images/sound-images/sound/set-volume-channel.png)

Sets the volume level for the specified channel, which is multiplied against the global volume level. Specify a value between [0-100] inclusive.

```
setVolumeForChannel([NUMBER]/100, [INT]);
```

***

### <a name="fade-sound-channel"></a> Fade Volume In / Out on Channel

![fade in sound on channel int over number secs](https://static.stencyl.com/pedia2/block-images/sound-images/sound/fade-sound-channel.png)

Fades the sound volume level for the specified channel in (to 100%) or out (to 0%) over time. Duration is given in seconds.

```
fadeInSoundOnChannel([INT], [NUMBER]);
fadeOutSoundOnChannel([INT], [NUMBER]);
```

***

### <a name="fade-sound-channel-percent"></a> Fade Volume to Percent on Channel

![fade sound to number % on channel int over number secs](https://static.stencyl.com/pedia2/block-images/sound-images/sound/fade-sound-channel-percent.png)

Fades channel volume to the given percent.

```
fadeSoundOnChannel([INT], [NUMBER], [NUMBER]);
```

***

### <a name="set-panning-channel"></a> Set Panning on Channel

![set panning to number % for channel int](https://static.stencyl.com/pedia2/block-images/sound-images/sound/set-panning-channel.png)

Sets the panning of a channel (negative 100% is far left, positive 100% is far right).

```
setPanningForChannel([NUMBER]/100, [INT]);
```

***

### <a name="set-position-channel"></a> Set Position on Channel

![set position for channel int to int](https://static.stencyl.com/pedia2/block-images/sound-images/sound/set-position-channel.png)

Set position for sound on a specific channel in milliseconds.

```
setPositionForChannel([INT], [INT]);
```

***

### <a name="get-position-channel"></a> Sound Position on Channel

![get position for channel int](https://static.stencyl.com/pedia2/block-images/sound-images/sound/get-position-channel.png)

Returns the current playback position of the sound on the specified channel in milliseconds.

```
getPositionForChannel([INT])
```

***

### <a name="get-length-channel"></a> Length of Track on Channel

![get length for channel int](https://static.stencyl.com/pedia2/block-images/sound-images/sound/get-length-channel.png)

Returns the length of the sound on the specified channel in milliseconds.

```
getSoundLengthForChannel([INT])
```

***

### <a name="get-length-sound"></a> Length of Sound

![get length for sound](https://static.stencyl.com/pedia2/block-images/sound-images/sound/get-length-sound.png)

Returns the length of the specified sound in milliseconds.

```
getSoundLength([SOUND])
```

***

### <a name="text-to-sound"></a> Get Sound with Name

![sound with name text](https://static.stencyl.com/pedia2/block-images/sound-images/sound/text-to-sound.png)

Returns a sound, given its name. 

```
getSoundByName([TEXT])
```

***
