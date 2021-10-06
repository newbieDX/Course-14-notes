# Course-14-notes
# Map making

There are many ways to make maps
1. Visualization in R: ggmap, tmap
2. INLA and Shiny
3. GIS and spatial analysis
4. Leaflet

# R package sf
ggplot2 geom_sf


# Let's make some maps!!

R-code:
library(sf);library("rnaturalearth");library("rnaturalearthdata")
world <- ne_countries(scale = "medium", returnclass = "sf")
ret <- class(world)
world %>% ggplot() + geom_sf(aes(fill = pop_est)) + scale_fill_viridis_c(option = "plasma", trans = "sqrt")
coord_sf(xlim = c(

