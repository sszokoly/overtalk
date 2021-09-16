# overtalk
<<<<<<< HEAD
This module computes total overtalk time in seconds in a stereo WAV file, which occurs when both channels carry audio event. In addition, it also calculates total silence time, when none of the channels contain audio event and total talk time for both channels, when audio event was detected. It can also accept two mono WAV files. Consult https://auditok.readthedocs.io for supported keyword arguments. This is meant to analyze audio files of phone conversations, when one channel has the caller audio and the other has the callee audio.
=======
This module computes total overtalk time in seconds in a stereo WAV file, which occurs when both channels carry audio event. In addition it also calculates total silence time, when none of the channels contain audio event, and total talk time for both channels. It can also accept two mono WAV files. Consult https://auditok.readthedocs.io for supported arguments.
>>>>>>> 1e53febb807d91e9417300f6e20646c6b25c1e5b

### example ###
```
>>> from overtalk import Overtalk
>>> overtalk = Overtalk(
        energy_threshold=50,
        analysis_window=0.1,
        min_dur=0.2,
        max_dur=10,
        max_silence=0.2
    )
>>> overtalk.load("sample.wav")
>>> print(overtalk.overtalk)
3.25
```
## Requirements

- Python 3.x
- Auditok

## License

MIT, see: LICENSE.txt

## Author

Szabolcs Szokoly <a href="mailto:sszokoly@pm.me">sszokoly@pm.me</a>
