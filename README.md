🖼️ Secure Data Hiding in Image Using Steganography
🔍 Project Overview
This project implements image steganography to securely hide and retrieve text messages inside an image. The hidden data is password-protected, ensuring only authorized users can extract the message.

📌 Features
✅ Stealthy Encryption – Hides text inside an image without noticeable visual changes.
✅ Password Protection – Only users with the correct password can extract the hidden message.
✅ Minimal Distortion – The quality of the image remains almost the same.
✅ Works with Any Image Format – Supports .png, .jpg, and other OpenCV-supported formats.
✅ Easy Encryption & Decryption – Simple command-line interface for usability.

🔐 How It Works
Encryption Process:
User selects an image as a carrier (cover image).
Secret message is input, which is combined with a password.
The message is embedded into the blue channel of the image’s pixels.
The modified image is saved as an encrypted image.
Decryption Process:
User provides the encrypted image and the password.
The program extracts the hidden message from the image pixels.
If the password is correct, the secret message is revealed.
If the password is incorrect, access is denied.
⚙️ Installation
1️⃣ Install Dependencies
bash
Copy
Edit
pip install opencv-python
or for headless systems (servers):

bash
Copy
Edit
pip install opencv-python-headless
2️⃣ Run the Program
bash
Copy
Edit
python stego.py
📜 Usage
Encryption:
bash
Copy
Edit
python stego.py
🔹 Select option 1 (Encrypt).
🔹 Provide image path, secret message, and password.
🔹 The encrypted image is saved as encrypted_image.png.

Decryption:
bash
Copy
Edit
python stego.py
🔹 Select option 2 (Decrypt).
🔹 Provide encrypted image path and password.
🔹 If the password is correct, the hidden message is displayed.

🛠 Technologies Used
Python 🐍
OpenCV (for image processing)
Steganography techniques (LSB method)
📌 Example Output
mathematica
Copy
Edit
Choose an option:
1. Encrypt a message into an image
2. Decrypt a message from an image
Enter choice (1/2): 1
Enter the image file path: myimage.jpg
Enter the secret message: Hidden text here
Enter the encryption password: securepass
✅ Encryption Successful! Encrypted image saved as encrypted_image.png
🔒 Security Note
This implementation uses basic LSB (Least Significant Bit) steganography, which is not cryptographically secure. For higher security, consider encrypting the message using AES encryption before hiding it inside the image.

💡 Feel free to contribute and enhance this project! 😊 🚀
