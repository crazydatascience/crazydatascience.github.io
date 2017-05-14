---
layout: post
title:  "How to install R and RStudio on Ubuntu"
date:   2017-04-24 00:31:37 +0200
last_update: 2017-04-26 00:31:37 +0200
categories: R Rstudio Ubuntu
excerpt: How to install R and RStudio on Ubuntu 16.04, 16.10 and 17.04.
comments: true 
---
`R` is an open source programming language and software environment for statistical computing and graphics. The R language is widely used among statisticians and data miners for developing statistical software and data analysis.

`RStudio` is a free and open-source integrated development environment (IDE) for R. 

In this tutorial we will install R and RStudio on Ubuntu 16.04, 16.10 and 17.04. 

Firstly, install R and Gdebi with apt (just copy and paste the code into a terminal): 

{% highlight bash %}
sudo apt install r-base r-base-dev gdebi
{% endhighlight %}

Now, let's move to the home directory and download the libraries `libgstreamer0.10` and `libgstreamer-plugins-base0.10`. At time of this writing, these packages need to be downloaded and installed manually to avoid errors during the installation of RStudio.

{% highlight bash %}
cd ~
wget https://launchpad.net/ubuntu/+archive/primary/+files/libgstreamer0.10-0_0.10.36-1.5ubuntu1_amd64.deb 
wget https://launchpad.net/ubuntu/+archive/primary/+files/libgstreamer-plugins-base0.10-0_0.10.36-2ubuntu0.1_amd64.deb
{% endhighlight %}

Then we install them with gdebi:

{% highlight bash %}
sudo gdebi libgstreamer0.10-0_0.10.36-1.5ubuntu1_amd64.deb 
sudo gdebi libgstreamer-plugins-base0.10-0_0.10.36-2ubuntu0.1_amd64.deb 
{% endhighlight %}

Finally, we download RStudio and install it!

{% highlight bash %}
wget https://download1.rstudio.org/rstudio-1.0.143-amd64.deb
sudo gdebi rstudio-1.0.143-amd64.deb
{% endhighlight %}

Done!

For more information, check out the [The R Project][r-project] official web site and the homepage of [RStudio][rstudio].


[r-project]: https://www.r-project.org/
[rstudio]: https://www.rstudio.com/
