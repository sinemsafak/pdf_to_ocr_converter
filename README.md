EN | TR

🇬🇧 English Version
FAST PDF OCR (Turkish)
A high-speed OCR pipeline for Turkish PDF documents using Tesseract, OpenCV, pdf2image and PyPDF.
Generates both a searchable OCR PDF and plain text output. Fully compatible with Google Colab.

🚀 Features
Fast OCR using multiprocessing
Turkish OCR support (tesseract-ocr-tur)

Produces:
searchable OCR PDF
plain text TXT
Automatic page preprocessing (grayscale + Otsu threshold)
Works directly in Google Colab
Adjustable DPI, OEM, and PSM parameters

📦 Requirements
Tesseract OCR + Turkish language pack
Python modules:
pdf2image
pytesseract
opencv-python
pypdf
pillow
tqdm

🔧 Installation (Google Colab)
from google.colab import drive
drive.mount('/content/drive')

!apt-get -q update
!apt-get -q install -y tesseract-ocr tesseract-ocr-tur poppler-utils
!pip -q install pdf2image pillow pytesseract opencv-python pypdf tqdm

🧠 Usage
Update input/output file paths:
INP = "/content/drive/MyDrive/<YOUR_FOLDER>/<YOUR_FILE>.pdf"
OUT_PDF = "/content/drive/MyDrive/<OUTPUT_FOLDER>/output.pdf"
OUT_TXT = "/content/drive/MyDrive/<OUTPUT_FOLDER>/output.txt"

Running the script will:
Convert PDF pages to PNG
Preprocess each page (grayscale + Otsu threshold)
Perform OCR with Tesseract
Generate an OCR-embedded PDF and a TXT file

⚡ Performance
Utilizes all available CPU cores (multiprocessing)
300 DPI by default (configurable)
PSM 6 (single text block — fastest mode)

📁 Output Files
File	Description
*_FAST_manual.pdf	Searchable PDF with OCR text layer
*_FAST_manual.txt	Extracted plain text


🇹🇷 TÜRKÇE (Turkish Version)
TR | EN
FAST PDF OCR (Türkçe)
Tesseract, OpenCV, pdf2image ve PyPDF kullanarak Türkçe PDF belgeleri için yüksek hızlı OCR dönüştürme aracıdır.
Bu araç hem OCR katmanlı aranabilir PDF hem de düz metin TXT çıktısı üretir.
Tamamen Google Colab ile uyumludur.

🚀 Özellikler
Çoklu işlem (multiprocessing) ile hızlı OCR
Türkçe OCR desteği (tesseract-ocr-tur)

Üretilen çıktılar:
aranabilir OCR PDF
düz metin TXT
Otomatik sayfa ön işleme (gri tonlama + Otsu threshold)
Doğrudan Google Colab üzerinde çalışır
DPI, OEM ve PSM parametreleri ayarlanabilir

📦 Gereksinimler
Tesseract OCR + Türkçe dil paketi
Python kütüphaneleri:
pdf2image
pytesseract
opencv-python
pypdf
pillow
tqdm

🔧 Kurulum (Google Colab)
from google.colab import drive
drive.mount('/content/drive')

!apt-get -q update
!apt-get -q install -y tesseract-ocr tesseract-ocr-tur poppler-utils
!pip -q install pdf2image pillow pytesseract opencv-python pypdf tqdm

🧠 Kullanım
Girdi ve çıktı dosya yollarını düzenleyin:
INP = "/content/drive/MyDrive/<YOUR_FOLDER>/<YOUR_FILE>.pdf"
OUT_PDF = "/content/drive/MyDrive/<OUTPUT_FOLDER>/output.pdf"
OUT_TXT = "/content/drive/MyDrive/<OUTPUT_FOLDER>/output.txt"

Bu betik şunları yapar:
PDF sayfalarını PNG’ye dönüştürür
Her sayfayı ön işler (gri ton + Otsu threshold)
Tesseract ile OCR uygular
OCR katmanlı PDF ve TXT dosyası oluşturur

⚡ Performans
Tüm işlemci çekirdeklerini kullanır
Varsayılan: 300 DPI (değiştirilebilir)
PSM 6 kullanır (tek metin bloğu — en hızlı)

📁 Çıktılar
Dosya	Açıklama
*_FAST_manual.pdf	OCR metin katmanı eklenmiş aranabilir PDF
*_FAST_manual.txt	OCR sonucu çıkarılmış düz metin
