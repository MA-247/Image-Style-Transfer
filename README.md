# Neural Style Transfer Using VGG19


## Overview

Neural Style Transfer synthesizes a new image by combining the **content** of one image with the **style** of another. This project leverages the pre-trained **VGG19** model to achieve compelling visual results, reimagining the content of a base image in the artistic style of a second image.

---

## Features

- **Content-Style Fusion**: Recreates content while applying an artistic style.
- **VGG19 Architecture**: Utilizes pre-trained layers from the VGG19 model for feature extraction.
- **Customizable Weights**: Adjust content and style influence using weighted loss parameters.
- **Optimization**: Employs the Adam optimizer for iterative loss minimization.

---

## Getting Started

### Prerequisites

- Python 3.7+
- TensorFlow
- NumPy
- Matplotlib
- Pillow

Install dependencies:
```bash
pip install tensorflow numpy matplotlib pillow
```

### Usage

1. **Prepare Images**: Place your content and style images in the project directory.
2. **Run the Script**:
    ```python
    python neural_style_transfer.py --content <path_to_content_image> --style <path_to_style_image>
    ```
3. **Output**: The generated image will be saved and displayed.

---

## Methodology

### Dataset
Two images are required:
- **Content Image**: Provides the structure and main elements.
- **Style Image**: Contributes the artistic flair.

### Model
- **VGG19**: Pre-trained on ImageNet, used to extract hierarchical features from content and style images.
- **Selected Layers**:
  - Content: `block5_conv2`
  - Style: `block1_conv1` to `block5_conv1`

### Loss Functions
- **Content Loss**: Preserves the structure of the content image.
- **Style Loss**: Matches the style image's textures using Gram matrices.
- **Total Loss**: Combines content and style loss weighted by customizable parameters.

---

## Results

- **Content Loss**: \(2.0556 \times 10^6\)
- **Style Loss**: \(2.1377 \times 10^6\)
- **Total Loss**: \(4.1934 \times 10^6\)

---

## Future Work

- **Efficiency**: Use modern architectures like EfficientNet for faster computation.
- **Real-Time Transfer**: Implement methods with instance normalization.
- **GANs**: Leverage generative models for higher realism and versatility.
- **Control**: Enable user-defined blending of multiple styles.

---

## Authors

- **Sheheryar Sohail** - [sohailsheheryar226@gmail.com](mailto:sohailsheheryar226@gmail.com)
- **Murtaza Anwaar** - [murtazaanwaar@gmail.com](mailto:murtazaanwaar@gmail.com)

---

