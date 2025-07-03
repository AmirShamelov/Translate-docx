# API for translating documents
___

### The main idea is developing an HTTP service based on FastAPI, which:
### 1. Accepts entry .a docx file from the user via a POST request.
### 2. Extracts text from this file.
### 3. Translates the extracted text using a third—party API (hereinafter referred to as API 1) available at: `http://34.9.223.19:8000/docs/`
### 4. Returns to the user .a docx file with the same formatting, but already translated text.
___
## Example

![docx file](/img/3.jpeg)
### Figure 1. docx file with kazakh language

![Swagger](/img/1.jpeg)
### Figure 2. POST endpoint with 2 parameters - direction and file
### In direction field you should choose translation language between ru-kk and kk-ru (Russian, Kazakh)
### In the file field you just need upload a .docx file

![translating docx file](/img/2.jpeg)
### Figure 3. Downloading the finished file

![translating docx file](/img/4.jpeg)
### Figure 4. docx file after text translation

### You can see that, after translating the text, the user received .a docx file with the original formatting preserved (paragraph, table), but it has little bugs in API translation.
### This text in docx file took approximately 2-3 minutes. However, if text will be longer it will take longer.
___


## How to run?

### 1. Docker:
### `docker-compose build`
### `docker-compose up`

### 2. main.py:
### `pip install -r requirements.txt`
### `uvicorn main:app --reload`

### Swagger url: `http://localhost:8000/docs`

___






