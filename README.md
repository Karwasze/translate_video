# translate_video

## What is it?

This script uses OpenAI's [Whisper](https://github.com/openai/whisper) to generate English subtitles for a provided video. The video can be in English or any other supported language. It also merges subtitles and the provided video into a single .mp4 container.

## How do I use it

1. Upload the video which you want to translate into your Google Drive
1. Click the **Open in Colab** button on top of the ```translate_video.ipynb``` file
1. Run the first code block to mount your Google Drive 
1. Provide the path to your video in Parameters section
1. Run all code using Ctrl/Command + F9 (Runtime -> Run all)
1. Wait for the output (20 minute movie takes about 7 minutes to process), it will be uploaded to your Google Drive

## Why do I need Google Colab to run it?

Using whisper requires a powerful GPU to run at a reasonable speed. You could run this notebook locally, but the processing speed will be significantly lower if you don't have a dedicated GPU. You can also take a look at [Whisper.cpp](https://github.com/ggerganov/whisper.cpp) which should be faster than the default implementantion.

## How is this different than similar projects (e.g. https://freesubtitles.ai)?

1. I couldn't get [freesubtitles.ai](https://freesubtitles.ai) to run (it's overloaded most of the time)
1. When I translated a longer movie (1h 40m), I noticed that Whisper creates incorrect timestamps when there's a longer pause in dialogues. I'm using a slightly tweaked model (https://github.com/jianfch/stable-ts) to fix that.
1. This notebook can be run locally.
1. I'm using the biggest (large) model size by default.
1. This notebook leverages free Google Colab GPUs to run, you can buy Colab Pro to increase it's processing speed easily.

## Known issues

* Subtitles seem to dissapear only after a new sentence is spoken

## Examples

* https://streamable.com/w7wl6b
* https://streamable.com/0wz6re


