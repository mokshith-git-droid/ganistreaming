🎯 GANI PERSONAL HUB

Created by: Mokshith
A complete personal dashboard combining study materials and entertainment in one secure, PIN-protected application.

🌐 Live App

URL: https://ganistreaming.vercel.app
Default PIN: 2010

---

📖 ABOUT THIS PROJECT

Welcome to GANI Personal Hub - your all-in-one digital space for both study and entertainment. This application provides a secure, organized, and beautiful interface to access your personal collection of movies, music, study materials, and games.

🎯 Features:

· 🔒 PIN-protected access for privacy
· 🎬 Movie streaming with embedded players
· 📖 PDF viewer with download/print options
· 🎵 Music player with playlist support
· 🎮 4 browser games for entertainment
· 📱 Fully responsive design
· 🎨 Beautiful dark theme with orange accents
· ⚡ Fast loading with pure HTML/CSS/JS

---

📁 PROJECT STRUCTURE

```
gani-personal-hub/
├── 📄 index.html          # PIN entry screen
├── 📄 home.html           # Main dashboard
├── 📄 manager.json        # Content database
├── 📖 README.md
├── 📁 posters/           # ALL posters/thumbnails
│   ├── 🖼️ movies/
│   ├── 🖼️ music/
│   ├── 🖼️ pdfs/
│   └── 🖼️ games/
├── 📁 movies/
│   ├── 📄 movies.html     # Movie browser
│   └── 📄 player.html     # Movie player
├── 📁 pdfs/
│   ├── 📄 pdfs.html       # PDF browser
│   └── 📄 player.html     # PDF viewer
├── 📁 music/
│   ├── 📄 music.html      # Music browser
│   └── 📄 player.html     # Music player
└── 📁 games/
    ├── 📄 games.html      # Games browser
    ├── 📄 tictactoe.html
    ├── 📄 memory.html
    ├── 📄 snake.html
    └── 📄 quiz.html
```

---

🚀 QUICK SETUP GUIDE

1. Change Security PIN

Edit index.html and modify:

```javascript
const CORRECT_PIN = "2010"; // Change to your preferred 4-digit PIN
```

2. Update Content Database

Edit manager.json with your actual content information and URLs.

3. Upload Poster Images

Add your poster images to the posters/ folder in these subfolders:

· posters/movies/ - Movie posters
· posters/music/ - Album covers
· posters/pdfs/ - PDF thumbnails
· posters/games/ - Game screenshots

---

📚 COMPLETE CONTENT ADDING GUIDE

🎬 ADDING MOVIES

Option 1: Internet Archive (Recommended)

1. Go to archive.org/create
2. Upload your MP4 video file
3. Wait for processing to complete
4. On the video page, click "Share" → "Embed"
5. Copy the entire iframe code
6. Use in manager.json:

```json
{
  "movies": [
    {
      "id": 1,
      "title": "Your Movie Title",
      "description": "Movie description",
      "poster": "https://raw.githubusercontent.com/yourusername/repo/main/posters/movies/movie1.jpg",
      "videoUrl": "<iframe src='https://archive.org/embed/your-video-id' width='800' height='450' frameborder='0' allowfullscreen></iframe>",
      "genre": "Action",
      "year": "2024"
    }
  ]
}
```

Option 2: Google Drive

1. Upload MP4 to Google Drive
2. Right-click → "Share" → "Anyone with link"
3. Copy the share link
4. Convert to embed URL:
   · Change: https://drive.google.com/file/d/FILE_ID/view
   · To: https://drive.google.com/file/d/FILE_ID/preview
5. Use in videoUrl field

Option 3: OneDrive

1. Upload MP4 to OneDrive
2. Right-click → "Embed"
3. Copy the embed code
4. Use in videoUrl field

Option 4: Dropbox

1. Upload MP4 to Dropbox
2. Share → Create link
3. Change www.dropbox.com to dl.dropboxusercontent.com in the URL
4. Use direct link in videoUrl

