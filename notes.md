# Thoughts about functionality

## Data types
There are two types of data (names in progress, we should try to be as generic as possible):
- `Identification`: the identification of a given set of samples (scales in this case) against a given set of criteria.
- `Description`: the "solution key" taken from a book (e.g. Braeger and Moritz) which, for each species, contains the possible valid values of each morphological characteristic. Columns are characteristics and rows are species.
- `CorrelationMatrix`: the matrix with a set of species as rows and columns. Eachs entry is a value between -1 and 1 that tells the "likelihood" of the species in the row to be identified as the species in the column.

## Things we can do with the data
There are multiple things we can do with the various data types:
- Given an `Identification` and a `Description`:
    - compute the scores and provide the potential identifications (`analyse`).
- Given a `Description`: 
    - generate the `CorrelationMatrix` of all species (`generate_correlation_matrix`).
- Given a `CorrelationMatrix`:
    - plot it as a heatmap (`plot`).
    - compute the symmetric `CorrelationMatrix` by averaging the matrix with its transpose (`symmetric`).
    - cluster the various species according to their similarity (`generate_dendrogram`).

## Other things we can do
- Generate random sample sheets with images taken from books. 

## Next steps
- Consider morphometric characteristics?