# Resizer-Task-7
Image Resizer Tool
from PIL import Image

def resize_image(input_path, output_path, width, height):
    try:
        # Open the image
        img = Image.open(input_path)

        # Resize the image
        resized_img = img.resize((width, height))

        # Save the resized image
        resized_img.save(output_path)
        print(f"✅ Image saved successfully as {output_path}")
    except Exception as e:
        print(f"❌ Error: {e}")

if __name__ == "__main__":
    # Get details from user
    input_path = input("Enter the input image path: ")
    output_path = input("Enter the output image path: ")
    width = int(input("Enter the new width: "))
    height = int(input("Enter the new height: "))

    resize_image(input_path, output_path, width, height)
