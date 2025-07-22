# 🎧 Amharic PDF to Audio Converter

A professional, responsive web application that converts Amharic PDF documents to audio using advanced text-to-speech technology.

![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Responsive](https://img.shields.io/badge/responsive-✓-brightgreen.svg)

## ✨ Features

### 🎨 **Professional Design**
- Modern gradient-based UI with clean aesthetics
- Responsive design that works on all devices
- Professional typography using Inter font family
- Intuitive card-based layout with proper visual hierarchy
- Beautiful animations and hover effects

### 📱 **Responsive & Mobile-First**
- CSS Grid layout that adapts to all screen sizes
- Touch-friendly interface for mobile devices
- Optimized layouts for desktop, tablet, and mobile
- Flexible containers and fluid typography

### 🔧 **Advanced Functionality**
- **Drag & Drop Upload**: Intuitive file upload with visual feedback
- **File Validation**: Automatic PDF format and size validation (50MB limit)
- **Progress Tracking**: Real-time progress indicator during PDF processing
- **Text Extraction**: Advanced PDF text extraction using PDF.js
- **Audio Controls**: Play, pause, stop, and volume control
- **Smart Voice Selection**: Automatic Amharic voice preference
- **Error Handling**: Comprehensive error handling with user-friendly messages

### 🌐 **Language Support**
- Primary support for Amharic (am-ET) language
- Fallback voice selection for better compatibility
- Right-to-left text direction support

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for loading external fonts and PDF.js library)

### Installation
1. Clone or download the repository
2. Open `index.html` in a web browser
3. Or serve it using a local web server:
   ```bash
   python3 -m http.server 8000
   # Then visit http://localhost:8000
   ```

## 📖 Usage

1. **Upload PDF**: 
   - Click the upload area or drag & drop your Amharic PDF file
   - Files up to 50MB are supported

2. **Process Document**:
   - Click "Process PDF" to extract text
   - Monitor progress with the progress bar
   - View extracted text in the right panel

3. **Convert to Audio**:
   - Click "Read Aloud" to start text-to-speech
   - Use volume control to adjust audio level
   - Use "Stop" button to halt playback

4. **Clear Data**:
   - Click "Clear" to reset the application

## 🛠️ Technical Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6+)
- **PDF Processing**: PDF.js library (v3.11.174)
- **Text-to-Speech**: Web Speech API
- **Styling**: CSS Grid, Flexbox, CSS Custom Properties
- **Icons**: Font Awesome 6.4.0
- **Typography**: Inter font family

## 🎯 Browser Support

- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+
- ⚠️ Speech synthesis availability may vary by browser and language

## 📐 Architecture

The application follows a clean, object-oriented architecture:

```
AmharicPDFConverter Class
├── File Handling
│   ├── Upload validation
│   ├── Drag & drop support
│   └── File metadata display
├── PDF Processing
│   ├── Text extraction
│   ├── Progress tracking
│   └── Error handling
├── Audio Management
│   ├── Speech synthesis
│   ├── Voice selection
│   └── Audio controls
└── UI Management
    ├── Alert system
    ├── Loading states
    └── Responsive updates
```

## 🔒 Security & Performance

- **File Validation**: Client-side PDF format and size validation
- **Error Handling**: Comprehensive try-catch blocks
- **Memory Management**: Efficient handling of large PDF files
- **Performance**: Optimized rendering and smooth animations
- **Accessibility**: ARIA labels and keyboard navigation support

## 📱 Responsive Breakpoints

- **Mobile**: < 768px (single column, touch-optimized)
- **Tablet**: 768px - 1024px (adaptive layout)
- **Desktop**: > 1024px (two-column grid layout)

## 🎨 Design System

### Colors
- Primary: #2563eb (Blue)
- Success: #059669 (Green)
- Warning: #d97706 (Orange)
- Error: #dc2626 (Red)
- Background: Linear gradient (#667eea to #764ba2)

### Typography
- Font Family: Inter (300, 400, 500, 600, 700)
- Responsive scaling with clamp()

## 📊 File Support

- **Supported Format**: PDF (.pdf)
- **Maximum Size**: 50MB
- **Text Requirements**: PDF must contain selectable text
- **Language**: Optimized for Amharic content

## 🔧 Customization

The application uses CSS custom properties for easy theming:

```css
:root {
  --primary-color: #2563eb;
  --primary-hover: #1d4ed8;
  --bg-primary: #ffffff;
  /* ... more variables */
}
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly across devices
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- [PDF.js](https://mozilla.github.io/pdf.js/) for PDF processing
- [Font Awesome](https://fontawesome.com/) for icons
- [Google Fonts](https://fonts.google.com/) for typography
- Web Speech API for text-to-speech functionality

## 📞 Support

For issues or questions:
1. Check the browser console for error messages
2. Ensure your browser supports the Web Speech API
3. Verify the PDF contains selectable text
4. Try with a smaller PDF file if processing fails

---

**Built with ❤️ for the Amharic community**

*Version 2.0.0 - Professional Edition*