---

📖 ADDING PDFs

Option 1: GitHub (Recommended)

1. Upload PDF files to your GitHub repo in a pdfs/ folder
2. Click the PDF file → "Raw" button
3. Copy the raw URL
4. Use in manager.json:

```json
{
  "pdfs": [
    {
      "id": 1,
      "title": "Mathematics Textbook",
      "description": "Complete math guide",
      "thumbnail": "https://raw.githubusercontent.com/yourusername/repo/main/posters/pdfs/math.jpg",
      "pdfUrl": "https://raw.githubusercontent.com/yourusername/repo/main/pdfs/mathematics.pdf",
      "category": "Education",
      "pages": "250"
    }
  ]
}
```

Option 2: Google Drive

1. Upload PDF to Google Drive
2. Share → "Anyone with link"
3. Copy the link
4. Convert to direct download:
   · Change: https://drive.google.com/file/d/FILE_ID/view
   · To: https://drive.google.com/uc?export=download&id=FILE_ID

Option 3: Dropbox

1. Upload PDF to Dropbox
2. Share → Copy link
3. Change the URL:
   · From: www.dropbox.com/s/FILE_ID/FILENAME.pdf?dl=0
   · To: dl.dropbox.com/s/FILE_ID/FILENAME.pdf?dl=1

Option 4: OneDrive

1. Upload PDF to OneDrive
2. Share → "Anyone with link"
3. Copy the link
4. Convert to direct download by adding ?download=1 to the URL

---

🎵 ADDING MUSIC

Option 1: GitHub (Recommended)

1. Upload MP3 files to your GitHub repo in a music/ folder
2. Click the MP3 file → "Raw" button
3. Copy the raw URL
4. Use in manager.json:

```json
{
  "music": [
    {
      "id": 1,
      "title": "Song Title",
      "artist": "Artist Name",
      "cover": "https://raw.githubusercontent.com/yourusername/repo/main/posters/music/cover.jpg",
      "audioUrl": "https://raw.githubusercontent.com/yourusername/repo/main/music/song.mp3",
      "genre": "Pop",
      "duration": "3:45"
    }
  ]
}
```

Option 2: Google Drive

1. Upload MP3 to Google Drive
2. Share → "Anyone with link"
3. Convert to direct download:
   · https://drive.google.com/uc?export=download&id=FILE_ID

Option 3: Dropbox

1. Upload MP3 to Dropbox
2. Share → Copy link
3. Change www.dropbox.com to dl.dropboxusercontent.com

Option 4: Internet Archive

1. Upload MP3 to archive.org/create
2. Get the direct file URL from the item page

---

🎮 GAMES COLLECTION

The hub includes 4 ready-to-play browser games:

1. Tic Tac Toe ⭕❌

· Classic X and O game
· Play against computer AI
· Score tracking

2. Memory Game 🎴

· Match pairs of cards
· Test your memory skills
· Move counter

3. Snake Game 🐍

· Classic snake gameplay
· Arrow key controls
· High score tracking

4. Quiz Game ❓

· 10 trivia questions
· Multiple choice answers
· Score system

---

🛠️ TECHNICAL DETAILS

Frontend Stack

· HTML5 - Structure and semantics
· CSS3 - Styling and animations
· JavaScript - Functionality and interactions
· No Frameworks - Pure vanilla code for maximum performance

Hosting & Storage

· Vercel - Application hosting (free tier)
· GitHub - Code repository and file storage
· Multiple CDNs - Support for various file hosting services

Security Features

· 🔒 PIN Protection - 4-digit code authentication
· 🚫 No User Data Collection - Complete privacy
· 💾 Local Processing - No external databases
· 🔐 Client-Side Only - No server-side vulnerabilities

Browser Compatibility

· ✅ Chrome (Recommended)
· ✅ Firefox
· ✅ Safari
· ✅ Edge
· ✅ Mobile Browsers (iOS/Android)

---

