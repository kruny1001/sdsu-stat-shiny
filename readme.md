https://hub.docker.com/r/rocker/shiny/

#Build Shiny Server Image
docker build -t ge-lab/shiny .

#Run Shiny Server Docker Image
docker run --rm -p 3838:3838 \
    -v $(pwd)/shinyapps/:/srv/shiny-server/ \
    -v $(pwd)/shinylog/:/var/log/ \
    -v $(pwd)/RSet/:/usr/local/src/myscripts \
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
sudo docker exec -i -t happy_dijkstra /bin/bash
sudo docker exec -i -t sad_brown /bin/bash
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

https://www.cyberciti.biz/faq/how-do-i-compress-a-whole-linux-or-unix-directory/
# How to compress the files
For example, you want to compress shinyapps directory with one file. you can use below commandline
```
tar -zcvf shinyapps.tar.gz shinyapps/
```

# How to extract file
tar -zxvf shinyapps.tar.gz -C /shinyapps


#nginx setup
http://askubuntu.com/questions/764222/nginx-installation-error-in-ubuntu-16-04
http://deanattali.com/2015/05/09/setup-rstudio-shiny-server-digital-ocean/



Openssl problem
https://github.com/rocker-org/rocker/issues/124

ERROR: configuration failed for package ‘openssl’
* removing ‘/usr/local/lib/R/site-library/openssl’
ERROR: dependency ‘openssl’ is not available for package ‘httr’
* removing ‘/usr/local/lib/R/site-library/httr’
ERROR: dependency ‘httr’ is not available for package ‘plotly’
* removing ‘/usr/local/lib/R/site-library/plotly’

```
apt-get update
apt-get install libgdal-dev/unstable
sudo apt-get install libssl-dev
```
