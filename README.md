# BG Remover

BG Remover is a web-based tool that allows users to remove backgrounds from images using color selection and HSV (Hue, Saturation, Value) range adjustments. The tool provides both click and drag modes for selecting colors to remove from the image.

## Functionality

### Core Features
- **Image Upload**: Users can upload any image file to process
- **Background Removal**: Remove unwanted background colors from images
- **Color Selection**: Two methods for selecting colors to remove:
  - **Click Mode**: Click on a specific pixel to select its color
  - **Drag Mode**: Drag to select a region and sample colors from it
- **HSV Range Adjustment**: Fine-tune the range of colors to remove using Hue, Saturation, and Value sliders
- **Edge Feathering**: Smooth edges of the removed areas for a more natural look
- **Multiple Color Slots**: Support for up to 5 different color selections
- **Export**: Download the processed image as a PNG file with transparency

### User Interface

The interface is divided into three main sections:
1. **Header**: Contains the title, image upload button, and mode selection (Click/Drag)
2. **Canvas Area**: Left side shows the source image, right side shows the result
3. **Control Panel**: Right sidebar with color targets, HSV range controls, and export button

## How It Works

### Color Selection Process
1. Upload an image using the "OPEN IMAGE" button
2. Choose between "Click" or "Drag" mode
3. In Click mode: Click on a pixel in the source image to select its color
4. In Drag mode: Click and drag to select a region of the image
5. The tool automatically creates a color slot with appropriate HSV ranges

### HSV Range Controls
Each color slot has adjustable ranges for:
- **Hue**: Color type (0-179)
- **Saturation**: Color intensity (0-255)
- **Value**: Brightness (0-255)
- **Edge Feather**: Softens edges (0-12 pixels)

### Image Processing
The background removal algorithm works by:
1. Converting selected colors to HSV color space
2. Creating removal ranges based on the HSV sliders
3. Scanning each pixel in the image
4. Setting pixels within the removal ranges to transparent
5. Applying Gaussian blur for edge feathering if selected
6. Displaying the result with a checkered background to show transparency

### Export
Click the "EXPORT PNG" button to download the processed image with transparent background.

## Technical Implementation

The tool is built with HTML, CSS, and vanilla JavaScript with no external dependencies. Key technical aspects include:
- Canvas-based image manipulation
- Real-time HSV color space conversion
- Gaussian blur algorithm for edge feathering
- Responsive design that adapts to different image sizes
- Client-side processing (no server required)