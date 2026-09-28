# neoscope

neoscope is a voice recorder and live audio analyzer. It is one HTML file. It uses no libraries and no network. It works fully offline.

The interface uses the neocamera layout. The area where the camera viewfinder would be shows the audio scopes from neoaudioscope.

## Features

- **Live scopes.** Spectrum, spectrogram, stereo goniometer with correlation bar, and L/R level meters.
- **Solo view.** Tap a scope to show it full size. Tap it again to go back to the grid.
- **Record.** Push the red shutter button to start. Push it again to stop. The file downloads immediately.
- **MIDI toggle (bottom right).** When MIDI is off, the app saves a WAV file. When MIDI is on (yellow fill), the app saves a ZIP file. The ZIP file contains the WAV file and a MIDI file. The MIDI file has the detected notes and an estimated tempo.
- **Gain toggle (bottom left).** Push to change the input gain: 0 dB, +10 dB, −10 dB. The gain changes the scopes and the recording.
- **Clip indicator.** CLIP comes on red when the signal gets to full scale. Tap it to reset it.
- **Layouts.** Portrait layout for phones. Landscape layout for wide screens, with the controls in a column on the right.

## Keyboard

| Key   | Action           |
|-------|------------------|
| Space | Start/stop recording |
| M     | MIDI on/off      |
| G     | Change gain      |

## Requirements

- A modern browser with microphone access.
- The app asks for microphone permission at start.
- Some browsers block the microphone on `file://` pages. If this occurs, serve the file over `https://` or `localhost`.

## Notes

- Recordings are 16-bit PCM WAV at the device sample rate. A mono input gives a mono file.
- MIDI detection works best with one note at a time (voice, whistle, a single instrument line).
- You cannot change the MIDI setting during a recording.
