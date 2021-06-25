

Music is consumed daily by millions of animals, endless artifacts of art, that invoke emotions, thoughts or simply provide piece of mind. Music taste is a subjective with many qualitative factors, nevertheless looking at these compositions as amalgation of lyrical and audio features might help in indentifying trends and cluster usefull for music recommendation systems.

## Data Description

1. [Billboard Hot 100](https://www.billboard.com/charts/hot-100) charts are used as initial starting point. The Billboard charts tabulate the relative weekly popularity of songs and albums in United States. Weekly Hot 100 charts from year 1960 to 2020 were scraped with help of Beautiful Soup, a total of 28K+ unqiue tracks with artist and song names were saved.

2. As these charts only mention artist and song title with their weekly rank, [Spotify API](https://developer.spotify.com/documentation/web-api/) is used to obtain audio features such as:

- Danceability: Danceability describes how suitable a track is for dancing, a value of 0.0 is least danceable and 1.0 is most danceable.
- Acousticness: whether the track is acoustic, a measure from 0.0 to 1.0.
- Energy: Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. 
- Instrumentalness: The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content.
- Liveness: Higher liveness values represent an increased probability that the track was performed live.
- Loudness: The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track. Values typical range between -60 and 0 db.
- Speechiness: Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value.
- Tempo: The overall estimated tempo of a track in beats per minute (BPM). 
- Valence: A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).

3. Lyrics for the given set of tracks was obtained from [Genius API](https://docs.genius.com/). Additonal features described below were derived and saved along with lyrical text files.

- Overall Lyrical Sentiment (pos, neg, neu, compound) 
- Flesch-Kincaid Grade Level: which is equivalent to the US grade level of education, It shows the required education to be able to understand a text.
- Flesch Reading Ease: it gives a text a score between 1 and 100, with 100 being the highest readability score.
- Gunning fog index: a readability test for English writing, the index estimates the years of formal education a person needs to understand the text on the first reading.
- #num of difficult words
- #num of syllables
- #num of words
- #num of repeated lines

