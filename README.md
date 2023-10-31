# Swiftie
 install.packages("remotes")
remotes::install_github("wjakethompson/taylor")
taylor_all_song

# Option 1: tidytuesdayR package 
## install.packages("tidytuesdayR")

tuesdata <- tidytuesdayR::tt_load('2023-10-17')
## OR
tuesdata <- tidytuesdayR::tt_load(2023, week = 42)

library(tidyverse)
library(taylor)

write_csv(taylor_album_songs, "taylor_album_songs.csv")
write_csv(taylor_all_songs, "taylor_all_songs.csv")
write_csv(taylor_albums, "taylor_albums.csv")
# Option 2: Read directly from GitHub

taylor_album_songs <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-10-17/taylor_album_songs.csv')
taylor_all_songs <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-10-17/taylor_all_songs.csv')
taylor_albums <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-10-17/taylor_albums.csv')

@Manual{,
  title = {taylor: Lyrics and Song Data for Taylor Swift's Discography},
  author = {W. Jake Thompson},
  year = {2023},
  note = {https://taylor.wjakethompson.com,
https://github.com/wjakethompson/taylor},
}
