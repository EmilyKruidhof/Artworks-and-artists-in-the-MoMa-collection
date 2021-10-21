# Artworks and artists in the MoMa collection

These datasets are a cleaned version of the "artworks" and "artists" datasets on MoMa’s art collection made available online by the museum itself on Kaggle (https://www.kaggle.com/mfrancis23/museum-of-modern-art-collection/metadata), from which the data of this research was downloaded, and GitHub (https://github.com/MuseumofModernArt/collection). This dataset was used for the analyses for the research reported in the paper "Gender differences in representation of artists in the MoMa collection since the post-World War II period." Exploratory analyses were done in Excel by creating graphs using pivot tables.

The original “artists” file (downloaded in September 2021) consisted of 15,282 rows, each representing an artist with an ID and name (N = 15,282 artists). For each artist metadata, such as the nationality, gender, year of birth, and year of death are reported. Additionally, the “artworks” file (downloaded in September 2021) consists of 150,771 rows, each representing an artwork with a title (N = 150,771 artworks). For each artwork, metadata were also documented, such as the artist of the artwork and his or her characteristics (imported from the “artists” file), as well as year of creation and acquisition, classification of artwork, medium of artwork, and mean of acquisition (Francis & Museum of Modern Art, 2020).

Before performing the analyses, the "artworks" dataset was cleaned up in OpenRefine, where redundant whitespaces, specific characters, and combinations of symbols were removed. In addition, the variable "CreditLine" was manually recoded so that the variable only had four categories (gift, purchase, collection, and other). The variable "Date" was also manually recoded so that only one year was listed for each artwork. The values of the variable "Date of acquirement" were transformed to only the year of acquirement using RegExr and OpenRefine. In addition, all cases created by multiple artists and acquired before 1946 were removed from the dataset in connection with the research question. A data file of 102,249 artworks was the result. The "artists" dataset did not require any cleanup for our research question. 

References: 
