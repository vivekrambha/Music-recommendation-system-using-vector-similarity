# Music Recommendation System using Vector Similarity

This project implements an innovative music recommendation system that leverages segment pitches from the Million Song Dataset (MSD) and lyrical content from the Musixmatch dataset. The system uses LibROSA to extract segment pitches, process musical features, and compute cosine similarity to suggest similar songs.

## Features

- Segment pitch-based recommendation
- Lyrics-based recommendation
- A/B testing for evaluating recommendation effectiveness

## Methodology

The project consists of four major stages:

1. Data collection and feature extraction
2. Similarity calculation
3. Recommendation generation
4. Evaluation via A/B testing

### Feature Extraction

- Segment Pitches: Extracted from MSD HDF5 files and MP3 files using LibROSA
- Lyrics: Processed from Musixmatch dataset in bag-of-words format

### Similarity Calculation

Cosine similarity is used to measure the similarity between songs based on:
- Segment pitches vectors
- Lyrics word count vectors

### Recommendation Generation

The system generates recommendations by selecting the top N songs with the highest similarity scores for both segment pitches and lyrics.

## Dataset

The project uses the following datasets:

1. Million Song Dataset (MSD): For segment pitches
   - Download: [MSD Subset](http://millionsongdataset.com/pages/getting-dataset/#subset)

2. Musixmatch Dataset: For lyrics
   - Train set: [mxm_dataset_train.txt.zip](http://millionsongdataset.com/sites/default/files/AdditionalFiles/mxm_dataset_train.txt.zip)
   - Test set: [mxm_dataset_test.txt.zip](http://millionsongdataset.com/sites/default/files/AdditionalFiles/mxm_dataset_test.txt.zip)
   - SQLite database: [mxm_dataset.db](http://millionsongdataset.com/sites/default/files/AdditionalFiles/mxm_dataset.db)

## Setup

1. Clone this repository
2. Download the datasets and place them in the appropriate directories
3. Install the required dependencies (LibROSA, Pandas, NumPy, scikit-learn, NLTK)
4. Update the file paths in the code to match your local setup

## Usage

Run the parts of the file in ascending order:

1. Data collection and feature extraction
2. Similarity calculation
3. Recommendation generation
4. Evaluation via A/B testing

## Results

The system was evaluated using A/B testing with 24 participants. Key findings include:

- 62% of users preferred recommendations based on segment pitches, while 38% preferred those based on lyrics
- 41.7% of respondents preferred rhythm when looking for new music, 33.3% valued both lyrics and rhythm equally, and 25% preferred lyrics
- The effectiveness of segment pitches vs lyrics-based recommendations varied depending on the song

## Evaluation Insights

- Age groups 21-25 and 26-30 showed the most diverse music genre preferences
- For one test song, lyrics-based recommendations were slightly preferred
- For another test song, segment pitch-based recommendations were strongly preferred

## Future Work

- Integrate additional features such as timbre
- Expand analysis to include personal playlists
- Develop a feature to analyze a user's personal playlist and generate a unique vector matrix
- Use the unique vector matrix to recommend various playlists, increasing diversity and number of song recommendations

## Contributing

Contributions to improve the system are welcome. Please feel free to submit a Pull Request.

## Acknowledgments

- Million Song Dataset
- Musixmatch Dataset
- LibROSA library
- Queen Mary University of London
