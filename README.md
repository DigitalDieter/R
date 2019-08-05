![R-logo](img/R_logo.png)


## Installation / Dependencies

You need to install the following packages as Installation dependencies:

```bash
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
sudo add-apt-repository 'deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/'
sudo apt update
sudo apt-get -y install libzmq3-dev libcurl4-openssl-dev libssl-dev jupyter-core jupyter-client
```
#### Installation of r-base
```bash
sudo apt install -y r-base
```

Start R as root to keep installations
```bash
sudo -i R
```
To use R inside your jupyter notebook you have to install the following package inside the R console:
```bash
install.packages('IRkernel')
```
Install Packages
```bash
install.packages('IRkernel')
install.packages('tensorflow')
install.packages('keras')
install.packages("tfestimators")

install.packages(c('repr', 'IRdisplay', 'evaluate', 'crayon', 'pbdZMQ', 'devtools', 'uuid', 'digest'))
install.packages(c('vcd', 'readr', 'R.utils', 'randomForest'))

```


Setup R Kernel Systemwide
```bash
IRkernel::installspec(user = FALSE)
```


#### To create an executable script copy & paste the following command into the commandline:

```bash
dd of=hello.R<< EOF
sayHello <- function(){
   print('hello world')
}

sayHello()
EOF
chmod +x hello.R
```
#### For running the script execute the following command:

```bash
Rscript hello.R
```


```bash
dd of=download_fashion_MNIST.R<< EOF
download.file("http://fashion-mnist.s3-website.eu-central-1.amazonaws.com/train-images-idx3-ubyte.gz",
              "datesets/fashion-train-images-idx3-ubyte.gz")
download.file("http://fashion-mnist.s3-website.eu-central-1.amazonaws.com/train-labels-idx1-ubyte.gz",
              "datesets(fashion-train-labels-idx1-ubyte.gz")
download.file("http://fashion-mnist.s3-website.eu-central-1.amazonaws.com/t10k-images-idx3-ubyte.gz",
              "datesets/fashion-t10k-images-idx3-ubyte.gz")
download.file("http://fashion-mnist.s3-website.eu-central-1.amazonaws.com/t10k-labels-idx1-ubyte.gz",
              "datesets/fashion-t10k-labels-idx1-ubyte.gz")
EOF
chmod +x download_fashion_MNIST.R
```

