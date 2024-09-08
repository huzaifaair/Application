# Application
Applications develop through C# .Net Framework
Application Overview: EMP Media Player

Introduction: EMP (Entertainment Media Player) is a desktop application developed using C# designed to allow users to play and manage their multimedia files offline. EMP is similar to VLC Media Player in functionality, offering support for various media formats with an intuitive and user-friendly interface. The application focuses on simplicity and flexibility, enabling users to create and manage playlists, control playback, and enjoy media offline. It stores user-created playlists in both JSON and TXT formats for easy access and management without the need for a complex database.

Key Features:
Media Playback:

EMP supports multiple audio and video formats, allowing users to enjoy their media files without worrying about compatibility.
Basic playback controls such as play, pause, stop, fast-forward, and rewind are easily accessible.
Playlist Management:

Users can create, edit, and delete playlists.
Playlists are stored in JSON and TXT formats, making them easy to access, modify, and transfer between devices.
Playlists include detailed information about media files such as titles, file paths, durations, and formats.
User-Friendly Interface:

EMP is designed with simplicity in mind, offering a clean and intuitive interface that users can navigate with ease.
The layout ensures that essential functions are easily reachable, promoting a seamless experience.
Customization:

Users can customize their playback preferences, including volume, subtitles (if available), and playback speed.
EMP allows the personalization of media libraries and playlists, enabling users to curate their own collections.
File-Based Storage:

Instead of using a traditional database, EMP stores user data such as playlists in JSON and TXT formats. This lightweight storage approach simplifies the application while allowing flexibility in managing user data.
Offline Functionality:

EMP is a completely offline application, making it ideal for users who prefer to play media locally without requiring an internet connection or cloud storage.
Technical Architecture:
Language: C#
Storage: Playlists and media metadata are stored in JSON and TXT files.
Playback Library: The application uses a C# media library (such as NAudio or similar) to handle playback of various media formats.
UI Framework: Windows Forms or WPF (depending on implementation), providing a desktop user interface for interaction.
User Roles and Rights:
Since EMP is an offline, file-based media player, the application doesn't require complex user roles or access rights. However, two basic user levels may exist:

Default User:
Can play, pause, stop, and rewind media.
Can add, remove, and organize media files in playlists.
Can customize personal playback settings.
Guest (Optional):
Can only play media files but has limited access to creating or modifying playlists and settings.
File Management:
JSON Playlist Storage:

Playlists are saved in JSON format, allowing for structured and detailed storage of media file information. Each playlist contains an array of media items with attributes like title, duration, file path, and format.
Example JSON Structure:

json
Copy code
{
  "playlistId": 1,
  "name": "My Favorite Playlist",
  "mediaItems": [
    {
      "mediaId": 101,
      "title": "Song 1",
      "filePath": "C:/Music/song1.mp3",
      "duration": "3:45",
      "format": "MP3"
    }
  ]
}
TXT Media Storage:

Media items can also be stored in TXT files, with each file containing key-value pairs representing media attributes.
Example TXT Structure:

makefile
Copy code
MediaID: 101
Title: Song 1
FilePath: C:/Music/song1.mp3
Duration: 3:45
Format: MP3
Connectivity and Data Handling:
Since the application is offline and uses file-based storage:

Reading Data: EMP reads playlists from JSON or TXT files by deserializing them into C# objects using libraries like Newtonsoft.Json for JSON.
Writing Data: When users create or modify playlists, the application serializes the data back into JSON or writes it as a TXT file.
This file-based storage approach eliminates the need for a traditional database and allows users to easily transfer their playlists between different devices.
Potential Enhancements:
Advanced Media Features:
Support for subtitles, multiple audio tracks, and more advanced media controls such as looping and shuffling.
Playlist Sharing:
Although the app is offline, users could potentially export their JSON or TXT playlists to share with others or transfer between devices.
Customization and Skins:
Allow users to customize the look and feel of the media player with skins, themes, or layout changes.
Conclusion:
EMP Media Player offers a powerful, offline solution for users looking to manage and play their media files with ease. Its use of JSON and TXT for storage provides a lightweight and flexible approach, while the user-friendly interface makes it accessible to all types of users. Future development could expand upon its current features to include more advanced media playback options and personalization, enhancing the user experience even further.







