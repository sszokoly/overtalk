# overtalk
This module computes overtalk time in a stereo WAV file, which occurs when both channels carry audio event. In addition it also calculates total silence time, when none of the channels contained audio event, and total talk time for both channels.
It can also accept two mono WAV files.

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
3.00000001
```
## Requirements

- Python 3.x
- Auditok

## License

MIT, see: LICENSE.txt

## Author

Szabolcs Szokoly <a href="mailto:sszokoly@pm.me">sszokoly@pm.me</a>
