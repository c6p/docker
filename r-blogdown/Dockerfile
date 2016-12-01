FROM c6prmk/r-base-dev:debian
MAINTAINER Can Altıparmak <can6parmak@gmail.com>

## Install blogdown, dependencies and cleanup
RUN apt-get update -qq && \
    apt-get install -y --no-install-recommends \
        pandoc pandoc-citeproc libxml2-dev libssl-dev libcurl4-openssl-dev && \
    R -q -e "install.packages('devtools'); \
             devtools::install_github('rstudio/blogdown'); \
             blogdown::install_hugo()" && \
    apt-get clean && \
	rm -rf /var/lib/apt/lists/* /tmp/* /usr/share/doc/* \
        /usr/share/man/* /usr/share/groff/* /usr/share/info/* \
        /usr/share/lintian/* /usr/share/linda/* /var/cache/* /usr/share/R/doc/*

CMD ["R"]
