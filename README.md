# Social Media Transcripts Extractor

## Overview

The **Social Media Transcripts Extractor** is a Python project that allows you to fetch and extract transcripts from social media platforms, specifically YouTube and Instagram. With this tool, you can retrieve video transcripts from YouTube channels or individual video links. While the project currently supports YouTube, it also has a placeholder for Instagram functionality, which can be extended in the future.

## Features

- Fetch transcripts from YouTube channels by providing the channel ID.
- Fetch transcripts from individual YouTube videos by providing the video link.
- Extract text from the obtained transcripts.
- Save transcripts and text transcripts as JSON files for further analysis.

## Getting Started

To get started with the **Social Media Transcripts Extractor**, follow these steps:

1. Clone the repository to your local machine.

2. Install the required Python libraries using pip:

   ```
   pip install streamlit youtubesearchpython
   ```

3. Run the Streamlit app:

   ```
   streamlit run your_app.py
   ```

4. Use the Streamlit interface to select the social media platform (currently supports YouTube) and input the required information.

5. Click the "Fetch Data" button to fetch and display transcripts.

## Usage

The project consists of two main components:

1. `YouTubeTranscriptExtractor`: This class provides methods to fetch short videos from a YouTube channel, retrieve transcripts for those videos, and extract text from the transcripts. It also includes a method to save the obtained data as JSON.

   ```python
   extractor = YouTubeTranscriptExtractor()
   short_videos = extractor.get_short_videos_from_channel(channel_id)
   transcripts = extractor.get_transcripts(short_videos)
   text_transcripts = extractor.extract_text_from_transcripts(transcripts)
   extractor.save_to_json(transcripts, 'transcripts.json')
   extractor.save_to_json(text_transcripts, 'text_transcripts.json')
   ```

2. Streamlit Interface: The Streamlit application provides a user-friendly interface for interacting with the YouTube transcript extraction functionality. Users can input a YouTube Channel ID or a video link, fetch data, and view transcripts.

## Example

Here is an example of how to use the **Social Media Transcripts Extractor** in your own Python script:

```python
if __name__ == "__main__":
    channel_id = "UCgkKA7xEOoBQNpC5TJxPLiw"
    extractor = YouTubeTranscriptExtractor()
    
    short_videos = extractor.get_short_videos_from_channel(channel_id)
    short_videos = short_videos[:10]
    transcripts = extractor.get_transcripts(short_videos)
    
    # Save transcripts to JSON
    extractor.save_to_json(transcripts, 'transcripts.json')
    
    # Extract text from transcripts
    text_transcripts = extractor.extract_text_from_transcripts(transcripts)
    
    # Save text transcripts to JSON
    extractor.save_to_json(text_transcripts, 'text_transcripts.json')
```

## Future Enhancements

The project has room for expansion and can be extended with the following enhancements:

- Complete the Instagram data collection functionality.
- Add support for more social media platforms.
- Implement more advanced text analysis and visualization features.
- Develop a web-based user interface for easier interaction.

Feel free to contribute to the project and make it even more versatile and useful!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

The **Social Media Transcripts Extractor** project was created by Aryan and is inspired by the need for extracting and analyzing social media transcripts for various purposes.

Enjoy using the tool, and happy coding!