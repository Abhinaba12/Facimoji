# Facimoji
Machine Learning Project
![Screenshot (181)](https://user-images.githubusercontent.com/88977627/190387676-318bc39d-ef97-4e75-9d44-7cad19cd9bae.png)

Creating face emojis using Python can be a fun and educational exercise. There are several ways you can create or display face emojis using Python. Here, I will show you two different approaches:

Using Unicode characters:
You can simply print Unicode characters for various emojis.

1.Drawing custom face emojis using libraries like `PIL` (Pillow) or matplotlib:
This method involves creating and customizing face emojis by drawing them programmatically.

2.Method 1: Using Unicode Characters
This is the simplest method where you use Unicode strings to print emojis.

**python**
# Print some face emojis using their Unicode representations
print("\U0001F600")  # 😀 Grinning face
print("\U0001F601")  # 😁 Beaming face with smiling eyes
print("\U0001F602")  # 😂 Face with tears of joy
print("\U0001F603")  # 😃 Grinning face with big eyes
print("\U0001F604")  # 😄 Grinning face with smiling eyes
print("\U0001F605")  # 😅 Grinning face with sweat
print("\U0001F606")  # 😆 Grinning squinting face

Method 2: Drawing Custom Face Emojis with Pillow
Using the Pillow library, you can draw a simple face emoji.

First, ensure you have Pillow installed:
**base*
pip install pillow

**python**
from PIL import Image, ImageDraw

# Create a blank image with a white background
image = Image.new('RGB', (200, 200), 'white')
draw = ImageDraw.Draw(image)

# Draw the face (a yellow circle)
face_color = (255, 204, 0)
draw.ellipse((20, 20, 180, 180), fill=face_color, outline='black')

# Draw the eyes (two black circles)
eye_color = 'black'
draw.ellipse((60, 60, 80, 80), fill=eye_color)
draw.ellipse((120, 60, 140, 80), fill=eye_color)

# Draw the mouth (a black arc)
draw.arc((60, 100, 140, 160), start=0, end=180, fill='black', width=5)

# Save the image
image.save('smiling_face_emoji.png')

# Show the image
image.show()

This script creates a simple smiling face emoji and saves it as `smiling_face_emoji.png`. You can open and view this file to see the created emoji.
