# Picture-in-Picture Screen Sharing

This project demonstrates how to implement picture-in-picture screen sharing using the `navigator.mediaDevices.getDisplayMedia()` API in JavaScript. It allows you to select a media stream (your screen) and display it in a video element. You can then enable picture-in-picture mode and disable it by clicking a button.

## Usage

To use this project, follow these steps:

1. Open the web page in a supported browser.

2. Click the "Select Media Stream" button to prompt the browser to select a media stream (your screen) to share.

3. The selected media stream will be played in the video element on the page.

4. Click the "Start Picture in Picture" button to enable picture-in-picture mode for the video element.

5. To exit picture-in-picture mode, click the "Stop Picture in Picture" button.

Note: This project uses the `navigator.mediaDevices.getDisplayMedia()` API, which may not be supported in all browsers. Please refer to [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/API/Screen_Capture_API/Using_Screen_Capture) for browser compatibility details.

## Code Explanation

- The `selectMediaStream()` function is an async function that prompts the user to select a media stream (display media) using `navigator.mediaDevices.getDisplayMedia()`. It assigns the media stream to the `srcObject` property of the `videoElement` and starts playing the video when the metadata is loaded.

- The `button` element has an event listener attached to it, which, when clicked, disables the button, requests picture-in-picture mode for the `videoElement` using `videoElement.requestPictureInPicture()`, and then re-enables the button.

- The `catch` block in the `try-catch` statement inside `selectMediaStream()` logs any errors that occur while trying to access the media stream.

- The `selectMediaStream()` function is called when the page loads to initiate the screen sharing process.

Feel free to modify the code as needed and integrate it into your own projects.

## License

This project is licensed under the [MIT License](LICENSE).
