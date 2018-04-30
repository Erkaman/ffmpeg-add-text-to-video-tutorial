# Adding Text to a Video File with ffmpeg

By burning text subtitles into a video, we can use ffmpeg as a quick and dirty way
of adding text to a video. Let us say we want to add text to the video `original.mp4`, which
is rendered a `.gif` below

![Animated](gifs/original.gif)

Then we simply specify a subtitle file of the format `.ass`(Advanced Substation Alpha), 
and feed it to ffmpeg as follows:

```
ffmpeg -y -i original.mp4 -vf subtitles=text.ass original_with_subs.mp4
```

and this gives us a video with text added:

![Animated](gifs/original_with_subs.gif)

The file `text.ass` can be found in the repo, and it contains explanatory comments. The
specification of the subtitle format can be found [here](https://www.matroska.org/technical/specs/subtitles/ssa.html).

