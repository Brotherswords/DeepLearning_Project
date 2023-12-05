# Audio Separation Project Using U-Net
## Project Overview
This project focuses on separating audio components from complex spectrogram data using a modified U-Net architecture. The goal is to isolate individual elements (such as vocals, drums, and bass) from mixed audio signals, which is a significant challenge in the field of audio processing. This project was done by Lavan Vivekanandasarma, Brian Hagerty, Jake McKnight, Matt Ward

## Model Description
The core of this project is the Spectrogram U-Net model, a deep learning model designed to handle high-resolution audio spectrograms. The model's architecture is tailored for the efficient processing of audio data and includes the following key components:

## Input Layer: Accepts spectrograms with a shape of 1025x20680x1.
- Downsampling Path: A series of convolutional layers with batch normalization and dropout, extracting features at multiple scales.
- Skip Connections: Preserve detailed spatial information through the network.
- Bottleneck Layer: Processes the most abstracted features of the audio.
- Upsampling Path: Expands the processed features and combines them with details from the skip connections.
- Output Layer: Produces the final separated audio component using a linear activation function.
