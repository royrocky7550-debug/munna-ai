# Munna AI — Android App Starter

এটি Expo React Native দিয়ে তৈরি ব্যক্তিগত AI chat app starter। এতে Gemini AI chat, বাংলা/হিন্দি/ইংরেজি, স্থানীয় chat history, New Chat, Clear History, API key settings এবং dark UI আছে।

## ১. Gemini API Key
https://aistudio.google.com/apikey থেকে Gemini API key তৈরি করো। App চালু হলে Settings (⚙) থেকে key পেস্ট করে Save করো।

**নিরাপত্তা:** এই starter-এ key ফোনের AsyncStorage-এ থাকে এবং ফোন থেকে Gemini-তে request যায়। এটি ব্যক্তিগত পরীক্ষার জন্য। Public app বা অন্যদের কাছে বিতরণের আগে secure backend/proxy ব্যবহার করো। Key কাউকে দিও না, source code-এ hardcode করো না।

## ২. GitHub-এ কোড আপলোড
1. https://github.com/new খোলো, `munna-ai` নামে repository বানাও।
2. ZIP extract করে ফাইলগুলো repository-তে upload করো।

## ৩. মোবাইল থেকে Codespaces
1. Repository-তে Code > Codespaces > Create codespace on main চাপো।
2. Terminal-এ চালাও:

```bash
npm install
npx expo start --tunnel
```

3. Preview-এর জন্য Expo Go ব্যবহার করতে পারো।

## ৪. APK তৈরি
Terminal-এ চালাও:

```bash
npm install -g eas-cli
eas login
eas build:configure
eas build -p android --profile preview
```

Build শেষ হলে EAS build page-এ APK download link পাবে।

## সীমাবদ্ধতা
- Gemini API key লাগবে; quota/মডেল-প্রাপ্যতা Google account ও region অনুযায়ী বদলাতে পারে।
- GitHub Codespaces ও Expo EAS-এর free usage সীমিত হতে পারে।
- এটি starter app; streaming, voice, cloud sync, login বা multi-device history নেই।
- Gemini model বর্তমানে `gemini-2.5-flash` হিসেবে সেট করা। API-তে model unavailable দেখালে Google AI Studio-তে উপলভ্য model অনুযায়ী App.js-এর `MODEL` বদলাও।
