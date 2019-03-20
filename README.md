OpenCPU App: ocpusits
------------------

Simple OpenCPU Application. To install in R:

## Prerequisites

- Running [opencpu](https://www.opencpu.org/) server.

## Installation

    install.packages("devtools")

    library(devtools)
    install_github("ammaciel/ocpusits")

    library(opencpu)
    ocpu_start_server("ocpusits")

    docker run -d -p 8004:8004 ammaciel/ocpusits

    http://localhost:8004/ocpu/library/ocpusits/www/

    # Lookup the container ID
    docker ps

    # Drop a shell
    docker exec -i -t container_id /bin/bash

    # Score remotely
    curl -v localhost:5656/ocpu/user/inpe/library/ocpusits/R/TSoperation/json -d 'name_service="WTSS-INPE"&coverage="MOD13Q1"&bands="evi"&longitude="-56"&latitude="-12"&start_date="2001-01-01"&end_date="2002-01-01"'
