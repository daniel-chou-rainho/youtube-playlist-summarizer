# YouTube Playlist Transcript Summarizer

The YouTube Playlist Transcript Summarizer is a Python script designed to automatically generate summaries of YouTube video transcripts using OpenAI's GPT-4 model. This script provides a structured and organized way to convert and digest video content into text format.

## Features

1. **Video URL Extraction**: Extracts all video URLs from a specified YouTube playlist.

2. **Transcript Extraction**: Retrieves the English transcripts for each video. Tries different English language codes (en-GB, en-US, en) when the transcript isn't found. Lists videos without an English transcript separately.

3. **Command Prepending**: Prepends a markdown formatting guide to each transcript for the GPT-4 model.

4. **Prompt Checking**: Checks if the total token count for each command-transcript combination exceeds the limit for different versions of GPT models (GPT-3.5-turbo, GPT-3.5-turbo-16k, GPT-4, GPT-4-32k).

5. **Cost Calculation**: Calculates the estimated cost for processing each transcript with the GPT models based on the token count and model pricing.

6. **Text Generation**: Uses GPT-4 model to generate summaries for each transcript and saves them as individual text files. 

7. **Markdown to HTML to PDF Conversion**: Converts the markdown text into HTML, and then the HTML into a PDF, with each response placed on a separate page.

## Usage

1. Provide a YouTube playlist URL to the `get_video_urls()` function.
2. The script will automatically extract transcripts, check prompts, calculate costs, generate summaries, and finally convert the summaries to a PDF.

## Requirements

- Python 3.6 or higher
- openai
- youtube_transcript_api
- pytube
- collections
- re
- transformers
- tqdm
- os
- markdown
- weasyprint

Please install these dependencies using pip:

```shell
pip install openai youtube_transcript_api pytube transformers tqdm markdown weasyprint
```
