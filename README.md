# 🌾 Wheet Scraper

This project uses [Scrapy](https://scrapy.org/) to scrape images of a **single ear of wheat** from the internet.

---

## 📦 1. Clone the Repository

Start by cloning the repository:

```bash
git clone https://github.com/Beeezus/wheet_scraper.git
cd wheet_scraper
```

---

## 🐍 2. Set Up Virtual Environment & Install Dependencies

It's best to isolate your environment using `venv`.

### On macOS/Linux:

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### On Windows:

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```


---

## 🔎 3. Find a Resource with Wheat Ear Images

To scrape images of a single ear of wheat, you’ll need a source website that meets these criteria:
- Publicly accessible
- Contains images of a **single wheat ear**

Good candidate resources include:

- [Google Images](https://images.google.com) – Search for “single ear of wheat”
- [Wikimedia Commons](https://commons.wikimedia.org/wiki/Main_Page)
- [Pixabay](https://pixabay.com)
- [Pexels](https://www.pexels.com)

Choose a domain with static image URLs.

---

## 🕷️ 4. Create a Scrapy Spider

Scrapy will be used to crawl and extract image data.

### You need to initialize the Scrapy project :

From the root directory (where `scrapy.cfg` should live):

```bash
scrapy startproject wheet_scraper .
```

> The dot (`.`) at the end tells Scrapy to use the current directory.

### Create a spider:

```bash
cd wheet_scraper/spiders
scrapy genspider wheat_images example.com
```

Replace `example.com` with the domain you plan to scrape.

This will generate a file called `wheat_images.py`.

---

## ✏️ 5. Edit the Spider Code

Open `wheat_images.py` and update it with a basic image-scraping structure:

```python
import scrapy

class WheatImagesSpider(scrapy.Spider):
    name = "wheat_images"
    allowed_domains = ["example.com"]
    start_urls = None # Replace with the URL of the page you want to scrape

    def parse(self, response):
        # Extract image URLs here
        pass
        
```
---

## ▶️ 6. Run the Spider

From the project root directory:

```bash
scrapy crawl wheat_images
```

To save the output to a JSON file:

```bash
scrapy crawl wheat_images -o images.json
```

---

## 🛠️ 7. Commit your code 

- Create a branch with your solution:
- Name should contain the developer name (i.e. vic_zagranowski-wheat-scraper)
- Push your code

---

## ✅ Done!

You now have a working Scrapy project to start scraping images of wheat ears from the web. 🌾
