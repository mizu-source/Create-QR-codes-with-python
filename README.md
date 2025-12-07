# Create-QR-codes-with-python
This Python program generates a QR code from any URL entered by the user. After typing the link, the script creates a QR code image using the qrcode library and saves it automatically. The generated image can be scanned with any smartphone to open the provided URL quickly and easily.

import qrcode

url = input("Enter the URL: ").strip()
file_path = "C:\\Users\\abdou\\OneDrive\\Desktop\\qrcode.png"

qr = qrcode.QRCode(
    version=1,
    box_size=10,
    border=5
)

qr.add_data(url)
qr.make(fit=True)

img = qr.make_image(fill_color="black", back_color="white")
img.save(file_path)

print("QR code saved at:", file_path)



#dont forget to install "pip install qrcode and pip install pillow"
