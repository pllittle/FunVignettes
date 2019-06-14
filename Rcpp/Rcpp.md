---
title: "R, Rcpp, and RcppArmadillo"
author: "Paul L."
---

# Introduction

This markdown is designed to illustrate how Rcpp/RcppArmadillo can be integrated into R functions to improve computational runtime. Armadillo documentation can be found [here](http://arma.sourceforge.net/docs.html "Click Me!").

# Data types

Unlike R, C++ variables need to be defined. In the example below, an Armadillo vector is initialized with length 5 and all elements set to 0.

```{cpp}
arma::vec aa = arma::zeros<arma::vec>(5);
```

To set elements, we could do this manually or with a for loop. Notice that the loop iterator variable is an unsigned integer of type `arma::uword`.


```{cpp}
aa.at(0) = 1;
aa.print("aa = ");

for(arma::uword ii = 0; ii < aa.n_elem; ii++){
	aa.at(ii) = ii + 1;
}
aa..print("aa = ");
```

# Regression

#

# EM Algorithm

# Multiple Threads


