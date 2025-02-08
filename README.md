# Dify Electron App

## Overview

Dify is an Electron-based application that displays a web page from `http://localhost/apps`. The application is built to run on macOS and provides a simple interface to view the specified web page.

## Features

- Displays the web page from `http://localhost/apps`
- Includes a standard macOS title bar with window controls (minimize, maximize, close)

## Installation

1. Download the `.dmg` file from the `dist` directory.
2. Open the `.dmg` file and drag the `dify` app to your Applications folder.
3. Launch the `dify` app from your Applications folder.

## Usage

1. Ensure that a web server is running at `http://localhost/apps`.
2. Open the `dify` app.
3. The app will display the web page from `http://localhost/apps`.

## Changing the Endpoint

To change the endpoint that the Dify app accesses, follow these steps:

1. Open the `main.js` file in the project directory.
2. Locate the line that sets the URL for the `win.loadURL` method:
   ```javascript
   win.loadURL('http://localhost/apps');
   ```
3. Replace `'http://localhost/apps'` with the desired endpoint URL. For example:
   ```javascript
   win.loadURL('http://your-new-endpoint.com');
   ```
4. Save the changes to `main.js`.
5. Rebuild the application:
   ```bash
   npm run build
   ```

## Development

### Prerequisites

- Node.js v22.13.1
- npm 10.9.2

### Setup

1. Clone the repository.
2. Install dependencies:
   ```bash
   npm install
   ```

### Running the App

To run the app in development mode:
```bash
npm start
```

### Building the App

To build the app for macOS:
```bash
npm run build
```

The built `.dmg` file will be located in the `dist` directory.

## License

This project is licensed under the MIT License.
