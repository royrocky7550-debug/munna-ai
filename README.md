# Munna AI

A simple Android AI chat app built with React Native and Expo.

## Features
- Bengali-friendly chat interface
- Gemini API integration
- Local chat history
- Dark theme

## Build an APK
1. Upload these project files to your GitHub repository.
2. Open the repository in a cloud development environment with Node.js.
3. Run `npm install`.
4. Install EAS CLI: `npm install -g eas-cli`.
5. Run `eas login` and `eas build:configure`.
6. In `app.json`, remove the placeholder `extra.eas.projectId` block if EAS asks to configure it automatically.
7. Run `eas build -p android --profile preview`.
8. When the cloud build finishes, open the APK link on your phone and install it.

## Gemini API key
Create a key in Google AI Studio and enter it inside the app. This starter stores the key locally on your device. Do not distribute this version publicly with a personal API key; a production app should call a secure backend so the key is not exposed in the client.

## Note
Cloud builds and Gemini API usage may have free-tier limits and may require account sign-in. No phone-number-free signup is guaranteed.
