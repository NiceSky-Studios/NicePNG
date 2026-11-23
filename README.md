# NicePNG

NicePNG is a small native PNGTuber app written in Swift/AppKit. It listens to your microphone and swaps
between an idle image and a talking image, with a bounce while you speak.

## Requirements
- macOS 12 or late

## Using it
- Right-click the avatar (or press Cmd+,) for Settings.
- Load your PNGs: File menu, Settings, or drag files onto the window
  (one file = idle, two files = idle + talking). With no images loaded, a built-in blob avatar is used.
  If you only load an idle image, the avatar just bounces when you talk.
- Watch the Mic Level bar while talking and set Threshold just below its peak.
- "Reduce background noise" (on by default) filters the mic to the speech range, learns your room's
  steady noise level (fans, hum, hiss) and ignores very short sounds like keystrokes. With it on, the
  meter shows how far you are above that background noise. Turn it off for plain loudness.
- For OBS: pick Chroma Green/Blue and add a Chroma Key filter, or use Window Capture with the
  Transparent background. Enable "Clean window" to hide the window buttons and shadow.
  Drag the avatar itself to move the window.

## Notes
- The app is ad-hoc signed, so macOS may ask for microphone permission again after a rebuild.
  If it gets stuck: `tccutil reset Microphone com.example.nicepng`
- Change the app name or bundle ID at the top of `build.sh`.

# Installation
1. Visit the [NicePNG Releases page](https://github.com/NiceSky-Studios/NicePNG/releases).
2. Download the latest DMG.
3. Move NicePNG to your Applications and open it.
4. Grant it the permissions asked for.
