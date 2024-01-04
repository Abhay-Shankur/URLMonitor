# URLMonitor
The project involves the development of a Chrome extension and a Flask web application to enhance web browsing security. The extension monitors website URLs visited by the user, sending each URL to a Flask server for analysis. The Flask server checks if the URL is protected and, if so, redirects the user to a designated login page.

Key Components:

1. **Chrome Extension:**
   - Monitors URL changes in the browser tabs using the `chrome.tabs.onUpdated` event.
   - Sends each URL to the Flask server for protection checking.

2. **Flask Server:**
   - Listens for URL checking requests from the Chrome extension at the `/check_url` endpoint.
   - Performs protection checks on received URLs and responds with whether they are protected.
   - If a URL is protected, the server redirects the user to a login page or a QR code generation page.

3. **Web Authentication:**
   - If a protected URL is detected, the user is redirected to a login page for authentication.
   - Alternatively, the user may be redirected to a page that generates dynamic QR codes for enhanced security.

4. **Firebase Integration:**
   - Utilizes Firebase Realtime Database for storing and retrieving dynamic data, such as tokens and user credentials.
   - The Flask server interacts with Firebase for real-time updates and authentication.

5. **Dynamic QR Code Generation:**
   - Generates dynamic QR codes containing verifiable credentials for secure user interactions.
   - The QR code content is stored in Firebase, ensuring uniqueness and validity.

Overall, the project aims to provide a security layer by checking the protection status of visited URLs, prompting user authentication when necessary, and incorporating dynamic QR codes for secure interactions. The combination of the Chrome extension and Flask server creates a seamless and secure web browsing experience for users.
