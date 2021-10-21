# Artworks and artists in the MoMa collection

These datasets are a cleaned version of the "artworks" and "artists" datasets on MoMa’s art collection made available online by the museum itself on Kaggle (https://www.kaggle.com/mfrancis23/museum-of-modern-art-collection/metadata), from which the data of this research was downloaded, and GitHub (https://github.com/MuseumofModernArt/collection). This dataset was used for the analyses for the research reported in the paper "Gender differences in representation of artists in the MoMa collection since the post-World War II period." Exploratory analyses were done in Excel by creating graphs using pivot tables.


**The original dataset**

The original “artists” file (downloaded in September 2021) consisted of 15,282 rows, each representing an artist with an ID and name (N = 15,282 artists). For each artist metadata, such as the nationality, gender, year of birth, and year of death are reported. Additionally, the “artworks” file (downloaded in September 2021) consists of 150,771 rows, each representing an artwork with a title (N = 150,771 artworks). For each artwork, metadata were also documented, such as the artist of the artwork and his or her characteristics (imported from the “artists” file), as well as year of creation and acquisition, classification of artwork, medium of artwork, and mean of acquisition.


**Cleaning of the dataset**

To clean up the “artworks” dataset, the csv file was first imported into OpenRefine. Firstly, in OpenRefine, the leading and trailing whitespaces were removed for each column. Next, specific characters, such as hyphens and parentheses, and common combinations of redundant symbols, such as “c.”, were removed in the columns that required it by using a Python code. Three variables that we wanted to use in the analyses needed further cleaning, namely means of acquisition (“CreditLine” in the original data file), year of creation (“Date”), and year of acquirement (“DateAcquired”). This will be further explained below.

For “means of acquisition”, all 953 original values were manually divided into four different categories: gift (N = 78,851), collection (N = 11,926), purchase (N = 9,387), and other (N = 225, missing value). The value purchase was assigned when the original value showed that the museum intended to acquire the artwork. The value “gift” was assigned when it showed that the museum had acquired the artwork through someone else. Finally, the value “collection” had been awarded to artworks acquired in large quantities at a time by the museum.

The variable year of creation was also manually recoded, because the notation could vary enormously from case to case. For example, in many cases months were also mentioned or even multiple years. It was therefore decided to assign only one year, namely the year that was mentioned first.
The variable year of acquisition consisted of an exact date in the format “dd/mm/yyyy” in the original data file. Since the year of acquirement was sufficient for our analysis, the original format was converted to the format “yyyy-mm-dd” in RegExr and then a new column was created in Excel in which only the year was noted.
Finally, to make the data file more manageable, we chose to remove some cases from the data file. Firstly, the artworks that were made by multiple artists were removed, because this would also make analyzing the gender of the artists more difficult. Secondly, the artworks that had been acquired by the museum before the end of the Second World War period (1946) were also removed in connection with the delineation of our research question. These transformations led to the final “artworks” data file (N = 102,249) used in the analyses. 
