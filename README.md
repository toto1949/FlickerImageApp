

#  Flickr Image Search App

A SwiftUI-based iOS application that allows users to search and view public images from Flickr using tags. Built with Combine, async/await, and MVVM architecture.

---

## ✨ Features

- 🔍 Real-time image search using Flickr’s public feed API
- 🖼 Grid layout showing thumbnail images
- 📄 Detailed view with image metadata
- ⏳ Non-blocking loading indicator during searches
- ⌨️ Real-time updates using Combine’s `debounce`
- 🧠 Handles multi-tag (comma-separated) searches
- ♻️ Deduplicates images across multiple tag results
- 🧭 Loads default images when search field is empty
- 📤 Image sharing from detail view
- 🧑‍🦯 Accessibility with VoiceOver and Dynamic Type
- 🔁 Smooth animated transition from grid to detail view

---

## 🧪 Technical Stack

- **Language**: Swift 5.9+
- **UI**: SwiftUI
- **Architecture**: MVVM
- **Concurrency**: async/await
- **Reactive Programming**: Combine
- **Tested on**: iOS 17 (Xcode 15+)


## 🔗 API

Public Flickr Feed API (no key required):

```
https://api.flickr.com/services/feeds/photos_public.gne?format=json&nojsoncallback=1&tags={searchTerm}
```

- Accepts single or comma-separated tags
- Returns public image feed in JSON format

---

## 🧭 Core Functionality

### 🔍 Search View

- Built with `@Published` and Combine
- `debounce(for: .milliseconds(400))` to avoid excessive API calls
- Displays a grid of thumbnails
- Automatically loads default images on empty input
- Calls appropriate search based on single or multiple tags

### 🖼 Detail View

- Full-size image display
- Image title
- Author name
- Clean HTML-parsed description
- Formatted publish date (localized)
- Image dimensions (parsed from HTML)
- Share button for image + metadata
- Animated image transition

---

## 🧪 Tests

- Basic unit test covers image fetching logic using dependency-injected mock `NetworkManaging`.
- Designed for easy testability and expansion.

---

## 🚀 Getting Started

1. **Clone the repo:**

```bash
git clone https://github.com/toto1949/FlickerImageApp.git
cd FlickerImageApp.git
```

2. **Open in Xcode:**

```bash
open FlickerImageApp.xcodeproj
```

3. **Build and Run:**
   - Run on iOS Simulator or real device (iOS 17+)

---

## ✅ Extra Credit Implemented

- [x] Dynamic Type
- [x] VoiceOver labels
- [x] UI transition animation
- [x] Image dimensions in detail
- [x] Image sharing
- [x] Unit tests
- [x] Graceful error handling

---

## 💡 Design Considerations

- Combine for reactive search
- Swift concurrency for async-safe API calls
- Avoids retain cycles with `[weak self]`
- Fully non-blocking UI
- Clean separation of concerns (MVVM)

---

## ⏱ Time Allocation

> The app was developed in under **3 hours** as per the coding challenge guidelines. Extra features were prioritized over boilerplate to maximize value within the time constraint.

---

## 📸 Demo
[![Watch the demo](https://img.youtube.com/vi/YOUR_VIDEO_ID/0.jpg)](https://drive.google.com/file/d/1RxM1xREAI5kA6Uw0ddFbr1K6vMqrZLDM/view?usp=drive_link)

---

## 👤 Author

**Taoufiq El Moutaouakil**  
Senior iOS Developer  
[LinkedIn](https://www.linkedin.com/in/taoufiq-el-moutaouakil-746374228/) • [Portfolio](https://www.taoufiqelmoutaouakil.info.s3-website-us-east-1.amazonaws.com/)




