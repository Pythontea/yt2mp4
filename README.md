from pytube import YouTube

# Set the URL of the video you want to download
url = input(">>>Pass the Link<<<")

# Create a YouTube object with the URL
yt = YouTube(url)

# Get the highest resolution available
video = yt.streams.filter(progressive=True, file_extension='mp4').order_by('resolution').desc().first()

# Download the video
video.download("/Users/mac/Mk4")

