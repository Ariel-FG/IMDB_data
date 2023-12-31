# IMDB_data
#### data cleaning notebook
> data source and table details: [IMDB datasets](https://developer.imdb.com/non-commercial-datasets/).
## Tables used:
+ name_basics
+ title basics
+ title_ratings


## Cleaning
+ name_basics:
  - Null titles dropped
  - Date columns converted from object to numeric
  - Narrowing professions to [actor, actress, director]
  - Birth year filtered to 1900+
  - separated into three tables that contain the following:
      - table 1: nconst, primaryName, birthYear, deathYear
      - table 2: nconst, KnownForTitles (unnested)
      - table 3: nconst, primaryProfession (unnested)
+ title basics:
    - isAdult column values corrected only [0,1] accepted
    - primaryTitle column nan values dropped
    - year columns type changed and years over 2023 dropepd
    - genres column unnested
+ title ratings: no need for processing

