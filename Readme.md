# Multi-Modal Image Search Engine & Google-Style Image Search

This repository contains two implementations of image search systems. The code is provided in two distinct modes:

1. **Multi-Modal Image Search Engine with Advanced Analytics:**  
   - Uses three state-of-the-art models (ResNet50, Vision Transformer, and CLIP) for feature extraction.  
   - Supports searching by image or by text (CLIP-only).  
   - Provides detailed analytical visualizations such as similarity charts, model comparisons, t-SNE feature space projection, similarity distribution analysis, heatmaps, and confidence analysis.  
   - Built with an interactive Gradio UI where users can switch between search modes and view several analytical plots.

2. **Google-Style Image Search:**  
   - Mimics the visual style of Google Image Search.  
   - Uses similar models (ResNet50, ViT, CLIP) to extract features from images.  
   - Displays a “similarity badge” on images (in a style similar to Google’s view).  
   - Provides a simplified Gradio interface with a layout that closely resembles Google Image Search.  
   - Supports both text-based (only available with CLIP) and image-based queries.

Both implementations use major open-source libraries such as PyTorch, FAISS, Gradio, and Transformers. Each version downloads sample images from online sources (e.g. Picsum) and builds the index for similarity search from a local image folder.

---

## Table of Contents

1. [Overview](#overview)  
2. [Features](#features)  
3. [Installation](#installation)  
4. [Usage Instructions](#usage-instructions)  
5. [Project Structure](#project-structure)  
6. [Configuration](#configuration)  
7. [Contributing](#contributing)  
8. [License](#license)  

---

## Overview

This repository offers two different code implementations for image search:

- The **Multi-Modal Image Search Engine with Advanced Analytics** provides detailed analysis and visualization of search results with multiple graphs. It supports both image-to-image and text-to-image queries by leveraging three pre-trained models.
- The **Google-Style Image Search** mimics the popular Google Images interface, offering a clean and simple design that highlights similarity scores with a badge, much like the official Google interface.

---

## Features

### Multi-Modal Image Search Engine with Advanced Analytics

- **Models Supported:**  
  - ResNet50 (CNN)  
  - Vision Transformer (ViT)  
  - CLIP (for both image and text queries)

- **Query Modes:**  
  - Image-based search  
  - Text-based search (using CLIP only)

- **Analytical Visualizations:**  
  - Similarity Bar and Pie Charts  
  - Model Comparison Charts  
  - t-SNE Feature Space Projections  
  - Similarity Distribution and Boxplots  
  - Heatmaps showing model-result overlap  
  - Confidence and decay rate analysis

- **Interactive UI:**  
  - Built with Gradio, featuring tabs for multiple chart views and sample search examples.

### Google-Style Image Search

- **Models Supported:**  
  - ResNet50, Vision Transformer, and CLIP

- **Query Modes:**  
  - Image-based search and text-based search (CLIP only)

- **Interface Highlights:**  
  - Similarity badge overlays on images (appearing in the top-left corner)  
  - Layout inspired by Google Image Search with examples and settings in an accordion

- **Interactive UI:**  
  - Simple Gradio interface, allowing users to choose between text and image queries, adjust parameters, and view results in a gallery.

---

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/multi-modal-image-search.git
   cd multi-modal-image-search
   ```

2. **Set Up a Virtual Environment (Optional but Recommended):**

   ```bash
   python3 -m venv venv
   source venv/bin/activate       # Linux/macOS
   venv\Scripts\activate          # Windows
   ```

3. **Install Required Dependencies:**

   ```bash
   pip install -q faiss-cpu torch torchvision transformers gradio pillow requests tqdm matplotlib seaborn scikit-learn
   ```

---

## Usage Instructions

Each implementation includes code to download sample images from the web and build indices for a local image folder.

### Running the Multi-Modal Image Search Engine with Advanced Analytics

1. **Start the System:**  
   - The system downloads sample images (by default, 60 images) and builds indices for each model.  
   - It then launches a Gradio web interface with multiple tabs for various visualizations.

2. **Querying:**  
   - Choose either **Image Search** or **Text Search**.  
   - Select the desired model from the dropdown (ResNet50 / ViT / CLIP).  
   - Adjust the number of results and then click the search button.  
   - Results along with various analytical charts will be displayed.

### Running the Google-Style Image Search

1. **Start the System:**  
   - The system downloads sample images (default is 50 images) and builds indices.  
   - A Gradio interface with a Google-like look is launched.

2. **Querying:**  
   - Choose between text and image search using a radio button.  
   - For image search, upload an image; for text search, input a search query (only supported with CLIP).  
   - Adjust settings such as model selection and number of results, and click the search button.  
   - The resulting gallery of images will display similarity badges on each image.

---

## Project Structure

```
.
├── main.py                   # Main entry point; contains the code for initializing and launching the UI.
├── advanced_engine.py        # Contains the Multi-Modal Image Search Engine with Advanced Analytics.
├── google_style_engine.py    # Contains the Google-Style Image Search implementation.
├── requirements.txt          # Lists all dependencies.
├── image_database/           # Folder for downloaded sample images.
├── README.md                 # This file.
└── LICENSE                   # License file (MIT).
```

---

## Configuration

- **Image Folder:**  
  Default image download folder is set to `./image_database`. Adjust paths if using your own dataset.

- **Model Options:**  
  Models are loaded and selected through the constructor lists (i.e., `['resnet50', 'vit', 'clip']`).

- **Search Parameters:**  
  Modify the default number of search results, similarity thresholds, or visualization settings directly in the code if needed.

---

## Contributing

Contributions, improvements, and bug fixes are welcome. Please:

- Open an issue to discuss changes.  
- Fork the repository and submit a pull request.  
- Follow the existing coding style and add tests or documentation for new features.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Thank you for exploring this repository! Choose the implementation that best fits your application and feel free to provide feedback or contribute.

---

