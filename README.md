# Amharic PDF to Audio Converter

A professional web application that converts Amharic PDF documents to audio with enhanced text-to-speech functionality.

## Features

- **PDF Text Extraction**: Extract Amharic text from PDF documents
- **Multiple TTS Options**: Browser TTS, Azure Cognitive Services, Google Cloud TTS
- **Native Amharic Voices**: Support for high-quality Amharic speech synthesis
- **Smart Voice Detection**: Automatically detect and use the best available Amharic voice
- **Cloud TTS Integration**: Use Azure or Google Cloud for premium Amharic voices
- **Responsive Design**: Works on desktop and mobile devices

## How to Improve Amharic Audio Output

### Problem
Most browsers don't have built-in Amharic voices, resulting in poor audio quality when using browser TTS.

### Solutions

#### 1. **Use Azure Cognitive Services (Recommended)**

Azure provides high-quality native Amharic voices:

- **Voices Available**:
  - `am-ET-MekdesNeural` (Female) - Natural sounding
  - `am-ET-AmehaNeural` (Male) - Natural sounding

- **Setup**:
  1. Go to [Azure Speech Services](https://azure.microsoft.com/services/cognitive-services/speech-services/)
  2. Create a free account (includes 500,000 characters/month free)
  3. Get your API key from the Azure portal
  4. In the app, click "TTS Settings"
  5. Select "Azure Cognitive Services"
  6. Enter your API key and region
  7. Choose your preferred Amharic voice

#### 2. **Use Google Cloud Text-to-Speech**

Google Cloud also supports Amharic TTS:

- **Setup**:
  1. Go to [Google Cloud TTS](https://cloud.google.com/text-to-speech)
  2. Create a project and enable the TTS API
  3. Get your API key
  4. In the app, select "Google Cloud TTS" in settings
  5. Enter your API key

#### 3. **Browser Voice Optimization**

For browsers that do support some Amharic voices:

- **Enhanced Detection**: The app now searches for:
  - Language codes: `am`, `AM`, `am-ET`
  - Voice names containing: `amharic`, `ethiopia`
  - Related languages with similar scripts (Arabic, Hebrew, etc.)

- **Smart Fallback**: When no Amharic voice is found:
  1. Tries Arabic/Hebrew voices (similar script systems)
  2. Falls back to high-quality English voices
  3. Provides clear notifications about voice selection

## Technical Improvements Made

### 1. **Enhanced Voice Detection**
```javascript
const amharicVoice = voices.find(voice => 
  voice.lang.includes('am') || 
  voice.lang.includes('AM') ||
  voice.lang === 'am-ET' ||
  voice.name.toLowerCase().includes('amharic') ||
  voice.name.toLowerCase().includes('ethiopia')
);
```

### 2. **Cloud TTS Integration**
- Azure Speech Services integration with SSML
- Automatic audio blob generation and playback
- Error handling with fallback to browser TTS
- Support for multiple Amharic neural voices

### 3. **Smart Fallback System**
- Priority-based voice selection
- Unicode-friendly voice preferences
- Detailed logging for debugging

### 4. **Settings Management**
- Persistent settings storage
- Real-time TTS provider switching
- Voice testing functionality
- Easy configuration reset

## Usage Instructions

1. **Open the Application**
   ```bash
   # Start a local web server
   python3 -m http.server 8000
   # Open http://localhost:8000 in your browser
   ```

2. **Configure TTS Settings**
   - Click "TTS Settings" button
   - Choose your preferred TTS provider
   - Enter API credentials if using cloud services
   - Test your voice settings

3. **Process PDF**
   - Upload an Amharic PDF file
   - Click "Process PDF" to extract text
   - Click "Read Aloud" to hear the audio

## Best Practices for Amharic TTS

1. **Use Cloud Services**: For best results, use Azure or Google Cloud TTS
2. **Choose Appropriate Voice**: Female voices often have better Amharic pronunciation
3. **Adjust Speed**: Slower speech rates (0.8-0.9) improve comprehension
4. **Test Different Providers**: Some voices handle specific Amharic dialects better
5. **Chunk Long Text**: Break very long documents into smaller sections

## Troubleshooting

### No Amharic Voice Available
- Check if you're using a supported cloud TTS provider
- Verify your API keys are correct
- Try different browser (Chrome/Edge have better voice support)

### Poor Audio Quality
- Switch from Browser TTS to Azure/Google Cloud
- Adjust voice speed and pitch settings
- Try different voice options (male/female)

### API Errors
- Check your internet connection
- Verify API key permissions
- Ensure you haven't exceeded usage limits

## Development

Built with:
- Vanilla JavaScript (ES6+)
- PDF.js for PDF processing
- Web Speech API for browser TTS
- Azure Speech Services API
- Google Cloud Text-to-Speech API

## License

© 2024 Amharic PDF to Audio Converter. Developed by Melkamu Muluneh.