# Video Files

This folder contains the background video files for the landing page.

## Required Files

### Primary Video
- **hero-background.mp4** - Main background video (required)
  - Format: MP4 with H.264 codec
  - Duration: 10-30 seconds
  - Resolution: 1280x720 or 1920x1080
  - File size: Under 25MB for GitHub

### Optional Files
- **hero-background.webm** - WebM format for better browser support
- **poster.jpg** - Video thumbnail/poster image

## Video Specifications

### Recommended Settings
- **Codec**: H.264 (MP4) or VP9 (WebM)
- **Frame Rate**: 24-30 fps
- **Bitrate**: 2-5 Mbps
- **Audio**: None (will be muted anyway)
- **Duration**: 15-20 seconds for seamless looping

### Compression Tips
Use FFmpeg to optimize your video:

```bash
# Compress for web (under 5MB)
ffmpeg -i input.mov -c:v libx264 -crf 28 -preset slow -s 1280x720 -r 24 -an output.mp4

# Create WebM version
ffmpeg -i input.mov -c:v libvpx-vp9 -crf 30 -s 1280x720 -r 24 -an output.webm
```

## Mobile Behavior
- Videos are automatically disabled on mobile devices
- Falls back to static background image
- Improves performance and saves bandwidth

## Upload Instructions
1. Drag your video file into this folder
2. Rename it to exactly: `hero-background.mp4`
3. Commit the changes
4. Your landing page will automatically use the new video

---

*The landing page will work with a fallback image if no video is uploaded.*