📱 MOBILE EXPERIENCE

The application is fully responsive and optimized for:

· 📱 Smartphones (iOS/Android)
· 💻 Tablets (iPad/Android tablets)
· 🖥️ Desktop Computers (All screen sizes)
· 📺 Smart TVs (Browser access)

---

🚀 DEPLOYMENT INSTRUCTIONS

Step 1: Prepare Your Content

1. Gather all your movies, PDFs, and music files
2. Create poster images for each item (300x400px recommended)
3. Upload files to your preferred hosting service

Step 2: Set Up GitHub Repository

1. Create a new GitHub repository
2. Upload all project files
3. Organize folders as shown in the structure above

Step 3: Deploy to Vercel

1. Go to vercel.com
2. Sign in with GitHub
3. Import your repository
4. Deploy with default settings
5. Your app will be live at your-app.vercel.app

Step 4: Custom Domain (Optional)

1. Buy a domain from any registrar
2. Add domain in Vercel project settings
3. Update DNS records as instructed
4. Your hub will be available at yourdomain.com

---

🔧 TROUBLESHOOTING

Common Issues & Solutions:

🔴 PIN not working

· Check browser console for errors (F12 → Console)
· Verify PIN is correctly set in index.html
· Clear browser cache and try again

🔴 Videos not playing

· Verify embed codes are correct
· Check if hosting service allows embedding
· Test URLs directly in browser

🔴 PDFs not loading

· Ensure PDF URLs are direct download links
· Check file permissions on hosting service
· Verify URLs work when pasted directly in browser

🔴 Music not playing

· Confirm audio URLs are direct links to MP3 files
· Check file size limits on hosting service
· Test audio URLs in browser audio player

🔴 Images not loading

· Verify image URLs are correct
· Check file paths in manager.json
· Ensure images are uploaded to correct folders

---

💡 PRO TIPS

Content Organization

· Use consistent naming for files
· Keep poster images under 500KB each
· Organize content by categories in manager.json
· Use descriptive titles and descriptions

Performance Optimization

· Compress images before uploading
· Use appropriate file formats (MP4 for video, MP3 for audio)
· Keep individual files under 100MB for better loading
· Use CDN URLs for faster delivery

User Experience

· Change PIN regularly for security
· Organize content logically in categories
· Use high-quality poster images
· Write clear descriptions for all content

---

📞 SUPPORT & CONTRIBUTION

Creator: Mokshith
GitHub: mokshith-git-droid
Live Demo: ganistreaming.vercel.app

Getting Help

1. Check the browser console for error messages
2. Verify all file paths and URLs are correct
3. Test individual components separately
4. Check network requests in Developer Tools

Feature Requests

This project is designed to be modular and extensible. You can easily add:

· New content types (videos, books, etc.)
· Additional games
· Custom themes
· Enhanced features

---

🎉 WELCOME MESSAGE

To the User:

Welcome to your personal digital sanctuary! 🏠

This application was created with the vision of providing you with a secure, private space where you can access all your study materials and entertainment in one beautifully organized interface.

What makes this special:

· 🛡️ Your Privacy First - No data collection, no tracking, just your content
· 🎨 Beautiful Design - Clean, dark theme that's easy on the eyes
· ⚡ Lightning Fast - No bloat, just pure performance
· 📱 Always Accessible - Works on any device, anywhere
· 🔒 Complete Control - You own and control all your content

How to get the most out of it:

1. Personalize - Change the PIN to something memorable
2. Organize - Add your content with clear titles and descriptions
3. Explore - Try all the features and games
4. Enjoy - This is your space, make it yours!

Whether you're studying for exams, relaxing with movies, or taking a break with games, this hub is designed to be your perfect companion. The interface is intuitive, the experience is seamless, and most importantly - everything stays private and secure.

Thank you for choosing GANI Personal Hub. May it serve you well in both your studies and leisure time! 📚🎬🎵

---

Built with care by Mokshith
🎯 Study Smart, Relax Better