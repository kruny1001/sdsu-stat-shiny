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
  
docker run --rm -p 3838:3838 -v $(pwd)/shinyapps/:/srv/shiny-server/ -v $(pwd)/shinylog/:/var/log/ rocker/shiny
