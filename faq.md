# FAQ

## Why isn't it working?
There are a few prerequisites for the app to work. Make sure you've done the following:
 - Turn on "Device Broadcast Status" in your Spotify app settings.
 - Make sure you're on the same wifi as your bulbs.
 - Discover the bulbs you want to use (bottom left icon in Music Blitz).
 
Now play some music in Spotify. You should see a drawer notification showing either "Getting song data" or "Running light show".
If you see the message "Unable to get song data", look below for troubleshooting info.

If you don't see any notifications, make sure Music Blitz is enabled (the light bulb on the main screen in the top left corner should be 
"on", not crossed out; tap it to toggle). Sometimes Android can be slow about delivering messages between apps, but if
been playing your song for more than 30s and have checked everything about, something really odd is happening, so please 
send me an email.

## Why do I see "Unable to get song data"?
Music Blitz shows this notification when it knows you're playing a song, but isn't able to get data from Spotify for it.
Most often the reason is that the Spotify login information has expired in Music Blitz. Open the app and allow the "loading"
notification to complete. Of course, if you don't have an internet connection, then it won't be able to get song data, so make sure
you're online.

Occasionally, a song doesn't have information available. Unfortunately, there's not much to do in this situation. In the future, 
I might have the app take a default behavior to perform some random light flashes just to keep things going, but right now it doesn't.

## Why's the interface so basic?
I was going for a minimalist thing. 

## What do all these settings mean?
Check on the [settings](settings.md) page for more info.

## Why does Music Blitz only work with Spotify?
Spotify has some awesome data available that makes it a lot easier to create a good light show. Using the microphone, like the default app
and some others, is not as effective. I have some ideas how I might go about creating an app that works with other music you play on
your phone, but while it would use ideas from Music Blitz, if I ever get to it, it'll likely be a separate app entirely.

## I have an idea. Can you implement it?
You can post feature requests to the project's [Github issue page](https://github.com/saites/music-blitz/issues).

## The app crashed. What should I do?
First of all, sorry! I try my best to test everything, but sometimes setups don't go as expected. If you're able, please please please 
send a crash report through Android. It makes it ten million times easier. If you're not able or willing to do that, please send me an
email or file an issue on the [Github issue page](https://github.com/saites/music-blitz/issues) and I will look into it.

## I love the app. How can I help you?
Thanks! If you like the app, please leave a favorable review on [Google Play](https://play.google.com/store/apps/details?id=com.saites.spotlight) and tell all of your friends who are also in the intersection of Lifx, Android, and Spotify users :).
