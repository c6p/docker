FROM c6prmk/r-base-dev:ubuntu
MAINTAINER Can Altıparmak <can6parmak@gmail.com>

## Install dependencies
RUN apt-get update -qq && \
    apt-get install -y --no-install-recommends \
        pandoc pandoc-citeproc libxml2-dev libssl-dev libcurl4-openssl-dev && \
    apt-get clean && rm -rf /tmp/* /var/lib/apt/lists/*

## Install blogdown and cleanup
RUN R -q -e "install.packages('devtools'); \
             devtools::install_github('rstudio/blogdown'); \
             blogdown::install_hugo()" && \
    rm -rf /tmp/* /usr/share/man/* /usr/share/groff/* /usr/share/info/* \
        /usr/share/lintian/* /usr/share/linda/* /var/cache/man/*

CMD ["R"]
