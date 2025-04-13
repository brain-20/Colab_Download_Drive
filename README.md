EXAMPLE SNIPPET with image to show how to transfer large files from GDrive to Colab.
(View image in preview and the code in code view)

![image](https://github.com/user-attachments/assets/d5373be0-2a3b-485c-846c-9e8a82ceb5be)


# ---------------------------
# Download and extract "images.zip"
# ---------------------------
images_id = "1kk4VQbo7epPmsOsBM-VN2s0V8lbKqlRT"  # you get this for yourself if you share files, copy that link and paste it here.
images_file = "images.zip"
if not os.path.exists(images_file):
    print("Downloading images dataset...")
    !gdown "https://drive.google.com/uc?id={images_id}" -O {images_file}
    print("Extracting images dataset...")
    !unzip -q {images_file} -d content/dataset
else:
    print(f"'{images_file}' already exists, skipping images download.")
