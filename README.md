### OCR-Tesseract4


```html
https://pypi.org/project/pytesseract/
https://github.com/tesseract-shadow/tesseract-ocr-re
```

### Usage

```python
import requests

image = open('path_to_image.file', 'rb').read()

# if calling from another service in docker compose
r = requests.post('http://tesseract:8888/image_to_string', files={'file': image})

# if calling from another elsewhere in docker compose
r = requests.post('http://<local_or_aws_endpoint>:8888/image_to_string', files={'file': image})

print(r.text)

# if calling to get readable pdf
r = requests.post('http://<local_or_aws_endpoint>:8888/image_to_readable_pdf', files={'file': image})

# save the readable pdf
with open('output.pdf', 'wb') as f:
    f.write(r.content)
```


### Folder Structure

```
|   .gitignore
|   docker-compose.yml
|   preocr.py
|   README.md
|
+---lzw
|       decoder.py
|       encoder.py
|       README.md
|
\---tesseract
    |   app.py
    |   config.py
    |   Dockerfile
    |   requirements.txt
    |   wsgi.py
```    