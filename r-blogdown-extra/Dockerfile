FROM c6prmk/r-blogdown:ubuntu
MAINTAINER Can Altıparmak <can6parmak@gmail.com>
RUN R -q -e "install.packages(c('readr', 'DT', 'leaflet', 'quantmod', 'dygraphs'), repo='https://cran.rstudio.com')"
CMD ["R"]

