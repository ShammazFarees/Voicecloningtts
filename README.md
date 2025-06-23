# Voice Cloning with Open-Source TTS Models

## Features
- Clone voices from short audio samples (<10 seconds)
- Fine-tune models efficiently using LoRA
- Support for multiple TTS models (XTTS-v2, YourTTS, etc.)
- Generate natural-sounding speech with proper prosody
- Hugging Face integration for easy model sharing

## Installation
git clone https://github.com/ShammazFarees/Voicecloningtts.git
cd VoiceCloningTTS
pip install -r requirements.txt

## Quick Start
o Prepare your dataset:
python preprocess.py --input_dir ./samples --output_dir ./processed
o Fine-tune the model:
python train.py --config configs/lora_config.yaml
o Generate cloned voice:
from inference import clone_voice
clone_voice(text="Hello world!", reference_audio="target.wav", output_path="output.wav")

## Supported Models
XTTS-v2
YourTTS
CSM-1B (for conversational TTS)

## Project Structure
VoiceCloningTTS/
├── configs/          # Configuration files
├── data/             # Sample datasets
├── models/           # Pretrained models
├── scripts/          # Utility scripts
├── inference.py      # Voice cloning demo
├── train.py          # Training script
└── requirements.txt  # Dependencies

## Results
Model	Naturalness (1-5)	Training Time (hrs)	VRAM Usage
XTTS-v2	4.3	6	16GB
+ LoRA	4.1	3	8GB

## References
XTTS-v2 Paper
LoRA Paper
HuggingFace TTS

## License
MIT License 
