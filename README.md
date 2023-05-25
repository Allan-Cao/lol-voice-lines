# LoL Voice Lines Dataset

This project aims to provide a comprehensive machine-friendly dataset of voice lines for all champions in the popular online game League of Legends. The dataset has been created by scraping the League of Legends wiki with efforts to clean up the data to remove inconsistencies. Although the author has done his best to clean up the data, it is essential to note that certain outliers may still exist in the dataset.

## Data Cleaning Methodology

- Actions (indicated by the boolean `is_spoken`) are non-spoken text in the format `"champion name" + "verb"`. (e.g. Ahri cries., Ahri giggles.)
- Sound effects (often written as `<effect> SFX` in the wiki) have been removed as they are neither spoken nor non-spoken *text*.
- Voice lines that contain only voice line data have their outer quotations removed and are otherwise not modified.
- Voice lines that contain actions that modify the voice line have those kept in their original format, between asterisks (*) or parentheses. In that case, the voice line is kept within double quotations (").
- Sung or otherwise formatted/styled text has had its formatting removed.
- Duplicates have been removed
- Text is encoded in UTF-8 to preserve special symbols.