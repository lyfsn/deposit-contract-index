# Hex to Little Endian Converter

## Introduction

This project provides a simple yet effective web interface for converting hexadecimal strings into their little endian numerical representation. The primary function of this web page is to allow users to input a hexadecimal string and display the corresponding little endian number. It's designed with a user-friendly interface, featuring aesthetic gradients and a clean layout to enhance user experience.

## Features

- **User Input**: Accepts hexadecimal strings as input through a clean and straightforward text field.
- **Conversion Logic**: Utilizes a JavaScript function to convert the input hexadecimal string to a little endian number.
- **Responsive Design**: The page layout is fully responsive, making it accessible on various devices and screen sizes.
- **Elegant UI**: The interface is designed with a pleasing color gradient, providing a refreshing and modern look.

## How to Use

1. **Enter Hex String**: Input your hexadecimal string in the text field provided. The hex string should not contain any spaces or non-hex characters.
2. **Convert**: Click the 'Convert' button to perform the conversion.
3. **View Result**: The result of the conversion will be displayed below the button, indicating the numeric value in little endian format.

## Technical Details

The core functionality is powered by the following JavaScript function:

```
function littleEndianToNumber(hexString) {
    const byteArray = hexString.match(/.{1,2}/g).map(byte => parseInt(byte, 16));
    const bigEndianArray = byteArray.reverse();
    const bigEndianHexString = bigEndianArray.map(byte => byte.toString(16).padStart(2, '0')).join('');
    return parseInt(bigEndianHexString, 16);
}
```

## Setup

To set up this project on your local machine:

1. Download or clone the repository.
2. Open the `index.html` file in a web browser.

No additional installation or setup is required.

## Conclusion

This Hex to Little Endian Converter is an easy-to-use tool for anyone needing to perform this specific type of data conversion. Its simple interface and effective functionality make it a handy utility for developers, students, and anyone interested in data formats and conversion.
