# GANI STREAMING SERVICES

Personal streaming app with PIN protection and subtitle support.

## Features
- PIN: 2010
- HTML5 video player with SRT subtitle support
- OneDrive direct MP4 links
- Netflix-like UI
- Continue watching (coming soon)

## Setup
1. Edit `movies.json` with your movie data
2. Upload MP4 files to OneDrive and get direct links
3. Upload SRT files to OneDrive for subtitles
4. Update `movies.json` with your URLs
5. Deploy to Netlify/Vercel

## Movie Format in movies.json
```json
{
  "id": 1,
  "title": "Movie Name",
  "description": "Movie description",
  "poster": "https://poster-image-url",
  "videoUrl": "https://direct-onedrive-mp4-link",
  "subtitleUrl": "https://direct-onedrive-srt-link",
  "genre": "Available Movies"
}