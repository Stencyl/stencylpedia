# Sound & Images > Sound

***

> Read our [Sounds](http://www.stencyl.com/help/view/playing-sounds-and-music/) article for an explanation of these blocks.

***

## Playback

### [Play/Loop] Sound

![play-sound-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/play-sound4.png)

Plays (or loops) the chosen sound on the next available channel.

```
playSound([SOUND]);
loopSound([SOUND]);
```

***

### Stop all Sounds

![stop-sounds-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/stop-sounds.png)

Immediately stops playback of all sounds.

```
stopAllSounds();
```

***

## Volume

### Set Volume

![set-volume-sound-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/set-volume.png)

Sets the global sound volume level. Individual channels maintain their own volume level, which is multiplied against the global volume level. Specify a value between [0-100] inclusive.

```
setVolumeForAllSounds([NUMBER]/100);
```

***

### Fade [In/Out]

![fade-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/fade-sounds.png)

Fades the global sound volume level in (to 100%) or out (to 0%) over time, given in seconds.

```
fadeInForAllSounds([NUMBER]);
fadeOutForAllSounds([NUMBER]);
```

***

## Channels

### [Play/Loop] on Channel

![play-channel-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/play-sound-channel.png)

Plays (or loops) a sound on the specified channel. If one was previously playing on the channel, it stops and gets replaced.

```
playSoundOnChannel([SOUND], [NUMBER]);
loopSoundOnChannel([SOUND], [NUMBER]);
```

***

### [Stop/Pause/Resume] on Channel

![stop-channel-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/control-sound-channel.png)

Controls playback of a sound on the specified channel (if one is playing). Stopping a sound and resuming will force it start from the beginning.

```
stopSoundOnChannel([NUMBER]);
pauseSoundOnChannel([NUMBER]);
resumeSoundOnChannel([NUMBER]);
```

***

### Set Volume on Channel

![volume-channel-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/set-volume-channel.png)

Sets the volume level for the specified channel, which is multiplied against the global volume level. Specify a value between [0-100] inclusive.

```
setVolumeForChannel([NUMBER]/100, [NUMBER]);
```

***

### [Fade In / Fade Out] on Channel

![fade-channel-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/fade-sound-channel.png)

Fades the sound volume level for the specified channel in (to 100%) or out (to 0%) over time. Duration is given in seconds.

```
fadeInSoundOnChannel([NUMBER], [NUMBER]);
fadeOutSoundOnChannel([NUMBER], [NUMBER]);
```

***

### Sound Position on Channel

![sound-position-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/get-position-channel.png)

Returns the current playback position of the sound on the specified channel in milliseconds.

```
getPositionForChannel([NUMBER])
```

***

### Length of Track on Channel

![length-channel-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/get-length-channel.png)

Returns the length of the sound on the specified channel in milliseconds.

```
getSoundLengthForChannel([NUMBER])
```

***

### Length of Sound

![length-sound-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/get-length-sound.png)

Returns the length of the specified sound in milliseconds.

```
getSoundLength([SOUND])
```

***

### Get Sound with Name

![get-sound-by-name-block](http://static.stencyl.com/pedia2/block-images/6%20-%20Sound%20%20Images/0%20-%20Sound/text-to-sound.png)

Returns a sound, given its name. 

```
getSoundByName([TEXT])
```

***
