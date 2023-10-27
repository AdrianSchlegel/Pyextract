# Pyextract
Welcome to Pyextract! Pyextract is a powerful tool for extracting text from images using Tesseract OCR, and it's designed to work with a variety of languages.

### Features
Supports multiple languages, with the option to specify the desired language for text extraction.
Option to save extracted data to a specified location.
Ability to use images from the clipboard or a specific directory for text extraction.
Prints the result to the console.

### Prerequisites
Before you begin, ensure you have the following installed on your system:

- Python 3.x
- Git
- Homebrew (for macOS users)
- Tesseract OCR (Installation Guide below)
- Tessdata for more language support

###Installation Steps
Clone the Repository:

```git clone https://github.com/AdrianSchlegel/Pyextract.git```

1. Install Tesseract OCR:

- On macOS, use Homebrew:

```brew install tesseract```

For other operating systems, please follow the appropriate instructions to install Tesseract OCR.

2. Install Tessdata:

Tessdata is required for language support in Tesseract. Install it using Homebrew:

```brew install tessdata```

3. Configuration
Edit the configuration settings according to your needs:

language: Set to 'eng' for english. For a list of available languages, see: Tesseract OCR Languages
save_data: Set to False if you don't want to save the extracted data. If True, specify the save_location.
save_location: The directory where extracted data will be saved. Only relevant if save_data is True.
use_clipboard_for_input: Set to True to use images from the clipboard for text extraction. If False, the script will use images from the path_to_directory.
path_to_directory: The directory containing images for text extraction. This is used if use_clipboard_for_input is False.
print_result: Set to True to print the extracted text to the console.
Usage
After configuring, run the Pyextract script. If use_clipboard_for_input is True, copy an image to your clipboard, and the script will attempt to extract text from it. If it's False, the script will use images from the specified directory.

Notes
It's essential to ensure that Tesseract OCR and Tessdata are correctly installed for the script to work.
The language data for Tesseract needs to be compatible with the version of Tesseract you have installed.

______________________________________________________________________________________________________________

# How Pyextract Works

Pyextract is a versatile tool that leverages the power of Tesseract OCR (Optical Character Recognition) to extract text from images. It's designed to be user-friendly and efficient, providing two primary modes of operation: extracting text from images on the clipboard and processing multiple images from a folder. Here's how each mode works:

## Clipboard Mode

### 1. Copy an Image to Clipboard:
The user copies an image to the clipboard. This can be any image that contains text they want to extract.

### 2. Run Pyextract:
When Pyextract is executed, it checks the clipboard for any images.

### 3. Text Extraction:
If an image is found on the clipboard, Pyextract uses Tesseract OCR to analyze the image and extract the text.

### 4. Replace Image with Text:
The extracted text is then placed back onto the clipboard, replacing the original image. This allows the user to easily paste the extracted text into any text field or document.

### 5. Optional Saving:
If the save_data configuration is set to True, the extracted text will also be saved to the specified save_location.


## Folder Mode

### 1. Images in a Folder:
The user places multiple images in a specified folder (path_to_directory). These images are the ones from which they want to extract text.

### 2. Run Pyextract:
Pyextract is executed with use_clipboard_for_input set to False.

### 3. Batch Processing:
Pyextract goes through each image in the specified folder, using Tesseract OCR to extract text from each one.

### 4. Text Files Creation:
For each image, Pyextract creates a corresponding .txt file containing the extracted text. These text files are typically saved in the same folder as the images or in the specified save_location if save_data is True.

### 5. Result Output:
If print_result is set to True, the extracted text from each image is also printed to the console.

______________________________________________________________________________________________________________

# ERRORS:

# When experiencing errors make sure that:
- You have all prerequisites installed correctly
- Make sure you have chmod +x main allowed
- make sure the script exists in the $PATH

### If this still doesn't work create an issue and I will help you troubleshoot!

Happy text extracting with Pyextract!
