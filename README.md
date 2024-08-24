# DMS-Colab-downloader
Here's an updated README that includes instructions specifically tailored for running the project in Google Colab:

---

## Overview

This project is a versatile tool for downloading and uploading files from various sources, including HTTP/HTTPS links, YouTube videos, and torrents. Designed to be run in Google Colab, it also offers features such as zipping and splitting files, and uploading them to the University of Moratuwa (UoM) Document Management System (DMS).

### Features

- **Download Manager:**
  - Download files from HTTP/HTTPS URLs with a progress bar.
  - Download YouTube videos in different resolutions with optional subtitles.
  - Download files from torrent magnet links.

- **File Management:**
  - Automatically create and manage a `downloads` directory for storing downloaded files.
  - Zip multiple files and split large zip files into smaller parts.
  - Combine split zip files back into a single archive.

- **Uploader:**
  - Upload files directly to UoM DMS with progress tracking.
  - Supports uploading multiple files and folders.

### Running the Project in Google Colab

To run this project in Google Colab, follow these steps:

1. **Open Google Colab:**
   - Go to [Google Colab](https://colab.research.google.com/) and open a new notebook.

2. **Install Required Libraries:**
   - Run the following cell to install the necessary Python libraries:
     ```python
     !pip install pycurl tqdm pytube libtorrent
     ```

3. **Copy the Project Code:**
   - Copy the code from the project's main script into a cell in your Colab notebook.

4. **Run the Code:**
   - Execute the cells as needed to download, manage, and upload files.
   - Example usage:
     ```python
     # Download a file from a URL
     download_normal("https://example.com/file.zip")
     
     # Download a YouTube video
     download_youtube_video("https://www.youtube.com/watch?v=dQw4w9WgXcQ")
     
     # Download a torrent file
     download_torrent("magnet:?xt=urn:btih:...")
     
     # Zip files and upload to DMS
     selected_files = handle_upload()
     upload_files(selected_files)
     ```

### Installation

All installations are done directly in Google Colab. Ensure that you install the necessary libraries at the beginning of your session:

```python
!pip install pycurl tqdm pytube libtorrent
```

### Usage

1. **Download Files:**
   - Download files from a URL:
     ```python
     download_normal("https://example.com/file.zip")
     ```
   - Download YouTube videos with optional subtitles:
     ```python
     download_youtube_video("https://www.youtube.com/watch?v=dQw4w9WgXcQ")
     ```
   - Download files using a torrent magnet link:
     ```python
     download_torrent("magnet:?xt=urn:btih:...")
     ```

2. **Manage Downloads:**
   - Zip files and folders into a single archive:
     ```python
     handle_zip()
     ```
   - Split large zip files into smaller parts:
     ```python
     # This is done automatically during the zipping process based on user input
     ```

3. **Upload Files:**
   - Upload files or folders to DMS:
     ```python
     selected_files = handle_upload()
     upload_files(selected_files)
     ```

### Configuration

- **Credentials:**
  The script requires UoM credentials to upload files to the DMS. These credentials are hardcoded for now:
  ```python
  username = 'your_username'
  password = 'your_password'
  ```
  It's recommended to update these values or use environment variables for better security.

### Error Handling

The tool includes basic error handling for network requests, file downloads, and uploads. In case of any errors, appropriate messages will be displayed to guide the user.

### Contributing

If you'd like to contribute to this project, please fork the repository, create a new branch, and submit a pull request. Contributions in the form of bug reports, feature requests, or code improvements are welcome.

### License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

### Contact

For any inquiries or support, feel free to reach out to the project maintainer at `your_email@example.com`.

---

This README should give users clear instructions on how to run your project in Google Colab, along with the necessary setup and usage details.
