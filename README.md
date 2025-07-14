Set Up a Virtual Environment (Optional but Recommended):

bash
python3 -m venv venv
source venv/bin/activate       # Linux/macOS
venv\Scripts\activate          # Windows
Install Required Dependencies:

bash
pip install -q faiss-cpu torch torchvision transformers gradio pillow requests tqdm matplotlib seaborn scikit-learn
Usage Instructions
Each implementation includes code to download sample images from the web and build indices for a local image folder.

Running the Multi-Modal Image Search Engine with Advanced Analytics
Start the System:

The system downloads sample images (by default, 60 images) and builds indices for each model.
It then launches a Gradio web interface with multiple tabs for various visualizations.
Querying:

Choose either Image Search or Text Search.
Select the desired model from the dropdown (ResNet50 / ViT / CLIP).
Adjust the number of results and then click the search button.
Results along with various analytical charts will be displayed.
Running the Google-Style Image Search
Start the System:

The system downloads sample images (default is 50 images) and builds indices.
A Gradio interface with a Google-like look is launched.
Querying:

Choose between text and image search using a radio button.
For image search, upload an image; for text search, input a search query (only supported with CLIP).
Adjust settings such as model selection and number of results, and click the search button.
The resulting gallery of images will display similarity badges on each image.
Project Structure
nsis
.
├── main.py                   # Main entry point; contains the code for initializing and launching the UI.
├── advanced_engine.py        # Contains the Multi-Modal Image Search Engine with Advanced Analytics.
├── google_style_engine.py    # Contains the Google-Style Image Search implementation.
├── requirements.txt          # Lists all dependencies.
├── image_database/           # Folder for downloaded sample images.
├── README.md                 # This file.
└── LICENSE                   # License file (MIT).
Configuration
Image Folder:
Default image download folder is set to ./image_database. Adjust paths if using your own dataset.
Model Options:
Models are loaded and selected through the constructor lists (i.e., ['resnet50', 'vit', 'clip']).
Search Parameters:
Modify the default number of search results, similarity thresholds, or visualization settings directly in the code if needed.
Contributing
Contributions, improvements, and bug fixes are welcome. Please:

Open an issue to discuss changes.
Fork the repository and submit a pull request.
Follow the existing coding style and add tests or documentation for new features.
License
This project is licensed under the MIT License. See the LICENSE file for details.

Thank you for exploring this repository! Choose the implementation that best fits your application and feel free to provide feedback or contribute.





