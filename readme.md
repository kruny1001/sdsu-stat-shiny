https://hub.docker.com/r/rocker/shiny/

#Build Shiny Server Image
docker build -t ge-lab/shiny .

#Run Shiny Server Docker Image
docker run --rm -p 3838:3838 \
    -v $(pwd)/shinyapps/:/srv/shiny-server/ \
    -v $(pwd)/shinylog/:/var/log/ \
    ge-lab/shiny

docker run --rm -p 3838:3838 \
  -v $(pwd)/shinyapps/:/srv/shiny-server/ \
  -v $(pwd)/shinylog/:/var/log/ \
  rocker/shiny

docker run --rm -p 3838:3838 -v $(pwd)/shinyapps/:/srv/shiny-server/ -v $(pwd)/shinylog/:/var/log/ ge-lab/shiny


docker run -d -p 3838:3838 \
    -v $(pwd)/shinyapps/:/srv/shiny-server/ \
    -v $(pwd)/shinylog/:/var/log/ \
    gelab/shiny

#access terminal
sudo docker exec -i -t tender_hugle /bin/bash

R

gplots
install.packages("gplots")

PGSEA
source("https://bioconductor.org/biocLite.R")
biocLite("PGSEA")
biocLite("fgsea")
biocLite("gage")
biocLite("ReactomePA")
biocLite("pathview")
install.packages("plotly")
install.packages("DT")

From R console,
  to exit q()
