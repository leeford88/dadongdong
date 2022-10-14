


Hello , World


- 👋 Hi, I’m 大东东@leeford88
- 👀 I’m interested in nagix doker git python...
- 🌱 I’m currently learning git...
- 💞️ I’m looking to collaborate on doctor...
- 📫 How to reach me is http://localhost:55000...

<!---
leeford88/leeford88 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->import cv2
import numpy as np
import pickle
import pyaudio
import struct
import math
import argparse
import os
def read_frames(file, video_folder):
frames = []
cap = cv2.VideoCapture(os.path.join('videos', video_folder, file))
frame_rate = cap.get(cv2.CAP_PROP_FPS)
if not cap.isOpened():
print("Error opening video file")
while cap.isOpened():
ret, frame = cap.read()
if ret:
frames.append(frame)
else:
break
cap.release()
return frames, frame_rate
frames, frame_rate = read_frames('normal.mov', 'bill_gates')

def next_frame_index(i, reverse):
if i == len(frames) - 1:
reverse = True
if i == 0:
reverse = False
if not reverse:
i += 1
else:
i -= 1
return i, reverse

