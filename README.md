# Outfit Builder App

A simple AI-powered web application that allows users to upload clothing items, remove their backgrounds, and combine them into clean outfit previews.

---

## Features

* Upload clothing images (tops, pants, shoes)
* Automatic background removal
* Combine items into a full outfit
* Save generated outfits as images
* Fast API backend

---

## Tech Stack

* Backend: Python + FastAPI
* Image Processing: Pillow
* Background Removal: rembg
* Server: Uvicorn

---

## Project Structure

```
outfit-app/
│
├── app/
│   ├── main.py
│   ├── routes/
│   │   ├── upload.py
│   │   ├── outfit.py
│   │
│   ├── services/
│   │   ├── image_service.py
│   │   ├── outfit_service.py
│   │
│   ├── models/
│   │   ├── clothing.py
│   │   ├── outfit.py
│   │
│   ├── utils/
│   │   ├── file_handler.py
│
├── static/
│   ├── uploads/
│   ├── processed/
│   ├── outfits/
│
├── requirements.txt
├── README.md
```

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/TimonLudwig1/Outfit-Builder.git
```

2. Create a virtual environment:

```bash
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Run the App

```bash
uvicorn app.main:app --reload
```

Open in browser

---

## API Usage

### Upload Image

**POST** `/upload/`

Parameters:

* `file`: image file
* `category`: `"top"`, `"pants"`, `"shoes"`

Response:

```json
{
  "id": "uuid",
  "category": "top",
  "image": "static/processed/xyz.png"
}
```

---

### Create Outfit

**POST** `/create-outfit/`

Request Body:

```json
{
  "top": "path/to/top.png",
  "pants": "path/to/pants.png",
  "shoes": "path/to/shoes.png"
}
```

Response:

```json
{
  "outfit": "static/outfits/outfit.png"
}
```

---

## How It Works

1. The user uploads an image
2. The app removes the background
3. The processed image is stored
4. Multiple items are combined vertically into a single outfit image

---

## Notes

* For best results, use images with a clear subject and simple background
* Background removal quality may vary depending on the image

---

## License

This project is open-source and available under the MIT License.

