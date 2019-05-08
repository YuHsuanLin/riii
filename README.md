# R 語言基礎

### CLASS 1
- http://rpubs.com/YorkLin/riii_190509

## Download R
- http://cran.csie.ntu.edu.tw/bin/windows/base/R-3.5.3-win.exe 
- http://course.largitdata.com/course/33

## Download RStudio
- https://download1.rstudio.org/desktop/windows/RStudio-1.2.1335.exe 
- http://course.largitdata.com/course/34

## install R 3.5 on ubuntu16.04
step 1: add key

in terminal
```
gpg --keyserver keyserver.ubuntu.com --recv-key E084DAB9
gpg -a --export E084DAB9 | sudo apt-key add -
```

step 2: add source
```
sudo vi /etc/apt/sources.list
```

貼上以下文字
```
deb https://cloud.r-project.org/bin/linux/ubuntu xenial-cran35/
deb http://debian.linux.org.tw/ubuntu/ bionic-backports main restricted universe
```
step 3: use apt-get install r
```
sudo apt-get update
sudo apt-get install r-base r-base-dev
```

## write R code in jupyter notebook
step 1: open R in terminal, install all packages using the following lines
```
# in R console
> install.packages(c('repr', 'IRdisplay', 'evaluate', 'crayon', 'pbdZMQ', 'devtools', 'uuid', 'digest'))
> devtools::install_github('IRkernel/IRkernel')
```
if installing devtools failed:
- https://www.digitalocean.com/community/tutorials/how-to-install-r-packages-using-devtools-on-ubuntu-16-04
```
sudo apt-get install build-essential libcurl4-gnutls-dev libxml2-dev libssl-dev
```

step2: install R kernel
```
#in R console
> IRkernel::installspec()
```

step3: start jupyter notebook, select R kernel
```
#in terminal
jupyter notebook
```



