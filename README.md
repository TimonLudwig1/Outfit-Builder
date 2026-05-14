# Outfit Builder (Desktop App)

A simple Python desktop application that allows users to upload clothing images (tops, pants, shoes), remove their backgrounds, and generate a combined outfit preview.

---

## Features

- Upload clothing images (top / pants / shoes)
- Automatic background removal
- Combine items into a single outfit image
- Simple desktop UI (Tkinter)
- Save generated outfits locally

---

## Tech Stack

- Python
- Tkinter → GUI (desktop interface)
- Pillow → image processing
- rembg → AI background removal

---

## Project Structure

```
outfit-builder-desktop/
│
├── app.py                      
│
├── services/
│   ├── image_service.py        
│   ├── outfit_service.py       
│   ├── storage_service.py      
│
├── data/
│   ├── outfits.json            
│
├── assets/
│   ├── temp/                   
│   ├── output/                 
│
├── utils/
│   ├── file_handler.py        
│
├── requirements.txt
└── README.md
---

How It Works

1. User uploads clothing images
2. Background is removed automatically
3. Images are assigned to categories (top, pants, shoes)
4. Images are combined vertically into a single outfit
5. Result is displayed in the app
6. You can save outfits