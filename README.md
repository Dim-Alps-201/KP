# I.
# I ran this to install R and get it working with jupyter:
# sudo apt-get install -y r-base

## but the above gave me an older version of R than I wanted, so then I ran the next 4 lines from here https://cran.r-project.org/bin/linux/ubuntu/ ; might need to change 'cran40' at some point and I skipped their 2nd of 5 lines; need to press Y or enter sometimes
# sudo apt update
# wget -qO- https://cloud.r-project.org/bin/linux/ubuntu/marutter_pubkey.asc | sudo tee -a /etc/apt/trusted.gpg.d/cran_ubuntu_key.asc
# sudo add-apt-repository "deb https://cloud.r-project.org/bin/linux/ubuntu $(lsb_release -cs)-cran40/"
# sudo apt install --no-install-recommends r-base

## then I had to run these but probably I won't have to next time
# sudo Rscript -e "install.packages(c('base64enc', 'rlang'), repos='https://cloud.r-project.org')" && \
# sudo Rscript -e "update.packages(ask=FALSE, repos='https://cloud.r-project.org', checkBuilt=TRUE)"
# sudo Rscript -e "update.packages(ask=FALSE, repos='https://cloud.r-project.org', checkBuilt=TRUE)"

# pip install jupyter
## hopefully the above was not needed; also seemingly it did not work since I got Error in IRkernel::installspec(user = FALSE) : jupyter-client has to be installed but “jupyter kernelspec --version” exited with code 1.
# sudo apt install jupyter-client
## said "Y"
# sudo Rscript -e "install.packages('IRkernel', repos='https://cloud.r-project.org'); IRkernel::installspec(user=TRUE)"
# code --install-extension REditorSupport.r
# sudo chmod -R 777 /usr/local/lib/R/site-library
# ctrl+shift+p -> developer: reload window
# to use R kernel: top right -> click -> "Select Another Kernel..." -> Jupyter Kernel -> /usr/lib/R/bin/R
## next line from https://gist.github.com/tonybenoy/bd3576139861ac27b02f459abfd3a414
# sudo apt-get install -y libcurl4-openssl-dev libfontconfig1-dev libxml2-dev libharfbuzz-dev libfribidi-dev libfreetype6-dev libpng-dev libtiff5-dev libjpeg-dev
## next line from running $ sudo Rscript -e "install.packages('fs', repos='https://cloud.r-project.org')"
# sudo apt-get install -y libuv1-dev
## next time I will do this by means of a devcontainer

# II. I installed Python 3 kernel, seemingly from something in the ctrl+shift+P interface
# III. I installed Jupyter notebook something-or-other, seemingly from something in the VS code-like app store thing on the sidebar in the github codespace
