# pc.jpg
import requests

# Cloud storage image URL
url = "YOUR_CLOUD_STORAGE_URL"  # Replace this with the actual image URL

# Send a request to download the image
response = requests.get(url)

# Check if the image download is successful
if response.status_code == 200:
    with open("Pc.jpg", "wb") as file:
        file.write(response.content)
    print("Image downloaded successfully.")
else:
    print("Failed to download the image.")
