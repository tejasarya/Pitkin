# Pitkin

library(sf)

.councildistricts.geojson <-
st_read("City_Council_Districts.geojson")

find_district <- function(lon, lat, sp_polygon = .councildistricts.geojson) {
    res <- character(0)
    cnt = 1
    
    for(lo in lon){
        la <- lat[cnt]
        which.row <- sf::st_contains(sp_polygon, sf::st_point(c(lo,la)), sparse = FALSE) %>%
        grep(TRUE, .)
        
        cnt <- cnt+1
        
    }
    return(res)
}
