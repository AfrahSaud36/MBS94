from PIL import Image

def convert_to_binary(image_path, width=50):
    img = Image.open(image_path)
    
    img = img.convert('L')
    
    aspect_ratio = img.height / img.width
    height = int(aspect_ratio * width * 0.55) 
    img = img.resize((width, height))

    binary_image = ""
    for y in range(img.height):
        for x in range(img.width):
            pixel = img.getpixel((x, y))
            binary_image += '1' if pixel < 128 else '0'
        binary_image += "\n"

    return binary_image

image_path = '/Users/afrahsaud36/Downloads/الأمير-محمد-بن-سلمان-بن-عبدالعزيز.webp'  # Replace with your image file path
binary_art = convert_to_binary(image_path, width=50) 
print(binary_art)
