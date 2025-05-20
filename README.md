# Physics Light Chain (Gyro)

This project is a single-page web application that demonstrates an interactive physics-based chain simulation. It utilizes the Matter.js physics engine to create a chain that responds to user interactions (mouse/touch dragging) and device orientation (gyroscope) for gravity manipulation.

## Core Functionalities

*   **Physics Simulation**: A chain composed of multiple segments is simulated using Matter.js, exhibiting realistic physics behavior.
*   **Interactive Chain**: Users can click and drag segments of the chain.
*   **Gyroscope-Controlled Gravity**: If motion sensors are enabled and available on the device, the direction of gravity in the simulation dynamically changes based on the device's tilt.
*   **Visual Feedback**: The application provides visual cues for interactions, such as when the chain is pulled to its maximum extent.

This initial content covers the basics. More details about features, improvements, and usage will be added in subsequent steps.

## Key Features

*   **Mouse/Touch Interaction**: Drag individual chain segments with your mouse or finger.
*   **Max Pull Feedback**: When a segment is pulled beyond a certain limit:
    *   The interaction is clamped to prevent the chain from overstretching.
    *   The device vibrates (if supported by the browser and device).
    *   The segment temporarily changes color to indicate it's at the limit.
*   **Dynamic Gravity via Sensors**: Click the "Enable Motion Sensors" button. If permission is granted and sensors are available:
    *   The simulation's gravity will be controlled by your device's tilt (using `DeviceOrientationEvent`).
    *   Real-time sensor data (Beta for front/back tilt, Gamma for left/right tilt) and the resulting gravity vector are displayed.
*   **Responsive Design**: The simulation viewport and elements adjust to the browser window size.

## Recent Improvements

*   **Code Organization**:
    *   CSS styles have been moved to an external `style.css` file.
    *   JavaScript logic has been moved to an external `script.js` file, improving the modularity and maintainability of `index.html`.
*   **Visual Enhancements**:
    *   The chain segments now have a brighter, "light-like" appearance (Aqua fill with a White stroke).
    *   The links between chain segments have been styled to complement the new look.
*   **UX Refinements**:
    *   The sensor information display is now more clearly formatted with line breaks.
    *   Messages regarding sensor permissions and status have been made more user-friendly.
*   **Code Clarity**:
    *   Comprehensive comments have been added to `script.js` and `style.css` to improve code understanding.

## How to Run

1.  Clone this repository or download the files (`index.html`, `style.css`, `script.js`).
2.  Open the `index.html` file in a modern web browser that supports JavaScript and the Device Orientation API (for gyroscope features).
3.  To experience gyroscope-controlled gravity, click the "Enable Motion Sensors" button when prompted or visible on the page. You may need to grant permission for the browser to access motion sensor data.

## File Structure

*   `index.html`: The main HTML file that provides the page structure and includes the canvas for the simulation.
*   `style.css`: Contains all the CSS rules for styling the page elements, including the simulation canvas, information display, and button.
*   `script.js`: Holds all the JavaScript logic for the application. This includes setting up the Matter.js physics engine, creating the chain, handling user interactions (mouse/touch), integrating gyroscope data, and managing UI updates.
*   `README.md`: This file, providing information about the project.

## Deploying as a GitHub Pages Website

This project is ready to be deployed as a GitHub Pages website. Follow these steps to make it live:

1.  **Navigate to Repository Settings**:
    *   Go to your repository on GitHub where these files are pushed.
    *   Click on the "Settings" tab (usually near the top of the repository page).

2.  **Configure GitHub Pages**:
    *   In the left sidebar of the Settings page, click on "Pages" (under the "Code and automation" section).
    *   Under the "Build and deployment" section:
        *   For "Source", ensure "Deploy from a branch" is selected.
        *   Under "Branch":
            *   Select your main branch (commonly named `main`, `master`, or similar) from the dropdown.
            *   Ensure the folder is set to `/ (root)`.
        *   Click "Save".

3.  **Access Your Live Site**:
    *   After saving, GitHub will start building your page. This might take a minute or two.
    *   Once deployed, the URL for your live site (e.g., `https://<your-username>.github.io/<repository-name>/`) will be displayed at the top of the GitHub Pages settings section.
    *   You can then visit this URL to see your Physics Light Chain simulation live!

**Note**: Since this project uses the Device Orientation API for gyroscope features, these specific features will only work if you access the live GitHub Pages website on a device that has motion sensors (like a smartphone or tablet) and if you grant the necessary permissions when prompted by the browser.
