# IP-Adapter FaceID with Stable Diffusion

This project demonstrates the use of the **IP-Adapter FaceID** model in conjunction with the **Stable Diffusion Pipeline** to generate high-quality, photorealistic images conditioned on face embeddings. It leverages face detection and feature extraction from the **InsightFace** library and employs **Hugging Face's Diffusers** for image generation.

---

## Features

- **Face Embedding Extraction**: Uses the `buffalo_l` model from InsightFace for accurate face analysis.
- **IP-Adapter Integration**: Implements the IP-Adapter FaceID model for conditioning Stable Diffusion on face embeddings.
- **Customizable Prompts**: Generate photorealistic images guided by textual prompts.
- **High-Quality Image Output**: Outputs 512x512 images with adjustable inference steps and sampling options.
- **Easy Configuration**: Pre-trained model checkpoints are automatically downloaded from Hugging Face.

---

## Output
![image](https://github.com/user-attachments/assets/a5187095-b735-40c1-bf6e-bce60a781140)



## Setup

### Prerequisites
Ensure the following dependencies are installed:

- Python 3.8+
- CUDA-enabled GPU (recommended for faster inference)
- Required Python libraries:

```bash
pip install torch torchvision diffusers huggingface_hub insightface opencv-python matplotlib
```

---

## Usage

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Prepare the Environment
Ensure all dependencies are installed as per the prerequisites.

### 3. Place an Input Image
Copy your input image to the repository directory. Update the file path in the script:

```python
image_path = "./IMG20230128132730.jpg"
```

### 4. Run the Script
Execute the script to generate images:

```bash
python generate_images.py
```

### 5. View and Save Outputs
Generated images will be saved in the `generated` directory. You can also view them in a 2x2 grid display.

---

## Parameters

- **Prompt**: Define the content of the generated image. Example:
  ```python
  prompt = "photo of a man in black shirt"
  ```

- **Negative Prompt**: Specify undesired attributes for the output. Example:
  ```python
  negative_prompt = "monochrome, lowres, bad anatomy"
  ```

- **Inference Steps**: Adjust the number of steps for the DDIM scheduler:
  ```python
  num_inference_steps = 30
  ```

- **Seed**: Set a random seed for reproducibility:
  ```python
  seed = 2023
  ```

---

## Project Structure

```
├── generate_images.py  # Main script
├── requirements.txt    # Dependencies
├── generated/          # Output directory
├── IMG20230128132730.jpg  # Example input image
└── README.md           # Project documentation
```

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- **InsightFace** for face detection and embedding extraction.
- **Hugging Face** for providing pre-trained models and the Diffusers library.
- **Stable Diffusion** for enabling photorealistic image generation.

---

## Contact

For questions or support, feel free to reach out:
- **Email**: vedantpankar2@gmail.com
