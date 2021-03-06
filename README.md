# Node.js Barcode Reader for Raspberry Pi

The sample demonstrates how to use [Dynamsoft Barcode Reader SDK](http://www.dynamsoft.com/Products/Dynamic-Barcode-Reader.aspx) and Node.js to create Web barcode reader on Raspberry Pi.

## Getting Started

### How to install Node.js on Raspberry Pi
1. Remove the pre-built Node:

    ```
    sudo apt-get remove node
    ```
2. Download [Node.js](https://nodejs.org/en/download/) for your Pi devices.
3. Add the Node path to **~/.bashrc**:

    ```
    vim ~/.bashrc
    export PATH=$PATH:/home/pi/node-v4.4.0-linux-armv7l/bin
    source ~/.bashrc
    ```

### How to build barcode reader using Dynamsoft Barcode Reader SDK
1. Contact [support@dynamsoft.com](mailto:support@dynamsoft.com) to get Dynamsoft Barcode Reader SDK for Raspberry Pi.
2. Extract the package and generate a symbolic link:

    ```
    sudo ln -s <DynamsoftBarcodeReader>/lib/libDynamsoftBarcodeReader.so /usr/lib/libDynamsoftBarcodeReader.so
    ```
3. Install **node-gyp**:

    ```
    npm install -g node-gyp
    ```
4. Build **dbr.so**:

    ```
    node-gyp build
    ```
5. Install dependent node modules:

    ```
    npm install express formidable
    ```
6. Start the server:

    ```
    node server.js
    ```
7. Visit **http://localhost:2016/index.htm**

    ![Raspberry Pi Node.js Barcode Reader](http://www.codepool.biz/wp-content/uploads/2016/03/rpi_node_barcode-1-1024x576.png)
    
## Blog
[How to Build Node.js Barcode Reader on Raspberry Pi](http://www.codepool.biz/raspberry-pi-nodejs-barcode-reader.html)
