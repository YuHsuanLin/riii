# R 語言基礎

## Download R
- http://cran.csie.ntu.edu.tw/bin/windows/base/R-3.5.1-win.exe
- http://course.largitdata.com/course/33

## Download RStudio
- https://download1.rstudio.org/RStudio-1.1.447.exe 
- http://course.largitdata.com/course/34

## install r 3.5 on ubuntu
step 1: add key
# in terminal
gpg --keyserver keyserver.ubuntu.com --recv-key E084DAB9
gpg -a --export E084DAB9 | sudo apt-key add -

step 2: add source
sudo vi /etc/apt/sources.list
## 貼上以下文字
deb https://cloud.r-project.org/bin/linux/ubuntu xenial-cran35/
deb http://debian.linux.org.tw/ubuntu/ bionic-backports main restricted universe

step 3: use apt-get install r
sudo apt-get update
sudo apt-get install r-base r-base-dev


## write R code in jupyter notebook
step 1: open R in terminal, install all packages using the following lines
```
# in R console
> install.packages(c('repr', 'IRdisplay', 'evaluate', 'crayon', 'pbdZMQ', 'devtools', 'uuid', 'digest'))
> devtools::install_github('IRkernel/IRkernel')
```

step2: install R kernel
```
#in R console
> IRkernel::installspec()
```

step3: start jupyter notebook, select R kernel
```
#in terminal
jupeter notebook
```
