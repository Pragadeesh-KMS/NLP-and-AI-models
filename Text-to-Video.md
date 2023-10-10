
# Text-to-Video Generation with Diffusers and Transformers

[![Open in Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/19zgHhigij_PzCyNEkR8aduPcaU62rmAq?usp=sharing)
Use the above link to access the colab file.


This code snippet demonstrates how to generate a video from a text prompt using Diffusers, Transformers, and PyTorch. It utilizes the `diffusers` library to create a Diffusion Pipeline for text-to-video generation.

## Installation

To run this code, you'll need to install the necessary Python libraries using pip:

```bash
!pip install diffusers transformers accelerate torch -q
```

## Usage

```python
import torch
from diffusers import DiffusionPipeline, DPMSolverMultistepScheduler
from diffusers.utils import export_to_video

# Create a Diffusion Pipeline
pipe = DiffusionPipeline.from_pretrained("damo-vilab/text-to-video-ms-1.7b", torch_dtype=torch.float16, variant="fp16")

# Configure the scheduler
pipe.scheduler = DPMSolverMultistepScheduler.from_config(pipe.scheduler.config)

# Enable model CPU offload
pipe.enable_model_cpu_offload()

# Define a text prompt
prompt = "dog chasing a man"

# Generate video frames from the text prompt
video_frames = pipe(prompt, num_inference_steps=25).frames

# Specify the desired output video file path
video_path = "output.mp4"

# Export video frames to the specified video file
export_to_video(video_frames, video_path)
```

Replace `"dog chasing a man"` with your desired text prompt, and specify the desired output video file path in `video_path`.

