# Audio Minutes Generator

A Python-based AI agent that converts audio recordings into detailed meeting minutes using LLaMA and OpenAI APIs. This tool automates the process of transcribing and summarizing meetings, saving time and improving accessibility.

## Features

- Audio file input support (WAV, MP3, M4A)
- Speech-to-text conversion using OpenAI's Whisper API
- Intelligent summarization using LLaMA for initial processing
- Enhanced context understanding with OpenAI GPT for final output
- Structured meeting minutes generation with key points, action items, and decisions
- Support for multiple speakers identification
- Markdown and PDF export options

## Prerequisites

- Python 3.8 or higher
- OpenAI API key
- LLaMA API key
- ffmpeg (for audio processing)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/audio-minutes-generator.git
cd audio-minutes-generator
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your API keys
```

## Usage

1. Basic usage:
```python
from audio_minutes import MinutesGenerator

generator = MinutesGenerator('path/to/audio/file.mp3')
minutes = generator.generate()
```

2. With custom configuration:
```python
config = {
    'language': 'en',
    'identify_speakers': True,
    'output_format': 'markdown'
}
generator = MinutesGenerator('path/to/audio/file.mp3', config)
minutes = generator.generate()
```

## Configuration Options

- `language`: Target language for transcription (default: 'en')
- `identify_speakers`: Enable speaker identification (default: True)
- `output_format`: Choose between 'markdown' or 'pdf' (default: 'markdown')
- `summarization_level`: Control summary detail level (1-5, default: 3)
- `include_timestamps`: Add timestamps to minutes (default: False)




## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- OpenAI for their Whisper API
- LLaMA team for their language model
- Contributors and maintainers

## Contact

For support or questions, please open an issue on the GitHub repository or contact [your-email@example.com].
