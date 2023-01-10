# Installing from my source
I've had to make some changes to the way the audio is loaded. Using soundfile to load the audio, as done [here](https://github.com/NVIDIA/NeMo/blob/main/nemo/collections/asr/parts/preprocessing/segment.py#L207), loads the audio as stereo instead of monochannel as required for our ASR experiments.

Therefore, I had to replace the loading function with librosa, see [here](https://github.com/chrisemezue/NeMo/blob/main/nemo/collections/asr/parts/preprocessing/segment.py#L207).


From source
1. Follow the installation guidelines given [here](https://github.com/NVIDIA/NeMo/tree/main#installation).
2. Use this installation mode to install my changes.

```
apt-get update && apt-get install -y libsndfile1 ffmpeg
git clone https://github.com/chrisemezue/NeMo
cd NeMo
pip install -e .
```