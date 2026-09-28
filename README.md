# neoscope

**Version 1.1.1**

neoscope is a voice recorder and live audio analyzer. It is one HTML file. It uses no libraries and no network. It works fully offline.

The interface uses the neocamera layout. The area where the camera viewfinder would be shows the audio scopes from neoaudioscope.

## Features

- **Live scopes.** Spectrum, spectrogram, stereo goniometer with correlation bar, and L/R level meters.
- **Solo view.** Tap a scope to show it full size. Tap it again to go back to the grid.
- **Record.** Push the red shutter button to start. Push it again to stop. The file downloads immediately.
- **MIDI toggle (bottom right).** When MIDI is off, the app saves a WAV file. When MIDI is on (yellow fill), the app saves a ZIP file. The ZIP file contains the WAV file and a MIDI file. The MIDI file has the detected notes and an estimated tempo.
- **Lo Cut (bottom left).** Push to turn on the low-cut filter (yellow fill). The filter is a 12 dB/octave high-pass filter at 80 Hz. It changes the scopes and the recording. It is off at start.
- **Gain (top right).** Push to change the input gain: −24, −10, 0, +10, +24 dB. The gain changes the scopes and the recording. It is 0 dB at start.
- **Clip indicator.** CLIP comes on red when the signal gets to full scale. Tap it to reset it.
- **Layouts.** Portrait layout for phones. Landscape layout for wide screens, with the controls in a column on the right.

## Keyboard

| Key   | Action           |
|-------|------------------|
| Space | Start/stop recording |
| M     | MIDI on/off      |
| G     | Next gain step   |
| Shift+G | Previous gain step |
| L     | Lo Cut on/off    |

## Requirements

- A modern browser with microphone access.
- The app asks for microphone permission at start.
- Some browsers block the microphone on `file://` pages. If this occurs, serve the file over `https://` or `localhost`.

## Notes

- Recordings are 16-bit PCM WAV at the device sample rate. A mono input gives a mono file.
- MIDI detection works best with one note at a time (voice, whistle, a single instrument line).
- You cannot change the MIDI setting during a recording.
- A recording stops automatically at the WAV file size limit (4 GB, approximately 6 hours at 48 kHz). On phones, the memory limit of the browser can be lower than this.
