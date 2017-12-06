# Settings
Music Blitz has several different settings that customize how the lights react to the music you're playing.
Most of the settings take effect immediately, but a few require the music to be reprocessed, which requires pausing/unpausing your
song, switching to a different song, or restarting the song (all of these will cause the song to be re-evaluated).

## Notifications

### Show Notifications
This option turns on/off drawer notifications that show up when getting music data or running a light show. 
If a notification is currently displayed, you may have to pause and unpause your music for the notification to go away.
Error notifications may still be shown.

## Light Colors 
These options influence when in the music the light pulses and what color they use.

### Beat Detection
Beat Detection is the “when” part of the equation. The different options change which part of the music Music Blitz pays attention to when choosing to send a pulse. Since these options require extra processing to set up, you’ll have to pause and unpause your music for this change to take effect, or wait for the next song to start.

#### Dynamic
In Dynamic mode, lights are flashed based on relatively constant chunks of sound in the music. This mode adjusts the length of the flash based on how long the chunk is.

#### Beats And Bars
This is the original Music Blitz mode. In this mode, Music Blitz flashes the lights rhythmically based on a guess of the beat of the music.
##### Use Beat Thresholds
Some songs technically have a high tempo, but don't really "feel" intense. This option automatically tones down the flashing for music that fits this description. When turned on, if the song’s Energy or Danceability is less than the minimum on the sliders, Music Blitz only flashes beats that are also predicted as bar markers.
##### Energy Min
The required minimum “energy” for a song in order for it to flash
##### Dance Min
The required minimum “danceability” for a song in order for it to flash

#### Frequency 
This mode flashes the lights when impulses match the specified frequency band(s). There are 8 frequency bands, ranked low (Band 1) to high (Band 8).
##### Use unique frequency bands
When turned on, you can choose a different frequency band on a bulb-by-bulb basis. When turned off, pulsing is determined by the Default Frequency Band, and the flashed bulbs are determined by your sync settings.
##### Default Frequency Band
This is the frequency band used for all bulbs if the above option is turned on.
##### Frequency Bands
This list shows the frequency band selected for each bulb. If you turn on `Use unique frequency bands`, then you can change these values, and when an impulse on the band is detected, any bulb with that band will flash.

### Color Mode
This setting affects how Music Blitz determines which color to set the bulb. When you change these options, you should see the effect right away.

#### Timbre
In timbre mode, the color color is based on sound variations within the song; if the sounds are more similar, the color is more similar. This option is currently the most hand-wavy. In the future, I want to support “intrasong variation” (in which a song should use more colors, but its colors have no relation to other songs’ colors) and “intersong variation” (in which two songs that sound similar should have similar colors, at the expense of the song itself using fewer colors).

#### Pairs
This mode chooses a color among a list of colors, based on whether the current sound is likely a bar marker (that is, the first beat in a musical bar). 

### Color Pairs
This is the list of colors it uses. It rotates through the list over time, based on major variations in the music’s sound.

#### Pitches
This color mode chooses the color based on beat’s pitch relative the root key of the music. You select colors for each of the 12 pitches. So, if the song is in the key of C, then Pitch 1 is C, Pitch 2 is C#, Pitch 3 is D, etc.
##### Pitch Colors
This is the color to use for each pitch; pitches are relatively the root key of the music.

#### Static
This color mode choose a color on a bulb-by-bulb basis
##### Static Colors
These are the colors that bulb should use when in static mode.

### Color Temperature
This is the Lifx color temperature, just like what you can set through the Lifx app.

### Saturation
This is the color saturation. When turned all the way up, the color is fully saturation; all the way down, the lights appear white (in which case the color temperature is much more apparent).

### Timing offset
This option attempts to align the peak of the bulb’s flash with the predicted peak loudness of the music playing at the time of flashing. Most of the time, it should make the lights feel more in time with the music. When its turned off, the flashes start with the predicted beat impulse, so if the blink length is long, it might appear behind the music by several tens of miliseconds. For `Beats and Bars` and `Frequency` modes, that means the entire wave is shifted to start earlier, so its peak will match the impulse of the music. For `Dyanmic` mode, the wave starts with the beginning of the musical section and its peak is aligned to the loudest part of the section (as a result, `Party` and `Chill` Pulse modes aren't used if this option is on).

## Intensity
These options determines what a specific flash looks like, independent of its color.

### Pulse Mode
This is the waveform for the light flash. Note that `Party` and `Chill` are ignored if you're using `Dynamic` beat detection with `Timing Offsets` turned on.

#### Party
 This mode biases the peak light intensity towards the beginning of the waveform.
#### Chill
 This mode biases the peak light intensity towards the end of the waveform.
#### Balanced
 This mode places the peak light intensity in the middle of the waveform.
#### Super Chill 
 This mode linearly interpolates directly to the new brightness and color, rather than peaking at any specific point.

### Blink Length
 This is how long the flash lasts, but depends on the Beat Detection. In `Beats and Bars` mode, pulses last longer because pulses are farther apart in time, and less likely to interfer with on another. In `Frequency Mode`, there are a lot more "hits", so pulses are automatically shortened, but still based on this value. In `Dynamic Mode`, pulse lengths depend on the length of the musical section.
 
### Brightness
These values are the minimum and maximum brightness levels the lights will take. The minimum brightness is used as a baseline for the 
bulbs. When beats are detected, it flashes the lights based on how loud the current sound is relative the rest of the song, up to the 
maximum brightness value.

### Loudness Sensitivity
This affects how much the loudness of the sound affects the brightness of the flash. When the sensitivity is higher, quieter sounds 
are much dimmer, so sounds have to be a lot louder before reaching at or near the maximum brightness; when the sensitivity is lower,
brightness variation is less apparent, with most sounds causing the lights to flash close to their maximum brightness.

## Synchronization
When Music Blitz detects a beat, this option changes which of the bulbs should show it.

### Sync Mode
#### One Bulb Per Group
Flashes one bulb in each group on each beat
#### Treat Group As One
Flashes all the bulbs in a single group, and rotates among groups
#### Only One of Enabled
Flashes only one bulb of all the enabled bulbs
#### Use All Enabled
Uses all the bulbs for every beat

## Spotify
### Log out of Spotify 
Logs Music Blitz out of your Spotify account; however, Music Blitz attempts to login each time it’s opened, since Spotify access is necessary for it to function. You must use Spotify to disconnect Music Blitz from your account entirely
