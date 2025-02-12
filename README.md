# Color Palette Emotion Analysis 🎨
A data science project exploring the emotional impact of color palettes in famous artworks. By analyzing the colors used in art and their associated emotions, this project uncovers the hidden emotional language artists use to tell stories through color.

## Table of Contents
- Introduction
- Objectives
- Installation
- Usage
- Data
- Analysis Methods
- Results & Insights
- Contributing
- License

## Introduction
This project investigates how the color choices in famous paintings affect their emotional expression. Using machine learning techniques like KMeans clustering, the project extracts dominant color palettes from images of artworks and maps those colors to specific emotions. Additionally, advanced analyses such as color harmony detection and art movement comparisons help provide further insights into how artists use color to evoke particular feelings.

## Objectives
**Color Palette Extraction:** Extract dominant colors from paintings using KMeans clustering.

**Emotional Mapping:** Map color palettes to specific emotions to analyze how colors influence emotional responses.

**Advanced Analysis:**
- Investigate color harmonies (e.g., complementary, analogous, triadic).
- Compare emotional palettes across various art movements (Renaissance, Baroque, Modernism).

**Visualization:** Visualize color palettes, emotional distributions, and other advanced insights to understand the emotional impact of colors in art.

## Installation
To get started, clone this repository and install the necessary dependencies:

```
git clone https://github.com/spitzer4/color-palette-emotion-analysis.git

cd color-palette-emotion-analysis

pip install -r requirements.txt
```

## Usage
**1. Load Artwork Images**
Place your artwork images in the artworks/ folder. The project will automatically load all .jpg or .png files in this folder.

**2. Extract Color Palettes**
The project will extract color palettes from the artwork images and display them.

```
# Load and process images

from image_processing import load_images, extract_colors, plot_palette

images, filenames = load_images('artworks/')

for img, fname in zip(images, filenames):
    palette = extract_colors(img)
    plot_palette(palette, title=f'Palette of {fname}')
```

**3. Emotional Mapping**
Map the extracted color palettes to emotions using predefined rules.

```
from emotion_analysis import analyze_emotions

emotions = analyze_emotions(palette)

print(emotions)
```

**4. Advanced Analysis**
Perform color harmony analysis (Complementary, Analogous, Triadic) and compare emotional palettes across different art movements.

```
from advanced_analysis import analyze_harmony, get_art_movement

# Get color harmonies
harmonies = analyze_harmony(palette)
```

## Data
The dataset consists of images of famous artworks. You can either use your own collection or download public datasets from sources like:

**WikiArt Dataset:**
Kaggle Artworks Dataset

Place the artwork images in the artworks/ folder for processing.

## Analysis Methods
- **KMeans Clustering:** Used to extract dominant colors from the artwork images.
- **Emotional Mapping:** Colors are mapped to specific emotions based on predefined color-emotion associations.
- **Color Harmony:** Analyzing complementary, analogous, and triadic color relationships to understand their emotional impact.
- **Art Movement Comparison:** Categorizing artworks based on their movement (Renaissance, Baroque, etc.) to compare color-emotion patterns.

## Results & Insights
