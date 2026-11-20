## Metadata
### Data Summary
The project uses scanned artworks on the public API of the Art Institute of Chicago [3], which includes information of the year(s) the artwork was produced, 
the movement, medium, country, name of the piece, the artist, and the scanned piece. These categories allow us to create and run the classification model based 
on the genre that the curator has assigned the artwork, which range from movements, to time periods, to regional and cultural arts. This API will be scraped for 
the data, downloaded into a CSV with the images of artworks downloaded into a folder and each image in the CSV will be connected to its link, its genre, year, 
artist, country of origin, and piece name. The data will have to be preprocessed to determine the movements with enough entries to make stronger predictions and 
whether some genres have to be merged, removed, or remapped.  An additional CSV of genre names and counts was also produced by the scraping code.
### Provenance
All this data originates from the public Art Institute of Chicago API (https://api.artic.edu) and their IIIF image server, which possesses and owns the artworks 
that they have scanned and reproduced on this API. The classifications of genre, time period, name of piece, medium, and artists are all the same as the Art 
Institute of Chicago’s official site. The data was then scraped and reduced to movements that had at least five pieces within their classifications 
(a total of 1611) and saved into a CSV file produced within that Colab script and the individual images were saved into a folder holding all the individual 
scanned artworks. This API may be updated by the Art Institute of Chicago, so the pieces that are scraped may be different depending on when the code is run.
### License
The Art Institute of Chicago reproduces digital images of artwork on its public API, and was only scraped for artworks and data marked for public use and licensed 
under the Creative Commons Zero (CC0) license, which allows for reuse and for use in investigations. The scraped code ensured none of the scraped artworks were 
under copyrights limitations as well.
### Data Dictionary
| Variable | Description | Units/Type | Source |
|:---:|:---:|:---:|:---:|
title | Title of artwork | string | https://api.artic.edu
artist | Name of artist of the piece | string | https://api.artic.edu
date_display | Date artwork was officially displayed | string | https://api.artic.edu
place_of_origin | Country that art was produced in | string | https://api.artic.edu
medium | Type of medium art was created with | string | https://api.artic.edu
movement | Movement or time-period that classifies peice | string | https://api.artic.edu
all_styles | List of movements and styles that classify the piece | string | https://api.artic.edu
image_url | Link to image from public API | string | https://api.artic.edu
local_path | File path for where downloaded image is locally saved | string | https://api.artic.edu
### Exploratory Plots
<img width="2265" height="1630" alt="image" src="https://github.com/user-attachments/assets/376500d2-f169-435f-92e8-754ae827c7e1" />

<img width="2075" height="1555" alt="Screenshot 2026-11-20 144123" src="https://github.com/user-attachments/assets/f0afdb26-8e4b-42cf-bc82-4e81097fb5c6" />


