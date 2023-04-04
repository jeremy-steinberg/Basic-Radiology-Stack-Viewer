# Radiology Stack Scroller

This is a simple web application for viewing a stack of radiology images. The html file is only around 10kb. The application allows the user to scroll through the images using a vertical scrollbar, select the stack, and provides buttons for adjusting the brightness and contrast, zooming, panning, and magnification of the images. The application is built using HTML, CSS, and JavaScript, and needs to run on a web server due to CORS limitations. This was created because I couldn't find any open source non-DICOM radiology image viewers. The usage case would be for very lightweight applications where a DICOM server isn't required and you just want to scroll through simple radiology pictures. Creation was co-authored with GPT-4. The license is CC-Zero

## Features

- Display radiology images in a web browser, including radiology stacks
- Navigate through the images in a stack using a scrollbar
- Adjust images using the brightness/contrast, zoom, and pan buttons
- Switch between different stacks (e.g., Axial, Sagittal) for the stack selector version

## Project Structure

```
root_directory/
    ├── Axial/
    │   ├── image1.jpg
    │   ├── image2.jpg
    │   └── ...
    ├── Sagittal/
    │   ├── image1.jpg
    │   ├── image2.jpg
    │   └── ...
    └── your_html_file.html
```

## Getting Started

1. Clone or download this repository to your local machine.
2. Within the Stack Selector folder, organize your MRI image files into separate folders based on their orientation (e.g., Axial, Sagittal) within the root directory. Each folder should contain the respective image files for that orientation.
3. Open Stack Scroller.html in your favorite code editor
4. Update the stacks object in the JavaScript code to include the image file paths for each orientation. For example:

```
const stacks = {
  Axial: [
    "Axial/image1.jpg",
    "Axial/image2.jpg",
    // ... other axial image paths
  ],
  Sagittal: [
    "Sagittal/image1.jpg",
    "Sagittal/image2.jpg",
    // ... other sagittal image paths
  ],
};
```

5. To run the application, you will need to have Python installed on your machine. You can download the latest version of Python from the official website.

Once you have Python installed, follow these steps:

Open a terminal or command prompt and navigate to the project directory.
Start the Python web server by running the following command:
```
python -m http.server 8000
```
Open a web browser and navigate to http://localhost:8000/.
You should now see the radiology image viewer application.

## Usage

To use the application, follow these steps:

Select a stack using the toolbar buttons on the top
Scroll through the image stack using the vertical scrollbar to the right of the canvas.
Adjust the brightness and contrast of the image using the "Brightness/Contrast" button. Click and drag the mouse to adjust the brightness and contrast.
Zoom in and out of the image using the "Zoom" button. Click and drag the mouse to zoom in and out. The focal point of the zoom will be where the initial mouse click was.
Pan the image using the "Pan" button. Click and drag the mouse to pan the image.
To reset the image to its original state, click the "Reset" button.

## Customization

You can customize the appearance and functionality of the application by modifying the HTML, CSS, and JavaScript code. For example, you can change the background color of the toolbar or the canvas, or add additional buttons for other image manipulation tasks.
Contributing

Contributions to this project are welcome. If you find a bug or have an idea for a new feature, please open an issue or submit a pull request.
