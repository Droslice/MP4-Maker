# Convert MP3s to a Single MP4 with Cover Image

This Python script merges multiple MP3 files in a folder into a single audio file and then converts it into an MP4 with a static cover image. This is useful for creating long audio compilations with a visual representation.

## Features
- Merges all MP3 files in a specified folder into a single file.
- Maintains the order of files based on filename sorting.
- Converts the merged MP3 into an MP4 with a custom cover image.
- Uses `pydub` for audio processing and `ffmpeg-python` for video encoding.

## Optional Description
This project is perfect for anyone looking to create **long-form audio content** with a **custom static image**, making it ideal for **podcasts, audiobooks, music compilations, and educational content**. Whether you want to publish content on YouTube or simply archive audio in a more engaging format, this script simplifies the process.

## Requirements
Ensure you have the following installed before running the script:

### Install Dependencies
```bash
pip install pydub ffmpeg-python
```

### Install FFmpeg
Make sure FFmpeg is installed on your system. You can download it from [FFmpeg Official Website](https://ffmpeg.org/download.html).

## Usage
1. **Place all your MP3 files** in a folder (e.g., `mp3_folder`).
2. **Add a cover image** (e.g., `cover.jpg`) in the same directory as the script.
3. **Run the script**:
   ```bash
   python merge_mp3_to_mp4.py
   ```

## How It Works
1. The script scans the `mp3_folder` for MP3 files and sorts them alphabetically.
2. It concatenates all MP3s into a single file called `merged_audio.mp3`.
3. It uses FFmpeg to convert `merged_audio.mp3` into `final_output.mp4` with `cover.jpg` as a static image.
4. The output is a video file with a still image and merged audio.

## File Structure Example
```
/project-folder/
│-- mp3_folder/
│   │-- track1.mp3
│   │-- track2.mp3
│   │-- track3.mp3
│-- cover.jpg
│-- merge_mp3_to_mp4.py
│-- README.md
```

## Output
- **Merged Audio:** `merged_audio.mp3`
- **Final Video:** `final_output.mp4`

## Customization
- **Change the Cover Image**: Replace `cover.jpg` with your desired image.
- **Modify Audio Quality**: Adjust the bitrate in `merged_audio.export(output_mp3, format="mp3", bitrate="192k")`.
- **Resize Cover Image**: Modify the FFmpeg `vf="scale=1280:720"` parameter to adjust video resolution.

## License
This project is open-source under the MIT License.

## Contributions
Feel free to submit pull requests or suggest improvements!

---
🚀 Enjoy your audio-to-video conversion!

